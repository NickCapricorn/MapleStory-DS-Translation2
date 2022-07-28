# MapleStory DS Translation

## Getting Started

### Tools Needed 
1) **LazyDS** - Used to unpack and repack the NDS game contents.</br>
2) - **MapleTrans 1.0** - Used to import and export the .txt script files from Korean base roms/translations. (Red Snail 0.4)
   - **MapleTrans 1.1** - Used to import and export the .txt script files from Japanese base roms/translations.
3) Any NDS emulator. **MelonDS**, **DeSmuME**, **RetroArch** or **RALibRetro**.

### Process
1) Unpack MapleStoryDS (Red Snail 0.4).nds / MapleStoryDS (Korea).nds / MapleStoryDS (Japan).nds / MapleStoryDS (ChineseFanTranslation).nds / MapleStoryDS (Chinese_ENG).nds with **lazyDS**
- The RedSnail 0.4 & Chiense_EN translations both have all the menu/items/skills/cards fully translated so it is easier to use those unless you know JP/KR/CN.
2) Load All Content with **MapleTrans** 
- MapleTrans will act as if it's crashing and not responding when you start loading the data, just let it sit for a few mins and it'll start.
3) Export text script with **MapleTrans**.
4) Play game and when text appears that you want to translate, find the proper .txt file for the line of text and edit.
- Easiest method I found was to use **Visual Code Studio** or **Notepad++** they both have an option to **Search for text through multiple files**. 
- If multiple files show up flagging as the text being in them, make sure the text is identical. If they are, change them both. For whatever reason sometimes this occurs. (I assume it has something to do with multiple merging story paths).
5) When looking at the current textbox displaying in game, try keeping the line count and character length in mind. When adding in/changing dialogue **[\n]** will cause a line break in game. 
- You have a limit of what the text box looks like in game to add text, there is no way to add more text boxes to any person's dialogue so you have to make it fit.
- This section will take a bit of trial and error. How I got used to it was having a save state right before the dialogue, change it import it and repack and load it up and see how it looks. Eventually you'll get to the point where you won't have many issues.
- Having save states everywhere is good to do so you can easily get back to where you were and make sure it displays correctly with no screen wrapping or cutting off characters.
6) Import text script with **MapleTrans**
- It will show that it's re-importing all text but if you scroll through, it'll only import ones where it detects changes.
7) **MapleTrans** File > Save All
7) Repack the .NDS file in **lazyds**
8) Load up in your emulator and check out your changes.
- Make sure you use the newly created .nds file and not an old one.
9) If the changes work and you're satisfied, submit changes to the github.
- Only submit changes to the specific lines you changed and not just copy/paste all the .txt file contents in the off chance that someone else had dialogue lines translated within that same .txt
10) Going back in to translate? No need to re-unpack or re-export text. Just keep editing in your files and import & pack again once you make more changes.
- You could grab all the content off github from time to time if you want to keep your files somewhat up to date with everyone elses changes as well.

### Imprtant Word Highlighting
- [\n] used for linebreaks, make sure not to space the words out for these example: "Hello Adventurer, Welcome[\n] to the World of MapleStory.[\n]My name is Minerva,[\n]"
- <NameHere> will highlight names in Green. Normally used when characters use another characters name.
- \[name:S_PC\] will reference your character name
- text inside "『 』" will be highlighted. Normally used when hints/keywords/town names/important notes are displayed.

If I find more I'll add them here.

### How I've been doing it

- Unpacked & exported text scripts from RedSnail 0.4, (Korea) & (Japan)
- Playing on the RedSnail 0.4 patch
- Search files for text in **Visual Code Studio** & open all 3 version's of the file, EN,KR & JP.
- Google Translate KR & JP into english (which somehow gives a better translation then the broken english one from Red Snail)
- Between the three translations and seeing what's going on in game, you can easily piece stuff together to see what's going on.
- Save changes, import text files back in and repack
- Launch game, test if text is within the box and nothing cuts off
- Upload only the lines altered to github and replace Korean text lines if everything in game was working and translation seemed fine.

### Random Info
- Korean text files are uploaded to this github repo which makes it easier to know how much translation is left or what was missed.
- Github really hates putting files/folders in numerical order and they have to stay labeled this way for the importing back in so we just have to live with it.
- The .txt file names and the lines the text is on in the .txt files are the same across all versions of the game. ex; You're using the "Red Snail 0.4" patch and the line you want to change is "\MapleKR\text\IN\STAGE\GLOBAL\60.GMM.txt on line 122" it will be in the same directory/line in any other version.
- Dialogue for a single character/event can sometimes be mixed between multiple .txt files. If you started in \MapleKR\text\IN\STAGE\GLOBAL\60.GMM.txt and don't see the next line of dialogue in that same file, chances are it's in another one.
