# CHOP Virtual Library

This is a repository of courses originally written for the [DART program](https://arcus.github.io/education_modules/), lightly adapted here for use within CHOP's WorkDay Learning LMS. 
For more information about the materials and the DART project (including how you can contribute!) see [the DART modules repository](https://github.com/arcus/education_modules). 

## How to export a course for use in WorkDay Learning

To upload a course to WDL, you will need the [LiaScript Exporter](https://github.com/LiaScript/LiaScript-Exporter).

With testing, we've found that this approach has worked well: 

1. First, make sure you have a current version of [nodejs](https://formulae.brew.sh/formula/node), using *one* of the following commands:

```
brew install node
brew upgrade node
```

2. Then install the [LiaScript Exporter](https://github.com/LiaScript/LiaScript-Exporter):

```
sudo npm install -g --verbose @liascript/exporter
```

3. Then, from the `virtual_library` root directory, export one of these courses using a command like the following:

```
liaex -i sql_basics/sql_basics.md --format scorm2004 --scorm-embed --output wdl_uploads/wdl_sqlbasics
```

This will produce a file called `wdl_sqlbasics.zip` in the `wdl_uploads` subdirectory.
You can then upload this file to the WDL shared drive and use it to [create a digital course](https://chop365.sharepoint.com/:b:/r/sites/Workday/Shared%20Documents/Learning%20Admin/Create%20a%20Digital%20Course.pdf?csf=1&web=1&e=CAdW6U). 


<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
