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

Each module also has an overview file (e.g. `sql_basics_overview.md`), which includes just the module overview content, including description, learning objectives etc. 
When you create a course in WDL, render this overview file (you can use the [lia preview in VS Code](https://liascript.github.io/vscode/) or the [liascript live editor](https://liascript.github.io/LiveEditor/)) and copy-paste the overview in as a the course description in WDL. 

## How to adapt a DART module for addition here

1. Copy the module subdirectory from education_modules and paste it in this repo.
2. Open the module file within the subdirectory (e.g. `sql_basics.md`) and change the import statement(s) in the metadata to point to this repo rather than education_modules.
3. Make a copy of the module file (e.g. `sql_basics.md`) and name it with `_overview`, like `sql_basics_overview.md`. You should now have two markdown files in your module subdirectory.
4. In the module file (e.g. `sql_basics.md`), remove most of the metadata. Keep only the following fields: 
    * title
    * comment
    * language
    * mode
    * the import statement(s)
5. In the overview file, (e.g. `sql_basics_overview.md`), replace all the module content (after the metadata section) with just `@overview`.
6. Preview **both** the overview and the module files. Look closely for anything that should be adjusted for publication within WDL (note that for nontrivial updates it may make sense to record them as an issue in the repo to track work). This may include the following: 
    * Links to other modules (these should be replaced with WDL links)
    * Instructions to open external websites for practice (e.g. regexone, positcloud). We should review these processes. 
    * Content that was written for a non-CHOP audience and should now be revised to more closely hew to CHOP practice and standards, especially reference to tools or techniques that will be unavailable for most CHOP users or are against CHOP policy. 

## Guidelines for creating a new course

All Virtual Library courses should have a similar structure and aesthetic, to make them recognizable and reduce learners' cognitive load when completing multiple courses. 
Ensure any new course meets the following requirements: 

- Each course must include the Virtual Library logo as its image in WDL
- Use the following tag(s) in WDL: [WHAT TAGS??]
- There must be explicitly stated learning objectives in the description/overview
- Course content may not drift from its learning objectives (don't include substantial content not in service of the stated learning objectives)
- Use clear, informative headings (e.g. "Joining on multiple fields" is better than something like "Now it gets more complicated")
- Every course should be written in markdown and parsed via liascript, according to the instructions here. Make use of the macros in this repository to reuse standard language (e.g. for the overview) across multiple modules.

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
