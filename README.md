
Chronicle makes it easy for Pathfinder Society GM's to collect player info and generate chronicle sheets right from the scenario PDFs.

# Installation:

Chronicle requires JRuby 1.5 and various gems. The docsplit gem requires GraphicsMagick and Poppler to be installed. If you do not have these installed, first install the <code>graphicsmagick</code> and <code>poppler</code> packaged. I used brew to do this by running:

$ brew install graphicsmagick poppler

Once you have these packages installed, then installing the chronicle gem should be as easy as:

$ gem install chronicle

# Setup:

To sign and initial your chronicle sheets, you'll need create two images: <code>signature.png</code> and <code>initials.png</code>. These files must be placed in your home directory under the <code>.chronicle</code> subdirectory. The signature file should be 500x100 and the initials file should 100x100. Both should be 300dpi.

# Usage:

I organize the scenarios I run into directories (folders). Each directory contains the scenario PDF as well as the other materials I use to run the session. All the chronicle commands listed below are run in a terminal from a directory such as this. 

This instructions are probably more detailed than you need, but just in case...

## Preparing to Play

0. Open a terminal and change to your scenario directory.
0. Run <code>chron-prepare AScenarioFile.pdf</code>. 

This should create a file called <code>chronicle_sheet.png</code> in the current directory.

## Creating an Online Signup Form
0. First, [click here to create](https://docs.google.com/previewtemplate?id=0Ann48md_Q6mkdGtocUJ4NVZhQjVSdWRidzUtU3dKOHc&mode=public) a simple online signup form for your session.
0. Give your signup form a name and a description and hit "Save". 
0. Click "See responses"&rarr;"Spreadsheet", and select the "ScenarioMetadata" sheet
0. If you haven't already, [register your event at paizo.com](https://secure.paizo.com/pathfinderSociety/myAccount/eventCoordinator) and use the information provided to fill in the "ScenarioMetadata" sheet
0. Click "Form"&rarr;"Go to live form". Copy the signup form URL, and fill out the form once for the character you plan to give your GM reward to.
0. You can now publish the signup form URL to let people know how to sign up for your session. Consider updating the URL field for the event on paizo.com.

## Generating Chronicle Sheets
0. Go to https://docs.google.com and open your registration form spreadsheet.
0. Select the "Signups" sheet and review the information to ensure it is correct.
0. Select the "ChronicleSheetInfo" sheet and fill in the results of the scenario in columns D through G
0. Click "File"&rarr;"Download As..."&rarr;"CSV (Current Sheet)". I like to save this file to a "rosters" subdirectory under my scenario directory.
0. Open a terminal and change to your scenario directory.
0. If you need to mark out any items that the players did not earn, open up your favorite image editor and mark up chronicle_sheet.png. 
0. Run <code>chron-finish rosters/[new roster file].csv</code>. 

Done! A chronicle sheet for each character (including your GM reward character) should have been created in the <code>sheets</code> directory. If you want to generate your sheets to a different directory, you can pass that as the second parameter to <code>chron-finish</code>.

### About Chronicle

Modit was written by Ben Rady, and is distribuited under the MIT License

Copyright (c) 2010 Ben Rady <benrady@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
