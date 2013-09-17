---
layout: page
title: "macosx and ios recommendations"
date: 2013-08-21 16:12
comments: true
sharing: true
footer: true
---

* <a href="#macosxbasic">macosx basic</a>
* <a href="#macosxintermediate">macosx intermediate</a>
* <a href="#macosxadvanced">macosx advanced</a>
* <a href="#iosbasic">ios basic</a>
* <a href="#iosintermediate">ios intermediate</a>
* <a href="#iosadvanced">ios advanced</a>

<div id="macosxbasic"></div>

#macosx basic

##basic keyboard shortcuts

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

I like using a dvorak–layout keyboard as I touch–type; this can be set in system preferences — keyboard

##[alfred][]

alfred preferences — alfred hotkey: cmd+space  
[alfred faves workflow][] creates lists of favourite folders and files  
[alfred last changed files workflow][] hans' rename file workflow is also nice  
[wifi toggle][] turns wifi on/off  
[alfred create new file workflow][] Create a file in the frontmost Finder window. Enter touch followed by a filename to create a file. You can hold down “Command” while pressing “Return” to open the file after it’s created. This workflow also uses Alfred’s new feedback system: by selecting the options in the results list, you can store commonly-created filenames for faster access or store paths where you often create files, which can then be accessed by entering touch, a filename, and the keyword at. Hold down “Control” while pressing “Return” to forget saved paths and filenames  
[alfred show hidden files workflow][] Show and hide hidden files in Finder  
[alfred copy path workflow][] copies the path of the selected file in Finde

[alfred]: http://www.alfredapp.com
[alfred faves workflow]: http://dferg.us/favorite-folders-workflow
[alfred last changed files workflow]: http://www.alfredforum.com/topic/1715-find-files-recently-changed-similar-to-trickster-functionality/
[alfred create new file workflow]: http://alfred.daniel.sh
[wifi toggle]: https://github.com/aiyodk/Alfred-Extensions/tree/master/AlfredApp_2.x/Wi-Fi-Toggle
[alfred show hidden files workflow]: https://www.dropbox.com/s/xj2ayvsmzyd1ln3/Magician.alfredworkflow
[alfred copy path workflow]: http://lucatnt.com/2013/04/some-useful-alfred-2-workflows/


##storing data
All non–security–sensitive important data saves to a single folder that is shared with dropbox. this provides an offsite copy and enables reliable syncing between phone and computer.

To get the most of this, when I display this special folder in Finder, I sort by reverse modified date (so that most recently modified files/folders) appear at the top. Each file is prepended with the date of creation (or another more relevant date) in the form YYYYMMDDexampleprefix.andsuffix this makes finding today's files especially easy (or any other files for which you know the creation date) via Alfred (open alfred, choose file search, enter today's date — the key sequence for me is "caps lock", "space", ";dd"). I use Keyboard Maestro (see later) to set the date via the ";dd" shortcut to produce YYYYMMDD, you can use many simpler or more complex methods to do the same.

##[dropbox][]
(free) great service. I use it to backup and share a single folder of (mainly) text files

[dropbox]: https://www.dropbox.com/tour

##[f.lux][]
(free) alters the colours on the screen to make it look nicer during nighttime (when you need colour–accuracy, you can switch it off)

[f.lux]: http://justgetflux.com

##[vlc][]
(free) plays a lot of different video formats and can handle subtitles

[vlc]: https://videolan.org/vlc/

<div id="macosxintermediate"></div>

#macosx intermediate

