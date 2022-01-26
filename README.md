# mscons-parser

Python3 Class to parse EDIFACT MSCONS messages and converter to get a csv file from an MSCONS file.

Only the variant of MSCONS that is used by the utilies in Luxembourg will be tested. This is version 2.1a of the German MSCONS formats. The data will be accepted as liberally as possible so that possibly other dialects will also get read correctly.

Originally written by @jay-christnach.

Small changes were made by @flo-f to optimize for version 2.4 of the German format.

## How to use

```bash
python3 mscons2csv.py samples/DE-example.mscons.txt
python3 mscons2csv.py samples/TL-example.mscons.txt
```

This will create a file named `DE-example.mscons.txt.csv` in the `samples` folder.


## Components

### msconsparser.py
Stores the loadprofiles and the metadata extracted from an MSCONS file in its data structures.

### mscons2csv
Writes a semicolon delimited file with load profile data

### statemachine.py
a simple state machine that is used by msconsparser

### segmentgenerator.py
provides a next() function to return the next segment to be analysed. Segments are delinited by "'" in EDIFACT

## TODO
* docstrings and more comments and info
* adding command line options to mscons2csv
