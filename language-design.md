_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question**

Pick three quotes from the readings about language design. Good candidates
are:

- Something you agreed with / resonates with your own experience
- Something you disagree with
- Something that is interesting, a new idea or perspective you'd like to remember
- Something you didn't understand

For each quote, describe what it was about the quote that led you pick it.

**Response**

"If you give a person a fish, he can eat for a day.
If you teach a person to fish, he can eat his whole life long.
If you give a person tools, he can make a fishing pole—and lots of other tools! He can
build a machine to crank out fishing poles. In this way he can help other persons to catch
fish" [Steele, 1998].

I think that this is a pretty good way to think about programming in general, but it definitely 
could use some nuance. For example, the tools we give programmers have to be chosen carefully: if 
we give them two hammers (maybe structs and classes), but forget to give them a screwdriver (say, 
overloaded operators), the types of things they can create will be limited. Likewise, if we give 
them too many tools, they'll spend all their time searching through the bucket of puzzlingly-shaped 
drill bits for a normal Phillips head. Just because a certain tool (like a hashmap) can be built 
with other tools (like classes), doesn't necessarily mean we shouldn't give them both tools, 
especially if it reduces "boilerplate..., which is annoying and error-prone" [Bloch, 2006]. The set 
of tools must be carefully curated to avoid warts, both of the missing and tacked-on varieties.

"That’s not Greek, it’s Klingon. The Perl version uses fewer characters, which many geeks would no 
doubt see as more efficient or precise; but Stefik says that the Quorum version accomplishes 
exactly the same commands" [Pavlus, 2012].

The author here is for some reason conflating "fewer characters" with "more efficient or precise." 
What the author lauds as "more readable code" is often just code that has its syntactic sugar 
removed. The Quorum for-loop is really just a while loop with an unrelated variable being updated 
inside it; this might be easier to grok for a brand-new programmer, but it slows down the 
comprehension for anyone above that level. The point of syntactic sugar, like for...in loops in 
JavaScript, is to simplify the wording of something every programmer already knows how to do, to 
allow it to be written and read much faster. As someone who originally started programming with 
MIT's Scratch then moved to other languages with C-like syntax, it feels weirdly infantilizing to 
demand that all languages be absolutely readable to any person. This seems like demanding that the 
entire legal code be rewritten using only the thousand most common English words, simpleWikipedia 
style. I'm all for making CS an easier field to enter, and making syntax less arcane; however, I 
feel like tools like Scratch and Jupyter notebooks already fill that niche; there's no need to 
completely replace code with lines of prose.

"We should remember that 'knowing' a language is a poor proxy for being able to think rigorously. 
It is one thing to have learned the syntax of a language and another to have grasped the underlying 
paradigms" [Yang and Rabkin, 2015].

The way the CS job market is structured really incentivizes this sort of language collection. 
People in tech, especially recent graduates, try to pad out their resume with as many languages as 
possible: it doesn't matter if you've only used C# once, it's going on your resume to make the 
"Technologies" section bigger and to give you an edge over the other applicants. I'm hoping this 
is, in some ways, partially starting to shift. I've seen quite a few jobs demanding "strong 
reasoning skills" and "experience in object-oriented programming", rather than a laundry list of 
C-based languages. One of the things I think Harvey Mudd's CS department does best is emphasizing 
rigorous thinking about problems in abstract ways, instead of just in terms of how languages can 
solve them. CS5, CS81, and CS140 especially have improved the way I think about problems in 
general, even those outside of the CS field.


---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

A well-designed language is one that, first and foremost, fits its purpose. A language that is 
worse at its intended purpose than other languages is not a good language. For example, if I design 
a statistical modeling language that only lets me draw pictures of cows, my language is not a 
well-designed statistical modeling language (although it might be a good bovine sketching 
language). However, just because a language fits its current purpose, it may not necessarily always 
fit that purpose. This is what Steele is so concerned about: languages must be able to grow and 
evolve, in part driven by their users, in order to stay relevant [Steele, 1998]. Sometimes, though, 
too much growth can be a bad thing: languages can become bloated masses, used for things far 
outside of their original purpose. Growth must be controlled, and focused around making the 
language better at its specific niche. Conversely, a language should not be too small; if users 
find themselves using the same boilerplate code or external library in every single program, 
perhaps its time to grow the language a bit. Still, "you can always add things later, but
you can’t take them away" [Bloch, 2006]; make sure everything added will work. Finally, a 
well-designed language is human-centered: it must be intelligible to its users and have consistent 
notation [Bloch, 2006].