##intermediate keyboard shortcuts

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
ctrl-b | move back one
ctrl-f | move forward one
ctrl-n | move next line
ctrl-p | move previous line
cmd-` | to shift to between the current and next windows within the same application
<span style="white-space:nowrap;">ctrl-cmd-shift-4</span> | select screen area to capture to image in clipboard (handy for pasting screenshots in an email)
ctrl-shift-power | (on macbook air) lock screen, if require password immediately is set for after sleep or screen saver begins
F1-F12 | in system preferences, keyboard; use all F1, F2, etc. keys as standard function keys (press the Fn key to use the special features printed on each key)
tab | in system preferences, keyboard shortcuts; enable full keyboard access (tab can move keyboard focus in all controls)

##[keyboardmaestro][]
£24.45 but super useful for automating repetitive tasks. I also use it for text replacement (instead of using the MacOSX built–in text replacement, or textexpander) — it can do date formatting, which I often use in filenames. If you have an application that does not have working keyboard shortcuts for the functions you want, you can create them yourself using keyboardmaestro. (e.g. [excel paste value][]) I also like that I can disable and enable macros at will, so it is possible to enable only the set that I want active currently rather than all the macros I ever use. I often use Alfred to launch keyboardmaestro macros via applescript.

A useful advantage of using keyboardmaestro for macro creation is that you can specify precisely which apps you must be in to run a particular macro; this is especially good for reusing the same hotkey for slightly different functions in different apps.

I would recommend *not* using keyboard maestro's image recognition because it can be processor intensive (my macbook air 2010 became very hot) this may be because very rarely it fails to recognise an image and keeps searching "forever".

Use the preferences: sync macros option to save the preferences file to dropbox so you can use the same settings across different computers.

[keyboardmaestro]: http://www.keyboardmaestro.com
[excel paste value]: https://www.dropbox.com/s/9awnbcaaszrl0ql/20130405excelpastespecial.kmmacros

##[bettertouchtool][]
(free) versatile tool, I use it simply for shortcuts to resize and move windows across two screens, selecting a key and mouse combination that can be used with one hand. have hidden the menubar icon, so to access the preferences, start the app

 |
---: | :---
cmd threefingerswipeup | maximise window
cmd threefingerswipedown | move window to next monitor
cmd threefingerswipeleft | maximise window left
cmd threefingerswiperight | maximise window right
cmd threefingerclickswipeup | maximise window tophalf
<span style="white-space:nowrap;">cmd threefingerclickswipedown</span> | maximise window bottomhalf
**safari–specific** |
threefingerswipeleft | switch to next tab (ctrl–tab)
threefingerswiperight | switch to previous tab (ctrl–shift–tab)

[bettertouchtool]: http://www.boastr.de

##[shortcat][]
(free, may not be free in future) allows you to select elements on screen via accessibility functions to create keyboard shortcuts for onscreen UI elements (only works with programs that have accessibility functions enabled). Very useful you want to write keyboardmaestro macros making use of this ability (I find this more reliable and less processor intensive than using keyboardmaestro's inbulit image recogintion, where it can be used). *default shortcut access using shift-cmd-space*

I use this often in keyboardmaestro macros to open up the 1password popup in safari

[shortcat]: http://shortcatapp.com

##[anki][]
(free for desktop, expensive for mobile) i use the mobile version mainly, but if I didn't have pythonista programs for text editing on the iphone I would have to rely instead on the desktop version for data entry/editing

[anki]: http://ankisrs.net

##[marked][]
£2.49 most people use this to preview their markdown, I sometimes use this as an alternative window into the document I am editing.

fletcher's guide to [multimarkdown syntax][multimarkdown syntax guide]  
michel's guide to php-markdown/multimarkdown [table syntax][]

[table syntax]: http://michelf.ca/projects/php-markdown/extra/#table
[marked]: http://markedapp.com
[multimarkdown syntax guide]: https://github.com/fletcher/MultiMarkdown/wiki/MultiMarkdown-Syntax-Guide

##[multimarkdown composer][]
£7.99 if sublime text is too complex (yes it reminds me of emacs); my other favourite simple text editor as I keep notes in large files and use markdown a lot; I use a customised solarized dark theme, and I like how the smart pairs function works and that links are clickable in editing mode

[multimarkdown composer]: http://multimarkdown.com

##[1password][]
$49.99 in–built automation limited to browser passwords, but you can use keyboardmaestro to help with other password systems (e.g. vpn). expensive but the saved time is worth it.

[1password]: https://agilebits.com/onepassword

##[fantastical][]
£13.99 I don't start this at login because I don't like the icon cluttering my menubar — there is no option to disable it, even via broomstick though if you pay for bartender, it will hide it for you)

[fantastical]: http://flexibits.com/fantastical

##[parallels desktop][]
£29.95 [parallels education store price][] if you have to use a virtual machine for work like I do, this is worth the investment (in my case I have to use the Windows version of MS Access!)

[parallels desktop]: http://www.parallels.com/products/desktop/
[parallels education store price]: http://store.apple.com/uk-edu/product/H9892ZM/B/parallels-desktop-8-for-mac-education-edition

##[inkscape][]
(free) SVG vector graphics editor; .svg vector graphics files can be edited and rescaled without loss of fidelity

[inkscape]: http://inkscape.org

##[handbrake][]
(free) convert dvds to movie files

[handbrake]: http://handbrake.fr

##[gimp][]
(free) bitmap graphics editor

[gimp]: http://www.gimp.org

##[filezilla][]
(free) file transfer client that works with secure FTP (sFTP)

[filezilla]: https://download.filezilla-project.org

##[clear][]
£4.99 mainly use to drag tasks between lists (multiple window support) and rearranging lists; otherwise use iphone version instead

[clear]: http://www.realmacsoftware.com/clear/

##[due][]
£6.99 use iphone app mainly

[due]: http://www.dueapp.com

##[byword][]
£6.99 I now use sublime text instead, but that's much more expensive. Byword has a useful focus mode (shortcut cmd-enter) hides/dims everything except your chosen text (line, paragraph)

[byword]: http://bywordapp.com

##[nvalt][]
(free) I don't use this much anymore, as I prefer to consolidate my notes into larger files organised by subject

nvaltforgtd is a nice way to use nvalt for gtd, tagging http://mcdaniel.blogs.rice.edu/?p=153
nv tips http://bitfieldconsulting.com/notational-velocity

[nvalt]: http://brettterpstra.com/projects/nvalt/

##[midisheetmusic][]
(free) am very impressed with the free midi sheet music program. download a midi file and play it with just the computer while displaying sheet music. if you want to play the midi through to the piano, then can download the free version of synthesia and it will do it for you.

[midisheetmusic]: http://sourceforge.net/projects/midisheetmusic/?source=dlp

<div id="macosxadvanced"></div>

#macosx advanced

##advanced keyboard rebinding

 | 
---: | :--- | :---
caps lock | tap | access alfred
caps lock | hold | shift–ctrl–alt–cmd
right shift | tap | access alfred snippets
right shift | hold | normal shift

I don't want to remember a lot of shortcut keys; alfred allows me to use shortcuts in a slightly different way, by typing a few letters (e.g. for screen saver, activate alfred, type scr) I make this more practical by binding tapping the caps lock key to activate alfred, via a combination of system preferences, pckeyboardhack and keyremap4macbook. I also rebind holding down the caps lock key to represent shift–ctrl–alt–cmd and also tapping the right shift key to the alfred snippets/clipboard history as I use this function a lot as well (it's surprising how useful multiple copy/paste can be once you are used to it)

* **system preferences** keyboard — modifier keys — caps lock key: no action
* **[pckeyboardhack][]** (free) setting — caps lock — change caps lock to 80 (F19)  — future options would be cmd_r or opt_r to F18 etc . NB remember to change caps lock configuration in system to "no action" as per http://pqrs.org/macosx/keyremap4macbook/pckeyboardhack-usage.html.en
* **[keyremap4macbook][]** (free) goto tab misc&uninstall, select open private.xml, paste the following code (based on [brett][] and [pqrs][]); if you already have other modifications there, just paste the "items"

here's the code

	<?xml version="1.0"?>
	<root>
		<item>
			<name>F19 to F19</name>
			<appendix>(F19 hold to Hyper (ctrl+shift+cmd+opt) + F19 Only, send cmd+space)</appendix>
			<identifier>private.f192f19_cmdspace</identifier>
			<autogen>
				--KeyOverlaidModifier--
				KeyCode::F19,
				KeyCode::COMMAND_L,
				ModifierFlag::OPTION_L | ModifierFlag::SHIFT_L | ModifierFlag::CONTROL_L,
				KeyCode::F19,
			</autogen>
		</item>
			<item>
			<name>Shift_R to Shift_R</name>
			<appendix>(Shift_R hold to Shift_R + Shift_R Only, send F18)</appendix>
			<identifier>private.shiftr2shiftr_f18</identifier>
			<autogen>
				--KeyOverlaidModifier--
				KeyCode::SHIFT_R,
				KeyCode::SHIFT_R,
				KeyCode::F18,
			</autogen>
		</item>
	</root>

* go back to change key tab, select reload xml; the two options above should now appear at the top of the menu
* enable both options
* restart the computer to finish enabling the keys (you'll want to be able to bring alfred up e.g. with cmd-space later)
* set alfred to activate on F19, alfred features/clipboard/viewer hotkey to F18
* can use same method to allocate "keytap only" to fn, leftshift, leftctrl, leftalt, leftcmd, rightcmd, rightalt or most other keys

**[keyboardcleantool][]** (free) lovely tool temporarily disables the keyboard for when a cat wants to sit on your laptop or a baby wants to play with the keyboard

[pckeyboardhack]: http://pqrs.org/macosx/keyremap4macbook/pckeyboardhack.html.en
[keyremap4macbook]: http://pqrs.org/macosx/keyremap4macbook
[keyboardcleantool]: http://blog.boastr.net/?p=2452
[brett]: http://brettterpstra.com/2012/12/08/a-useful-caps-lock-key/
[pqrs]: https://pqrs.org/macosx/keyremap4macbook/document.html

**[internal screen rotation][]** hold down command and option keys while selecting display preferences in system preferences; note you'll have to close system prefs first. (made a [keyboardmaestro macro][screenrotate] for this)

[internal screen rotation]: http://osxdaily.com/2010/12/28/rotate-mac-screen-orientation
[screenrotate]: https://www.dropbox.com/s/ky1fu275p4cdmxr/screenrotation.kmmacros

**[pmset][]** slow waking from sleep because of battery saving settings (warning: while doing this will make it quicker for the machine to return from standby, it will drain more battery more quickly). default is 3600 (1 hour)

* check current settings: pmset -g
* change to 24hours by: sudo pmset -a standbydelay 86400
* change to 2hours by: sudo pmset -a standbydelay 7200

[pmset]: http://www.ewal.net/2012/09/09/slow-wake-for-macbook-pro-retina/

##[sublime text][]
$70 (no educational discount) expensive but powerful (and speedy) editor. the distraction–free mode and solarized(dark) theme are nice too. I also like the smart pairs function. Emacs may be a better long–term investment but sublime text is easier for a newcomer to use.

 | 
---: | :---
cmd–r | (goto symbol) allows you to move between headers easily in a markdown document
cmd–p | (goto anything) then # then searchterm to jump to next occurrence in the current document
ctrl–minus | jump back (sublime text 3–only)
cmd–ctrl–p | switch project within window (make some projects to hold collections of files/folders that you use together) — though in practice am using two windows (often placed directly over each other) for two different projects and switching between them using cmd–`
cmd–d | select word, repeat to use multiple cursors to select subsequent words/phrases
cmd–u | unselect word/phrase
cmd–k–d | (sequential k then d) to skip to next candidate. left or right to move cursors within selected word
cmd–ctrl–g | select all occurrences of word/phrase
cmd–click | non–successive lines start multiple cursor, or
<span style="white-space:nowrap;">cmd–shift–L</span> | highlight column with cursor then cmd–shift–L to start column–mode multiple cursor (useful if you want to edit multiple lines at specified places). you can move the cursors as you would a normal cursor e.g. cmd–left to go to the beginning of the line (if you have text running across multiple lines you might want to do cmd–left a few times to ensure it really is the beginning of the line rather than the beginning of the wrapped line)

