<!--
dart_title: Transform Data with pandas
dart_module_id: pandas_transform
dart_author:   Elizabeth Drellich
email:    drelliche@chop.edu
version: 2.0.2
current_version_description: Replaced SageMathCells with Pyodide cells for better usability
module_type: standard
docs_version: 2.0.0
language: en
narrator: UK English Female
mode: Textbook

title: Transform Data with pandas

comment:  This is an introduction to transforming data using a Python library named pandas.

long_description: This module is for learners who have some familiarity with Python, and want to learn how the pandas library can handle large tabular data sets. No previous experience with pandas is required, and only an introductory level understanding of Python is assumed.

estimated_time_in_minutes: 60

@pre_reqs
Before starting this module it is useful for you to:

- have some familiarity with tabular data: data stored in an array of rows and columns.

- have an introductory level exposure to coding in Python, which could be acquired in the Python Basics sequence of modules ([Functions, Methods, and Variables](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/python_basics_variables_functions_methods/python_basics_variables_functions_methods.md#1); [Lists and Dictionaries](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/python_basics_lists_dictionaries/python_basics_lists_dictionaries.md#1); and [Loops and Conditional Statements](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/python_basics_loops_conditionals/python_basics_loops_conditionals.md#1)).
@end

@learning_objectives  



- Import `pandas` and use functions from the `pandas` package.
- Load data into a `pandas` DataFrame.
- Use the `.loc` method to explore the contents of a DataFrame
- Filter a DataFrame using conditional statements.
- Transform data in a DataFrame.

@end

good_first_module: false
data_task: data_wrangling
coding_required: true
coding_level: intermediate
coding_language: python

@sets_you_up_for

- python_practice

@end

@depends_on_knowledge_available_in 

- python_basics_variables_functions_methods
- python_basics_lists_dictionaries
- python_basics_loops_conditionals

@end

@version_history 

Previous versions: 

- [1.1.1](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/255170ae36834565696b5d7e6e3e6621172a5666/pandas_transform/pandas_transform.md#1): Updated highlight boxes for greater clarity, other minor changes

- [1.0.2](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/4c378ba6d211f8ca852d4df9a550edb249cd3c68/pandas_transform/pandas_transform.md#1): Initial version

@end

import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros.md
import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros_python.md
import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md

-->

# Transform Data with pandas

@overview

@dart_citation