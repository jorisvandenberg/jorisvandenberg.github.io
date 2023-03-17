---
title: Naming conventions
---

## config names
  
conf_stat_raw|unique_grouping_[subject](_includeallhits)(_forever)(_4weeks)  
conf => fixed  
stat => fixed  
raw|unique => are we counting raw or unique hits  
grouping => PerHour, PerDay, XDaysTotal  
subject => what are we counting? Referrers, SearchEngineReferrer,Hits  
includeallhits => optional ONLY IF we don't restrict the output to 2xx and 3xx hits  
forever => optional ONLY IF we don't restrict  the output to x days  
4weeks => optional ONLY IF we look at the last 4 weeks only  

## statement names

stmt_raw|unique_grouping_[subject](_includeallhits)(_forever)(_4weeks)  
stmt => fixed  
raw|unique => are we counting raw or unique hits  
grouping => PerHour, PerDay, XDaysTotal  
subject => what are we counting? Referrers, SearchEngineReferrer,Hits  
includeallhits => optional ONLY IF we don't restrict the output to 2xx and 3xx hits  
forever => optional ONLY IF we don't restrict  the output to x days  
4weeks => optional ONLY IF we look at the last 4 weeks only  

## file names

raw|unique_grouping_[subject](_includeallhits)(_forever)(_4weeks)_what.html  
raw|unique => are we counting raw or unique hits  
grouping => PerHour, PerDay, XDaysTotal  
subject => what are we counting? Referrers, SearchEngineReferrer,Hits  
includeallhits => optional ONLY IF we don't restrict the output to 2xx and 3xx hits  
forever => optional ONLY IF we don't restrict  the output to x days  
4weeks => optional ONLY IF we look at the last 4 weeks only  
what => table, linegraph, 4WeeksLinegraph
