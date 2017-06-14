---
inFeed: true
description: load data
dateModified: '2017-06-14T19:22:08.132Z'
datePublished: '2017-06-14T19:22:09.542Z'
title: ''
author: []
publisher: {}
via: {}
sourcePath: _posts/2017-06-14-this-means-nothing.md
starred: false
datePublishedOriginal: '2017-06-14T19:21:02.963Z'
_type: Blurb

---
load data

infile 'ORDTRHST.CSV' "str '\\r\\n'"

append

into table MWEXPORT

fields terminated by ',' 

OPTIONALLY ENCLOSED BY '"' AND '"'

trailing nullcols

(

DCOUNTER,

GRP1,

GRP2,

GRP3 CHAR(4000),

SUM1,

SUM2,

SUM3,

SUM4,

SUM5,

SUM6,

SUM7,

SUM8,

SUM9,

TABLENAME "DECODE(:DCOUNTER, 'TABLENAME', 'TABLENAME', 'ORDTRHST')",

ID char(4000)

)