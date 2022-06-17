# Refactor, by Martin Fowler

A book on principles and techniques to improve the style of your code without changing its functionality. I once read somewhere a comment on this book: you either know it or you don't. If you're a decent coder it should be in your instinct how to refactor your code. And if you need to read a book for how to do it, coding is probably not the right business for you.

I'm still reading this book though, for two purposes. One is to make sure that I'm noting missing anything obvious. The other is to find better ways to articulate these ideas to my teammates, who's backgrounds are mainly in math and signal processing rather than solid CS or software engineering.

(This is a note I once made for myself. Don't give up simply because your teammates don't buy your argument immediately. Insist to your idea, repeat it, find the best way to deliver it. As long as both sides are well-intended, its a healthy dispute, not a pointless quarrel).

The book gives examples in JavaScript.

## A example

The first one tenth of the book gives an examplary refactoring on a small piece of code. Some insights from this section

* Make sure your code is test covered. *My comment: perhaps use what's avaible, don't bother to create extra test for refactoring only*. Indeed the boot later recommended so, as found in early chapter two 'The two hats'.
* Give the code a strucutre. Read the code, use refactoring to put your understanding into code, then test to see if you get it right. 'Camping rule': always leave the code in a better state than before you touch it.
* Ignore performance when you refactor. It's always easier to tune a well structured code. Focus on you immediate target. *My commnet: Again if you don't know how to differentiate refactoring from tuning, you probably don't know how to tune anyway.*
* Take small steps, compile, run, test. One runs faster in tiny steps, and may stop anytime, as often needed in daily work.
* Any fool can write code that a compute understands. Good programmer wirtes code that human understands; Set aside the dispute on what good style means, perhpas the true test of good code is how easy it is to change it. *My comment: think about not in the context of the instance of your team, not an abstract class.* **TODO make this pun sound better**

## Principles

### What is refactoring

* Refactoring should be scilent to user. Don't leave your code in a broken status (that might as well be restructuring)
* Know if you are developing new features, or refactoring. The two requires you to take different approaches

### Why refactoring

* Refactoring maintains software design, which decays otherwise. E.g. duplicated code
* Refactoring makes software easy to understand

### When to refactoring, and when not to

* Refactor upon three strikes. *My comment: definitely not a rigid rule, but you probably know better what to encapsulate when you repeat yourself twice rather than once,*
* Refactor when getting ready for major new feature
* Refactor for comprehensibility and obsolete code

* Refactor makes it easier to change the code. Do not refactor if you dont' have to change it (take it as a black box), or ready to rewrite everything

* Code review and pair programming? *My comment: can we afford that? Ignore the costy part and focus on the economic part: refactoring should make us run faster*

### On convincing people to refactor

* "If you are a tech lead in a team, it's important to show team members that you value improving the health of a code base.";
* "... the most dangerous way that people get trapped is when they try to justify refactoring in terms of 'clean code', 'good engineering practice', or similar moral reaons. The point of refactoring isn't to show how sparkly a code base is. We refactor becuase it makes us faster-faster to add features, faster to fix bugs." *My comment: this is probably the biggest lesson I take from this book. For those who 'has it in their instinct', it's hard to realize the difference between 'it will help all of us' and 'just do what I say', expecially as they speak to people without the instinct: lack of good counter arguments makes it harder to develop your own good arguments*

### On refactoring as a team

* Code ownership: 'some orginizations like any piece of code to have a single programmer as an owner, and only allow that programmer to change it'. My comment: As frequent, we may count on the original author to change the code, to avoid taking blames
* It's important that each member can refactor when they need to, without interfering withou other's work. 
* Perhaps code ownership works better when 'one have to review the changes' rather than 'one is responsible for all changes'. *My comment: again this works better when we have good structure already. I don't want to work on a mess and then be blamed for it.*
* Internal code is easy to tackle, but what if you have to change something public? Expand shrink may help, but the unfavored API may last forever. no simple answer to that

### Refactoring for specific fields/demands

* Some team has found a way to do safe refactoring on large code base with poor coverage: that is, to use a limited set of refactorings proven safe. It is language-specific, and requires carefully following of steps.
* Jay Bazuzi's description of safe 'method extraction' in C++. **TODO find reference and insert link**
* Working effectively with legacy code, by Feathres: get the system under test by finding seams in the program where you can insert tests.
* You Aren't Gonna Need It: respond to demands rather than prepare for everything. *My comment: the author intended to say how refactoring may be more efficient and flexible than extensive preparatory thinking. What I see from this, however, is not to always think about 'Ah if only somebody did this right in the first place'. It probably could have never happened, and it didn't. So respond to the demand.*
* Refactoring database? *My comment: no need now, may review for later demand*
* Automated refactoring? *My comment: no need now, may review for later demand*

### Miscellaneous

* "If I follow the refactorings carefully, I shouldn't break anything-but what if I make a mistake? (Or, knowing me, `s/if/when`.)". *My comment: a nice joke*
* The book mentioned the language of SmallTalk and some of its early developers as tracable origin of refactoring ideas. Interestingly, GoF design pattern also mentioned SmallTalk alot. It must be interesting to see how this lauguage flourished and decayed.
* Refactoring Workbook by Bill Wake: practices
* Refactoring to Patterns, by Josh Kerievsky, shows how to use refactoring to evolve towards most valuable patterns in GoF book. (双厨狂喜?)

## Code Smells

* This is the part where you can trust your instinct without getting too far off.
* **TODO blank notes for now. Take notes when something interesting is encountered.**

## Building Test

* When you report a bug, start by writing a test to expose that bug. *My comment: 1. steady recurrence of the bug. 2. test is also a great part of documentation. 3. Test driven my work on top of 2. *