modify by going into sublime text preferences — browse packages

my current sublime text preferences — user preferences

	{
		"caret_style": "solid",
		"color_scheme": "Packages/User/makiaea.tmTheme",
		"font_face": "AvenirNext-UltraLight",
		"font_size": 11.0,
		"gutter": false,
		"line_numbers": false
	}

my current sublime text preferences — distraction free preferences
 
	{
 		"font_size": 24,
 		"wrap_width": 0
	}

my current sublime text VBScript.sublime-settings (there are a lot of comments in the code I have to work with, so word wrap is on…)

	{
		"gutter": true,
		"line_numbers": true,
		"wrap_width": 0,
		"word_wrap": "true"
	}

my current theme is based on a custom solarized dark theme with markdown highlighting https://gist.github.com/eleclerc/1904917/download#
and is stored in /Users/maki/Library/Application Support/Sublime Text 3/Packages/User/makiaea.tmTheme

you can create your own shortcuts to projects or even open them from the command line e.g.  for sublime text 3: /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /Users/maki/Documents/Dropbox/datafiles/20130416maki.sublime-project

If you need to use VBScript syntax highlighting, https://github.com/SublimeText/VBScript is a nice package to download

I set a keyboardmaestro shortcut F1 to switch to sublime text, and keyboardmaestro cmd–enter to toggle distraction free mode

