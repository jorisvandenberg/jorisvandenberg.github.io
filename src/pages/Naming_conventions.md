---
title: Naming conventions
---

## config names

conf_stat_raw|unique_[subject](_includeallhits)(_forever)(_4weeks)
conf => fixed 
stat => fixed
raw|unique => are we counting raw or unique hits
subject => what are we counting? Referrers, SearchEngineReferrer,Hits
includeallhits => optional ONLY IF we don't restrict the output to 2xx and 3xx hits
forever => optional ONLY IF we don't restrict  the output to x days
4weeks => optional ONLY IF we look at the last 4 weeks only

## statement names

stmt_raw|unique_[subject](_includeallhits)(_forever)(_4weeks)
stmt => fixed
raw|unique => are we counting raw or unique hits
subject => what are we counting? Referrers, SearchEngineReferrer,Hits
includeallhits => optional ONLY IF we don't restrict the output to 2xx and 3xx hits
forever => optional ONLY IF we don't restrict  the output to x days
4weeks => optional ONLY IF we look at the last 4 weeks only

## file names

raw|unique_[subject](_includeallhits)(_forever)(_4weeks).html
raw|unique => are we counting raw or unique hits
subject => what are we counting? Referrers, SearchEngineReferrer,Hits
includeallhits => optional ONLY IF we don't restrict the output to 2xx and 3xx hits
forever => optional ONLY IF we don't restrict  the output to x days
4weeks => optional ONLY IF we look at the last 4 weeks only
