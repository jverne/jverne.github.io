---
date: '2025-10-16 12:05 -0400'
title: Guidelines for the Successful Tactical Developer
---
# Guidelines for the Successful Tactical Developer

You are a technical person, possibly a coder, but you probably know a whole bunch about other technologies. To you, it's just stuff you figured out. But other people have noticed this. And now you are on a call with a customer[^1] who has run into a very weird and very _critical_ problem that, on the face of it, should be _impossible_. It is your job to make sense of this and get the bottom of the problem. Ideally, by yesterday[^2].

Congratulations and felicitations! You are now a Tactical Developer. Your cape[^3] is in the mail, along with pre-paid card for the local coffee shop. You'll need it.

Tactical development is a very special kind of technical work. It involves synthesizing information from a variety of uneven sources, building a model or idea of a situation in time in one's mind, and communicating the complicated story to peers and customers.

Your work is done only when a full root cause analysis has been shared in your issue tracking ticket, and maybe even some technical notes about possible fixes, ranked in order of effort required[^4].

Here are some of my rules for better living through tactical development. This is a work in progress.

## 1. Customers lie

- They might not even know they are lying. People want to help and may have a preconceived notion of what you want to hear. Or they heard what they are reporting from someone else. Do not trust them. They will lie and think they are helping.

- All information is provisional until it is backed up by other evidence.

- For critical information, always ask the same question multiple times in different ways, ideally at different times. Because you will get slightly different information each time, allowing you to build a more accurate representation of the truth.

- There is a reason people dislike talking with lawyers[^5]. They ask hard questions, distrust all answers, and usually have a pretty good idea what the answers are already. If you hear something outlandish or unlikely, be aware! Impossible things are impossible, but undefined behaviour[^6] is infinite in its expression. Your aim is to identify that undefined behaviour and trap it in a corner.

## 2. Customers are as confused as you are

- You are usually speaking with someone who only has second- or third-hand understanding of the problem. They don't know the details any more than you do, and are as confused as you are. Nothing makes sense. All is confusion, darkness, and lament. The angels weep.

- Always, *always*, **always**:
  - Keep notes and emails short. No one reads further than 10 lines. Most stop comprehending at 5. At this point, if you are still reading this document you are a statistical outlier. Go you!
  - If you must offer a full technical assessment, say perhaps for a weekly peer update, then offer a tight _precis_ at the top, followed by a clear "TL;DR" for the rest.
  - **Know your audience.** When discussing things with your peers, you can use internal jargon, and get into the weeds. For most others, including technical people not immediately fluent in the technical space you find yourself in, keep it generic. It is ok and correct to hand-wave technical details. Save the details for the incident ticket.
  - Don't be like this document! Stay away from obscure figures of speech and idiomatic phrases.

- When asking for something, be pedantically, annoyingly specific. You don't know if the same people are reading your reports, or gathering what you ask. Someone might have stepped in to cover for someone. English is the _lingua franca_ of technology companies, but not everyone comes to English with the same confidence.

  - If you need some logs or reports be excruciatingly clear _what_ logs and _which_ reports.

  - Call things by their names. If everyone just calls them "the logs" but you know that it is exposed as a gesture labelled
  "Device Debug Logs" use that term. Every time. This will save at least one round-trip misunderstanding over a long weekend, where now you have to explain to your manager that the critical issue is stalled because your contact is in a different time zone and didn't give you what you wanted on Friday.

  - At least early in the conversation, and occasionally over time, be sure to clarify this by showing examples for how to collect these things.

  - Help harried, disorganized people help you by giving them bullet point lists of tasks and preconditions even if you know that those preconditions are probably already in place. Don't just say "collect the logs". Rather, say something like:
  
    - Enable full "DEBUG" logging using the Frobnitz Logger control.
    - Set up the Xyzzy device with the Fnord configuration.
    - Make note of the wallclock time.
    - Reproduce the problem as reported only once.
    - Stop the DEBUG logger.
    - Collect the DEBUG logs (you can download them from the same interface) and send them in along with the wallclock time details noted earlier.

## 3. Work from first principles

- Always work from the known to the unknown. If something is unclear or unknown, then anything derived from it cannot be trusted.

- "Spit-balling" is fine, but you absolutely cannot build a successful solution on guesswork. Test those assertions. If you can't test them, then they are nothing more than fantasy and cannot be trusted. Save the hand-waving for your science-fiction novel. (Yes, I know you are writing a science fiction novel.)

- Help yourself and help others by stating your assumptions up front when asking for a clarification or information. When asking for a piece of information that you know hinges on a possibly shared assumption, state that assumption.

  - i.e., don't just assume they are using that API or setting that 99.999% of people use; say something like, 'Assuming you are using 'Frobnitz' setting, leaving it at the default of 'Xyzzy', can you please report the value of the 'Fnord' result?"

## 4. Keep it simple, silly

- Simplify, simplify, simplify. Complicated problems are complicated. They cannot be understood until each part is understood.

- Real problems have multiple contributing factors. We operate under the "Swiss cheese" model[^7], where the holes have to line up to cause that "weird" or "impossible" problem. It is your job to tell the story about how they lined up.

## 5. Practice the Beginner's Mind

- Even the saltiest, grumpiest bearded curmudgeon has not seen it all. Prepare to be surprised at the breadth and depth of astonishment that awaits the Tactical Developer.

- Know that years of experience is also a lie: the ways modern systems can fail are near infinite and you should prepare to be constantly surprised.

- Do not let your experience fool you! Always remember that undefined behaviour is infinite in its expression.

- Try to maintain a beginner's mind[^8] when trying to comprehend this infinite.

- There is a perverse humour is comprehending how foolish these systems of ours are; embrace this. Remember that the worst days make the best stories.

[^1]: For "customer" you can also substitute any of the following: vendor, partner, peer, etc.

[^2]: If everything is "mission critical" then nothing is mission critical. But customers will want you to know how important this all is. We can acknowledge this, but our job and how we do it doesn't change.

[^3]: No capes in the server room, please.

[^4]: _A Guide to Writing Good Bug Reports_ is still in the early editing stage.

[^5]: Though, Shakespeare wouldn't dare call out tactical folks. He relied on them for solving 11th hour folio publishing issues.

[^6]: Undefined behaviour is the set of all behaviours that overlaps with defined behaviour. "Working correctly" and "super-intelligent purple rhesus monkeys flew out of my server" are, under the right circumstances, possibly both defined and undefined behaviours.

[^7]: The [Swiss cheese](https://en.wikipedia.org/wiki/Swiss_cheese_model) model of accident causation is a model used in risk analysis and risk management.

[^8]: [Shosin](https://en.wikipedia.org/wiki/Shoshin), an attitude of openness, eagerness, and lack of preconceptions
