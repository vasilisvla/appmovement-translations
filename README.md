# App Movement Translations

This project provides the translation files required to translate the online platform (.POT files), Android app template (.xml files), and iOS (.strings files). 

## Software
In order to translate aspects of the App Movement platform we recommend the following software:  

[POEdit](https://poedit.net)  - A cross platform PO file editor.

## Getting Started

The project files you require to get started can be found under

` Master/Platform`  
` Master/Android`  
` Master/iOS`

**Platform** (.POT files)  
This folder holds the files for the content on the App Movement website, database, API, emails, and model validation messages.

**Android** (.XML files)  
This folder holds the .xml strings file used in the translation of the Android template.

**iOS** (.strings files)  
This folder holds the .strings files used in the translation of the iOS template

### Folder Structure

We recommend that you Fork this repo to begin contributing to it. If it's easier you can simply email your new translations to a.garbett@newcastle.ac.uk

**Start copying the existing "Example Language" folder** in the root directory and renaming it to your desired language i.e. Greek.

Your project folder should now look like this:

`/[Your Desired Language]/Platform` (an empty folder that will only contain **working .PO files** and **does not** contain the master .POT files)  
`/[Your Desired Language]/Android` (this folder should contain .XML files)  
`/[Your Desired Language]/iOS` (this folder should contain .strings files)

Once you have created your project folder proceed with the steps below.

## Platform Translations
When translating with .POT files you can either:

- 1) **Start a new translation**, using the .POT file as your reference file (see "New Platform Translation" below)
- 2) **Continue working** on an existing .PO file (see "Continue Working" below)
- 3) **Update your working translations** from a new .POT file (see "Update Translations" below)

#### 1) New Platform Translation
When starting from a new .POT file (no existing translation files .PO have been created)

Start by opening POEdit
  
- Click 'Create New translation' and navigate to the project folder.  
- Nagivate to the translation project folder
- Select Platform > default.pot (or validation_errors.pot) to create a new translation .po file
- Click 'Open'

You will then be prompted with "Language of the Translation", from the drop down list select your desired language you wish to translate into i.e. Greek

- Click OK
- File > Save As > **Save the file to /[Your Desired Language]/Platform** as either *default* or *validation_errors* (which ever file you originally opened)
- **DO NOT** add a file extension (i.e. do not add .POT or .PO the editor will do this for you). 

Now you have a working .PO and .MO file to begin translating the App Movement Strings.

### 2) Continue Working  
If you have already created a new platform translation file (in the "New Platform Translation" step above), and you have the .PO and .MO files saved somewhere then proceed with the following:

Start by opening POEdit

- Click 'Edit a translation'
- Navigate to the project folder
- **Make sure to select the .PO file**
- Select Platform > default**.po** (or validation_errors**.po**) 
- Click 'Open'

You can now continue translating the .PO file until you have finished

### 3) Update Translations
There may be a point at which new development has ocurred and the developers have added, altered, or removed text from the platform. In this case we'll need you to update your translations file (.PO) using the template file (.POT) to update from.

Start by opening POEdit

- Click 'Edit a translation'
- Navigate to the project folder ([your desired language]/Platform)
- **Make sure to select the .PO file**
- Select Platform > default**.po** (or validation_errors**.po**) 
- Click 'Open'

Now we want to update the current .PO file with the new translation sentences found in the .POT file that has been updated.

In the navigation bar go to:

- Catalog > Update from POT file...
- Navigate to the master files folder
- Select Master Files > Platform > default**.pot** or validation_errors**.pot** 
- Click 'Open'

Now your translation file (.PO) should be updated with the new strings and you can proceed to translate the new sentences.

## Translating with POEdit
In the translation file (.PO) you'll notice that some strings have a **%s** inside the string. These are subjects in the sentence which you need to move within the translated sentence, in regards to how you might write it in the localised langauge.

##### String subjects (%S)
String subjects are represented as %s and you will need to move the subject accordingly.

For Example:  
` Hi Andy, how are you today?`

This might look like:  
` Hi %s, how are you today?`

In the translations you perform you might also encounter multiple subjects.  

For Example:  
` 150 People supported the idea for Breastfeeding Friendly Places, congratulations!`

This might look like:  
` %s People supported the idea for %s`

In this instance the platform will render the string on a first come first served basis with the first %s being passed the "150" element and the second %s being passed the "Breastfeeding Friendly Places".

#### Inline HTML Tags (i.e. \<span>\</span> or \<strong>\</strong>)
You might encounter \<span>\</span> or \<strong>\</strong> tags within the translation string. The \<span>\</span> or \<strong>\</strong> tags might also wrap around a %s, in this case the final translated string **MUST** keep the \<span>%s\</span> around the string subject (%s).

For Example:  
` It is not up to you to gather <strong>150 people<strong> in the next <strong>14 days</strong>.`

This might look like:
` It is now up to you to gather <strong>%s people</strong> in the next <strong>%s days</strong>.` 

## Important - What are .POT, .PO and .PO 
**Portable Object Template (.POT)** - These files are the main reference files generated by the development team and you should only use them through POEdit as your reference file.  

**Do not add .POT files to your language folder** (i.e. /[Your Desired Language]/Platform)

**Portable Object (.PO)** - This is your working file which you open and edit with your translation works and should be stored under /[Your Desired Language]/Platform/. 

This .PO file is derived from the reference .POT file.

**Machine Object** - This is read by the software to render the fonts derived from the .PO files

**Never open the .mo file with a text editor as this will destroy the translations made in a localised character set**


## Android Translations (.xml files)

 In order to begin translating the Android .xml file, open it in your preferred XML editor. We recommend [Sublime Text Editor](https://www.sublimetext.com/).
 
**Store your version of the android strings file under**:
 
 `[Your Desired Language]/Android/strings.xml`



When editing the XML make sure that you only edit the text between the opening and closing tags \<string name="name">**HERE**\</string>.

For Example:  
`<string name="review_option_a">Rating Option A</string>`

Might look like this:
`<string name="review_option_a">**My new translated string**</string>`

Do not remove any of the lines in the document and do not change the text after the name=""  
(i.e. \<string name="**NEVER CHANGE ME**">But you can change me\<string>)

## iOS Translations (.strings files)
In order to begin translating the iOS .strings files, open either the Localizable.strings or Main.strings in a text editor of your choice. We recommend [Sublime Text Editor](https://www.sublimetext.com/).

**Store your version of the .strings file under**:  
`[Your Desired Language]/iOS/[Localizable.strings or Main.strings]`

When editing the .strings file make sure to only edit the correct part. See below for an example:

```
/* Class = "UIButton"; normalTitle = "Tap to search here"; ObjectID = "0oP-94-2qw"; 
"0oP-94-2qw.normalTitle" = "***[Your translated text here]***";
```

or 

```
/* No comment provided by engineer. */
"Email Invalid" = "***[Your translated text here]***";
```



