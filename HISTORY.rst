.. :changelog:

History
-------

0.1.28 (2017-07-27)
______________________

* Added reader for Lattice FPGA devices (except iCE40). (Thanks, Adrien Descamps!)


0.1.27 (2017-05-24)
______________________

* Fixed issue #11 (blank lines in CSV file were skipped and multiple parts ran together).


0.1.26 (2017-05-21)
______________________

* Fixed issue #18 (crash when symbol side for pin was left blank).


0.1.25 (2017-05-03)
______________________

* Fixed problem caused by pin side designators not being lower-case (e.g., "Left").


0.1.24 (2016-12-22)
______________________

* Fixed Xilinx reader function to parse leading comments in their FPGA pin files.


0.1.23 (2016-12-13)
______________________

* Added ability to create hidden pins.


0.1.22 (2016-11-29)
______________________

* Fixed readers for Xilinx, STM32, PSoC devices.
* Pins on multiple sides of a symbol are now distributed in a more attractive manner.


0.1.21 (2016-09-20)
______________________

* Extra stuff on starting line of library no longer kill kilib2csv.


0.1.20 (2016-09-16)
______________________

* Fixed bug where kilib2csv was choking on footprint lists in part definitions.


0.1.19 (2016-09-16)
______________________

* Added utility to test kilib2csv and kipart on randomly-generated CSV part files.


0.1.18 (2016-09-14)
______________________

* kilib2csv utility added to convert KiCad schematic symbol libraries into CSV files suitable for input to KiPart.


0.1.17 (2016-06-15)
______________________

* Use same type of sorting for unit names as for pin names so (for example) unit 'ADC_12' comes before unit 'ADC_2'.


0.1.16 (2016-06-12)
______________________

* Added reader for CSV-formatted pinout files exported from the STM32CubeMx tool. (Thanks, Hasan Yavuz OZDERYA!)


0.1.15 (2016-02-17)
______________________

* Added reader for Xilinx Ultrascale FPGAs.
* Fixed insertion of spaces between groups of pins when pin number starts with '*'.
* Replaced call to warnings.warn with issues() function.
* fix_pin_data() now strips leading/trailing spaces from pin information.


0.1.14 (2016-01-30)
______________________

* Fixed incorrect y-offset of pins for symbols that only have pins along the right side.


0.1.13 (2015-09-09)
______________________

* The number of pins in a bundle is now appended to the pin name instead of an '*'.


0.1.12 (2015-09-03)
______________________

* Added capability to insert non-existent "gap" pins that divide groups of pins into sections.


0.1.11 (2015-09-02)
______________________

* future module requirement added to setup.py.


0.1.10 (2015-08-26)
______________________

* Now runs under both Python 2.7 and 3.4.


0.1.9 (2015-08-21)
______________________

* The bundling option now only bundles pins where that operation makes sense:
  power input pins (e.g., VCC and GND) and no-connect pins.


0.1.8 (2015-08-17)
______________________

* Input data from the CSV file is now scanned for errors and fixed before it can cause problems
  in the library file.


0.1.7 (2015-08-14)
______________________

* Added reader functions for Xilinx Virtex-6 and Spartan-6.
* Broke-out reader functions into separate modules.
* TXT and CSV files are now acceptable as part data files, but the reader has to be built to handle it.


0.1.6 (2015-08-13)
______________________

* Fuzzy string matching is now used for the column headers.
* Choice-type options are now case-insensitive.


0.1.5 (2015-07-29)
______________________

* Multiple parts can now be described in a single CSV file.
* Added function and option for reading Cypress PSoC5LP CSV files.
* Simplified key generators for sorting pins by name or number.
* Improved ordering of pins by name.


0.1.4 (2015-07-27)
______________________

* Added option for approximate (fuzzy) matching for pin types, styles and orientations (sides).


0.1.3 (2015-07-26)
______________________

* Multiple pins with the same name are now hidden by reducing their pin number size to zero
  (rather than enabling the hidden flag which can cause problems with power-in pins).


0.1.2 (2015-07-24)
______________________

* Symbols can now have pins on any combination of left, right, top and bottom sides.
* Added option to append parts to an existing library.
* Refactored kipart routine into subroutines.
* Added documentation.


0.1.1 (2015-07-21)
______________________

* Fixed calculation of pin name widths.
* Made CSV row order the default for arranging pins on the schematic symbol.
* Fixed sorting key routine for numeric pin numbers.
* Spaces are now stripped between fields in a CSV file.


0.1.0 (2015-07-20)
______________________

* First release on PyPI.
