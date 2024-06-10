# guess
Automagic convert things

## guess(input[, opts]) => Any
```
import guess from '@ludlovian/guess'

x = guess(stringishInput)
```

Guesses the type & converts the given input.

The default guesses:
- `null`, `undefined` are returned as is
- strings are converted to numbers if they don't result in `NaN`
- strings `true` and `false` are converted to `Boolean`s

If given the `options` object can have the following keys to turn on additional conversion
- `bool: true` will try to convert any strings beginning with 't' or 'f' in any case, or try to convert via a number
- `decimal: decimalFunction` will try to convert any strings that look like decimals
- `xml: xmlFunction` will try to convert xml-ish strings
- `date: true` will try to convert ISO date strings to `Date`

Anything is returned as is
