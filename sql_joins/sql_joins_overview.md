<!--
dart_module_id: sql_joins
dart_author: Joy Payton
dart_title: SQL Joins
email: paytonk@chop.edu
version: 1.2.2
current_version_description: Add three new additional resources; make liascript link(s) point to first page
module_type: standard
docs_version: 2.0.0
language: en
narrator: US English Female
mode: Textbook
title: SQL Joins
comment: Learn about SQL joins: what they accomplish, and how to write them.
long_description: Usually, data in a SQL database is organized into multiple interrelated tables.  This means you will often have to bring data together from two or more tables into a single dataset to answer your research questions.  This "join" action is accomplished using `JOIN` commands.  This module teaches types of joins, join criteria, and how to write `JOIN` code.
estimated_time_in_minutes: 60

good_first_module: false
data_domain: ehr
data_task: data_wrangling
collection: learn_to_code
coding_required: true 
coding_language: SQL
coding_level: intermediate
sequence_name: sql
previous_sequential_module: sql_intermediate
@sets_you_up_for

@end
@depends_on_knowledge_available_in

- sql_intermediate
- database_normalization

@end

@learning_objectives  


- Understand the parts of a JOIN
- Describe the "shapes" of SQL JOINs: inner, left, right, and full
- Explain what "join criteria" are

@end

@pre_reqs

Learners should have experience writing SQL code on single tables.  If you have successfully used a "SELECT... FROM... WHERE" SQL statement on a single table, and have at least seen "GROUP BY" commands in action, even if you would need help writing the GROUP BY code, you have enough code ability.  We also highly recommend that you understand the concepts of one-to-many data relationships and database normalization to get the most out of this module. 

If you need to develop basic SQL fluency we recommend our module [SQL Basics](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/sql_basics/sql_basics.md#1).  For more intermediate topics, we suggest our module [SQL Intermediate](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/sql_intermediate/sql_intermediate.md#1).  Finally, to learn about one-to-many data relationships and database normalization, consider our [Database Normalization](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/database_normalization/database_normalization.md#1) module.

@end

@version_history

Previous Versions:

- [1.1.7](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/3607dfd4824bc9fe39edbdc62a47e28d0a863c7a/sql_joins/sql_joins.md#1): Typo fix; update metadata
- [1.0.1](https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/d428e9f66a2161e96ea4ca32b42049fab2d27088/sql_joins/sql_joins.md#1): Original version, with improved feedback link

@end

import: https://raw.githubusercontent.com/arcus/virtual_library/main/_module_templates/macros.md

script: https://cdn.jsdelivr.net/npm/alasql@0.6.5/dist/alasql.min.js
attribute: [AlaSQL](https://alasql.org)
           by [Andrey Gershun](agershun@gmail.com)
           & [Mathias Rangel Wulff](m@rawu.dk)
           is licensed under [MIT](https://opensource.org/licenses/MIT)

script: https://cdnjs.cloudflare.com/ajax/libs/PapaParse/4.6.1/papaparse.min.js
attribute: [PapaParse](https://www.papaparse.com)
           by [Matthew Holt](https://twitter.com/mholt6)
           is licensed under [MIT](https://opensource.org/licenses/MIT)

script: https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js
attribute: [jQuery](https://jquery.com/)
           is licensed under [OpenJS Foundation](https://openjsf.org/)

@AlaSQL.eval
<script>
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
// BUILD FUNCTIONS
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

function buildHtmlTable() {
  // Builds the HTML Table out of myList, and writes output to the id attribute assigned via the "@0" argument to this marco.
  var columns = addAllColumnHeaders(myList);
  for (var i = 0 ; i < myList.length ; i++) {
    var row$ = $('<tr/>');
    for (var colIndex = 0 ; colIndex < columns.length ; colIndex++) {
      var cellValue = myList[i][columns[colIndex]];
      if (cellValue == null) { cellValue = ""; }
      row$.append($('<td/>').html(cellValue).css({
      "padding-left": "1em",
      "padding-right": "1em"
      }));
    }
    $(@0).append(row$);
  }
  try { // Error Handling for no null.
    var rowCount = document.getElementById(@0.substring(1)).rows.length - 1;
  } catch(err) {
    var cnt = 0
  }
  if (rowCount > 0) {
    var complete_message = "Query Execution Complete! (See Result Set Below)..."
  } else {
    var complete_message = "No Data to Return.."
  }
  return JSON.stringify(complete_message, null, 3);
}
function addAllColumnHeaders(myList) {
  // Creates and Returns Header Row From Array Data Provided as Input.
  var columnSet = [];
  var headerTr$ = $('<tr/>');
  for (var i = 0 ; i < myList.length ; i++) {
    var rowHash = myList[i];
    for (var key in rowHash) {
      if ($.inArray(key, columnSet) == -1){
        columnSet.push(key);
        headerTr$.append($('<th/>').html(key));
      }
    }
  }
  $(@0).append(headerTr$);
  return columnSet;
}
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
try {
    var myinput=`@input`
    myinput=myinput.replace(/;/, ""); // remove all semi-colon
    var myStriptArray= myinput.split(';');
    var arrayLength = myStriptArray.length;
    console.clear();
    for (var i = 0; i < arrayLength; i++) {
        if((myStriptArray[i].trim()).length != 0) { // ignore blank queries.
            var myList=alasql(myStriptArray[i]);
        }
        if (myList != 1  & ((myStriptArray[i].trim()).length) != 0) { // If data is returned, format output as table.
            $(@0).html(""); // clear out existing data
            buildHtmlTable();
        } else {
            $(@0).html(""); // clear out existing data
            JSON.stringify("No Data to Return..", null, 3);
        }
    }
} catch(e) {
  let error = new LiaError(e.message, 1);
  try {
    let log = e.message.match(/.*line (\d):.*\n.*\n.*\n(.*)/);
    error.add_detail(0, e.name+": "+log[2], "error", log[1] -1 , 0);
  } catch(e) {
  }
  throw error;
}
</script>
@end

@AlaSQL.buildTable_disease
<script>
    alasql("DROP TABLE IF EXISTS disease;");
    alasql("create table disease (subject_id integer, lung_cancer boolean);");
    alasql("INSERT INTO disease VALUES (3,'TRUE');");
    alasql("INSERT INTO disease VALUES (5,'FALSE');");
    alasql("INSERT INTO disease VALUES (8,'FALSE');");
</script>
@end

@AlaSQL.buildTable_smoking
<script>
    alasql("DROP TABLE IF EXISTS smoking;");
    alasql("create table smoking (subject_id integer, smoking_pack_years integer);");
    alasql("INSERT INTO smoking VALUES (2,10);");
    alasql("INSERT INTO smoking VALUES (3,10);");
    alasql("INSERT INTO smoking VALUES (4,0);");
</script>
@end

-->

# SQL Joins

@overview

@dart_citation