Set [marked][marked build] to open current (markdown) file, processed (uses build, shortcut cmd-b)

[marked build]: http://support.markedapp.com/kb/how-to-tips-and-tricks/marked-bonus-pack-scripts-commands-and-bundles

[sublime text]: http://www.sublimetext.com

##[d3][]
d3.js is a great javascript library for plotting graphs. I use it to plot data from csv and tsv files.

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

[d3]: http://d3js.org
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

##[mamp][]
useful for testing d3 locally, alternatively use the python web server as explained in [oreilly d3 setup][] and above. 

* download, install
* open new app "mamp"
* select server root directory
* select start page (use notation relative to root)
* set to start servers on mamp start
* set to stop servers on mamp stop
* [mamp documentation][]
* your localhost is something like http://localhost:8888/MAMP/?language=English

[mamp]: http://www.mamp.info/en/index.html
[mamp documentation]: http://documentation.mamp.info/en/mamp/first-steps
[oreilly d3 setup]: http://chimera.labs.oreilly.com/books/1230000000345/ch04.html#_setting_up_a_web_server

##[launchservices][]
for developers that launch apps a lot: rebuild your Launch Services database on Mountain Lion (use at your own risk!):

	sudo /System/Library/Frameworks/CoreServices.framework/Versions/Current/Frameworks/LaunchServices.framework/Support/lsregister -kill -r -domain local -domain system -domain user

