<img width="1274" height="521" alt="TitleImage" src="https://github.com/user-attachments/assets/2d9762ef-7662-4479-a7b4-4d590faf2c2b" />

Welcome to the Hollow Knight Text Database! This app is a searchable repository of all the text in Hollow Knight and (eventually) Silksong, including their content updates. Don't know how to run code or query a database? Not a problem! This app handles everything for you; all you need to do is tell it what you want!

# Set Up

## Install the Hollow Knight Font (Optional)

This app uses the same font as the games: Trajan Pro. While it *shouldn't* be necessary to install this font for the app to run, it is highly recommended as all of the interface formatting is built around it. The font file (.ttf) is included in this repository. Simply download the file and double click it. Your system should then give you the option to install the font. **You only have to do this once.**

## Download the App

### Mac

Download the **HKTD_Mac.zip** file. Double click the .zip file to extract the HKTD application. You can now move the app wherever you'd like on your system and the .zip file can be safely deleted.

You may get an error when verifying the app along the lines of "This app is damaged and can't be opened". This is a security measure that Apple uses to ignore apps not downloaded through the App Store. To fix this, right click the app and select "copy". Then in the search bar, open the Terminal program. In the terminal type "xattr -dr com.apple.quarantine " then paste the path to the app in the terminal. The full terminal command should look like "xattr -dr com.apple.quarantine <copied_path>/HKTD.app" where <copied_path> should be the path to where you placed the app on your system. Press Enter in the terminal, and the app should work from now on.

### Windows

Download the **HKTD_Windows.zip** file. Double click the .zip file to open its contents. Drag the HKTD application out of the opened .zip file to extract it. You can now move the app wherever you'd like on your system and the .zip file can be safely deleted.

## Run the App

Simply doulbe click the application to launch it! It will likely take a bit of time to launch (10-20 seconds), especially the first time, so don't worry.

<img width="1401" height="773" alt="Sample" src="https://github.com/user-attachments/assets/83c1a006-3b61-4260-ae10-c8351cbed24c" />

# Using the App

## Filter Types

This app queries a database of all the text in the Hollow Knight games, which is a lot and not entirely useful as a whole. So you can trim the text to only include specific entries by using **Filters**. There are five types of filters that you can use: **Game**, **Source**, **Type**, **Topic**, and **Keyword**.

**Game:** Filter according to the game the text came from. Options are **H**ollow **K**night (HK), the **H**ollow **K**night: **H**idden **D**reams update (HK:HD), the **H**ollow **K**night: **L**ife**b**lood (HK:LB) update, the **H**ollow **K**night: **G**rimm **T**roupe (HK:GT) update, the **H**ollow **K**night: **G**od**m**aster (HK:GM) update, **S**ilk**s**ong (SS), and the **S**ilk **S**ong: **S**ea of **S**orrow (SS:SS) update (*NOTE: Silksong text not currently implemented*).

**Source:** The source of the given text. Examples include NPCs, Journal Entries, Lore Tablets, etc.

**Type:** The type of text. Options are Dialogue (text spoken by NPCs), Dream Nail (text prompted by using the Dream Nail), and Text (Non-spoken text such as menu descriptions or journal entries).

