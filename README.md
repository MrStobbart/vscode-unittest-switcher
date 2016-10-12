# Switch the unit test / production code.

This extension supports that switch the `unit test` / `production code`.

## Features
- Switch the `unit test` / `production code`.
    - Editor context menu `Go to Test/Code`.
    - Keyboard Shortcut `CTRL + 9` key.
    - Invoke `>Go to Test/Code` to the Command Palette(F1).
- Customizable suffix rule of `unit test`.

#### Example

![Navigation](images/preview.gif)

- If you are editing a `foo.js`, When the Command Palette(F1) `Go to Test/Code`(or press key `CTRL + 9` on editor), switched to `fooSpec.js`.

## Settings
- suffix rule of `unit test`.
```json
{
    // UnitTest suffix
    "unittest-switcher.unittest.suffix": [
        "Spec",
        "-spec",
        "Test",
        "-test",
        ".test"
    ],
}
```
- Default switchig rule is...

|Switch?|production code|unit test|
|----|----|----|
|Yes|foo.js|fooSpec.js|
|Yes|foo.js|foo-spec.js|
|Yes|foo.js|fooTest.js|
|Yes|foo.js|foo-test.js|
|Yes|foo.js|foo.test.js|
|No|foo.js|foo.test.ts|
|No|foo.js|fooSpec.js.map|

## Keyboard Shortcuts

The extension defines a editor keyboard shortcut for the `CTRL + 9` key.

## Hommage

It pays tribute to [QuickJUnit](https://github.com/kompiro/quick-junit).

## Release Notes

### 0.0.2

- Release to minimum features.

## License

MIT &#xA9; 2016 Takashi HOMMA (takas-ho)
