# Regex Unravelled: "Hello World" 👋

Regular expressions, or regex, are a method devised by this mathematician fella Stephen Cole Kleene in 1951. These expressions are incredibly useful for searching, matching, and manipulating text strings in a precise yet flexible way. This guide aims to simplify regex by giving a simple explanation with a simple example, it's by no means comprehensive in its utilization but it should provide you with a template to work with.

## Summary

This guide breaks down a simple regex for the ever popular "Hello World". We'll explore different components of regex and iterations of our regex template to see how they can be used to refine our searches and extractions.

## Regex

`/hello[ ]world/g`

## Table of Contents

- [⚓ Anchors](#anchors)
- [🔢 Quantifiers](#quantifiers)
- [🔀 OR Operator](#or-operator)
- [🔠 Character Classes](#character-classes)
- [🚩 Flags](#flags)
- [👥 Grouping and Capturing](#grouping-and-capturing)
- [🔲 Bracket Expressions](#bracket-expressions)
- [💰🐢 Greedy and Lazy Match](#greedy-and-lazy-match)
- [✋ Boundaries](#boundaries)
- [🔙 Back-references](#back-references)
- [👀 Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
##


### Anchors ⚓

Anchors (^ for start, $ for end) are helpful if you wish to match the start or end of a string or line.  

`/^hello world$/g`

☝️ This matches "hello world" only if it's the entire string.

##
### Quantifiers 🔢

Quantifiers (*, +, ?, {n}, {n,}, {n,m}) adjust how many times a character or group appear.

`/hello[ ]world{2,3}/g` 

☝️ This example matches "hello worldd" or "hello worlddd".
##
### OR Operator 🔀

The OR operator (|) lets you look for this or that or that or this, basically giving you options. When you use it you can find all of either.

`/hello|world/g`

☝️ This matches "hello" or "world".

##
### Character Classes 🔠

Character classes ([]) match any one character from a set. In our first example [] contains only a space but can contain other values such as [.] or [-] or a combo.

`/hello[- ]world/g`

☝️ This matches "hello-world" or "hello world".
##
### Flags 🚩

Flags are important for scope, they modify the behavior of the regex. They sit outside the '/' at the end of the regex. There's 'g' (global search), 'i' (case-insensitive), 'm' (multiline), 's'(single line) , 'u' (unicode) and 'y' (sticky). There are others as well. They can be used alone or in combination.

`/hello[- ]world/gim`

☝️ This example applies global, case-insensitive, and multiline search to "hello world".
##
### Grouping and Capturing 👥

Grouping with parentheses () makes it easy to pick out specific parts of the text you're interested in. It's like highlighting important bits to use later.

`/(hello)[ ](world)/g`

☝️ This example picks out "hello" and "world" separately, so you can, for example, find them switched around in a string like "world hello".
##
### Bracket Expressions 🔲

Bracket expressions match one character from a specific set, such as [abc] for "a", "b", or "c". Our previous example in Character class covers this utilization already with [- ]

`See character class selection`

☝️❗☝️❗☝️❗
##
### Greedy and Lazy Match 💰🐢

Hilariously named, greedy quantifiers match as much as possible, while lazy quantifiers match as little as possible. For me this one was difficult to conceptualize its use, but imagine you are searching for the letter "a" on a string of "aaa", greedy match would take all 3, but lazy would simply take the first instance of a. 

`/hello[ ]world?/g `💰 (greedy)

 vs ⚔️

`/hello[ ]world??/g` 🐢 (lazy)
##
### Boundaries ✋

Boundaries (\b) make sure your search sticks to whole words ONLY. They're restrictive. Boundaries!

`/\bhello world\b/g`

☝️ This example finds "hello world" only when it's standing by itself, not when it's part of a bigger word.
##
### Back-references 🔙

Back-references match the same text as previously matched by a capturing group. Like repeats.

`/(hello)[ ]\1/g`

☝️ This example matches "hello hello".
##
### Look-ahead and Look-behind 👀

Look-ahead and look-behind assertions match based on prior or preceding text without including it in the match.

`hello(?=[ ]world)/g`

☝️ This example matches "hello" only if it's followed by " world".
##

## Additional resources  📖 📖 📖

Here's some extra resources that helped me and might help you too.

- [YouTube](https://www.youtube.com/watch?v=sXQxhojSdZM) - I found this explanation concise and entertaining, maybe it will help you understand!

- [Regexr](https://regexr.com/) - It's a helpful tool for actually practising using regex and it helps conceptualizing usage.

## Author 👉😎

I hope this guide helps you understand and utilize regex! Good luck out there!

GitHub: [JohnM89](https://github.com/JohnM89)

👋