---
layout: page
title: "mac and ios"
date: 2013-08-21 16:12
comments: true
sharing: true
footer: true

---

map of topics: [pdf][map-pdf],[ithoughts][map-ithoughts],[markdown][map-markdown]

[map-ithoughts]: https://www.dropbox.com/s/7ndlfwv4y4280h4/20140526techrecommendations.itmz
[map-pdf]: https://www.dropbox.com/s/sseg1lvb64ghrax/20140526techrecommendations.pdf
[map-markdown]: https://www.dropbox.com/s/i3c5p9x3bd0hgtf/20140526techrecommendations.markdown
[map-opml]: https://www.dropbox.com/s/pwwkdeazykzov5t/20140526techrecommendations.opml

* <a href="#capture">capturing data</a>
* <a href="#do">action data</a>
* <a href="#show">show data</a>
* <a href="#learn">learning</a>
* <a href="#shortcuts">shortcuts</a>

<div id="capture"></div>

## new ideas as text

<div id="drafts"></div>

##### drafts
[drafts][] £1.99ios jot down ideas, process them later. Can use custom dropbox actions to append text to specific files in dropbox. You can search within your text in drafts, which byword for ios can only do outside the file in a dropbox folder.

here's a drafts x-callback-url I call from launchcenter pro for sending fleksy text straight to a specified dropbox file, then return to fleksy: (first copy and clear all written in fleksy using two–finger swipe up)

	drafts://x-callback-url/create?text=[clipboard]&action=todropboxmakiaea&afterSuccess=Delete&x-success={{fleksy://}}

and the drafts action todropboxmakiaea itself contains:

* path: /datafiles/
* file predefined: fromdrafts
* ext: md
* write: append
* template: [[draft]]

[drafts]: http://agiletortoise.com/drafts
[x-callback-url]: http://agiletortoise.com/developers/drafts/

## mindmap

<div id="ithoughts"></div>

##### ithoughts

[ithoughts][] £6.99ios/£39.99mac(ithoughtsx) mindmaps; can import/export markdown; has full–screen mode and responsive hide/show branches for presentations. more versatile than mindnod, for example has intra–document search like editorial does. does not have a free web–hosted map display service, but if you are using dropbox you can host the files yourself. ithoughts url scheme example action and list (e.g. for use in launchcenterpro):

	ithoughts://Maps/makiaea/20131210maki

	ithoughts://[[list:ithoughts action set|maki=Maps/makiaea/20131210maki|tech=Maps/makiaea/20140526techrecommendations]]

[ithoughts]: http://toketaware.com

<div id="mindnode"></div>

##### mindnode