**Topic:** The topics addressed by the text. Examples include Void, Hallownest, Dreams, etc. These topics are admittedly subjective and many of them overlap, so scrolling through the full list is recommended so you can get a sense of what's included. There are some specific examples to highlight, however. Void, Vessels, Hollow Knight, The Knight, Infection, and Radiance are separate topics. Anything related to the nail weapon or the Nailmasters (Oro, Mato, Sheo, and Sly) is grouped under the topic of Nail. Anything related to Herrah, Monomon, or Lurien is grouped under the topic of Dreamers. If you'd like to change any of the topics on these entries, or add new ones, you can do so (see the [Editing the Data](#editing-the-data) section below). *NOTE: While Silksong text hasn't been added yet, some topics have been adjusted based on information provided by Silksong, namely the Delicate Flower being given the topic of Everbloom and Lifeblood being given the topic of Plasmium.*

**Keyword:** Search the text itself and/or the conditions required for a given word or letter pattern.

## Using Filters

The **Game**, **Source**, **Type**, and **Topic** Filters consist of two lists: terms to include and terms to exclude. Individual entries can be moved from one list to the other by clicking on the word, then using the **<** or **>** button to move the entry. Additionally, the **<<<** and **>>>** buttons will move all entries from one list to the other.

The **Keyword** Filter allows you to enter in your own term you'd like to search the text for. Typing in a keyword and clicking the **+** button will add it to the list of keywords underneath. To remove a keyword, type it again and click the **-** button. Keywords are **case-insensitive**, and **match whole words**. For example, using the keyword *Infect* will match all entries using *Infect* or *infect* as a complete word (i.e. surrounded by spaces or punctuation). If you want exact matches regardless of whether or not they're complete words, put the keyword in quotation marks. For example, using the keyword *"Infect"* will match all entries using those letters, such as  *Infect*, *Infection*, or *Infected*.

The **Keyword** Filter searches the text entries themselves, but by checking the top box underneath the keyword list, you can also search the conditions. For example, using the keyword *First Encounter* and checking the "Include Condition" box will show you all the dialogue that occurs the first time you encounter an NPC (i.e. the condition of the text contains *First Encounter*). By default, the keyword filter looks for all text that contains *any* of the listed keywords. For example, using keywords *ghost* and *shadow* will return all text that contains the word *ghost* and/or the word *shadow*. If you want only the results that contain both *ghost* **and** *shadow*, check the second box under the keyword list. This box tells the app to only return text that contains **all** of the listed keywordsv(*NOTE: Using this option will always ignore the Condition of the text*).

You can use **any and/or all** of these filters at the same time! But, there are somethings to be aware of:

Firstly, **All** of the filter conditions must be met by a text entry in order to be included in the results. Think of this like using the word **and** in a sentence: The included text will have its Game in the Included Games List **AND** its Source in the Included Sources list **AND** its Type in the Included Types list **AND** its Topics in the Included Topics list **AND** contain any keywords (if used). For more complicated queries (i.e. filter combinations that would use **OR** instead of **AND**), see the [Advanced Queries](#advanced-queries) section below.

Secondly, the **Topics** Filter prioritizes the Included topics over the Excluded. For Example, if topic *A* is included and topic *B* is excluded, and entry that has both topics *A* and *B* will be included in the results.

When you're filters are set, press the **Search** button and the table will populate with all matching results.

## Menu Options

The dropdown menus in the top left of the application have some useful functions:

**Menu: GitHub** and **Menu:ReadMe** will open the GitHub page in your default internet browser or the ReadMe.txt file in your default text editor.

**Menu: Quit** will close the application.

**Data: Import Data** will ask you to input a Excel File (.xlsx), which it will use to rebuild the database using the new data (see the [Editing the Data](#editing-the-data) section below).

**Data: Revert Data** will revert the database to the original form it had when downloaded from GitHub. This will undo any changes made by the Import Data option.

**Data: Reset Filters** will quickly revert all the filters to their default state (include all games, sources, types, topics, and no keywords).

**Data: Multi-Query** will ask you to input multiple Excel Files (.xlsx) from previous queries, and combine them into a single Excel File (see the [Advanced Queries](#advanced-queries) section below).

**Data: Export .xlsx** and **Data: Export .csv** will save the results of your search as an Excel File (.xlsx) or Text File (.csv, entries separated by "|" ).

**Data: Export Info** will generate a Text File (.txt) with an overview of your search results, including the number of matches, the filters used, and a list of unique games, sources, types, and topics from the results.

**View: Full Text** and **View: Single Row** will adjust the results table to show either the full text for each entry, or reduce each entry to a single row.

## Editing the Data

Found a mistake in the data you want to fix? Want to change the topics of some of the text? Want to add new text? Want to replace all the text with those from a different game and still use the filter system??? You can do all of this and more!

The database and all of the filter options are generated dynamically from a spreadsheet when running the app. While you won't have direct access to the original spreadsheet (that way the **Revert Data** menu option will always work as a backup), you can make a copy of it by **Exporting** the full data set (all filters include everything, no keywords) to a *.xlsx* file. You can change the exported data however you like (with a few caveats listed below) in a spreadsheet software like Excel or Google Sheets, then **Import** the data back into the app. The app will then create a new database, with new filters, that you can use just like before. The changes to the database will last (even when the app is closed) until you either **Import** new data, or **Revert** the data to it's original state.

There are a few rules to editing the data so the application will still function properly. Firstly, the new data must maintain the structure of the original data: 6 columns - Game, Source, Type, Text, Condition, Topics - in that order. Secondly, the Game, Source, and Type columns can only have a single entry, not a list. Thirdly, the Text entry can handle special characters with one exception: quotation marks. Any " should be replaced with ' or removed. Finally, if an entry has multiple topics, enter them as a comma separated list and the application will separate them automatically.

*NOTE: If there are any major issues with the original data found on GitHub, please file an Issue report*

## Advanced Queries

To keep the application interface clean and user friendly, only one filter set (game, source, type, topic, and keyword) can be used at a time and the selected entries must meet the entire set. But sometimes, you might want to select entries that meet one filter criteria **OR** a different filter criteria.

For example, say you want all dialogue either spoken by Hornet or pertaining to Hornet. If you set the Source filter to only include Hornet and the Topics filter to only include Hornet, then the results will only include text where Hornet is speaking about herself since both filters need to be satisfied (i.e. text that satisfies Source:Hornet **AND** Topics:Hornet). This is not what you want. Instead, you want the individual results of Source: Hornet and Topics: Hornet merged together (i.e. text that satisfies Source:Hornet **OR** Topics:Hornet).

The app does not allow you to do separate queries like this at the same time, but it will let you merge past queries into a single result. Using the **Multi-Query** menu option, you can upload any number of *.xlsx* files from previous queries and it will automatically merge them into a single *.xlsx* file (removing any duplicate entries).

For the above example, you would save the output of Source:Hornet and Topics:Hornet individually, then use **Multi-Query** to merge the results into a single file. This file could then be **Imported** to the application for further filtering if you so choose.
