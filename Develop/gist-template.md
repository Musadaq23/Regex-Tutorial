# Matching Regular Expressions with a Hex value

This tutorial will explain how regular expressions match with hex values.

## Summary

I will be explaining the regex pattern to match a hex value with or without the '#' character. 

^#?([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})$

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

The ```^``` anchor matches the start of a string and the $ anchor matches the end of a string. Together they ensure that the entire string matches the pattern. ```^#[0-9a-fA-F]{6}$```

### Quantifiers

Quantifiers are used to match a certain number of instances of a character or group. In this case, you can use the ```{}``` notation to match a specific number of digits or letters. ```^#[0-9a-fA-F]{4}$```

### OR Operator

The OR operator is used to match one of several alternatives. In this case, you can use the ```|``` symbol to match either a 3-character or 6-character hex value. ```^#([0-9a-fA-F]{3}|[0-9a-fA-F]{6})$```

### Character Classes

Character classes are used to match a range of characters. In this case, you can use the ```[]``` notation to match any digit or letter between A and F, both upper and lower case. ```^#[0-9a-fA-F]{6}$```

### Flags

Flags are used to modify the behavior of the regular expression. In this case, you can use the i flag to make the regular expression case-insensitive. ```^#[0-9a-f]{6}$``` (with the i flag)

### Grouping and Capturing

The parentheses ```()``` are used for grouping and capturing. In our regex pattern, you use them to group the two alternatives separated by the ```|``` OR operator.

### Bracket Expressions

Bracket expressions, also known as character classes, match any character from a set of characters. In our regex pattern, the ```[A-Fa-f0-9]``` bracket expression matches any uppercase letter A-F, lowercase letter a-f or any digit from 0-9.

### Greedy and Lazy Match

Greedy and lazy matching refer to how regular expressions match patterns in a string. Greedy matching will match as many characters as possible, while lazy matching will match as few characters as possible. ```.*``` and ```.*?```

### Boundaries

Boundaries are special characters that match the start or end of a word or line. The most commonly used boundaries are the caret ```^``` and dollar sign ```$```, which match the start and end of a line.

### Back-references

Back-references allow you to match a previously matched group again in the same regex pattern. They are useful when you want to ensure that two parts of a string match. ```(A)\d\1``` would match ```A1A``` or ```A2A```, but not ```A1B```, because it requires that the same letter (```A```) appear on both sides of the digit.

### Look-ahead and Look-behind

Look-ahead and look-behind are types of assertions that allow you to match a pattern only if it is followed by or preceded by another pattern, respectively. Look-ahead assertions are denoted by ```(?=...)```, while look-behind assertions are denoted by ```(?<=...)``` for positive assertions and ```(?<!...)``` for negative assertions.

## Author

visit my Github, [Musadaq23](https://github.com/Musadaq23)

