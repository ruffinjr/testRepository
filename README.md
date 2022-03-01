# Bug AimBot

This action helps developers find bug incuding commits using a tool known as Locus

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
Locus looks at changes in code to determine which commits most likely caused the current bug.
