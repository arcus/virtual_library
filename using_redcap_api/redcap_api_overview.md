<!--
module_id: using_redcap_api
author:   Joy Payton
email:    paytonk@chop.edu
version: 2.0.5
current_version_description: Adds instructions for avoiding pushing API token to GitHub, adds information about environment variables, updates highlight boxes, and clarifies text editors
module_type: standard 
docs_version: 3.0.0
language: en
narrator: US English Female
mode: textbook
title: Using the REDCap API
comment:  REDCap is a research data capture tool used by many researchers in basic, translational, and clinical research efforts.  Learn how to use the REDCap API in this module.
long_description: If your institution provides access to REDCap, this module is right for you.  REDCap is a convenient and powerful way to collect and store research data.  This module will teach you how to interact with the REDCap API, or "Application Programming Interface," which can help you automate your data analysis. This will also help you understand APIs in general and what makes their use so appealing for reproducible research efforts.
estimated_time_in_minutes: 60

@pre_reqs

This module assumes that learners already have access to the REDCap application at their institution. Learners will benefit from having used REDCap in the past, although new users of REDCap may find this module useful if they watch an overview video about REDCap (included in this module).  This module requires that learners have either R (preferably with RStudio) or Python (preferably the Anaconda distribution with Jupyter) installed in order to work with the API.  Therefore, some experience with either R or Python is necessary, but template code will be provided within the module.  

@end

@learning_objectives  



- Define what an API is and why it's useful to researchers
- Enable API usage on REDCap projects
- Use the REDCap API to pull data into an R or Python data analysis

@end

good_first_module: false
collection: infrastructure_and_technology
coding_required: true
coding_level: intermediate
coding_language: r, python

@sets_you_up_for

@end

@depends_on_knowledge_available_in

@end


@version_history
[1.0.2](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/a4ea7a7f1f9264dabe952b68941fc9f0f656c9fc/using_redcap_api/using_redcap_api.md#1): make it clear that you need to have R or Python installed
@end


import: https://raw.githubusercontent.com/arcus/education_modules/main/_module_templates/macros.md

-->

# Using the REDCap API

@overview