[launchservices]: http://furbo.org/2013/04/22/launch-services-woes/

##quickcursor replacement
set ctrl–alt–cmd–delete to extract all text from current document, remember current application, open sublime text, paste  
waits until ctrl–alt–cmd–w to extract all text from current document, switch to previous remembered application, paste

based on:  
http://rocketink.net/2013/05/quickcursor-keyboard-maestro.html  
http://www.macdrifter.com/2011/11/keyboard-maestro-variables-remember-current-application.html

##useful helper programs

###safari extensions
* 1password
* adblock
* maybe (facebook cleaner)

###vpn toggle
using combination of 1password, keyboardmaestro, applescript and alfred for quick vpn toggling

* set record for password in 1password
* create macro in keyboardmaestro that opens 1password (pauses for you to type in password if you need to), searches for the record, copies the password into the clipboard
* runs the applescript to toggle vpn, which is already set with the vpn details
* pastes the password into the vpn window and starts it

to run, use the keyboardmaestro trigger by applescript, and paste that trigger applescript into alfred workflow with trigger vpn

###[broomstick][]
(free) hide f.lux, spotlight and dropbox icons from menubar. If you want a more comprehensive app and are willing to pay $15, try [bartender][]

[broomstick]: http://www.zibity.com/broomstick
[bartender]: http://www.macbartender.com

###[audacity][]
(free) open–source audio recorder

[audacity]: http://audacity.sourceforge.net

###[firefox][]
useful web browser, I use this with the [firebug][], [printedit][], [doubletapzoom][] extensions, and because some of my d3 graph manipulations don't work yet in my version of safari

Printing landscape in firefox: the Portrait and Landscape buttons (available when you use the print dialog in Safari) are not available on the print dialog in Firefox. To  change to landscape, go to File - Page Setup and select landscape.

[download youtube videos as mp4][] firefox extension to download and convert to mp4 (appears as "download" button within the firefox window)

[firefox]: http://www.mozilla.org/firefox
[firebug]: https://getfirebug.com
[printedit]: https://addons.mozilla.org/en-US/firefox/addon/print-edit/
[doubletapzoom]: https://addons.mozilla.org/en-us/firefox/addon/pinch-to-zoom-and-double-ta/
[download youtube videos as mp4]: https://addons.mozilla.org/en-us/firefox/addon/download-youtube/

###[ffmpeg][]
(free) open–source encoder (binary)

