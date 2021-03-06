# Changelog

All notable changes to similar are documented here.

## 1.2.0

* Make the unicode feature optional for inline diffing.
* Added Hunt–McIlroy LCS algorithm (`lcs`).
* Changed the implementation of Mayer's diff.  This has slightly changed the
  behavior but resulted in snigificantly improved performance and more
  readable code.
* Added `NoFinishHook` to aid composing of diff hooks.

## 1.1.0

* More generic lifetimes for `iter_changes` and `iter_inline_changes`.
* Added `iter_all_changes` shortcut as this is commonly useful.
* Added `iter_slices` to `DiffOp` to quickly get an iterator over the
  encoded slices rather than individual items like `iter_changes` does.
* Added the `utils` module with various text diffing utilities.
* Added `TextDiffRemapper` which helps with working with the original, pre
  `TextDiff` tokenization slices.

## 1.0.0

* Add `get_diff_ratio`.
* Add support for byte diffing and change the text interface to abstract
  over `DiffableStr`.
* Restructured crate layout greatly.  Text diffing is now on the crate root,
  some functionality remains in the algorithms.
* The `Change` type now also works for non text diffs.

## 0.5.0

* Add `DiffOp::apply_to_hook` to apply a captured op to a diff hook.
* Added missing newline handling to the `Changes` type.
* Made unified diff support more flexible through the introduction of
  the `UnifiedDiff` type.
* Fixed grouped diff operation to return an empty result if the diff
  does not show any changes.
* Added inline diff highlighting support.
* Changed word splitting to split into words and whitespace.
* Added support for unicode based word splitting (`TextDiff::from_unicode_words`).

## 0.4.0

* Change `get_close_matches` to use Python's quick ratio optimization
  and order lexicographically when tied.

## 0.3.0

* Added grapheme and character level diffing utilities.
* `DiffOp::as_tag_tuple` is now taking the argument by reference.
* Added `TextDiff::ratio`.
* Added `get_close_matches`.

## 0.2.0

* Fixed a bug in the patience algorithm causing it not not work.

## 0.1.0

* Initial release.
