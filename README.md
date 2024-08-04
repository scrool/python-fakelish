# fakelish

English-like word generator.

## Installation

```bash
$ pip install --upgrade fakelish
```

## Usage

Package provides command line interface (CLI) tool which by default prints ten
words of length 6 to 9 letters:

```bash
$ fakelish
Predrons
Isishere
Uncette
Tripulogy
Oderve
Mageholy
Refess
Butarisse
Eloplae
Roidia
```

For more options see help:
```bash
$ fakelish --help
```

## Contributing

Please read CONTRIBUTING.md for details of the process for submitting pull
requests.

## License

This project is licensed under the MIT License - see the LICENSE file for
details.

## Origin

CLI and python library is ported from go implementation of fakelish project.

Word data included in this project have been converted from
Javascript/Typescript implementation to pure json like this:

```bash
$ curl -s https://raw.githubusercontent.com/nwtgck/fakelish-npm/develop/lib/word-probability.ts | sed 's/.*} = {"\^/{"^/;s/;$//' > word-probability.json
```

## Acknowledgments

[Ryo Ota (@nwtgck)](https://github.com/nwtgck) for original Go and JavaScript/TypeScript versions and word data.

## Related projects

* Go language and CLI: <https://github.com/nwtgck/go-fakelish>
* JavaScript/TypeScript: <https://github.com/nwtgck/fakelish-npm>
