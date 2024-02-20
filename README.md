# regex-tutorial

As a web developer student for UCSD Fullstack Web Development Bootcamp, I have been given the opportunity to learn about regex "Regular Expressions." To be able to understand what a regex is, its purpose, find the search pattern a regex defines, and how I'm able to implement this throughout my developer journey.

In this tutorial I will breaking down the different parts of a regex I chose, giving you a better understanding what a regex is, and how it can be used!

## Summary

A regex also known as a Regular expressions, are a series of special characters that define a search pattern.
The regex I have chosen is called "Matching an Email." This search pattern is email validation, where its job is to check if the string will fulfill the requirements for a basic email.

"Matching an Email" regex:
```md
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

To start off, <br>
for every regex it is also considered as a literal, and it is always wrapped in slash characters **/** <br>
As shown below, our regex "Matching an Email" is wrapped in slash characters **/**

The "Matching an Email" regex:
```md
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

### Anchors

After starting our regex with wrapping foward slash **/** characters, we than begin our strings with the characters **^** and **$** known as anchors

The ^ anchor -> starts the string with the characters that follow it, after the opening /

The $ anchor -> ends the string with the characters that precede it, following the closing /

Opening / with the **^** anchor to start the string

```md
/^
```

Closing **$** anchor, following the closing /
```md
$/
```

### Bracket Expressions
After setting your Anchors,
To identify what certain types of characters we want to include in our string, we set those certain characters within **Bracket Expressions**!

**Bracket Expressions** are anything within the square brackets **[]** representing a range of characters that we want our string to match.

We use Square brackets to wrap our characters:
```md
[]
```

The string can contain any LOWERCASE letter between a to z, **a-z**
```md
/^[a-z]$/
```

The string can contain any number between 0 to 9, **0-9**
```md
/^[0-9]$/
```

The string can contain a underscore, backward slash, a period, and a hyphen
```md
/^[_\.-]$/
```

The **Three Bracket Expressions** for "Matching an Email" regex:
```md
[a-z0-9_\.-] [\da-z\.-] [a-z\.]
```

### Quantifiers
Now that we've identified the Bracket Expressions, we are able to add more to our regex using **Quantifiers**.

**Quantifiers** set the **limits** of the string that your regex matches (OR an individual section of the string).
Being able to set the **minimum** and **maximum** number of characters that your regex is looking for.

Some examples of **Quantifiers**:
* -> Matches the pattern zero or more times
+ -> Matches the pattern one or more times
? -> Matches the pattern zero or one time
{} -> Curly brackets can set **three types of limits** for a match
    1. { n } -> Matches the pattern exactly **n** number of times
    2. { n, } -> Matches the pattern at least **n** number of times
    3. { min, max } -> Matches the pattern from the minimum **min** amount and the maximum **max** amount,                                seperated by a comma within the curly brackets

The **Quantifiers** for "Matching an Email" regex:
For this these two seperate parts that make up our string, the + means the pattern within the brackets has to match one or more times to the characters provided
```md
([a-z0-9_\.-]+)
```
```md
([\da-z\.-]+)
```

For this part of the string, the **{2,6}** we have set a minimum of 2 characters and maximum of 6 characters
```md
([a-z\.]{2,6})
```

NOTE:
- **Quantifiers** must be identified and placed outside of the Square Brackets to set your limits properly

### Grouping Constructs
After adding our Quantifiers, say we wanted to set different types of limits to specific parts of our regex. This is where **Grouping Constructs** come to play!

With **Grouping Constructs** we are able to seperate a string with **( )** parenthesis. Each section within parentheses is known as a **subexpression**. By doing this we can make certain requirements needed to validate that part of the string.

The Grouping Constructs **subexpressions** for "Matching an Email" regex:

```md
([a-z0-9_\.-]+)
```

```md
([\da-z\.-]+)
```

```md
([a-z\.]{2,6})
```

NOTE:
- Anything inside the brackets does not require the string to meet ALL of these requirements, it can meet any of them

### Character Classes
A **Character Classes** defines a set of characters

The **Character Classes** "Matching an Email" third subexpression <br>
Inside our third subexpression the backward \d is our **Character Class**
```md
([\da-z\.-]+)
```

NOTE:
Similar to the bracket expression **[0-9]**, matches any Arabic numeral digit
```
\d
```

### Character Escapes

The **Character Escapes** represents as a backwards slash but where it is placed is very important. Inside a bracket expression would act differently.

The **Character Escapes** for "Matching an Email" regex:

Between our Second and Third subexpression, this **Character Escape** **\\.** tells us that before reading our third expression **([a-z\.]{2,6})** we must look for the **.** first
```md
/^   ([a-z0-9_\.-]+)   @   ([\da-z\.-]+)   \.   ([a-z\.]{2,6})   $/
```

## Author

If you have any questions, please contact me at businesswawj@gmail.com. You can also visit my GitHub page at https://github.com/lifewawj or come say hi on my socials @lifewawj 