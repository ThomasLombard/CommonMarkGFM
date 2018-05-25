CommonMarkGFM
=============

`CommonMarkGFM` is an extra thin wrapper around [cmark-gfm](https://github.com/github/cmark). Its purpose is to expose this C library to iOS projects, and be compatible out of the box with [Carthage](https://github.com/Carthage/Carthage) dependency manager.

You can add this dependency in your Cartfile:
```
github "benmuta/CommonMarkGFM"
```

Then, in any Swift source file:

```swift
import CommonMarkGFM
```
You would then have the `cmark-gfm` C library exposed and available to call from Swift.

For instance:

```swift
let markdownSource = "Lorem __ipsum dolor__ sit [amet](https://example.com). - *2018*"
let htmlCString = cmark_markdown_to_html(markdownString, markdownString.utf8.count, 0)
```

Current version of cmark-gfm: 0.28.3.gfm.12.