[ffmpeg]: http://ffmpegmac.net

###[pandoc][]
(free) publishing custom epub via command line

[pandoc]: http://www.johnmacfarlane.net/pandoc/

###[github][]
(free) share and store code online

[github]: https://github.com

###fsck to check hard disk
I run this occasionally (my disk is /dev/disk1, yours may be different)

	sudo fsck_hfs -l /dev/disk1

###[gpg][]
not that it seems to mean much in the PRISM era, but if you are expected to encrypt communications for legal reasons, then gpg is a good way of doing it. Also, [enigmail][] + thunderbird

[gpg]: https://gpgtools.org/#gpgsuite
[enigmail]: https://addons.mozilla.org/en-US/thunderbird/addon/enigmail/

###[fontforge][]
mac binary made by Pedro Amado

[fontforge]: http://www.typeforge.net/blog/2011/05/23/fontforge-binaries/

##block websites
set any websites you want to block in the following manner

	sudo nano /etc/hosts

add a line for each website you want to block:

	127.0.0.1 facebook.com

this tells the system to try to look for facebook.com locally — it will not find it, so returns page not found. optionally, flush the cache:

	dscacheutil -flushcache

<div id="iosbasic"></div>

#ios basic

##[what knot to do][whatknot]
(free) learn some useful knots. I really really like this app.

[whatknot]: http://www.columbia.com/iPhone-Knot-App/iPhone_App_Page-WhatKnot,default,pg.html

##[ibooks][]
(free) for reading books in epub format

[ibooks]: https://itunes.apple.com/us/app/id364709193

##[naturespace][] and [thunderspace][]
(free, £0.69) I like naturespace's "infinite shoreline" sound a lot; the lightning effect in thunderspace is great!

[naturespace]: http://www.naturespace.com
[thunderspace]: http://thunderspace.me

##[cobook][]
(free) combines your addressbooks

[cobook]: https://cobook.co

##[dropbox][]
(free) installing the app allows other apps access to your files on dropbox

[dropbox]: https://www.dropbox.com/mobile

##[mailbox][]
(free) currently only works for google mail accounts; great way of clearing your inbox, as it uses swipe actions to sort and move messages into the three categories I use: (a) to do, (b) to keep, (c) to wait. I use a similar system with email on my laptop by setting keyboard maestro shortcuts for the three categories that are restricted to the email program (F10 -> a, F11 -> b , F12 -> c, all conveniently located near the delete button; also cmd–F09 -> view inbox, cmd–F10 -> view folder a etc. NB this is easy in Thunderbird, as you can specify to move to or view folders, but Apple Mail workaround is to use favourite folders (drag and drop into favourites bar) and then use keyboardmaestro macros to activate standard favourite folders shortcuts… outcome is that you can hide your mailbox tree pane if you no longer need it.)

[mailbox]: http://www.mailboxapp.com

##[clear][]
£1.49 changed the use of gestures on non–jailbroken iphones; still a great todo list

##[vlc][]
(free) excellent support for different filetypes and subtitles

##[goodreader][]
£2.99 read pdfs and watch videos (note that subtitles do not appear to work well). also has good instructions for using [password access control][] on files or folders

[goodreader]: http://www.goodiware.com/goodreader.html
[password access control]: http://goodiware.com/gr-man-general.html#password

##[yogastudio][]
£1.99 url scheme to open in launch center pro is yogastudio://

[yogastudio]: http://yogastudioapp.com

##[zombies, run!][] and zombies, run! 2
get chased by (imaginary) zombies :)

[zombies, run!]: https://www.zombiesrungame.com

<div id="iosintermediate"></div>

#ios intermediate

##[due][]
I this for repeating reminders as it is very flexible in setting times e.g. repeat on three weekdays only. You can also add urls (and non–website ios urls) to the reminder, which will open automatically on completing the reminder.

example [due url scheme][] code:

	due:///add?title=entertitlehere&secslater=enternumberofsecondshere

due still asks us to confirm the timer addition but 

[due url scheme]: http://www.dueapp.com/developer.html

##[fantastical][]
best calendar i have used so far

##[felix][]
(not free) app.net client for ios. responsible developer, unlike netbot

[felix]: http://www.tigerbears.com/felix/

