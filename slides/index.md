- title : Design and Agile Architecture
- description : Connecting the Dots across the innovation spectrum
- author : Jon Roberts
- theme : sky
- transition : slide

***

## Design and Agile Architecture

**Alamo Agilistas**

August 16th, 2016

Jon Roberts

***

## Design and Agile Architecture
### Topics

- Can We Scale Agile?
- What Model Makes Sense?
- When, Why and How to Redesign?

***

### Levers of Transformation

![Culture Language and Systems](images/transformation_levers_3a.png)

---

### Levers of Transformation

![Culture Language and Systems](images/transformation_levers_3b.png)

---

### Levers of Transformation

![Culture Language, Systems, and ?????](images/transformation_levers_4a.png)

---

### Levers of Transformation

![Culture Language, Systems, and Design](images/transformation_levers_4b.png)

***

## Can We Scale Agile?

---

##  Useful concepts for scaling
### coordination and communication:

  <p class="fragment roll-n">mature processes and tools</p>
  <p class="fragment roll-n">comprehensive documentation</p>
  <p class="fragment roll-n">good contract negotiation</p>
  <p class="fragment roll-n">following a coordinated plan</p>

---

# Agile Values

| Individuals and Interactions      	| *Over* | Process and Tools            |
|-----------------------------------	|------- |-----------------------------	|
| Working Software                  	| *Over* | Comprehensive Documentation	|
| Customer Collaboration            	| *Over* | Contract Negotiation        	|
| Responding To Change              	| *Over* | Following a Plan            	|

***
- data-background : images/wat.gif

# WAT?

---
- data-background : images/bimodal.jpeg

## Is Gartner's BiModal IT Strategy Achievable?

<br/><br/><br/><br/><br/><br/><br/><br/>

## Is it Advisable?

---

### Tri-modal may be a better model

***

## Introducing
# Wardley Maps
### A strategic way to visualize tech stacks

---

### Who is Simon Wardley?

- Tech Executive at Early PAAS Pioneer
- Executive at Canonical while growing OpenStack Cloud Business in late 2000s
- Keynote Speaker at OSCon
- Wardley Map Introduction: http://blog.gardeviance.org/2015/02/an-introduction-to-wardley-value-chain.html

---

![sample wardley map](images/wardleymap1.png)

---

![sample wardley map](images/wardleymap2.png)

---

![sample wardley map](images/wardleymap3.png)

***

## When to Re-architect?
### At the "Seams"

***

## Sacrificial Architecture
[Sacrificial Architecture](images/sacrifice.png)

***




- Agile Transformation is Slow and Painful
  - Why?
    - Because it's difficult
      - Let's look at TPS
      - Pain vs Chronic Pain
    - Agile and Scrum are not designed to scale
      - examine principles of Agile
      - We need a third Mode
      - Agile is not Lean
      - The Three Attitudes
    - Conway's Revenge
      -
      - Legacy Designs are an Impediment
      - Is the RDBMS an Impediment?
      -

***

- Introduction
  - Something is Rotten in the State of Denmark
    - Software Craftsmanship Movement
      - Successor to XP
      - A singular focus on Scrum or other process methods neglects design
      - Quotes from Agile Manifesto Signatories
    - Agile is Dead?
      - Agile Manifesto was/is reactionary
    - WTF DevOps?
  - Venn Diagram
  - The Fourth Concern of Agile Transformation




- Types of Scaling
  - Scale up by features and functionality - more code and more developers
  - Scale up by Instances
    - same code running in more places
    - orthogonal data
  - Scale up by larger Instances
    - linked data, large graphs
- Towards <del>a Better Model</del> More and Better Models
  - Introduction
  - It's Not Really "Transformation" Anyways
    - Transformation vs. Transmutation

- *How Can We Do This?*


- Games
- Context of Growth
- Design relative to maturity
- Communication Structures and Design
- Networks and Hierarchies
- *HOW TO DO THIS?*

***

### What is FsReveal?

