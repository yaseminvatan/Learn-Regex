# Learn-Regex

# Regex Tutorial: Matching an Email

## Introduction

A regular expression (regex) is a powerful tool for matching patterns in strings. This tutorial breaks down a regex used to validate email addresses: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. By the end of this tutorial, you'll understand how each part of the regex contributes to ensuring the input is a valid email address.

## Table of Contents

1. [Anchors](#anchors)
2. [Character Classes](#character-classes)
3. [Quantifiers](#quantifiers)
4. [Groups and Captures](#groups-and-captures)
5. [Escaped Characters](#escaped-characters)
6. [Conclusion](#conclusion)
7. [References](#references)
8. [About the Author](#about-the-author)

---

## Anchors

**Regex Component:** `^` and `$`

- **Explanation:**  
  - `^` asserts that the match must start at the beginning of the string.  
  - `$` asserts that the match must end at the end of the string.  
- **Example:**  
  For the input `"user@example.com"`, the anchors ensure the regex validates the entire string, not just a substring.

---

## Character Classes

**Regex Components:** `[a-z0-9_\.-]` and `[\da-z\.-]`

- **Explanation:**  
  - `[a-z0-9_\.-]` matches any lowercase letter (`a-z`), digit (`0-9`), underscore (`_`), dot (`.`), or hyphen (`-`).  
  - `[\da-z\.-]` is similar but also includes `\d`, which matches digits (`0-9`).  
- **Example:**  
  In `"user.name@example.com"`, `user.name` and `example` match these character classes.

---

## Quantifiers

**Regex Components:** `+` and `{2,6}`

- **Explanation:**  
  - `+` matches one or more occurrences of the preceding element.  
  - `{2,6}` matches between 2 and 6 occurrences.  
- **Example:**  
  - `([a-z0-9_\.-]+)` ensures the local part (e.g., `user.name`) contains one or more valid characters.  
  - `([a-z\.]{2,6})` ensures the domain extension (e.g., `com`) is 2 to 6 characters long.

---

## Groups and Captures

**Regex Components:** `()`  

- **Explanation:**  
  Parentheses `()` create capturing groups, allowing specific parts of the match to be extracted.  
- **Example:**  
  - Group 1: `([a-z0-9_\.-]+)` captures the local part (e.g., `user.name`).  
  - Group 2: `([\da-z\.-]+)` captures the domain name (e.g., `example`).  
  - Group 3: `([a-z\.]{2,6})` captures the domain extension (e.g., `com`).

---

## Escaped Characters

**Regex Components:** `\.`  

- **Explanation:**  
  The backslash `\` escapes the dot `.` so it matches a literal period instead of any character.  
- **Example:**  
  In `"user.name@example.com"`, the `.` between `example` and `com` is matched literally.

---

## Conclusion

This regex ensures that an email address has a valid structure, including a local part, `@` symbol, domain, and a valid extension. By understanding each component, you can adapt the regex for other input validation needs.

---

## References

Here are some resources that were helpful in creating this tutorial:

1. [MDN Web Docs: Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)  
   Comprehensive guide on regex syntax and usage in JavaScript.

2. [Regexr](https://regexr.com/)  
   Interactive tool for testing and debugging regular expressions.

3. [Regex 101](https://regex101.com/)  
   An excellent platform for exploring and breaking down regex patterns.

4. [JavaScript.info: Regular Expressions](https://javascript.info/regular-expressions)  
   Detailed explanations and examples of regex in JavaScript.

5. [Coding Boot Camp: Regex Tutorial](https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial)  
   A beginner-friendly walkthrough of regex basics and common patterns.

---

## About the Author

I am Yasemin Vatan, a junior full-stack developer and computer science student. My passion for web development and regular expressions has driven me to create this tutorial. Visit my [GitHub profile](https://github.com/yaseminvatan) for more projects and tutorials.