[mindnode][] £6.99ios/£13.99mac(mindnodepro) mindmaps; currently cannot import markdown (if you need this now, try ithoughts, or if you use the mac app, you can paste in markdown using brett's [Converting Markdown to a mind map][] service. has free proprietary web–hosted map display service. note that syncing needs to be confirmed each time (icloud or dropbox). [mindnode url scheme][mindnodeurlscheme]; mindnode action set example [using folders][mindnodeurlschemefolder]:

	mindnode://[[list:mindnode action set|read=open?folder=makiaea&name=20140123read|tech=open?folder=makiaea&name=20131204techrecommendations|day=open?folder=makiaea&name=20131207daychallenges]]

(the double square brackets mean the content is not auto–encoded)

[mindnode]: http://mindnode.com
[mindnodeurlscheme]: http://mindnode.com/blog/post.php?s=2012-08-10-custom-url-schemes-in-mindnode-touch
[mindnodeurlschemefolder]: https://gist.github.com/aquarius/5823110
 [Converting Markdown to a mind map]: http://brettterpstra.com/2013/08/18/markdown-to-mind-map/

## full–res continuous camera

<div id="snappycam"></div>

##### snappycam

[snappycam][] £0.69ios burst photos in full iphone resolution, up to 20 frames per second on iphone5. Helpful for capturing baby photos!

[snappycam]: http://www.snappycam.com

## font

<div id="fontforge"></div>

##### fontforge

[fontforge][] free–mac create your own font. Warning; this is time–consuming! mac binary made by Pedro Amado

[fontforge]: http://www.typeforge.net/blog/2011/05/23/fontforge-binaries/

## audio

<div id="audacity"></div>

##### audacity 

[audacity][] free–mac open–source audio recorder

[audacity]: http://audacity.sourceforge.net

## image processing

<div id="gimp"></div>

##### bitmap

[gimp][] free–mac bitmap graphics editor

[gimp]: http://www.gimp.org

<div id="inkscape"></div>

##### vector

[inkscape][] free–mac SVG vector graphics editor; .svg vector graphics files can be edited and rescaled without loss of fidelity

[inkscape]: http://inkscape.org

## OCR scanning offline

<div id="prizmo"></div>

##### prizmo

[prizmo][] £2.99ios optical character recognition in scans does not require network connection, unlike some other scanning apps

[prizmo]: http://www.creaceed.com/iprizmo/about

## keyboard

<div id="fleksy"></div>

##### type without looking

[fleksy][] free–ios literally can type without looking at the screen. You must then move the text into another program for editing. (I especially like the invisible silent keyboard mode). Only has a qwerty keyboard, sadly no dvorak option yet. Launch Center Pro action list to use fleksy as input and send to Clear.

	launch://x-callback-url/clipboard/convert?format=plaintext&x-success=clearapp%3a%2f%2f[list:clear action set|lena=task/create?listName=lena&taskName=|now=task/create?listName=now&taskName=|write=task/create?listName=write&taskName=]{{[prompt-fleksy:Task]}}

[fleksy]: http://fleksy.com

<div id="command-c"></div>

##### copy text between ios and mac

[command-c][] £2.49ios/freemac copy text between ios devices and macs when on same wifi network; [eric's review][ericommandcreview], [frederico's review][fredericocommandcreview]

[command-c]: http://www.danilo.to/command-c
[ericommandcreview]: http://www.geekswithjuniors.com/note/how-command-c-replaces-pastebot-and-improves-my-workflow.html
[fredericocommandcreview]: http://www.macstories.net/reviews/command-c-a-local-clipboard-sharing-tool-for-os-x-and-ios-7/

<div id="1keyboard"></div>

##### mac keyboard as (limited) input to ios

[1keyboard][] £6.99 if you need to use your mac keyboard to type on your ios device (via bluetooth), e.g. for messaging on ios–only apps.

[1keyboard]: http://www.eyalw.com/1keyboard

<div id="do"></div>

<div id="markdown"></div>

# write
use markdown/multimarkdown: keep your base text in markdown format for flexibilty in using and editing it on a computer or a phone/tablet. brett's 2–minute [why markdown?][] and [ios text editors][]

[ios text editors]: http://brettterpstra.com/ios-text-editors/

## text or markdown

<div id="editorial"></div>

##### editorial

[editorial][] £4.99ios; excellent markdown and text editor with workflows, document search, move to header. the workflows are particularly useful; it's almost a mini keyboardmaestro on ios. am currently using editorial to create a wiki–style document page for my most frequently used documents. [editorialdocs][]

##### editorial workflows
[workflows][] modify them to suit your needs

[bookmarks][] save and read from a specific dropbox file in a directory, also saving the exact position of the cursor within the document   
[homescreen][] saves bookmark to current document onto the home screen, i use this for my main wiki file  
[reminder][] saves bookmark into a due or fantastical reminder (re–enable selection in the workflow if you want to go back to the specific last point you were in within the document)  

##### make editorial wiki
make your own workflow combining Set URL (include selected range) and set clipboard in order to copy a link to the current page into the clipboard  
[markdownlink][] select text to be linked, then use this to create markdown link based on current clipboard contents

##### make editorial shortcuts
for example, if you have several often–used documents, you can create workflows that open each of these, and set keyboard shortcuts/abbreviations for each of these workflows, and use them to swap between the documents. if you use abbreviations exclusively (i.e. combinations of letters) then you can use set these to open/save your bookmarks, for example, using the on–screen keyboard as well as a bluetooth keyboard. the bookmark system has an advantage that you can set the current location of the cursor readily. additionally you can set a bookmark for the bookmark file in order to edit it.

currently if you use abbreviations, you do have to have the cursor active for the abbreviations to type, and therefore activate.

You can also create a version of gabe's bookmarks workflows that saves only one single bookmark that is overwritten entirely each time it is saved, and set this to a special shortcut so that you can easily open that particular file, and also be able to set it to the current location using a shortcut. perhaps in future Ole might offer a facility to open the last cursor location for a file; this would be especially useful for longer files. You can do this process semi–manually by setting a new bookmark each time and deleting older ones for the same file. Alternatively, just make a shortcut to the file, and use the search function to find where you want to go (this works better if you are using an external keyboard).
 
[bookmarks]: http://www.macdrifter.com/2013/12/bookmarker-macros-for-editorial.html

[homescreen]: http://www.editorial-workflows.com/workflow/5881089591607296/C9cWHZLAVZQ

[reminder]: http://www.editorial-workflows.com/workflow/5773031167229952/WW0yEbgmZzY

[markdownlink]: http://www.editorial-workflows.com/workflow/5880461184204800/WykOoS1yXEM

[workflows]: http://www.editorial-workflows.com/workflows

[editorialdocs]: http://omz-software.com/editorial/docs/

[editorial]: http://omz-software.com/editorial/

## code or large files

<div id="sublime"></div>

##### sublime text

[sublime text][] $70mac expensive but powerful (and speedy) editor, especially good for large files. There are no print options,  you will need something like [marked2](http://makiaea.org/read/techrecommendations.html#marked2) or use another editor for print or export.

 | 
---: | :---
cmd–r | (goto symbol) allows you to move between headers easily in a markdown document
cmd–p | (goto anything) then # then searchterm to jump to next occurrence in the current document
ctrl–minus | jump back to previous cursor location (sublime text 3–only)
cmd-ctrl-shift-f | fullscreen mode (I bind this to hyper2-return)
cmd–ctrl–p | switch project within window (make some projects to hold collections of files/folders that you use together) — though in practice am using two windows (often placed directly over each other) for two different projects and switching between them using cmd–`
cmd–d | select word, repeat to use multiple cursors to select subsequent words/phrases
cmd–u | unselect word/phrase
cmd–k–d | (sequential k then d) to skip to next candidate. left or right to move cursors within selected word
cmd–ctrl–g | select all occurrences of word/phrase
cmd–click | non–successive lines start multiple cursor, or
<span style="white-space:nowrap;">cmd–shift–L</span> | highlight column with cursor then cmd–shift–L to start column–mode multiple cursor (useful if you want to edit multiple lines at specified places). you can move the cursors as you would a normal cursor e.g. cmd–left to go to the beginning of the line (if you have text running across multiple lines you might want to do cmd–left a few times to ensure it really is the beginning of the line rather than the beginning of the wrapped line)
tab | autocompletion — be careful with this!
cmd–number | switch to tab

modify by going into sublime text preferences — browse packages

my user preferences:

	{
		"caret_style": "solid",
		"color_scheme": "Packages/User/makiaea.tmTheme",
		"font_face": "AvenirNext-UltraLight",
		"font_size": 11.0,
		"gutter": false,
		"line_numbers": false
	}

my distraction free preferences; note the larger font size
 
	{
 		"font_size": 24,
 		"wrap_width": 0
	}

my VBScript.sublime-settings (lots of comments in the code, so word wrap is on…)

	{
		"gutter": true,
		"line_numbers": true,
		"wrap_width": 0,
		"word_wrap": "true"
	}

my [current theme][] is based on a custom [solarized dark theme][] with markdown highlighting and is stored in

	/Users/maki/Library/Application Support/Sublime Text 3/Packages/User/makiaea.tmTheme

you can create your own shortcuts to projects or even open them from the command line e.g. for sublime text 3:

	/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /Users/maki/Documents/Dropbox/datafiles/20130416maki.sublime-project

package for [highliting for VBScript syntax][]

<div id="smartmarkdown"></div>

[smartmarkdown][] sublime3 package for moving between and folding (markdown) headlines. install by downloading zip from github, renaming directory to "SmartMarkdown", then placing directory into

	/Users/yourusername/Library/Application Support/Sublime Text 3/Packages/

NB assumes #(space)headers, not #header as we are using. shortcuts:

 |
---: | :---
tab | toggle smart folding (when used within a header)
shift-tab | global toggle all folding (i use this often for navigation as i don't always remember the headings of all files)
cmd-shift-, | decrease header level
cmd-shift-. | increase header level
ctrl-c ctrl-n | move to next (any) headline
ctrl-c ctrl-p | move to previous (any) headline
ctrl-c ctrl-f | move to next same-or-higher-level headline
ctrl-c ctrl-b | move to previous same-or-higher-level headline

[sublimeacmeplumbing][] sublime3 package that commandeers the secondary mouse button in sublime text and lets you click to open urls including local file urls etc. NB only works for files which do not contain a space, and is useful really only for text or image files as the files will open within sublime text 3 rather than open in an external program

Set [marked][marked build] to open current (markdown) file, processed (uses build, shortcut cmd-b)

[marked build]: http://support.markedapp.com/kb/how-to-tips-and-tricks/marked-bonus-pack-scripts-commands-and-bundles
[sublime text]: http://www.sublimetext.com
[current theme]: https://www.dropbox.com/s/rqu9lb41xymcoya/makiaea.tmTheme
[solarized dark theme]: https://gist.github.com/eleclerc/1904917/download#
[smartmarkdown]: https://github.com/demon386/SmartMarkdown#v02-support-for-sublime-text-3-added-by-unowen
[sublimeacmeplumbing]: https://github.com/lionicsheriff/SublimeAcmePlumbing
[highliting for VBScript syntax]: https://github.com/SublimeText/VBScript

[dropbox]: https://www.dropbox.com/tour
[googledrive]: https://drive.google.com

# store

## data

<div id="dropbox"></div>
<div id="googledrive"></div>

##### dropbox and googledrive

Save non–security–sensitive important data to a single folder within [dropbox][] (free); makes an offsite copy and enables reliable syncing between phone and computer. also consider [googledrive][]

## code

<div id="github"></div>

##### github

[github][] (free) share and store code online

[github]: https://github.com

# email

## process inbox

<div id="dispatch"></div>

##### dispatch

[dispatch][] £2.99ios by the producers of due; gives better options for acting on messages rather than just sorting them like mailbox app does.

i set the quick action to "archive" which moves the message to my "lena" folder (personal messages); and set quick move to the "keep" folder (non–personal messages)

[dispatch]: http://www.dispatchapp.net

## retrieve long–term

<div id="mailmate"></div>

##### mailmate

[mailmate][] $50mac email app; NB the following does not work as of 20131119: can set up internal multi-stroke key bindings e.g. my ~/Library/Application Support/MailMate/Resources/KeyBindings/makiaea.plist contains something like:

	"m" = {
		"l" = ( "moveToMailbox:", "imap://you@imap.example.com/3lena" );
		"t" = ( "moveToMailbox:", "imap://you@imap.example.com/2do" );
		"w" = ( "moveToMailbox:", "imap://you@imap.example.com/4wait" );
		"k" = ( "moveToMailbox:", "imap://you@imap.example.com/5keep" );
		"m" = "moveToMailbox:"; // Opens the “Move to Mailbox...” window
	};

[mailmate]: http://freron.com/about/

# tasks

## timed irregular

<div id="due"></div>

##### due

[due][] £6.99mac £2.99ios very flexible for repeating reminders e.g. repeat on three weekdays only. You can also add urls (and non–website ios urls) to the reminder, which will open automatically on completing the reminder. I use this to remind me to do and redo things regularly, e.g. maintenance tasks

example [due url scheme][] code:

	due:///add?title=entertitlehere&secslater=enternumberofsecondshere

due still asks us to confirm the reminder. Would love a url scheme to set timers…

[due url scheme]: http://www.dueapp.com/developer.html
[due]: http://www.dueapp.com

## untimed irregular

<div id="recur"></div>

##### recur

[recur][] £0.69ios shows time since last marked task completed ("reverse–todo–list"). especially useful if a habit or task is irregular, but you don't want to be actively reminded of it, yet want to keep track of when you last did something to do with the task. can link to [carrot to–do][]

[recur]: https://itunes.apple.com/us/app/recur!-the-reverse-to-do-list/id715147898?mt=8
[carrot to–do]: http://meetcarrot.com

## timed regular

<div id="fantastical"></div>

##### fantastical

[fantastical][] £13.99mac (fantastical2 £2.99ios) make calendar entries by typing in "natural language" e.g. appointment today at 10

fantastical action set using fleksy:

	launch://x-callback-url/clipboard/convert?format=plaintext&x-success=fantastical2%3a%2f%2f[list:fantastical action set|reminder=parse?reminder=1&sentence=|event=parse?reminder=0&sentence=| search=search?query=]{{[prompt-fleksy: send to fantastical]}}

(single square brackets mean the content is auto–encoded)

[fantastical]: http://flexibits.com/fantastical

## list and random timed

<div id="clear"></div>

##### clear

[clear][] £4.99mac, £2.49ios) the original gesture–enabled to–do list. can drag tasks between lists. I use this for lists of tasks that I need to use across devices, and those that I sometimes reuse, e.g. packing lists, things to repair.

[clear]: http://www.realmacsoftware.com/clear/

# publish

## ebook (epub)

<div id="pandoc"></div>

##### pandoc

[pandoc][] free–mac publish custom epub via command line; [pandoc documentation][], [pandoc on ios][] via pythonista and webservice. example [shell script 1][songbook1 script], [shell script 2][songbook2 script], [shell script 3][songbook3 script] for creating three different epubs via pandoc from multiple markdown files, images and audio in the same root folder on a mac.

[pandoc]: http://www.johnmacfarlane.net/pandoc/
[pandoc on ios]: http://wcm1.web.rice.edu/pandoc-on-ios.html
[pandoc documentation]: http://www.johnmacfarlane.net/pandoc/README.html
[songbook1 script]: https://www.dropbox.com/s/h6k8tktblyjegrg/20131119epx-songbook.sh
[songbook2 script]: https://www.dropbox.com/s/j2gy89ow9wt0ncp/20131119epx-songbook2.sh
[songbook3 script]: https://www.dropbox.com/s/goi53748gckwpps/20140309epx-songbook2-audio.sh

## web

##### octopress

[octopress][] freemac oldie but goodie, can integrate with github for hosting pages

[octopress]: http://octopress.org

# rest

## soundscapes

<div id="naturespace"></div>
<div id="thunderspace"></div>

##### thunderspace and naturespace

[naturespace][] and [thunderspace][] pay–ios relaxing recordings of nature sounds created by using microphones placed on a dummy head — recreates spatial relationships really well. I like naturespace's "infinite shoreline" sound a lot; but mainly use thunderspace now.

[naturespace]: http://www.naturespace.com
[thunderspace]: http://thunderspace.me

<div id="show"></div>

## different screen colours at night

<div id="flux"></div>

##### f.lux

[f.lux][] free–mac changes screen colours to make them look warmer (redder) at night

[f.lux]: http://justgetflux.com

<div id="tranquility"></div>

##### tranquility

[tranquility][] free–mac night vision mode; helpful if you are not using a dark theme in your apps by default

[tranquility]: http://www.pixio.com/auto-updating-tranquility/

## range of formats / subtitles

<div id="vlc"></div>

##### vlc

[vlc][] (free mac and ios) plays a lot of different video formats and handles subtitles very well, sometimes buggy on playback

[vlc]: https://videolan.org/vlc/

<div id="infuse2"></div>

## local–wireless transfer

##### infuse2

[infuse2][] (infuse2pro £4.99ios) easy browser transfer of files

[infuse2]: http://firecore.com/infuse

## passwords

<div id="1password"></div>

##### 1password

[1password][] $39.99mac $31.99mac[educational][1password educational] £12.99ios password manager can remember your passwords across different machines. in–built automation limited to browser passwords. ios version restricted to opening passworded links within the app's own browser, use url scheme 

	ophttp://sitelocation

if you want to open a site using launchcenter pro for example, in 1password for ios. 

[1password]: https://agilebits.com/onepassword
[1password educational]: https://agilebits.com/store/educational

# calculator

## pair conversions

<div id="convertizo"></div>

##### convertizo

[convertizo][] freeios

[convertizo]: http://www.perfectdimension.com/apps/convertizo

## multiple conversions

<div id="amount"></div>

##### amount

[amount][] £0.69 convert units, reorder lists of units so your most–often used conversions are at the top of the page.

[amount]: http://marcotorretta.com/#amount

## visual

<div id="calca"></div>

##### calca

[calca][] £1.99ios£2.99mac

[calca]: http://calca.io

## visual scale in unit conversions

<div id="theconverted"></div>

##### the converted

[theconverted][] £1.99ios shows visual scales of conversions, great for showing and learning conversion ranges; reminiscent of a slide rule…

[theconverted]: http://ideon.co/theConverted

## programmable scientific

<div id="pcalc"></div>

##### pcalc

[pcalc][] $9.99ios/mac scientific calculator, if you don't want to do it in python etc.

[pcalc]: http://www.pcalc.com/iphone/

## tally

<div id="tally"></div>

##### tally

[tally][] free–iphone incrementable and decrementable tally, also can use x-callback-url. example [tally url scheme][], increments tally titled "test" and returns to editorial app:

	tally://x-callback-url/increment?title=test&x-success=editorial://

[tally]: http://agiletortoise.com/tally/
[tally url scheme]: http://agiletortoise.com/developers/tally/

## hide menubar icons

<div id="bartender"></div>

##### bartender

[bartender][] $15mac hides icons from menubar

[bartender]: http://www.macbartender.com

## compare file contents

<div id="kaleidoscope"></div>

##### kaleidoscope

[kaleidoscope][] $29.99educationmac nice interface to compare text/image files, folders; with a little bit of scripting/keyboardmaestro, can compare webpage text to yesterday's captured version e.g. set keyboardmaestro to capture the current text, then run

	#!/bin/bash
	DATE_TODAY=$(date +"%Y%m%d")
	DATE_MINUS=$(date -v -1d +"%Y%m%d")
	FILE_CONTENT=$(pbpaste)
	echo "$FILE_CONTENT" >> /path/"$DATE_TODAY"filename.txt
	/usr/local/bin/ksdiff /path/"$DATE_MINUS"filename.txt /path/"$DATE_TODAY"filename.txt

[kaleidoscope]: http://kaleidoscopeapp.com

## graphs

<div id="d3"></div>

##### d3.js

[d3.js][] free–mac is a great javascript library for plotting graphs. I use it to plot data from csv and tsv files.

You need to run a webserver to serve your files. I use an alfred workflow to run a local webserver on my mac: (see [oreilly d3 setup][] for a fuller explanation)

	cd /Users/hereismydatafolderthatiwishtoservelocally
	python -m SimpleHTTPServer 8888 &

And tend to view/print from firefox as css3 transform: translate is better supported currently in firefox than safari or chrome.

* [stacked grouped bar chart][]
* [square circle spiral illusion][]
* [color game][]
* [stacked–to–multiples bar graph][]
* [scott murray's d3 tutorials][]
* [gridlines][]
* [select tutorial][]
* [basic bar chart][]
* [bar chart text append][]
* [oreilly d3 book][]
* [api reference][]
* [variable precision in d3 format][]

[d3.js]: http://d3js.org
[stacked grouped bar chart]: http://bl.ocks.org/gencay/4629518
[square circle spiral illusion]: http://bl.ocks.org/mbostock/1386444
[scott murray's d3 tutorials]: http://alignedleft.com/tutorials/d3/
[stacked–to–multiples bar graph]: http://bl.ocks.org/mbostock/4679202
[color game]: http://color.method.ac/
[gridlines]: http://synthesis.sbecker.net/articles/2012/07/15/learning-d3-part-5-axes
[select tutorial]: http://www.jeromecukier.net/blog/2013/03/05/d3-tutorial-at-strata-redux/
[basic bar chart]: http://mbostock.github.io/d3/tutorial/bar-1.html
[bar chart text append]: http://alignedleft.com/tutorials/d3/making-a-bar-chart/
[oreilly d3 book]: http://chimera.labs.oreilly.com/books/1230000000345/ch02.html
[api reference]: https://github.com/mbostock/d3/wiki/API-Reference
[variable precision in d3 format]: http://stackoverflow.com/questions/10310613/variable-precision-in-d3-format
[oreilly d3 setup]: http://chimera.labs.oreilly.com/books/1230000000345/ch04.html#_setting_up_a_web_server

## web programming

<div id="firefox"></div>

##### firefox and firebug extension

[firefox][] free–mac use with the [firebug][] extension. some of my css3 d3 graph manipulations are better supported in firefox than safari

Printing landscape in firefox: the Portrait and Landscape buttons (available when you use the print dialog in Safari) are not available on the print dialog in Firefox. To change to landscape, go to File - Page Setup and select landscape.

Changing margins in firefox as of 20131009: go to address

	about:config

in the Filter field, type "print", change the relevant values (these differ between versions of firefox)

[firefox]: http://www.mozilla.org/firefox
[firebug]: https://getfirebug.com

## preview/export markdown output

<div id="marked2"></div>

##### marked2

[marked2][] $11.99mac invaluable preview for people who write in markdown

fletcher's guide to [multimarkdown syntax][multimarkdown syntax guide]  
example multimarkdown table: NB the complete specification of the beginnings and ends of lines, this maintains compatibility with both multimarkdown and pandoc

	 ||||
	 |:---|:---|:---|
	 |ᾄδειν | ᾖσε | ᾠδή|
	 |Ἄιδειν | Ἦισε | Ὠιδή|

and this is the resulting table:

||||
|:---|:---|:---|
|ᾄδειν | ᾖσε | ᾠδή|
|Ἄιδειν | Ἦισε | Ὠιδή|

michel's guide to php-markdown/multimarkdown [table syntax][]

[why markdown?]: http://brettterpstra.com/2011/08/31/why-markdown-a-two-minute-explanation/
[table syntax]: http://michelf.ca/projects/php-markdown/extra/#table
[marked2]: http://marked2app.com
[multimarkdown syntax guide]: https://github.com/fletcher/MultiMarkdown/wiki/MultiMarkdown-Syntax-Guide

<div id="learn"></div>

# read

## epub

<div id="marvin"></div>

##### marvin

[marvin][] £1.99ios for reading books in epub format, good customisation options e.g. page forward on tapping left–hand–edge, minimum margins, brightness control gesture, night mode; note does not utilise fonts embedded in epub files

[marvin]: http://marvinapp.com

<div id="ibooks"></div>

##### ibooks

[ibooks][] free–ios/mac for reading books in epub format, displays embedded epub font correctly

[ibooks]: https://itunes.apple.com/us/app/id364709193

# games

## cooperative mayhem

<div id="spaceteam"></div>

##### spaceteam

[spaceteam][] freeios/android cooperative game 2–4 players

[spaceteam]: http://www.sleepingbeastgames.com/spaceteam

## cooperative dance

<div id="bounden"></div>

##### bounden

[bounden][] £2.49ios use an app to dance with a friend?!? any excuse to dance is a good excuse, right?

[bounden]: http://playbounden.com

## get chased by zombies for fitness

<div id="zombies"></div>

##### zombies, run!

[zombies, run!][] pay–ios get chased by (imaginary) zombies :)

[zombies, run!]: https://www.zombiesrungame.com

## yoga

<div id="yogastudio"></div>

##### yogastudio

[yogastudio][] £1.99ios url scheme to open in launch center pro is yogastudio://

[yogastudio]: http://yogastudioapp.com

## knots

<div id="whatknot"></div>

##### what knot to do

[what knot to do][whatknot] free–ios learn some useful knots. I really really like this app.

[whatknot]: http://www.columbia.com/iPhone-Knot-App/iPhone_App_Page-WhatKnot,default,pg.html

## weather

<div id="weatherline"></div>

##### weatherline

[weatherline][] $2.99ios shows trends in weather using annotated line graphs

[weatherline]: http://weatherlineapp.com

# languages

## recognition games

<div id="mindsnacks"></div>

##### mindsnacks

[mindsnacks][] game–based word recognition app

[mindsnacks]: http://www.mindsnacks.com

## sentences and grammar

<div id="duolingo"></div>

##### duolingo

[duolingo][] free–ios sentences and grammar revision courses

[duolingo]: https://www.duolingo.com

## create and drill flashcards

<div id="anki"></div>

##### anki

[anki][] free–mac £17.49ios flashcards for learning through repeat exposure. great for learning languages etc. takes a lot of time to set up, but worth it. if I didn't use pythonista programs ([maki002][], [maki003][]) for text editing on the iphone I would use the desktop version for data entry/editing

[using custom fonts][] for anki mobile; shinsu handwritten and fangsong printed traditional chinese fonts, download at [cooltext.com][]

[anki]: http://ankisrs.net
[using custom fonts]: http://ankisrs.net/docs/am-manual.html#custom-fonts
[cooltext.com]: http://cooltext.com/Fonts-Unicode-Chinese
[maki002]: https://gist.github.com/makiaea/7628665
[maki003]: https://gist.github.com/makiaea/5099182

## astronomy

<div id="skysafari"></div>

##### skysafari pro

[skysafari pro][] £27.99ios great for astronomy, very calming when set on timelapse mode, stars revolving through the sky.

[skysafari pro]: http://www.southernstars.com/products/skysafari/

<div id="shortcuts"></div>

## trackpad/mouse gestures

<div id="bettertouchtool"></div>

##### bettertouchtool

[bettertouchtool][] free–mac versatile tool, e.g. for shortcuts to resize and move windows across two screens.

 |
---: | :---
cmd threefingerswipeup | maximise window
cmd threefingerswipedown | move window to next monitor
cmd threefingerswipeleft | maximise window left
cmd threefingerswiperight | maximise window right
cmd threefingerclickswipeup | maximise window tophalf
<span style="white-space:nowrap;">cmd threefingerclickswipedown</span> | maximise window bottomhalf
**safari–and-finder-specific** |
threefingerswipeleft | switch to next tab (ctrl–tab)
threefingerswiperight | switch to previous tab (ctrl–shift–tab)
**finder-specific** |
twofingerswiperight | back (cmd-[ )
twofingerswipeleft | forward (cmd-] )

[bettertouchtool]: http://www.boastr.de

## create workflows

<div id="alfred"></div>

##### alfred

[alfred][] £17mac find what you need on your mac; I especially like the multiple clipboard and workflows. Favourite alfred workflows are: [faves][] make lists of favourite folders and files, [last changed files][], [recent items][], [wifi toggle][], [create new file][], [show hidden files][], [copy path][], [youtube download][], [mavericks tags][], [keyboardmaestro macros][]

mavericks tags is especially helpful as you can now tag icloud documents in mavericks, and thus you can easily access them using mavericks tags.

[alfred]: http://www.alfredapp.com
[faves]: http://dferg.us/favorite-folders-workflow
[last changed files]: http://www.alfredforum.com/topic/1715-find-files-recently-changed-similar-to-trickster-functionality/
[create new file]: http://alfred.daniel.sh
[wifi toggle]: https://github.com/aiyodk/Alfred-Extensions/tree/master/AlfredApp_2.x/Wi-Fi-Toggle
[show hidden files]: https://www.dropbox.com/s/xj2ayvsmzyd1ln3/Magician.alfredworkflow
[copy path]: http://lucatnt.com/2013/04/some-useful-alfred-2-workflows/
[recent items]: http://www.alfredforum.com/topic/713-recent-docs-folders-apps-favorites-interaction-with-open-and-save-dialogs-now-with-auto-path-30/?hl=%2Brecent+%2Bitems
[youtube download]: http://dferg.us/youtube-download-alfred-2-workflow/
[mavericks tags]: http://markokaestner.com/blog/handle-mavericks-tags-with-alfred
[keyboardmaestro macros]: https://github.com/iansinnott/alfred-maestro

<div id="keyboardmaestro"></div>

##### keyboard maestro

[keyboardmaestro][] £24.45mac automates repetitive tasks. Can also create keyboard shortcuts for the functions or files you want (e.g. [excel paste value][]). Disable and enable macros, e.g. only the set that I want active. Can specify particular macros to be active only within certain apps — good for reusing the same hotkey for slightly different functions in different apps. Use the preferences: sync macros option to save the preferences file to dropbox so you can use the same settings across different computers.

[keyboardmaestro]: http://www.keyboardmaestro.com
[excel paste value]: https://www.dropbox.com/s/9tujfg45kgys2vu/20130405excelpastespecial.kmmacros
[macdrifter.com]: http://www.macdrifter.com/2011/11/keyboard-maestro-variables-remember-current-application.html

<div id="pythonista"></div>

##### pythonista

[pythonista][] £4.99ios run python scripts. e.g. text processing on the iphone

[pythonista]: http://www.omz-software.de/pythonista/

<div id="launch"></div>

##### launch center pro

[launch center pro][] £1.99iphone£2.99ipad can schedule opening of some apps — unfortunately not every single app can be launched. e.g. [new reminder][]; [launch center pro documentation][]; [federico's review of launch center pro 2.1][federicoreview]; example prompt calendar action using fantastical2:

	fantastical2://parse?sentence=[prompt]&notes=&add=1

example timed action using fantastical 2 (set timer to 8am saturday) this asks fantastical to make the new event one month in the future, on same day of the week, and add it immediately (add=1) rather than wait for confirmation

	fantastical2://parse?sentence=<;inserteventnamehere 8am>&notes=&add=1

youtube to set video list

	youtube://[list:youtube action set|gangnam style=9bZkp7q19f0|peppa1=qADHg8BHJJ4|peppa2=0u7-NUjrQXs]

[federicoreview]: http://www.macstories.net/reviews/launch-center-pro-2-1-fleksy-keyboard-lists-photo-attachments-and-share-sheets/
[new reminder]: http://launchcenterpro.com/mfw31w
[launch center pro documentation]: http://help.contrast.co/hc/en-us

[launch center pro]: http://appcubby.com/launch-center/

## keyboard shortcuts

why do keyboard shortcuts help? spend less time searching in menus or moving the mouse/trackpad for often–used functions.

##### basic mac shortcuts

 |
---: | :---
cmd-a | select all
cmd-c | copy
cmd-v | paste
cmd-tab | shift between current and last used application
cmd-w | close current window
cmd-q | close current application
alt-right | move one word right
alt-left | move one word left

##### intermediate mac shortcuts

 |
---: | :---
ctrl-a | beginning of line (or fn-left for home)
ctrl-e | end of line (or fn-right for end)
ctrl-d | forward delete
ctrl-k | kill to end of line
ctrl-y | yank the killed text back (separate from copy paste clipboard)
ctrl-o | paragraph break but keep cursor is same place
ctrl-t | transpose letters
opt-delete | delete previous word
ctrl-b | move back one letter
ctrl-f | move forward one
ctrl-n | move next line
ctrl-p | move previous line
cmd-` | to shift to between the current and next windows within the same application
<span style="white-space:nowrap;">ctrl-cmd-shift-4</span> | select screen area to capture to image in clipboard (handy for pasting screenshots in an email)
ctrl-shift-power | (on macbook air) lock screen, if require password immediately is set for after sleep or screen saver begins
F1-F12 | in system preferences, keyboard; use all F1, F2, etc. keys as standard function keys (press the Fn key to use the special features printed on each key)
tab | in system preferences, keyboard shortcuts; enable full keyboard access (tab can move keyboard focus in all controls)

I like using a dvorak–layout keyboard as I touch–type; this can be set in system preferences — keyboard

<div id="karabiner"></div>
<div id="seil"></div>

## advanced mac rebinding

This technique creates three special keys on your mac keyboard. Initially most people might start with just one special key, *hyper*, and later add others.

 | 
---: | :--- | :---
tab | tap | normal tab
tab | hold | hyper (shift–ctrl–alt–cmd) — less often used
caps lock | tap | access alfred
caps lock | hold | hyper2 (shift–ctrl–cmd) — most often used as it is in the home row
left shift | tap | access alfred snippets
left shift | hold | normal shift

Alfred and keyboardmaestro can be used easily without this, but rebinding three "helper" keys speeds access to shortcuts, applications, macros etc. Caps lock is taken over entirely, while tab and left shift retain their normal usage but are also given an additional property.

Keyboardmaestro is application–aware enough to know when you invoke it within applications, and has options to set shortcuts this way. Thus we can use two discrete levels of shortcuts: one general level, which is the same when activated from any application (hyper2+key), and a second application–specific level, which is unique to each application or set of applications (hyper+key).

You could also separate the usage of hyper2, for example, by combination of letters and numbers — combine hyper2 with letters for applications etc., combine hyper2 with numbers for specific files.

Here we also use Alfred as a shortcut "menu" for those shortcuts which we don't want to commit to memory as a hyper2+shortcut; that is, we activate alfred using caps lock (tap), the type a few letters (e.g. for screen saver, activate alfred, type scr).

Oddly enough, hyper+w, hyper+v, hyper+z, hyper+x do not work on my dvorak keyboard layout, because a dvorak v = . and w = , and z = / and these combinations are reserved for sysdiagnose and stackshot (programmer utilities within the operating system)

An additional bonus of this method is that your hands can stay on the "home row" more, and your left little finger gets more of a workout!

* system preferences keyboard — modifier keys — caps lock key: no action
* [seil][] free–mac setting — caps lock — change caps lock to 80 (F19)  — future options would be cmd_r or opt_r to F18 etc . NB remember to change caps lock configuration in system to "no action" as per [pqrs' notes][]
* [karabiner][] free–mac goto tab misc&uninstall, select open private.xml, paste the following code (based on [brett][] and [pqrs][]); if you already have other modifications there, just paste the "items". The syntax appears to be: (1) key to modify (2) when held, send this (3) when tapped, send this.

here's the code

	<?xml version="1.0"?>
	<root>
		<item>
			<name>F19 to F19</name>
			<appendix>(F19 hold to Hyper2 (ctrl+shift+cmd) + F19 Only, send F19)</appendix>
			<identifier>private.f192f19_cmdshiftctrl</identifier>
			<autogen>
				--KeyOverlaidModifier--
				KeyCode::F19,
				KeyCode::COMMAND_L,
				ModifierFlag::SHIFT_L | ModifierFlag::CONTROL_L,
				KeyCode::F19,
			</autogen>
		</item>
		<item>
			<name>Shift_L to Shift_L</name>
			<appendix>(Shift_L hold to Shift_L + Shift_L Only, send F18)</appendix>
			<identifier>private.shiftl2shiftl_f18</identifier>
			<autogen>
				--KeyOverlaidModifier--
				KeyCode::SHIFT_L,
				KeyCode::SHIFT_L,
				KeyCode::F18,
			</autogen>
		</item>
		<item>
			<name>Tab to Tab</name>
			<appendix>(Tab tap to Tab + Tab hold send Hyper (ctrl+shift+cmd+opt))</appendix>
			<identifier>private.tab2tab_cmdoptshiftctrl</identifier>
			<autogen>
				--KeyOverlaidModifier--
				KeyCode::TAB,
				KeyCode::COMMAND_L,
				ModifierFlag::SHIFT_L | 
				ModifierFlag::OPTION_L | ModifierFlag::CONTROL_L,
				KeyCode::TAB,
			</autogen>
		</item>
	</root>

* go back to change key tab, select reload xml; the options above should now appear at the top of the menu
* enable the options
* you can use misc&uninstall launch eventviewer to see if your new options are working
* restart the computer to finish enabling the keys (you'll want to be able to bring alfred up e.g. with cmd-space later)
* set alfred to activate on F19, alfred features/clipboard/viewer hotkey to F18
* can use same method to allocate "keytap only" to fn, leftshift, leftctrl, leftalt, leftcmd, rightcmd, rightalt or most other keys

[seil]: https://pqrs.org/osx/karabiner/seil.html
[karabiner]: https://pqrs.org/osx/karabiner
[brett]: http://brettterpstra.com/2012/12/08/a-useful-caps-lock-key/
[pqrs' notes]: https://pqrs.org/osx/karabiner/document.html.en
[pqrs]: https://pqrs.org/osx/karabiner/document.html.en

## stop keyboard input

<div id="keyboardcleantool"></div>

##### keyboardcleantool

[keyboardcleantool][] free–mac temporarily disable the keyboard for when a cat wants to sit on your laptop or a baby wants to play with the keyboard

[keyboardcleantool]: http://blog.boastr.net/?p=2452

# miscellaneous

[internal screen rotation][] hold down command and option keys while selecting display preferences in system preferences; note you'll have to close system prefs first. (made a keyboardmaestro macro for this; or if you use alfred, can make separate actions to activate [keyboardmaestro macros][screenrotate] for default, 90 or 270 degrees.)

[internal screen rotation]: http://osxdaily.com/2010/12/28/rotate-mac-screen-orientation
[screenrotate]: https://www.dropbox.com/s/pw9vyn1pdhryl41/20140604makiaeascreenrotation.kmmacros

<div id="midisheetmusic"></div>
[midisheetmusic][] free–mac download a midi file and play it with just the computer while displaying sheet music. if you want to play the midi through to the piano, then can download the free version of synthesia and it will do it for you.

[midisheetmusic]: http://sourceforge.net/projects/midisheetmusic/

<div id="aria"></div>
<div id="musescore"></div>

[aria maestosa](http://ariamaestosa.sourceforge.net) and [musescore](http://musescore.org) free–mac midi players and editors

[print to pdf][] great way to use the keyboard to open/print to pdf; create keyboard shortcut for the submenu as follows: system preferences - keyboard - shortcuts - all applications - add

	Save as PDF…
	Open PDF in Preview

assign these as cmd-s and cmd-o. When printing, i.e. cmd-p as usual, you now have shortcuts for the submenus, cmd-s and cmd-o. You may be able to do the same for other applications.

[print to pdf]: http://macsparky.com/blog/2013/10/print-to-pdf-revisited


<div id="parallels"></div>
[parallels desktop][] £34.95mac [education price][parallels education store price] if you need to use a virtual machine, this is worth the investment

[parallels desktop]: http://www.parallels.com/products/desktop/
[parallels education store price]: http://store.apple.com/uk-edu/product/H9892ZM/B/parallels-desktop-8-for-mac-education-edition


recommended safari extensions: 1password and adblock


<div id="multimarkdowncomposer"></div>
[multimarkdown composer][] £7.99mac text editor with excellent multimarkdown support — if sublime text is too complex, and your files are not the length of novels

[multimarkdown composer]: http://multimarkdown.com

 epub audio, with controls, looping, and autoplay, e.g.

	<audio src="audio/20140117imagine-original-clip-songbook.mp3" controls="controls" loop="loop" autoplay="autoplay">piano only</audio>

## creating

ios speak text — turn on via settings.app — general — accessibility — speak selection ON — voices — e.g. chinese (Hong Kong Sar China) — enhanced quality (very good speech synthesis, use by highlighting text and selecting the speak option)

In Finder, sort by reverse modified date, so most–recently modified files/folders appear at the top. Prepend files with creation date. I use a Keyboard Maestro "hyper2" shortcut to produce YYYYMMDD.

## typing polytonic greek on mac
unfortunately still not available in ios, but very usable on mac:

system preferences - keyboard - input sources; add greek - polytonic

system preferences - keyboard - shortcuts - input sources; select a key combination for changing the input source, e.g. hyper2–`

type a combination of keys to specify accents for the letter, before you enter the accented letter:

 |
---: | :--- | :---
smooth breather | ᾽ | ' 
rough breather | ῾ | " 
acute | ´ | ; 
diaresis | ¨ | :
circumflex | ῀ | \[ 
iota subscript | ι | {
grave | ` | ]
grave (also) | ` | }
circumflex with smooth breather | ῏ | - 
circumflex with rough breather | ῟ | _
acute with smooth breather | ῎ | /
acute with rough breather | ῞ | ?

you can get by with the single combining accents until you are comfortable with them, and then add the other keys as you gain speed. There are several other keys you can use, for grave with smooth or rough breather, diaresis with acute etc. ( ῍ ), ( ῝ ), ( ΅ )

Keyboardmaestro is very helpful in that it can keep the "locations" of its own shortcut keys the same across different input keyboards — for example when I use my normal em–space key combination, it is typed using the same physical keys on the keyboard and I don't have to shift gears to use the other alphabet for those shortcuts (I still have to shift for system–integrated i.e. non–keyboardmaestro shortcuts such as copy and paste).

for rarer accents such as ῑ, ῡ, ᾱ, ῒ, ΐ, ῐ, ᾰ, I use keyboardmaestro macros to insert the characters; for even rarer accents such as ᾱ́, ῑ́, ῡ́, ᾰ́, ῐ́, I also use keyboardmaestro macros but need additionally to use the unicode combining acute ( ́ ) NB you can copy and paste that combining acute into your own macros to use it, or search for "combining acute" in the character viewer and copy from there.

keyboardmaestro is also very helpful for creating emacs–style bindings for often–used keys combinations that would be awkward to type in sublime text when the keyboard input method is set to greek polytonic, e.g. I set hyper2–l (dvorak equivalent ctrl–n) to do "move cursor down to next line, after inserting a full stop", hyper2–d (dvorak equivalent ctrl–e) to do "move cursor to end of line".
