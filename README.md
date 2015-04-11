Solarized - SecureCRT settings
==========================

### [See official homepage for full content](http://ethanschoonover.com/solarized)

Configuration (SecureCRT)
--------------------

SecureCRT stores its configuration in a number of ini files.  You'll need to modify the Global.ini file and the Color Schemes.ini file to make Solarized available to your sessions. There are some specific modifications required to individual session configurations before they can use the Solarized colors so please read the detailed instructions if you are having trouble.  

1. Open the global.ini file and locate the line  beginning with **B:"ANSI Color RGB"**. Subsequent lines that begin with whitespace belong to the same entry.
2. Replace the lines in that entry with the lines below.
B:"ANSI Color RGB"=00000040
&nbsp; 07 36 42 00 dc 32 2f 00 85 99 00 00 b5 89 00 00 26 8b d2 00 d3 36 82 00 2a a1 98 00 ee e8 d5 00
&nbsp; 00 2b 36 00 cb 4b 16 00 58 6e 75 00 65 7b 83 00 83 94 96 00 6c 71 c4 00 93 a1 a1 00 fd f6 e3 00
3. Open the Color Shemes.ini and append the entries below to the file
B:"Solarized Dark"=00000044
&nbsp; 00 01 01 01 83 94 96 00 93 a1 a1 00 83 94 96 00 93 a1 a1 00 83 94 96 00 93 a1 a1 00 83 94 96 00
&nbsp; 93 a1 a1 00 00 2b 36 00 07 36 42 00 00 2b 36 00 07 36 42 00 00 2b 36 00 07 36 42 00 00 2b 36 00
&nbsp; 07 36 42 00
B:"Solarized Light"=00000044
nbsp; 00 01 01 01 65 7b 83 00 58 6e 75 00 65 7b 83 00 58 6e 75 00 65 7b 83 00 58 6e 75 00 65 7b 83 00
nbsp; 58 6e 75 00 fd f6 e3 00 ee e8 d5 00 fd f6 e3 00 ee e8 d5 00 fd f6 e3 00 ee e8 d5 00 fd f6 e3 00
nbsp; ee e8 d5 00
4. Open a sessions property and select the Terminal/Emulation Category. Select the ANSI Color and Use Color Scheme Checkboxes.  Select the Terminal/Appearance Category. Change the Current color scheme dropdown to either Solarized Light or Solarized Dark



