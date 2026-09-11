# freaky-colours

A Hangar package for the [FREAK](https://github.com/FREAK-lang-dev/Freak-lang) programming language

Meant to simplify the use of coloured output.

You don't need ANSI

---

## How to import?


Using the Hangar CLI tool:

`hangar add freaky-colours https://github.com/GemCreate/freaky-colours`

### Careful

An installed package is not visible to the compiler. freak build never reads hangar_modules/ and never reads [dependencies]. A use pkg::{…} line is rewritten to a comment before parsing, so nothing is imported and the first call into the package fails with unknown callable. Hangar today is a manifest and download tool. The link step that would make a dependency usable does not exist in V3.

---

## Usage Example:
```rust
-- FREAK CODE
setFG_blue()
sayC("THE TEXT IS BLUE!")
setBG_red()
sayC("THE BACKGROUND HAS TURNED RED")
resetColors()
sayC("Aww everything is back to normal")

setFG_magenta()
setBG_b_green() -- b before the colour indicates brightness
pilot age = askC("How old are you? ")
setFG_b_yellow()
sayC("You are " + age + " years old.")

```