A poorly-designed language lacks one or more of these features: it fails to evolve, is too small or 
too large for its purpose, or is nonsensical to everyone but its hardcore devotees. Symptoms of a 
poorly-designed language are re-using your own code constantly (the language is too small), having 
to check the documentation constantly (the language is too large or utterly unintelligible), and 
having keywords or operators that have behavior contrary to what most programmers would expect, 
like the Swift let keyowrd representing constants while the JavaScript let keyword representing 
variables, or having gray(100) represent the color white [Verou, 2014].

---

**Question**

How might the themes of _Growing a Language_ relate to notions from Fowler?

**Response**

As I've argued above, languages must grow within their current role. This is 
especially relevant to DSLs, as at some point, a "grown DSL" just becomes a general-purpose 
language. If I have an internal DSL, C-flat, that is a subset of the functions of the C language, 
and I continue to grow it piecemeal, eventually I'll just have C, which isn't really a 
domain-specific language anymore. This isn't to say that domain-specific languages shouldn't grow, 
just that more caution needs to be exercised.

---

**Question**

In what way is an API a language?

**Response**

The easy answer is that it is a mode of communication between two or more things, that provides an 
abstract way of communicating more complex concepts. Like other languages and programming 
languages, it has a fixed, unambivalent syntax, is used by computers to interface with other 
computers, and is documented so that users can learn how to utilize it in their own programs 
[Bloch, 2006].

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

"Every API is a little language, and people must learn to read and write it" [Bloch, 2006]. Thus, 
we must be sure that APIs (along with other languages), are as easy to understand as possible, 
especially as "it should rarely require documentation to read code written to a good API" [Bloch, 
2006]. If someone were to use something like gray(100) without checking the documentation, they 
might not realize that it actually gives them white [Verou, 2014]; when it comes to an API, this 
could be a dangerous, rather than an aesthetic, error.

---

**Question**

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other
words, people found it easier to work with code that looks more like a human language (e.g.,
English). Consider the following quote by William R. Cook, one of the creators
of AppleScript:

> The experiment in designing a language that resembled natural languages (English
> and Japanese) was not successful. It was assumed that scripts should be
> presented in “natural language” so that average people could read and write
> them. … In the end the syntactic variations and flexibility did more to confuse
> programmers than to help them out. It is not clear whether it is easier for
> novice users to work with a scripting language that resembles natural language,
> with all its special cases and idiosyncrasies. The main problem is that
> AppleScript only appears to be a natural language: in fact, it is an artificial
> language, like any other programming language. … even small changes to the
> script may introduce subtle syntactic errors that baffle users. It is easy to
> read AppleScript, but quite hard to write it.
> [[Cook 2007, page 1-20]](https://dl.acm.org/citation.cfm?doid=1238844.1238845)

Are these two experiences of natural languages at odds with one another? Would
you choose to include natural language in the design of a DSL? If so, how might
you do so? If not, why not?

**Response**

I think they are fundamentally incompatible in some ways; obviously there cannot be a programming 
language that resembles natural language but does not have natural language syntax. However, the 
reverse is not necessarily false: you certainly can create a language that has "natural-language 
replacements for some of the more abstruse syntax" [Pavlus, 2012] that doesn't "resemble natural 
languages" [Cook, 2007] A lot of the syntactic sugar added to languages in recent years (for-loop 
variations in JavaScript, f-strings in Python, etc.) utilizes natural language syntax to create a 
memorable way to write something that is already possible (but ugly to write) in the language. This 
definitely doesn't make a program read like a natural language, but it sure lowers the barriers to 
entry.

I would choose to include some natural language in the design of a DSL, but probably about the same 
amount as is present in general-purpose languages like Java and Python. However, it depends on the 
domain- Gherkin, which I explored on the last homework, was almost entirely natural language, which 
was important as the language was intended to be read by less technically-minded people. In 
general, however, I'm wary of natural language: the more natural language-like things are, the 
better people *think* they understand them; whether they actually do is often the opposite. Natural 
language carries a lot of ambivalence and connotations with it, which may not be universal; by 
separating a program from natural language, a lot of confusion can be avoided.

---