##[drafts][]
£1.99 currently my go–to place to temporarily store text ideas until I can process them. (input may be directly into drafts or from fleksy etc.) Use custom dropbox actions (this requires network connection) to append text to several specific files in my dropbox, set to automatically delete the draft after the action is complete — this helps streamline the workflow. I open one of the dropbox files when it is convenient, often on my macbook air, to process the text into its appropriate place. You can search your text in drafts, which byword cannot do. I also use it in conjunction with pythonista for anki data entry. Its [x-callback-url][] scheme is good for chaining automatic actions together on ios.

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

##[launch center pro][]
£1.99 use this mainly to launch pythonista scripts, drafts actions, and schedule opening of some apps. This greatly speeds up access to apps (although there are other faster ways if your iphone is jailbroken, via activator). unfortunately not every single app can be launched.

example timed action (set timer to 8am saturday) this asks fantastical to make the new event one month in the future, on same day of the week:

	fantastical://parse?sentence=<;inserteventnamehere 8am>&notes=

[launch center pro]: http://appcubby.com/launch-center/

##[pythonista][]
£4.99 run python scripts. I use this for text processing on the iphone, specifically for anki data input

[pythonista]: http://www.omz-software.de/pythonista/

##[fleksy][]
(free) a great keyboard for ios (I use invisible silent keyboard mode) — only has a qwerty keyboard, sadly no dvorak option yet. literally can type without looking at the screen. You must then move the text into another program for editing.

[fleksy]: http://fleksy.com

##[anki][]
£17.49 great for learning languages etc. takes a lot of time to set up, but worth it

##[1password][]
£12.99 password manager. restricted currently to opening passworded links within the app's own browser, use url scheme 

	ophttp://sitelocation

if you want to open a site using launchcenter pro for example, in 1password. does not sync currently very easily but will do eventually — but question is, do you want your password files to be on the web, even if encrypted?

##[skysafari pro][]
£27.99 great for astronomy, very calming when set on timelapse mode, stars revolving through the sky.

[skysafari pro]: http://www.southernstars.com/products/skysafari/

##[textexpander touch][]
£2.99 I use this for date expansion from a shortcut i.e. dda —> 20130319, as we can't use keyboardmaestro shortcuts in ios like we do on macos

[textexpander touch]: http://www.smilesoftware.com/TextExpander/touch/index.html

##[byword][]
£1.99 Unfortunately you cannot search text so longer files are hard to edit only on ios (rather than using the macos app). most ios text editors cannot do searching or jumping within the text to the term you have searched for, hopefully one will be developed soon that can do this. Brett Terpstra has a [nicely categorised table of ios text editors][]

[nicely categorised table of ios text editors]: http://brettterpstra.com/ios-text-editors/

##[editorial][]
£2.99 better than byword, but I don't have an ipad to use it with :) can't wait for an iphone version…

[editorial]: http://omz-software.com/editorial/

##[snappycam][]
£0.69 slightly lower quality than iphone native photographs, but at full iphone resolution, for bursts of up to 20fps. Helpful for capturing baby photos!

[snappycam]: http://www.snappycam.com

##[prizmo][]
£2.99 optical character recognition in scans does not require network connection, unlike some other scanning apps

[prizmo]: http://www.creaceed.com/iprizmo/about

<div id="iosadvanced"></div>

#ios advanced
the following apps are only available after jailbreaking the iphone, via the cydia jailbreak store; some of these issues are addressed by ios7. note that jailbreaking can break functions such as siri, so there are some downsides.

##jailbreaking gotcha
after backing up the phone,  wiping the phone, jailbreaking, then restoring the phone, you might experience a heart–stopping moment when you think that all you notes and application data may have been erased from the phone. This can occur if you have iTunes set not to sync applications — and if your notes are in applications that have not been synced or reinstalled since the wipe, then although the data is there in the data folders, the applications to reach the data are not (for the moment) available… I've forgotten this more than once and it's a shock until you remember!

##activator
(free) I no longer have to use the home button much. Finger gestures can be set via the Activator app to do many of the actions for which I would have previously needed to use the home button. For example, returning to the springboard homescreen (the icon screen) or to change from one app to another.

 | 
 ----: | :----
