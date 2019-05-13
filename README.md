# Deno Case Style [![Build Status](https://travis-ci.org/zekth/deno_case_style.svg?branch=master)](https://travis-ci.org/zekth/deno_case_style)

A string validator and formater for case Style

## Validate

Returns a boolean if the string is validated by the style Case:
```ts
import { validate } from "./mod.ts";

validate("SALADE-TOMATE-OIGNONS", caseStyle.screamingKebabCase); // true
validate("DIZ_IZ_DA_GLOBAL_VAL", caseStyle.screamingSnakeCase); // true
validate("SmokingIsBad", caseStyle.camelCase); // false
validate("imNotPascal", caseStyle.pascalCase); // false
```

## Format

Format the input string to the wanted style case
```ts
import { format } from "./mod.ts";

format("FOO Bar", caseStyle.kebabCase); // output: foo-bar
format("FOO Bar", caseStyle.snakeCase); // output: foo_bar
format("FOO Bar", caseStyle.camelCase); // output: fooBar
format("FOO Bar", caseStyle.pascalCase); // output: FooBar
format("FOO Bar", caseStyle.kebabCase); // output: foo-bar
format("FOO Bar", caseStyle.screamingKebabCase); // output: FOO-BAR
format("FOO Bar", caseStyle.screamingSnakeCase); // output: FOO_BAR

```
