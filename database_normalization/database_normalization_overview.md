<!--
dart_module_id: database_normalization
dart_author:   Joy Payton
dart_title: Database Normalization
email:    paytonk@chop.edu
version: 1.1.0
current_version_description: Switched framing of the one-to-many quiz to avoid ambiguity about one-to-many v.s. many-to-many.
module_type: standard
docs_version: 2.0.0
language: en
narrator: US English Female
mode: Textbook
title: Database Normalization
comment: Learn about the concept of normalization and why it's important for organizing complicated data in relational databases.
long_description: Usually, data in a relational database like SQL is organized into multiple interrelated tables with as little data repetition as possible. This concept can be useful to apply in other areas as well, such as organizing data in .csvs or in data frames in R or Python.  This module teaches underlying data considerations and explains how data can be efficiently organized by introducing the concepts of one-to-many data relationships and normalization.
estimated_time_in_minutes: 40

@pre_reqs
Learners should have experience working with data in tables.  This could included working with .csv files, SQL databases, R data frames, REDCap instruments, or other ways that data can be collected in tables. 
@end

@learning_objectives  

- Explain the significance of "one to many" data relationships and how these relationships affect data organization
- Describe how a normalized database is typically organized
- Explain how data can be linked between tables and define "primary keys" and "foreign keys"

@end

good_first_module: false

data_task: data_management
data_domain: ehr
coding_required: false

@sets_you_up_for
- sql_joins
@end

@depends_on_knowledge_available_in

@end

@version_history 
Previous versions: 

- [1.0.8](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/d367a7d5a0e9b6abdf67883b31d4a8894a13b17a/database_normalization/database_normalization.md#1): Initial version.

@end

import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros.md
-->

# Database Normalization

@overview

@dart_citation