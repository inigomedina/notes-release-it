Release It!
Michael T. Nygard
Pragmatic Bookshelf
2007

# Preface

Does “feature complete” mean “production ready”?

Too often, project teams aim to pass QA’s tests, instead of aiming for life in Production (with a capital P). That is, the bulk of your work probably focuses on passing testing.

But testing—even agile, pragmatic, automated testing—is not enough to prove that software is ready for the real world. The stresses and the strains of the real world, with crazy real users, globe-spanning traffic, and virus-writing mobs from countries you’ve never even heard of, go well beyond what we could ever hope to test for.

1. First, you need to accept that fact that despite your best laid plans, bad things will still happen.

2. Second, realize that “Release 1.0” is not the end of the development project but the beginning of the system’s life on its own.

3. Similarly, your design decisions made during development will greatly affect your quality of life after Release 1.0. If you fail to design your system for a production environment, your life after release will be filled with “excitement.”

There is an order of priorities:

1. Stability
2. Capacity
3. Good design
4. Monitoring
   Too many production systems are like Schrodinger’s cat—locked inside a box,  with no way to observe its actual state. Without information, it is impossible to make deliberate improvements.


# Introduction

Software design as taught today is terribly incomplete. It talks only about what systems should do. It doesn’t address the converse—things systems should not do. They should not crash, hang, lose data, violate privacy, lose money, destroy your company, or kill your customers.

In this book, we will examine ways we can architect, design, and build software—particularly distributed systems—for the muck and tussle of the real world. We will prepare for the armies of illogical users who do crazy, unpredictable things.

Software design today resembles automobile design in the early 90s: **disconnected from the real world**. Cars designed solely in the cool comfort of the lab looked great in models and CAD systems. Perfectly curved cars gleamed in front of giant fans, purring in laminar flow. The designers inhabiting these serene spaces produced designs that were elegant, sophisticated, clever, fragile, unsatisfying, and ultimately short-lived. Most software architecture and design happens in equally clean, distant environs.

You want to own a car designed for the real world. You want a car designed by somebody who knows that oil changes are always 3,000 miles late; that the tires must work just as well on the last sixteenth of an inch of tread as on the first; and that you will certainly, at some point, stomp on the brakes while you’re holding an Egg McMuffin in one hand and a cell phone in the other.


## Aiming for the right target

Most software is designed for the development lab or the testers in the Quality Assurance (QA) department.

Product designers in manufacturing have long pursued **“design for manufacturability”** —the engineering approach of designing products such that they can be manufactured at low cost and high quality. Prior to this era, product designers and fabricators lived in different worlds. Designs thrown over the wall to production included screws that could not be reached, parts that were easily confused, and custom parts where off-the-shelf components would serve. Inevitably, low quality and high manufacturing cost followed.


## Use the force

Your early decisions make the biggest impact on the eventual shape of your system.

The earliest decisions you make can be the hardest ones to reverse later. These early decisions about the system boundary and decomposition into subsystems get crystallized into the team structure, funding allocation, program management structure, and even time-sheet codes. **Team assignments** are the first draft of the architecture. (See ​Conway’s Law​.) It’s a terrible irony that these very early decisions are also the least informed. This is when your team is most ignorant of the eventual structure of the software in the beginning, yet that is when some of the most irrevocable decisions must be made.


## The Scope of the Challenge

The increasing scope of this challenge—to build software fast that’s cheap to build, good for users, and cheap to operate—demands continually improving architecture and design techniques. Designs appropriate for small brochureware websites fail outrageously when applied to thousand-user, transactional, distributed systems, and we’ll look at some of those outrageous failures.


## A Million Dollars Here, a Million Dollars There

Design and architecture decisions are also financial decisions. These choices must be made with an eye toward their implementation cost as well as their downstream costs. The fusion of technical and financial viewpoints is one of the most important recurring themes in this book.


## Pragmatic Architecture

I’ll reveal myself here and now as a strong proponent of agile methods. Their emphasis on early delivery and incremental improvements means software gets into production quickly. Since production is the only place to learn how the software will respond to real-world stimuli, I advocate any approach that begins the learning process as soon as possible.


