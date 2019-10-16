---
layout: post
title: Still Stuck on Day 8 of 30 Days Of Code Challenge
---

![Tuesday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Atom2.png)

## Day 8: October 16, Wednesday

**Today 's Progress**: I am working through getting [30-days-of-code](https://www.hackerrank.com/) I'm still stuck in Day 8.
**Thoughts**: While I could get past the timeout error using JS, Its not going to help me get through my problems with golang.

### Resources used:
  * [Github repo for 30 days of code](https://github.com/Johnny2136/30-Days-of-Code)
  * [HackerRank.com 30 days of code : Directories and Maps](https://www.hackerrank.com/challenges/30-dictionaries-and-maps/problem)
  * [GoLang playground](https://play.golang.org/)
  * [golangprograms.com](https://www.golangprograms.com/golang-package-examples.html)

### Objective

Work though the Problem with `Your code did not execute within the time limitsⓘ!` The test case is [here](https://hr-testcases-us-east-1.s3.amazonaws.com/17161/input02.txt?AWSAccessKeyId=AKIAJ4WZFDFQTZRGO3QA&Expires=1571242598&Signature=kwc65GXniSAWDeekbRa8vIDAyog%3D&response-content-type=text%2Fplain) yielding proper results as shown in the [Test case results](https://hr-testcases-us-east-1.s3.amazonaws.com/17161/output02.txt?AWSAccessKeyId=AKIAJ4WZFDFQTZRGO3QA&Expires=1571242382&Signature=xjUb5E2MavFp610b1QrKHbpYRHQ%3D&response-content-type=text%2Fplain) the issue is it failed to execute fast enough for the environments time out.


### Task

Given `n` names and phone numbers, assemble a phone book that maps friends' names to their respective phone numbers. You will then be given an unknown number of names to query your phone book for. For each `name` queried, print the associated entry from your phone book on a new line in the form `name=phoneNumber;` if an entry for `name` is not found, print Not found instead.
*Note:* Your phone book should be a Dictionary/Map/HashMap data structure.

### Input Format

The first line contains an integer, `n`, denoting the number of entries in the phone book.
Each of the `n` subsequent lines describes an entry in the form of 2 space-separated values on a single line. The first value is a friend's name, and the second value is an 8-digit phone number.

After the `n` lines of phone book entries, there are an unknown number of lines of queries. Each line (query) contains a `name` to look up, and you must continue reading lines until there is no more input.

*Note:* Names consist of lowercase English alphabetic letters and are first names only.

### Output Format

On a new line for each query, print Not found if the name has no corresponding entry in the phone book; otherwise, print the full `name` and `phoneNumber` in the format `name=phoneNumber`.

Sample Input
```
3
sam 99912222
tom 11122222
harry 12299933
sam
edward
harry
```
Sample Output
```
sam=99912222
Not found
harry=12299933
```
### My Code
```go
package main
import "fmt"

func main() {
 //Enter your code here. Read input from STDIN. Print output to STDOUT
 var n int
    m := make(map[string]int)
   // make map to store scanned data
    fmt.Scan(&n)
    //Scan test data
    var name string
    var number int
    for i := 0; i < n; i++ {
        fmt.Scan(&name)
        fmt.Scan(&number)
        m[name] = number
    }
    //Query for values
    var query string
    for {
        _, err := fmt.Scanf("%s", &query)
        if err != nil {
            break
        }
        if value, ok := m[query]; ok {
            fmt.Printf("%s=%d\n", query, value)
        } else {
            fmt.Println("Not found")
        }
    }
}
```


**Link(s) to work**

1. Working on my 30 days of Go on HackerRank.com.

Code is at [https://github.com/Johnny2136/30-Days-of-Code](https://github.com/Johnny2136/30-Days-of-Code).