slide single topleft down | fleksy
slide single topcentre down | launch center pro (see section above)
slide single topright down | sleep
slide single left in | ibooks
slide single right in | whatknot
slide single bottom left up | home button
<span style="white-space:nowrap;">slide single bottom centre up</span> | switcher
slide single bottom right up | bluetooth preferences (e.g. quickly add bluetooth keyboard)
slide single top out | thunderspace
slide single left out | 
slide single right out | anki
slide single bottom out | lastapp (changes to last used app) start from above keyboard if showing, to prevent accidental keystrokes)
slide left side up | clear
slide left side down | drafts
slide right side up | due
slide right side down | fantastical
power connected | sleep
power disconnected | sleep
slide left status bar | airplane toggle
slide right status bar | wifi toggle
hold status bar | rotation
slide double top down | activator
both volume buttons | snappycam (for quickest access) also activator disabled within snappycam so important events not missed
toggle mute switch twice | flashlight toggle (to prevent accidental toggle) plus sleep screen
tap and hold on status bar | rotation toggle
five finger pinch | volume down
five finger spread | volume up
four finger pinch | play/pause toggle
four finger spread | clock

this enables silent operation of the iPhone if you learn how to tap softly — if you regularly wake to take notes in the middle of the night while sharing a bed with a sleeping spouse or partner you will especially appreciate this!

##lastapp
(free) used in conjunction with activator to change to the last used app

##winterboard
(free) allows me to remove both the text under the icons and the text under the folders. download the "no clock" theme for winterboard and use it to remove the clock from the status bar (when you need the clock you can still use the clock app — i tend to set reminders in the due app mostly instead)

##nolockscreen
(free) the lockscreen is redundant for me. I keep no unencrypted secret data on my phone, and it is almost always with me. Thus I don't benefit from the lockscreen other than helping to switch off the phone quickly when the phone is inadvertently activated. So it is worthwhile for me to use the free jailbreak NoLockScreen app, which bypasses the lockscreen. As someone who turns off the screen on the phone a lot, there's a significant time and immediacy gain. 

##f.lux
(free) changes the hue of the phone's screen depending on what time of day it is. 

##swipeselection
(free) allows us to swipe on the keyboard to move the cursor or in conjunction with shift, to select text.

##sbprofiles
20130803 i don't use this anymore. unfortunately not 100% reliable currently (free; requires sbsettings to be downloaded and run once, wireless trigger (not toggle) requires payment) add airplane sbsettings toggle. I use this to automatically turn off airplane mode on certain mornings of the week, and turn it on again in the evening, turn on location tracking and open zombies, run! at the same time, etc. also it is quicker for turning on/off wifi etc than using ncsettings because it doesn't require you to close the notification centre after use. however it does need several minutes set up before it can be used, unlike ncsettings which is almost ready for immediate use.

##ncsettings
(free) if you don't want to set up profiles for your toggles with snprofiles, them ncsettings allows easy and visually attractive access to toggle switches, such as airplane mode and wifi. There are other useful toggles that I don't use as regularly, such as flash (especially useful if turning on the flash for long periods e.g.  emergency lighting— for shorter use i use the flashlight option within launch center pro), location services, screen rotation lock, and power, but these come in handy when needed, and using the NCSettings app for this takes much less time each time compared to the default settings app. note you'll need to enable the app in the notification center before you will see the settings appear.

##useful helper programs

###mobile terminal
(free) i use this mainly in conjunction with inetutils (free) to ping on the network

###nonewsisgoodnews, bolt, no page dots (chpwn), zeppelin
(free) hides apple's otherwise–obligatory newsstand icon; hides battery icon unless charging; hides page dots on home screen; hides carrier name (or you can choose an icon)

###fiveicondock, fiveiconswitcher, fivecolumnspringboard
(free) if you are already hiding the text labels of the icons, thiese are very usable. Unfortunately fiveiconfolder does not work currently.

###safarizwipez, tab+
(free) close safari tabs by swiping up or down in the safari tab switcher; remove 8 tab limit on safari

###recordmyscreen
(free) make recordings of your iphone screen, helpful for showing processes and workflows, for example.

### mxtube and youtubetomp3
(free) get video or audio from youtube

### volume step
(free) adjust volume by less than one full increment; especially useful if you listen at very low volume. I use 30% increments.