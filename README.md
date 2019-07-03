# Strings Lab 2

## Question 1

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"
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
```
var words = problem.components(separatedBy: " ")

for word in words {
print(word)
}
```

## Question 2

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
let testString = "  How   about      thesespaces  ?  "
//condensedString = " How about thesespaces ? "

```
```
var condensedString = testString.replacingOccurrences(of: "[ ]+", with: " ", options: .regularExpression)

print(condensedString)

```


## Question 3

Given a string with multiple words. Reverse the string word by word.

Example:

Sample Input: `"Swift is the best language"`

Sample Output: `"language best the is Swift"`

```
let regular = "Swift is the best language"
let words = regular.components(separatedBy: " ")

var reversedNames = [String]()

for arrayIndex in stride(from: words.count - 1, through: 0, by: -1) {
reversedNames.append(words[arrayIndex])
}
let joined = reversedNames.joined(separator: " ")
print(joined)
```

## Question 4

Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: `"danaerys dad cat civic bottle"`

Sample Output: `2`

```
let regularString = "danaerys dad cat civic bottle"
let regularWords = regularString.components(separatedBy: " ")
var palindromeCounter = 0

for word in regularWords {
if (String)(word) == (String)(word.reversed()){
palindromeCounter += 1

}}
print(palindromeCounter)

```
## Question 5

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true`

```
var input = "PPALLP"
var aTracker = 0

for char in input {
if char == "A" {
aTracker += 1
}
}
if input.contains("LL") || aTracker > 1 {
print("False")
}else {
print("True")
}

```
## Question 6

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:

Sample Input1: `("a", "b")`

Sample Output1: `False`

Sample Input2: `("aa", "aab")`

Sample Output2: `True`


```
var myTuple = ("magazine input", "ransom input")
var myBool = false
var count = 0

for i in myTuple.0 { //h, i
for j in myTuple.1 { //i
if j == i {
count += 1
continue
} else {
continue
}
}
}
if count == (myTuple.0).count {
myBool = true
}

print(myBool)
```
