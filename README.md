# Bug AimBot

This action helps developers find bug incuding commits using a tool known as Locus
Locus: LOcates bugs from software Change hUnkS

## Usage

```yaml
name: Call Locus

on:
  issues:
    type:
      - opened
        
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: 
```

## How it works

This action uses the text from the title and body of the issue and sends that and some other important information to our Locus tool.
Token corpora are created using the issue title and body as a bug report. Locus takes this bug report and all the changes committed before this bug was reported as the input. Each hunk is indexed as an independent document to be ranked based on the vector space model. The output of Locus is a ranked list of commits that most likely caused the bug.

## Limitations

* If a quotation mark is used in either the title or the body of the issue, it must have an accompanying quotation mark or the action will not work.
* The action relies on information from the title and body of issues, therefore it must be used as shown above.
