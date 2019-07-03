# Strings Lab 2

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1√

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
```

Example

Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```
``` swift
var problem = "split this string into words and print them on separate lines"

var newProblem = problem.components(separatedBy: " ")

for i in newProblem {
print (i)
}
```


## Question 2

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
let testString = "  How   about      thesespaces  ?  "
//condensedString = " How about thesespaces ? "
```


## Question 3√

Given a string with multiple words. Reverse the string word by word.

Example:

Sample Input: `"Swift is the best language"`

Sample Output: `"language best the is Swift"`

``` swift

var word = "Swift is the best language"
var reversed = word.components(separatedBy: " ").reversed()
var reversedWord = ""
for i in reversed {
reversedWord += "\(i) "
}
print (reversedWord, terminator: " ")

```


## Question 4√

Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: `"danaerys dad cat civic bottle"`

Sample Output: `2`
``` swift
var sampleWords = "danaerys dad cat civic bottle"
var reversedSampleWords = sampleWords.components(separatedBy: " ")
var palindromes = ""

for i in reversedSampleWords{
if i == String(i.reversed()){
palindromes += "\(i) "
}
}
palindromes.components(separatedBy: " ").count - 1
print(palindromes)
```

## Question 5√

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true`

```swift
let record = "PPALLP"
var letterA = ""
var lll = "LLL"

for i in record{
if i == "A"{
letterA += String(i)
}
}
if letterA.count > 1 || record.contains(lll)  {
print (false)
}else {
print (true)
}

```

## Question 6√

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:

Sample Input1: `("a", "b")`

Sample Output1: `False`

Sample Input2: `("aa", "aab")`

Sample Output2: `True`

```swift
let inputValue = (first:"aa", second: "aab")

let randomCheck = String(inputValue.second.sorted()).contains(String(inputValue.first.sorted()))
print(randomCheck)

```
