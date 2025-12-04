<!--
dart_module_id: r_basics_transform_data
dart_author: Joy Payton
dart_title: R Basics: Transforming Data With dplyr
module_id: r_basics_transform_data
author: Joy Payton
email: paytonk@chop.edu
version: 1.4.2
current_version_description: Improved boolean logic, pipe, and filter materials
module_type: standard
docs_version: 3.1.2
language: en
narrator: US English Female
mode: Textbook
title: R Basics: Transforming Data With dplyr
comment:  Learn how to transform (or wrangle) data using R's `dplyr` package.
long_description: Do you want to learn how to work with tabular (table-shaped, with rows and columns) data in R?  In this module you'll learn in particular how to select just the rows and columns you want to work with, how to create new columns, and how to create multi-step transformations to get your data ready for visualization or statistical analysis.  This module teaches the use of the `dplyr` package, which is part of the `tidyverse` suite of packages.

estimated_time_in_minutes: 60
r_file: r\_basics\_transform\_data

@pre_reqs

Minimal experience of using the RStudio IDE and writing R code (specifically, within an R Markdown document) is necessary to understand and use this material.  If you can understand and do the following, you'll be able to complete this course:

- Run a command that's provided to you in the console
- Use the Environment tab to find a data frame and learn more about it
- Insert a new code chunk in an R Markdown document

@end

@learning_objectives  



- Write R code that uses the `dplyr` package to select only desired columns from a data frame
- Write R code that uses the `dplyr` package to filter only rows that meet a certain condition from a data frame
- Write R code that uses the `dplyr` package to create a new column in a data frame

@end

good_first_module: false
data_task: data_wrangling
collection: learn_to_code
coding_required: true
coding_level: basic
coding_language: r
sequence_name: r_basics
previous_sequential_module: r_basics_visualize_data

@sets_you_up_for
- r_missing_values
- r_practice
- r_reshape_long_wide
- r_summary_stats
- data_visualization_in_ggplot2

@end

@depends_on_knowledge_available_in
- r_basics_introduction
- r_basics_visualize_data

@end

@version_history

Previous versions: 

- [1.3.7](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/d769533e4158ab653efaf46fa08a40a92a2a7ca0/r_basics_transform_data/r_basics_transform_data.md#1): Updated with new metadata and to remove references to Binderhub
- [1.2.0](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/81c8707b4fd08a93927f6a85e358ca3bca367420/r_basics_transform_data/r_basics_transform_data.md#1): Update highlight boxes
- [1.1.3](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/b71760c8078ef96d1f18d66d21aa27c9ebe42c4b/r_basics_transform_data/r_basics_transform_data.md#1): Update versioning, attribution, Posit.cloud

@end

import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros.md
import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros_r.md
import: https://raw.githubusercontent.com/LiaTemplates/mermaid_template/0.1.4/README.md
-->
# R Basics: Transforming Data With dplyr

@overview

@dart_citation
