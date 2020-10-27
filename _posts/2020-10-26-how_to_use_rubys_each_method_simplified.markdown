---
layout: post
title:      "How to use Ruby's .each method—simplified"
date:       2020-10-27 02:35:15 +0000
permalink:  how_to_use_rubys_each_method_simplified
---


The content of your blog post goes here.Ruby is one of my favorite languages because of its expressiveness, intuitiveness and ease of use. A good example of this is Ruby's **.each** method. Let's dive in!

First, we're going to set the variable **friends** equal to an array of names:

```friends = ["Daniel", "Jen", "Tony", "Ellen"]```

Now let's call the **.each** method on the friends array.

```
friends.each
```

When you call the **.each** method on friends, what you're doing is **iterating**, or **going through each** array element one-by-one.

When we call **.each** on the **friends** array, the iteration starts from the first array element "Daniel" and finishes at the last array element "Ellen":

```
first iteration:
["Daniel", "Jen", "Tony", "Ellen"]
    ^
``` 
```
second iteration:
["Daniel", "Jen", "Tony", "Ellen"]
             ^
``` 
```
third iteration:
["Daniel", "Jen", "Tony", "Ellen"]
                    ^
``` 
```
fourth and last iteration:
["Daniel", "Jen", "Tony", "Ellen"]
                             ^
``` 
Now that we have iteration down, let's talk about what a "block" is.

>What is a block?

A **block** is simply a piece of code that lives between *do* and *end*.

A block usually follows a method call. In our case the method is **.each** so the block will follow after:

```
The block:

do |name|  #the block starts here!
   #...some code to be executed...
end  #the block ends here!
```
```
The block following the .each method:

friends.each do |name|
   #...some code to be executed...
end
```

Now, you may be thinking what that |name| thing is inside the block.


|name| is called a **block parameter**.


> The "name" inside the double pipes || is just a placeholder. You can actually replace it with any valid variable name: |first_name|, |x|, etc.

As **.each** iterates through each name in the **friends** array, the name (e.g. "Daniel") will be passed *into* the block and be assigned to the variable inside the double-pipe.

```
friends.each first iteration:
["Daniel", "Jen", "Tony", "Ellen"]
    ^

"Daniel" gets assigned to the variable inside the block
parameter |name| and then gets passed into the block.
```
```
the block:

do |name|

# We're now inside the block
# The variable "name" is set equal to "Daniel" (name = "Daniel")

puts name 
# The above code gets executed and the console outputs "Daniel"
# >> "Daniel"

end 
# block ends for current iteration and moves to the next name
# in the friends array: "Jen"

``` 

These steps will continue for each name in the friends array until all names are outputted:


```
>> "Daniel" # first iteration
>> "Jen" # second iteration
>> "Tony" # third iteration
>> "Ellen" # fourth and last iteration
``` 

This is the **.each** method and **blocks** in a nutshell. I hope you found this helpful. Happy coding!
