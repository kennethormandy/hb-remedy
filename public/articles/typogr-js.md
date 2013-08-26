# Typogr Test

All of this is server side. Most of the following content is borrowed from the [Typogr.js readme](#).

## amp

Wraps ampersands in HTML with so they can be styled with CSS. Ampersands are also normalized to &. Requires ampersands to have whitespace or an   on both sides. Will not change any ampersand which has already been wrapped in this fashion.

This & That

```html
This <span class="amp">&amp;</span> That
```

## quotes

Wraps initial quotes in `<span class="dquo">` for double quotes or `<span class="quo">` for single quotes. Works inside the appropriate block elements.

"Hello"

```
&quot;Hello&quot;
```

Note that if you are quoting someone, it should really be wrapped in `<q>` tags and use CSS generated quotes instead.

## smartypants

* Straight quotes ( " and ' ) into “curly” quote HTML entities (‘ | ’ | “ | ”)
* Backticks-style quotes into “curly” quote HTML entities (‘ | ’ | “ | ”)
* Dashes into n-dash and m-dash entities (– | —)
* Three consecutive dots (“...”) into an ellipsis entity (…)

All without messing up code blocks:
```json
{
  "pretty": 'cool'
}
```

## widont

Based on Shaun Inman's PHP utility of the same name, replaces the space between the last two words in a string with `&nbsp;` to avoid a final line of text with only one word.

## ord

Wraps number suffix's in `<sup class="ord"></sup>` so they can be styled.

## caps

This isn’t actually documented yet. Multiple concecutive capital letters

## typogrify

Applies all of the following filters, in order:

* amp
* widont
* smartypants
* quotes
* ord