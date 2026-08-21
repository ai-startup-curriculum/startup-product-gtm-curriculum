# The Customer-Development Loop

## Motivation

At the IDEA stage almost every early startup is failing at the same thing: **they are building a product before they know what problem it solves, for whom, or in what shape it needs to arrive.** The most common founder story is not "we shipped and no one bought"; it is "we spent nine months shipping something no one had asked for, then discovered on launch day that the buyer we imagined does not exist as we imagined them."

Steve Blank named this failure mode and wrote the discipline that catches it. In *The Four Steps to the Epiphany* he argues that a startup is not a small version of a large company — it is **a temporary organisation searching for a repeatable, scalable business model** — and that the search runs on a distinct workflow parallel to product development, called **customer development** ([Blank 2005, PDF](https://web.stanford.edu/group/e145/cgi-bin/spring/upload/handouts/Four_Steps.pdf); [The Startup Owner's Manual companion](https://steveblank.com/2020/03/03/the-startup-owners-manual-1-a-step-by-step-guide-for-building-a-successful-company/)).

Customer development runs four steps: **Customer Discovery → Customer Validation → Customer Creation → Company Building.** This module lives entirely inside the first step. The rest of the track walks the other three.

The loop this chapter teaches is the pattern *inside* Customer Discovery — the ordered sequence of interview types that separates "*is the problem real?*" from "*is our solution shape right?*" from "*does the product actually deliver on it?*" Each interview stage is designed to catch a different failure mode. Doing them out of order — or skipping the first ones — is the fastest way to build a product no one asked for.

## Core concepts

### The three interview types, in order

The IDEA-stage discovery workflow runs three distinct interview types in a strict sequence. Each one has a different question, a different subject, and a different failure mode it catches.

| Stage | Question the interview asks | Subject of the conversation | Failure mode it catches |
|---|---|---|---|
| **Problem interview** | Does this problem exist for this person? Do they already work around it? How much? | The interviewee's life and past behaviour | **Assumed problem** — you built for a problem no one has, or one they tolerate cheaply |
| **Solution interview** | Given the problem, does *this shape* of solution register? Which shape do they gravitate to? | Concept sketches, competitors they use, mock flows | **Wrong solution shape** — the problem is real but this shape doesn't map to how they'd act |
| **Product interview** | Does the built (or MVP) product deliver on the promise? Where does it break? | The actual product, used in front of you or freshly by the user | **Wrong shipping order** — you built the wrong slice first, or the promise doesn't hold in software |

Blank's central claim is that these stages are **strictly ordered**. A solution interview cannot rescue an interview that should have been a problem interview — you will just get polite feedback on a mock. A product interview cannot rescue a solution interview — the user will demo the feature you ask them to, then never come back. Skipping stages compounds waste.

### Why the order matters

Each stage is designed to **kill a specific class of hypothesis cheaply.** The cheapness is the whole point.

- Killing an *assumed problem* takes 10 problem interviews across two weeks. Cost: your calendar.
- Killing a *wrong solution shape* takes 5–10 solution interviews with concept sketches. Cost: your calendar plus a Figma file.
- Killing a *wrong shipping order* takes a built MVP. Cost: **months of engineering time.**

If you skip problem interviews and go straight to product, you spend months of engineering time to discover a fact you could have learned in two weeks of phone calls. The interview stages exist to move the expensive falsifications earlier.

### The loop, not the funnel

Customer development is a **loop**, not a linear funnel. Every stage feeds back:

- Problem interviews reveal that your assumed customer segment does not have the problem — you re-select the segment and re-run problem interviews.
- Solution interviews reveal that the problem is real but your solution shape is wrong — you sketch a different shape and re-run solution interviews.
- Product interviews reveal that the shape is right but the product misses one critical job — you re-run problem interviews on the missing job.

Blank calls this **iteration inside the loop** and **pivots between loops**. An iteration is a small correction within the current hypothesis; a pivot is a change to the hypothesis itself (a different segment, a different problem, a different solution shape). This module trains iteration; mod-102 (PMF Signal and Measurement) trains the pivot / no-pivot decision.

## Concrete example — a walk-through

Imagine a founder who believes: *"solo consultants waste hours on invoicing; a smart invoicing tool will save them money."*

- **Problem interviews (weeks 1–3).** Talk to 15 solo consultants. Ask about their last invoice, in specifics. Do they actually spend hours? What do they do today? How often does it hurt? *Finding*: most spend 20 minutes a month, not hours. The problem is real for a small subset — high-volume consultants running 30+ invoices a month — but the mass segment is not in pain.
  - The problem interviews **killed the assumed customer segment**. Cost: 15 calls.
- **Re-select the segment.** Re-run problem interviews on high-volume consultants (agencies of 2–5 people, or freelance developers running many small gigs). *Finding*: this segment does spend hours, and they hate it because chasing late payment on 30 invoices is the actual pain, not the writing.
  - The problem interviews **found the sharper problem**. Cost: another 15 calls.
- **Solution interviews.** Sketch two shapes: (a) a smart invoicing tool that auto-generates invoices; (b) a chasing tool that automates late-payment follow-up on invoices you already send from your current tool. Show both to 8 people. *Finding*: they gravitate to (b) — the writing is not the bottleneck; the chasing is.
  - The solution interviews **killed the wrong solution shape**. Cost: 8 calls plus two Figma sketches.
- **Product interviews.** Ship a lightweight chasing tool. Sit with 5 users as they connect it to their existing invoicing. *Finding*: two of them cannot connect it because their invoicing tool has no API. The promise holds but only for a specific stack.
  - The product interviews **found the wrong shipping order**: integrations should have been first, not last.

Every failure mode above was caught in a **cheap** stage before an expensive stage began. That is what the loop is for.

## Common failure patterns

Three anti-patterns show up in the wild often enough to name:

- **The demo-driven pseudo-interview.** Founder walks a prospect through a slide deck, asks "would you use this?", records the polite yes. This is not a problem interview, a solution interview, or a product interview. It is a pitch dressed as research. Chapter 2 (Mom Test) is the whole antidote.
- **Skipping straight to product interviews.** Founder builds the MVP first, then "does discovery" by watching people use it. This can catch UX bugs but cannot catch the assumed-problem failure mode. If the problem was assumed wrong, you now have an MVP no one needs and no data to redirect it.
- **Running problem interviews forever.** The opposite failure. Founder spends six months in problem interviews without ever sketching a solution or shipping anything. Discovery becomes a way to avoid the risk of shipping. Blank's rule of thumb: **once you can predict what the next problem interview will say, move to solution interviews.**

## Where this fits in the module

This chapter names the loop and its stages. The rest of the module goes deep on each piece:

- Chapter 2 teaches the **question discipline** (Mom Test) that makes any interview stage produce information rather than compliments.
- Chapter 3 covers **recruiting the interviews** in the "do things that don't scale" tradition.
- Chapter 4 gives you the **outcome-level vocabulary** (Jobs-to-be-Done) that turns interview transcripts into a testable list.
- Chapter 5 (**solution and product interviews**) walks the specific mechanics of the later two stages.
- Chapter 6 covers the **corpus and synthesis** — how to store what you learn so a co-founder can act on it.
- Chapter 7 covers the **discovery report** — the ship-ready deliverable that ends this module.

## Summary

- A startup is a temporary organisation *searching* for a repeatable business model; customer development is the search workflow ([Blank 2005](https://web.stanford.edu/group/e145/cgi-bin/spring/upload/handouts/Four_Steps.pdf)).
- Inside discovery, run three interview types in order: **problem → solution → product**. Each catches a different failure mode (assumed problem, wrong shape, wrong shipping order).
- The order matters because each stage kills its failure mode more cheaply than the next stage would. Skipping ahead costs months.
- Iterate inside the loop when the hypothesis needs a correction; pivot between loops when the hypothesis itself is wrong.
- Two anti-patterns to watch: pitches dressed as interviews, and problem-interview infinity loops.
