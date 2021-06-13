---------------------------------
pdpapl - Bad Apple for the PDP-11
---------------------------------

In short, this program aims to draw the viral Bad Apple!! shadow-art
video by Anira on a video terminal connected to a PDP-11.
For those somehow unfamiliar: <https://youtu.be/FtutLA63Cp8>.

=== System requirements ===

- Extended Instruction Set
- KW11-L compatible line time clock
- Serial line interface set to transfer at or above 9600 baud*
- One of the following supported terminals, or one compatible with:
	- DEC VT100 series
	- DEC VT200 series
	- Generic "ANSI-compatible"

* Stock PDP-11 hardware caps out at 9600 baud, but hackers have
  managed to implement serial interfaces upwards of 19200 baud:
  <http://www.retrocmp.com/how-tos/41-interfacing-with-a-pdp-1105>

=== Compilation ===

An RX02 diskette image can be obtained from the author's website:
<https://www.ssterling.net/comp/pdpapl/files/> (select latest version).
This image is ready for use in a simulator; as of writing, it is not
known whether this software can run on original PDP-11 hardware.

Alternatively, the user may create their own image from these files
for use in any magtape, disk, or punched paper tape form; this requires
generating the requisite `VDATA.MAC' file using pdpaplas:
<https://www.gitlab.com/ssterling/pdpaplas/>.
Do note this may require EOL conversion to CRLF.

Once the volume is mounted (further commands assume `DK'), open the
source file (`PDPAPL.MAC') in a text editor and set the constants
under `PROGRAM CONFIGURATION' as appropriate.
Once this is complete, compile and run the program as such:

	.MACRO PDPAPL
	.LINK PDPAPL
	.RUN PDPAPL

=== Bugs ===

See `BUGS.TXT' for a list of known bugs.

Please report any bugs to the issue tracker:
<https://www.gitlab.com/ssterling/pdpapl/issues/>.
