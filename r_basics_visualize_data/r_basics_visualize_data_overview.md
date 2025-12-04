<!--
dart_module_id: r_basics_visualize_data
dart_author: Joy Payton
dart_title: R Basics: Visualizing Data With ggplot2
module_id: r_basics_visualize_data
author: Joy Payton
email: paytonk@chop.edu
version: 1.3.8
current_version_description: Added help boxes for color vs fill aesthetic mapping and how to get plots to show in the plot pane; make liascript link(s) point to first page
module_type: standard
docs_version: 2.0.0
language: en
narrator: US English Female
mode: Textbook

title: R Basics: Visualizing Data With ggplot2

comment:  Learn how to visualize data using R's `ggplot2` package.

long_description: Do you want to learn how to make some basic data visualizations (graphs) in R?  In this module you'll learn about the "grammar of graphics" and the base code that you need to get started.  We'll use the basic ingredients of a tidy data frame, a geometric type, and some aesthetic mappings (we'll explain what all of those are).  This module teaches the use of the `ggplot2` package, which is part of the `tidyverse` suite of packages.

r_file: r\_basics\_visualize\_data

estimated_time_in_minutes: 60

@pre_reqs

Minimal experience of using the RStudio IDE and writing R code (specifically, within an R Markdown document) is necessary to understand and use this material.  If you can understand and do the following, you'll be able to complete this course:

- Run a command that's provided to you in the console
- Use the Environment tab to find a data frame and learn more about it
- Insert a new code chunk in an R Markdown document

One potential way to get these basic skills is to take our [R Basics: Introduction](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/r_basics_introduction/r_basics_introduction.md#1) course.

This course is designed for R beginners with minimal experience and it is not an advanced course in `ggplot2`.  If you have experience with `ggplot2` already, you may find our ["Data Visualization in ggplot2"](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/data_visualization_in_ggplot2/data_visualization_in_ggplot2.md#1), which is more advanced, a better fit for your needs.

@end

@learning_objectives  



- Write R code that creates basic data visualizations
- Identify geometric plot types available in `ggplot2`
- Map columns of data to visual elements like color or position

@end

good_first_module: false
data_task: data_visualization
collection: learn_to_code
coding_required: true
coding_level: basic
coding_language: r
sequence_name: r_basics
previous_sequential_module: r_basics_introduction

@sets_you_up_for

- r_practice

@end

@depends_on_knowledge_available_in

-r_basics_introduction

@end

@version_history

Previous versions: 

- [1.2.1](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/3da1555f9e6e33cccf456d088ece3f0596896f38/r_basics_visualize_data/r_basics_visualize_data.md#1): Added two new highlight boxes with additional clarification, and technical updates that do not affect content. 
- [1.1.0](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/dd92856bddc5de758ca19c53e94b181877f20143/r_basics_visualize_data/r_basics_visualize_data.md#1): Updating formatting for highlight boxes.
- [1.0.7](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/b71760c8078ef96d1f18d66d21aa27c9ebe42c4b/r_basics_visualize_data/r_basics_visualize_data.md#1): remove second attribution location, add information about Posit Cloud, revision to correct image links referring to wrong branch + small changes to environment setup language to be exactly mirrored across all 3 R basics modules.

@end

import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros.md
import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros_r.md
-->
# R Basics: Visualizing Data With `ggplot2`

@overview

@dart_citation