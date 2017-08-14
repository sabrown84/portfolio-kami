---
layout: post
title: Work it Through
---

So here is the issue. I have been going through some of these algorithmic problems. They aren't easy yet so I usually do one and just keep going over it and over it until it sticks. I know there are many ways to get through them, but this is the way that works for me so far.

I've been learning Ruby and Ruby on Rails so that is the route that I took. I'm supposed to find the first duplicate in the array that has a minimal index. And if that doesn't exist then to return -1.

In first reading this I had a little fear in my heart, because I have information overload inside. I've read so many ruby questions that I don't know where to start most of the time. Therefore I had to think about it for a minute. Now, because it says "if that doesn't exist return -1" I know that I have to iterate somewhere. also I know this I am using arrays, and that means that as I iterate through them I need to put them somewhere...into and empty array. Based on these thoughts this is what I came up with:

```ruby
def firstDup(b)
  numbers = []
  b.each do |value|
    return value if numbers[value]
    numbers[value] = true
  end
  -1
end  
```
After seeing this I would explain it as "numbers" is the empty array that we are putting __values__ into. The array "b" is the mystery array that we are starting with and taking each element and looking at it and placing it into the "numbers" array until we find a __value__ that is a duplicate that is already in the "numbers" array. If we get to the end of the array and don't come across a duplicate then we return -1 and we are done.  
