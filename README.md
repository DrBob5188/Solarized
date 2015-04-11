Solarized - SecureCRT settings
==========================

### [See official homepage for full content](http://ethanschoonover.com/solarized)

Configuration (SecureCRT)
--------------------

SecureCRT stores its configuration in a number of ini files.  You'll need to modify the Global.ini file and the Color Schemes.ini file to make Solarized available to your sessions. There are some specific modifications required to individual session configurations before they can use the Solarized colors so please read the troubleshooting information if you are having difficulty.  

1. Open the global.ini file and locate the line beginning with **B:"ANSI Color RGB"**. Subsequent lines that begin with whitespace belong to the same entry.
1. Replace the lines in that entry with the lines below.<BR/>
B:"ANSI Color RGB"=00000040<BR/>
&nbsp;07 36 42 00 dc 32 2f 00 85 99 00 00 b5 89 00 00 26 8b d2 00 d3 36 82 00 2a a1 98 00 ee e8 d5 00<BR/>
&nbsp;00 2b 36 00 cb 4b 16 00 58 6e 75 00 65 7b 83 00 83 94 96 00 6c 71 c4 00 93 a1 a1 00 fd f6 e3 00<BR/>
1. Open the Color Shemes.ini and append the entries below to the file<BR/>
B:"Solarized Dark"=00000044<BR/>
&nbsp;00 01 01 01 83 94 96 00 93 a1 a1 00 83 94 96 00 93 a1 a1 00 83 94 96 00 93 a1 a1 00 83 94 96 00<BR/>
&nbsp;93 a1 a1 00 00 2b 36 00 07 36 42 00 00 2b 36 00 07 36 42 00 00 2b 36 00 07 36 42 00 00 2b 36 00<BR/>
&nbsp;07 36 42 00<BR/>
B:"Solarized Light"=00000044<BR/>
&nbsp;00 01 01 01 65 7b 83 00 58 6e 75 00 65 7b 83 00 58 6e 75 00 65 7b 83 00 58 6e 75 00 65 7b 83 00<BR/>
&nbsp;58 6e 75 00 fd f6 e3 00 ee e8 d5 00 fd f6 e3 00 ee e8 d5 00 fd f6 e3 00 ee e8 d5 00 fd f6 e3 00<BR/>
&nbsp;ee e8 d5 00<BR/>
1. Open a sessions properties and select the Terminal/Emulation Category. Select the ANSI Color and Use Color Scheme Checkboxes.  Select the Terminal/Appearance Category. Change the Current color scheme dropdown to either Solarized Light or Solarized Dark

Troubleshooting Information
--------------------
1. Ensure that in your session properties you have selected a Terminal type that supports color such as xterm. Editors like vi will not send color codes to vt100 terminals.
2. Make sure that you have closed SecureCRT before editing the ini files
3. Check the format of the lines you paste in to the ini files. The first line of each entry (beginning with B:) should have no whitespace at the beginning.  The second and subsequent lines (containing the rgb byte values) should begin with a single space.
4. You must make certain that you use one of the Solarized color schemes with the the ANSI colors or the default foreground and background colors will be incorrect.  In the SecureCRT ANSI colors dialog the normal foreground ANSI color is displayed/set on the far right of the top row of the Normal colors section.  The normal background ANSI color is displayed/set on the far left of the top row of the Normal colors section. Read the [knowledgebase article] (http://www.vandyke.com/support/tips/colorconfig.html "Overview of Color Configuration in SecureCRT") for more information on how color schemes work with ANSI Colors.
5. Find the SecureCRT config path.<BR/> Open a command prompt and type reg query "hkcu\Software\VanDyke\SecureCRT" /v "Config Path"

