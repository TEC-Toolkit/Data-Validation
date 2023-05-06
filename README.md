# Data validation

This repository contains the data validation module for the TEC Toolkit.

## Prerequisites

- [RDFox](https://www.oxfordsemantic.tech) (> v.6) [^NB]

[^NB]: RDFox is a commercial product, but anyone with a corporate email address can request a free RDFox trial license.
Moreover, Oxford Semantic Technologies offers research licenses for free to accredited entities.

In the following, we assume that it is installed and added to the PATH.

## Running (RDFox)

The main entry point is the `master` script.

This data validation module reads the RDF files and checks if some constraints are verified.

How to execute it:

```sh
RDFox sandbox <root> master
```

where `<root>` is the "scripts" folder (`.` if you are inside it).

## Operations

### Check if the data are "valid"

1. [Run the data validation module](#running-rdfox)
2. Check that all queries have **0** answers

### Add another validation check

1. Add a file "check-CUSTOM_NAME-rules" with the rules to check
2. Add a file "check-CUSTOM_NAME-queries" with the `ASK` queries
   - Note that the queries must return no answer if the check is passed
3. Add a new command `exec check CUSTOM_NAME` in the "validate" file

## Acknowledgments

Some parts have been adapted from the [PRObs system](https://github.com/probs-lab) (by the [UK FIRES project](https://ukfires.org)).
