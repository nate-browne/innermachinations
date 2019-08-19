---
layout: post
title: "Better CS"
date: 2019-8-19 12:00 -0700
categories: programming-languages CS education
---

## Getting Started with Functional Programming
---

I apologize for the delay in posts; I've been somewhat busy. That said, I'm excited to start up
a new series on this blog: a series of posts about becoming a better computer scientist. Don't worry,
I haven't forgotten about my music decomposition series; I'll do that one next week.
<br><br>
Better CS is aimed at making the reader into a better computer scientist (go figure). Each essay,
I'll be covering a different aspect of becoming a better computer scientist, ranging from learning
how to deal with proofs to reading research papers and textbooks to the job hunt. This first one will
will be about learning different ways of approaching programming, using the paradigm of functional
programming and the PL Haskell for examples.
<br><br>
Firstly, let me define some terms. A [*paradigm*](https://en.wikipedia.org/wiki/Programming_paradigm) in programming language theory
is a way to classify programming languages based on their features. The two main meta-categories of programming paradigms
are *imperative* (you tell the computer how to change its state) and *declarative* (you declare properties, but not
necessarily how to compute it). Under these meta-categories are more specific ones, such as *procedural* (group instructions
into procedures), *object-oriented* (group instruction based on what state they operate on), *logic* (desired result
is declared as the answer to a question using a system of facts and rules), and more.
<br><br>
Every programming language in existence fits into at least one paradigm, though some languages fit more than one.
For example, Python can be written in a functional way, a procedural way, or even an object-oriented way.
Java, by contrast, is strictly object-oriented. Even though it's not part of the topic, I'll quickly digress to show
an example of these paradigms using everyone's favorite example, <code>hello world</code>.
The output of each of these examples will be identical.
<br><br>
First, let's see what hello world looks like in a strictly object-oriented language. We'll use Java:
{% highlight java %}
public class Hello {
  public Hello() {
    super();
  }
  public void sayHello() {
    System.out.println("Hello world!");
  }

  public static void main(String[] args) {
    Hello hi = new Hello();
    hi.sayHello();
  }
}
{% endhighlight %}
<sup>I know that this is overkill and we only really need `main`, this is just an example for the sake of argument.</sup>
Note the class syntax which defines the module, and how `sayHello` can only be used in context of the class. Object-oriented
is commonly used in industry, where grouping things according into units seems "logical" (though this is contested, we'll revist this).
<br><br>
Next up, we'll do it in Python to demonstrate procedural programming.
{% highlight python %}
def say_hello() -> None:
  print("Hello world!\n")

if __name__ == "__main__":
  say_hello()
{% endhighlight %}
Notice the single procedure (`say_hello`) used and defined without the context of a class. This lends itself nicely to "quick and dirty"
programming, such as scripting.
<br><br>
Now, let's see this example in Haskell:
{% highlight haskell %}
hello :: IO()
hello = putStrLn "Hello world!"
{% endhighlight %}
Doesn't look too bad, right? Right. Now, let's get into some of the specifics.
<br><br>
[Haskell](http://haskell.org) is a statically typed, strongly typed, purely functional programming language created by some researchers in Glasgow, Scotland.
It is based heavily on [the lambda calculus](https://en.wikipedia.org/wiki/Lambda_calculus), a mathematical system
created by Alonzo Church to model computation (that's a story for another time, though).
Without getting into it, lambda calculus has three things: variables, abstractions (function definitions), and applications (function application). With just these three, you can be fully expressive and imitate *any* programming language.
<br><br>
Let's break down that first sentence. *Statically typed* means that all expressions must type-check at compile time to be allowed.
The alternative to this is *dynamic typing*/*duck typing*, used by languages like Python which follows this mantra:
> If it walks like a duck, looks like a duck, and quacks like a duck, then it's a duck.

This basically means that the interpreter doesn't typecheck and tries hard to make your expression work, and it throws a `TypeError`
if what you give it *truly* doesn't make sense. This is accomplished via a mechanism that I don't really feel like explaining, so
you can [read about it here](https://www.quora.com/What-is-Pythons-type-system) if you wanna know. It basically boils down to everything being an object in Python.
The reason this is nice is that you know *exactly* how everything will work ahead of time. No more "wait what does this function return?"
since you know exactly what type to expect back from it.
<br><br>
*Strongly typed* means that you don't get any type coercion. Languages like JavaScript (weakly typed) allow you to do stuff like this:
{% highlight javascript %}
"2" + 3 // evaluates to '23'
console.log(('b' + 'a' + + 'a' + 'a').toLowerCase());
// this ^ evaluates to 'banana'. Seriously, try it.
{% endhighlight %}
None of the above would work in Haskell. In fact, the top will give you an error saying something like
"<code>no instance of Num Char arising from a use of '+'</code>" or something like that.
Quick aside though, the top would work in Java (even though it's strongly typed) because the compiler
would change it to be `"2" + Integer.toString(3)` which typechecks out to be a `String`.
This is nice because it means that you don't have to worry about any weird compiler tricks making your
code not do what you think it'll do.
<br><br>
*Purely functional* means that Haskell is a language where every function is *pure*, i.e., every function has no side effects.
What does this mean in practical terms? It means that a function like this one would __never__ exist in Haskell:
{% highlight python %}
global_var = 5

def add_one(x: int) -> int:
  print("This is a side effect")
  global_var += 10
  return x + 1
{% endhighlight %}
The above function has two side effects; namely, it prints something to the screen as well as sets a global variable.
The fact that Haskell doesn't do this means that you don't have as much to worry about when you're reading it;
what you see is exactly what you get in terms of each function.
<br><br>
*This is nice, but why do I care? Why should I care about functional programming? Imperative works just fine.* 
The reason you should care is because learning how to code in a functional paradigm *will* improve your code that you
write in __all__ contexts. It'll help you understand stuff ranging from lambdas in Python to callbacks and promises
in JavaScript. You'll learn a new way of approaching problems. It'll help with learning languages like Rust.
And, you'll be able to code in a dope langauge at the end of it all. With that introduction out of the way, let's dive
in!
<br><br>
Here's a question: How would you sum up the values of a list of integers? Something like `[1,2,3] => 6`. Let's look at how this
would be approached in C++:
{% highlight c++ %}
#include <vector>

using std::vector;
using std::cout;
using std::endl;

int sum(vector<int> & vec) {
  int sum = 0;
  while(!vec.empty()) {
    sum += vec.back();
    vec.pop_back();
  }
  return sum;
}

int main(void) {
  vector<int> vec;
  vec.push_back(1);
  vec.push_back(2);
  vec.push_back(3);
  vec.push_back(4);
  cout << "The sum is: " << sum(vec) << endl;
  // Prints: The sum is 10
  return 0;
}
{% endhighlight %}
And here's three different versions in Haskell:
{% highlight haskell %}
import Prelude hiding (sum, reverse)
import Data.List (foldl')

-- Standard way
sum :: [Int] -> Int
sum [] = 0
sum (x:xs) = x + sum xs

-- Tail recursive way (optimized by compiler)
sum' :: [Int] -> Int
sum' lst = helper lst 0
  where
    helper :: [Int] -> Int -> Int
    helper [] sum = sum
    helper (x:xs) sum = helper xs (x + sum)

-- Use library function implementing the second way
sum'' :: [Int] -> Int
sum'' = foldl' (\acc x -> x + acc) 0
{% endhighlight %}
Few things to note here. One, Haskell has *no loops*. No `for`, no `while`. We get around this by making heavy use of *recursion*
(defining things in terms of itself), which is essentially [*mathematical induction*](https://en.wikipedia.org/wiki/Mathematical_induction).
We'll get into the latter during the post about proofs, but essentially, you define a problem in terms of its simplest form (base case) and then use that definition to solve a more general case. In terms of our `sum` function, the `sum` of an empty list is 0,
and the sum of a non-empty list is the sum of the element plus the sum of the list with that element removed. Looking at a simple case,
```
sum [1,2,3]
=> 1 + sum [2,3] # match the bottom pattern
=> 1 + 2 + sum [3] # match the bottom pattern
=> 1 + 2 + 3 + sum [] # match the base case
=> 1 + 2 + 3 + 0 # simplify
=> 6
```
We define this in Haskell by using pattern matching, going from specific down to general. The top pattern in `sum` says what
to do with an empty list (return 0). The bottom pattern says that any list that is composed of an element and the rest of the list
(so literally every other list) has a sum defined as that element plus the result of calling `sum` on the rest of the list.
`sum'` does the same, just using a technique known as [tail recursion](https://en.wikipedia.org/wiki/Tail_call) to allow
the compiler to optimize. The bottom is how I'd do it if I were using library functions (though I'd probably just use the built-in
`sum` instead...).
<br><br>
Two, Haskell syntax is weird, but really it looks like defining piecewise functions in math. This means that you can read through
well written Haskell and reason out what it is doing, providing you understand the weird little bits every so often.
<br><br>
Three, Haskell's purity is quite apparent here. No print statements or global state, just inputs and operations on them.
<br><br>
Now, how bout something a bit more fun? Let's implement a Python program and a Haskell module to calculate values for [Goldbach's conjecture](https://en.wikipedia.org/wiki/Goldbach%27s_conjecture).
Goldbach's conjecture (for those too lazy to click the link) basically states that any even integer greater than 2 can be represented
as the sum of two prime numbers. It's still unproven, but has been shown to work up to *very* large numbers.
<br><br>
First, let's do the Python. We'll need functions that check if an integer is prime, create a list of prime numbers, and finds the values
that sum up to our target. Let's get crackin.
{% highlight python %}
from typing import List

def is_prime(val: int) -> bool:
  if val == 1: # special case, 1 isn't prime
    return False
  for num in range(2, val - 1):
    if val % num == 0:
      return False
  return True

def prime_list(lo: int, hi: int) -> List[int]:
  return [x for x in range(lo, hi + 1) if self.is_prime(x)]

def get_goldbach(val: int) -> None:
  if val >= 4 and val % 2 == 0:
    primes = prime_list(2, val)
    bot = 0
    top = len(primes) - 1
    while True:
      lo = primes[bot]
      hi = primes[top]
      res = lo + hi
      if res == val:
        to_print = repr(val) + ' = ' + repr(lo) + ' + ' + repr(hi)
        print(to_print)
        return
      elif res > val:
        hi -= 1
      else:
        lo += 1
  else:
    raise ValueError("val must be >= 4 and even")

  if __name__ == "__main__":
    while True:
      try:
        val = int(input("Enter a number (EOF or ^C to quit): "))
        get_goldbach(val)
      except ValueError as e:
        print(e)
        continue
      except (KeyboardInterrupt, EOFError):
        print()
        print("Exiting...")
        break
{% endhighlight %}
Phew, that was hefty. Upon closer look, it's not really that complex, but it is definitely messy.
All of the impure functions everywhere make this Python, though readable, more complex than necessary.
Let's look at the same exact thing in Haskell, now:
{% highlight haskell %}
prime :: Int -> Bool
prime val = (length [x | x <- [2..val], val `mod` x == 0]) == 1

primeList :: Int -> [Int]
primeList val = [x | x <- [2..val], prime x]

goldbach :: Int -> IO()
goldbach val
  | val < 4 || odd val = error "val must be >= 4 and even"
  | otherwise = helper val $ primeList val
    where
      helper :: Int -> [Int] -> IO()
      helper val lst
        | lo + hi == val = putStrLn $ show val ++ " = " ++ (show lo) ++ " + " ++ (show hi)
        | lo + hi > val = helper val $ init lst
        | lo + hi < val = helper val $ tail lst
          where
            lo = head lst
            hi = last lst
      helper _ _ = error "This is unreachable but the compiler won't shut up"
{% endhighlight %}
Now, isn't that cleaner? I'm making use of Haskell's version of list comprehensions (they sort of look like the Python ones),
as well as Haskell stuff like `where` blocks, pattern matching, the `$` operator, list concatenation (the `++`), but nothing
here is really that unreadable if you know what the symbols mean. All of that clean goodness is possible because of the
magic of functional programming.<br>
<sup>If you want, try writing that same program in C++ (or god forbid, in Java) and see how nice *that* looks. Ew.</sup>
<br><br>
Hopefully this has served to give a quick intro to the joys of functional programming. If this interests you and you
want to learn more (yay!) check out the lectures from CSE 130 for a [Haskell crash course](https://nadia-polikarpova.github.io/cse130-web/lectures/02-haskell.html),
[datatypes and recursion in Haskell](https://nadia-polikarpova.github.io/cse130-web/lectures/03-datatypes.html),
and [higher ordered functions](https://nadia-polikarpova.github.io/cse130-web/lectures/04-hof.html) to get a bit more introduction, or even
[dive into the book *Learn You a Haskell*](http://learnyouahaskell.com/chapters) for __free__ to learn a ton about the language.
<br><br>
Thanks for sticking with me through this post! Next time in this series, I'll talk about how I improved at discrete math and how to enjoy
it.

---
*All code snippets shown should be fully functional programs. The Python can be thrown into a source file and run from the command line;
the C++ and Java can be put into their own respective files, compiled, and run, and the Haskell can be put into files and loaded into
`ghci`.*

---
[Go back](/innermachinations)
