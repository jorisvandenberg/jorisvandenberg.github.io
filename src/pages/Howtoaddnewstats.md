---
title: How to add new pages
---

## think

think about which stats you want, and more specifically: _why_

## sql

* open database_querydb.go
* write the sql statement

```go
querymap["stmt_queryname"] = " SELECT col1,col2 from table where col3 = ?"
```

> ? => parameter
> ?? => ?
> like '%' || ? || '%' => parameterised like

## config

* open config.ini and add a section for your new stat. Here's an example: 

```ini
[name_of_your_stat]
enabled                             = true
table_enabled                       = true
table_title                         = My title for |number_of_days_detailed| days
table_description                   = My pages description.
table_pagecontent                   = Line1|line2|line3
table_pagefooter                    = my pages footer text
table_filename                      = table_filename.html
table_index_name                    = index title |number_of_days_detailed| days
table_index_group                   = collection name
table_index_order                   = 15

linegraph_enabled                   = true
linegraph_title                     = linegraph title |number_of_days_detailed| days
linegraph_description               = Linegraph page subtitle.
linegraph_filename                  = linegraph_filename.html
linegraph_index_group               = hits
linegraph_index_order               = 15

linegraph_compare4weeks_enabled     = true
linegraph_compare4weeks_title       = my title
linegraph_compare4weeks_description = my description
linegraph_compare4weeks_filename    = 4weektable_filename.html
linegraph_compare4weeks_index_group = hits
linegraph_compare4weeks_index_order = 15
```

> the main switch is "enabled". If you put this one to "false", your stats simply won't be created
> there is a subswitch to enable/disable table_enabled, linegraph_enabled and linegraph_compare4weeks_enabled (hopefully, more to come in the future!)

## get the arguments

* open get_args.go
* add an argblock (around line 330)

## actually generate the stats

* open stats_generate.go and add a codeblock:

```go
/*
stat: describe the use of the stat
expecting 1/2/3/x htmls:
list_the_filenames.html
*/
parameters := []interface{}{parameter1,parameter2,parameter3}
tableheaders := map[string]string{
   "Title_1": "YEAR",
   "Title_2": "MONTH",
   "Title_3": "DAY",
   "Title_4": "NB UNIQUE HITS",
}
xaxisfields := []int{0, 1, 2}
valuefield := 3
func genstats(args, string_for_log , statname_from_config_ini , querydb_key , parameters , tableheaders , xaxisfields , valuefield , legend)
```

> fill parameters will all parameters (in the exact order) as they are needed by your sql query
> tableheaders are NEEDED, even for non-table stats. In this case they are passed but not used
> xaxisfields are needed, even for non-linegraph stats. Pass return index numbers of string fields you want to be used in the x-axis
> valuefield is the integer value that has to be used for graphing. It is needed and needs to be an integer
