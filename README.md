# Data validation

This repository contains the data validation module for the TEC Toolkit.

## Getting Started

These instructions explain how to run and customise the Data Validation module.

### Prerequisites

- [RDFox](https://www.oxfordsemantic.tech) (> v.6) [^NB]

[^NB]: RDFox is a commercial product, but anyone with a corporate email address can request a free RDFox trial license.
Moreover, Oxford Semantic Technologies offers research licenses for free to accredited entities.

In the following, we assume that it is installed and added to the PATH.

### Running (RDFox)

The main entry point is the `master` script.

This data validation module reads the RDF files and checks if some constraints are verified.

How to execute it:

```sh
RDFox sandbox <root> master
```

where `<root>` is the "scripts" folder (`.` if you are inside it).

### Functionalities

#### Check if the data are "valid"

1. [Run the data validation module](#running-rdfox)
2. Check that all queries have **0** answers

#### Add another validation check

1. Add a file "check-CUSTOM_NAME-rules" with the rules to check
2. Add a file "check-CUSTOM_NAME-queries" with the `ASK` queries
   - Note that the queries must return no answer if the check is passed
3. Add a new command `exec check CUSTOM_NAME` in the "validate" file

<!-- ## Deployment

Add additional notes about how to deploy this on a live system

## Built With

## Contributing

Please read [CONTRIBUTING.md](...) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

## Authors -->

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

Some parts have been adapted from the [PRObs system](https://github.com/probs-lab) (by the [UK FIRES project](https://ukfires.org)).

---

<div style="text-align: center">

  This tool is part of the [TEC-Toolkit](https://github.com/TEC-Toolkit).

  <img src="https://tec-toolkit.github.io/assets/Logo%20TEC.svg" alt="TEC-Toolkit Logo" width=10%/>

</div>
