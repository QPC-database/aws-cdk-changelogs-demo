0.5.1
-----

Released: November 28, 2010

### Small Changes

  * Fixed a problem where “SyntaxError: Invalid range in character class.” error
    appeared when using command-line version on Widnows
    ([GH-13](https://github.com/dmajda/pegjs/issues/13)).

  * Fixed wrong version reported by `bin/pegjs --version`.

  * Removed two unused variables in the code.

  * Fixed incorrect variable name on two places.

0.5
---

Released: June 10, 2010

### Big Changes

  * Syntax change: Use labeled expressions and variables instead of `$1`, `$2`,
    etc.

  * Syntax change: Replaced `:` after a rule name with `=`.

  * Syntax change: Allow trailing semicolon (`;`) for rules

  * Semantic change: Start rule of the grammar is now implicitly its first rule.

  * Implemented semantic predicates.

  * Implemented initializers.

  * Removed ability to change the start rule when generating the parser.

  * Added several compiler optimizations — 0.5 is ~11% faster than 0.4 in the
    benchmark on V8.

### Small Changes

  * `PEG.buildParser` now accepts grammars only in string format.

  * Added “Generated by ...” message to the generated parsers.

  * Formatted all grammars more consistently and transparently.

  * Added notes about ECMA-262, 5th ed. compatibility to the JSON example
    grammar.

  * Guarded against redefinition of `undefined`.

  * Made `bin/pegjs` work when called via a symlink
    ([issue #1](https://github.com/dmajda/pegjs/issues/1)).

  * Fixed bug causing incorrect error messages
    ([issue #2](https://github.com/dmajda/pegjs/issues/2)).

  * Fixed error message for invalid character range.

  * Fixed string literal parsing in the JavaScript grammar.

  * Generated code improvements and fixes.

  * Internal code improvements and fixes.

  * Improved `README.md`.

0.4
---

Released: April 17, 2010

### Big Changes

  * Improved IE compatibility — IE6+ is now fully supported.

  * Generated parsers are now standalone (no runtime is required).

  * Added example grammars for JavaScript, CSS and JSON.

  * Added a benchmark suite.

  * Implemented negative character classes (e.g. `[^a-z]`).

  * Project moved from BitBucket to GitHub.

### Small Changes

  * Code generated for the character classes is now regexp-based (= simpler and
    more scalable).

  * Added `\uFEFF` (BOM) to the definition of whitespace in the metagrammar.

  * When building a parser, left-recursive rules (both direct and indirect) are
    reported as errors.

  * When building a parser, missing rules are reported as errors.

  * Expected items in the error messages do not contain duplicates and they are
    sorted.

  * Fixed several bugs in the example arithmetics grammar.

  * Converted `README` to GitHub Flavored Markdown and improved it.

  * Added `CHANGELOG`.

  * Internal code improvements.