- Generates [reveal.js](http://lab.hakim.se/reveal-js/#/) presentation from [markdown](http://daringfireball.net/projects/markdown/)
- Utilizes [FSharp.Formatting](https://github.com/tpetricek/FSharp.Formatting) for markdown parsing
- Get it from [http://fsprojects.github.io/FsReveal/](http://fsprojects.github.io/FsReveal/)

![FsReveal](images/logo.png)

***

### Reveal.js

- A framework for easily creating beautiful presentations using HTML.


> **Atwood's Law**: any application that can be written in JavaScript, will eventually be written in JavaScript.

***

### FSharp.Formatting

- F# tools for generating documentation (Markdown processor and F# code formatter).
- It parses markdown and F# script file and generates HTML or PDF.
- Code syntax highlighting support.
- It also evaluates your F# code and produce tooltips.

***

### Syntax Highlighting

#### F# (with tooltips)

    let a = 5
    let factorial x = [1..x] |> List.reduce (*)
    let c = factorial a

---

#### C#

    [lang=cs]
    using System;

    class Program
    {
        static void Main()
        {
            Console.WriteLine("Hello, world!");
        }
    }

---

#### JavaScript

    [lang=js]
    function copyWithEvaluation(iElem, elem) {
        return function (obj) {
            var newObj = {};
            for (var p in obj) {
                var v = obj[p];
                if (typeof v === "function") {
                    v = v(iElem, elem);
                }
                newObj[p] = v;
            }
            if (!newObj.exactTiming) {
                newObj.delay += exports._libraryDelay;
            }
            return newObj;
        };
    }


---

#### Haskell

    [lang=haskell]
    recur_count k = 1 : 1 :
        zipWith recurAdd (recur_count k) (tail (recur_count k))
            where recurAdd x y = k * x + y

    main = do
      argv <- getArgs
      inputFile <- openFile (head argv) ReadMode
      line <- hGetLine inputFile
      let [n,k] = map read (words line)
      printf "%d\n" ((recur_count k) !! (n-1))

*code from [NashFP/rosalind](https://github.com/NashFP/rosalind/blob/master/mark_wutka%2Bhaskell/FIB/fib_ziplist.hs)*

---

### SQL

    [lang=sql]
    select *
    from
    (select 1 as Id union all select 2 union all select 3) as X
    where Id in (@Ids1, @Ids2, @Ids3)

*sql from [Dapper](https://code.google.com/p/dapper-dot-net/)*

---

### Paket

    [lang=paket]
    source https://nuget.org/api/v2

    nuget Castle.Windsor-log4net >= 3.2
    nuget NUnit

    github forki/FsUnit FsUnit.fs

---

### C/AL

    [lang=cal]
    PROCEDURE FizzBuzz(n : Integer) r_Text : Text[1024];
    VAR
      l_Text : Text[1024];
    BEGIN
      r_Text := '';
      l_Text := FORMAT(n);

      IF (n MOD 3 = 0) OR (STRPOS(l_Text,'3') > 0) THEN
        r_Text := 'Fizz';
      IF (n MOD 5 = 0) OR (STRPOS(l_Text,'5') > 0) THEN
        r_Text := r_Text + 'Buzz';
      IF r_Text = '' THEN
        r_Text := l_Text;
    END;

***

**Bayes' Rule in LaTeX**

$ \Pr(A|B)=\frac{\Pr(B|A)\Pr(A)}{\Pr(B|A)\Pr(A)+\Pr(B|\neg A)\Pr(\neg A)} $

***

### The Reality of a Developer's Life

**When I show my boss that I've fixed a bug:**

![When I show my boss that I've fixed a bug](http://www.topito.com/wp-content/uploads/2013/01/code-07.gif)

**When your regular expression returns what you expect:**

![When your regular expression returns what you expect](http://www.topito.com/wp-content/uploads/2013/01/code-03.gif)

*from [The Reality of a Developer's Life - in GIFs, Of Course](http://server.dzone.com/articles/reality-developers-life-gifs)*
