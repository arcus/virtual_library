<!--
dart_title: Data Visualization in seaborn
dart_module_id: data_visualization_in_seaborn
dart_author:   Rose Hartman
email:    hartmanr1@chop.edu
version: 1.5.0
current_version_description: Add `plt.close()` to code cells to prevent plot accumulation.
module_type: standard
docs_version: 3.0.0
language: en
narrator: UK English Female
mode: Textbook

title: Data Visualization in seaborn

comment:  This module includes code and explanations for several popular data visualizations using python's seaborn library. It also includes examples of how to modify seaborn plots to customize them for different uses.  

long_description: You can use the seaborn module in python to make many different kinds of data visualizations (also called plots or charts), including scatterplots, histograms, line plots, and trend lines. This module provides an example of each of these kinds of plots, including python code to make them using the seaborn module. It may be hard to follow if you are brand new to python, but it is appropriate for beginners with at least a small amount of python experience.

estimated_time_in_minutes: 60

@pre_reqs

This module assumes some familiarity with statistical concepts like distributions, outliers, and linear regression, but even if you don't understand those concepts well you should be able to learn and apply the data visualization content.
When statistical concepts are referenced in the lesson, links to learn more are generally provided.

This module also assumes some basic familiarity with python, including

- an introductory level exposure to coding in Python, which could be acquired in the Python Basics sequence of modules ([Functions, Methods, and Variables](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/python_basics_variables_functions_methods/python_basics_variables_functions_methods.md#1); [Lists and Dictionaries](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/python_basics_lists_dictionaries/python_basics_lists_dictionaries.md#1); and [Loops and Conditional Statements](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/python_basics_loops_conditionals/python_basics_loops_conditionals.md#1)).
- installing and importing python modules (you can learn about importing packages in our [Transform data with pandas module](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/pandas_transform/pandas_transform.md#4)).
- [reading in data](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/pandas_transform/pandas_transform.md#8)
- [manipulating data frames, including calculating new columns](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/pandas_transform/pandas_transform.md#17)

If you are brand new to python (or want a refresher) consider starting with [Demystifying Python](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/demystifying_python/demystifying_python.md#1) first.

@end

@learning_objectives  



- use seaborn to create several common data visualizations
- customize some elements of a plot, and know where to look to learn how to customize others

@end

good_first_module: false
data_task: data_visualization
collection: learn_to_code
coding_required: true
coding_level: basic
coding_language: python
sequence_name: data_visualization
previous_sequential_module: data_visualization_in_open_source_software

@sets_you_up_for

- python_practice

@end

@depends_on_knowledge_available_in

- pandas_transform
- data_visualization_in_open_source_software
- python_basics_variables_functions_methods
- python_basics_lists_dictionaries
- python_basics_loops_conditionals
- demystifying_python

@end

@is_parallel_to
data_visualization_in_ggplot2
@end

@version_history
Previous versions: 

- [1.4.3](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/f1ae61c8da0b2fb145f1c3cdc0c886aed606a25e/data_visualization_in_seaborn/data_visualization_in_seaborn.md#1): Add Python Basics series and Transform data with pandas as additional prerequisites; make liascript link(s) 
- [1.3.1](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/b9257316d82e99f51e1c1cb9819dc8c053aa1ed9/data_visualization_in_seaborn/data_visualization_in_seaborn.md#1): Change executable code blocks from sagemath to pyodide.
- [1.2.5](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/16a4a852199689a42f04555cb581cf2dcb90fb0f/data_visualization_in_seaborn/data_visualization_in_seaborn.md#1): Update highlight boxes, update front matter, and replace text with macros.
- [1.0.3](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/a4ea7a7f1f9264dabe952b68941fc9f0f656c9fc/data_visualization_in_seaborn/data_visualization_in_seaborn.md#1): Initial version, and fixed broken link to ggplot2 module. 
@end

import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros.md
import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros_python.md
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->

# Data Visualization in seaborn

@overview

@dart_citation