---
bibliography: ../bibliography.bib
bibFile: data/bib.json # path relative to project root
csl: ../ieee.csl
title: Kinematics Introduction
type: submodule
---

# Kinematics Introduction

## Prototyping in Paper

A second step is to ideate, mock-up, and prototype candidate mechanisms in paper.

While experts may have other tools, like CAD, along with intuition and experience, a novice can gain quick physical intuition by developing families of paper prototypes that help to eliminate infeasible designs, giving clues as to how to alter or optimize a design, and can often result in a very close-to-final kinematic structure. This is also the part of the process which requires the most intuition, creativity, and perseverance.

So what I do I mean by prototyping in paper? Do I mean go get a book on origami? No. Do I mean to use printer paper? Not necessarily. For me, paper is cheap, easy to work with using inexpensive tools, and can take you really really far down the path of making a novel and interesting mechanism. It can sometimes get you the whole way. But there can be pitfalls to prototyping in paper; there are a couple things you should know.

So how do you do it? First, break every rule you can think of. Get out paper, tape, cardboard, scissors, a stapler, glue, pins, ruler, etc. whatever you think will help you make things fast, break things that don't work, and try again without starting over. We'll figure out exactly what you made later.

As a note, I often suggest that to gain true intuition of how a mechanism will work, try to avoid one common error: don't move the output. Moving the output of a poorly defined device often is perfectly able to achieve the motion you are trying to attain. Paper links bend to your will, the complexity of the motion is handled gracefully by the stiffness balance of your creased hinges, and complexity is hidden. Now try to move the input and see if you can recreate that beautiful output motion. Harder, no? Humans are quite adept at simplifying quite difficult kinematic problems with their hands, eyes, and brains, but can't ignore them if they deal only with input motions.

What are the rules?

-   Make the joints weaker than the links. This is easy to understand.     If you are trying to make a jointed mechanism, you don't want your     mechansim to be the stiff parts
-   If you want a big robot you'll need thicker paper
-   Paper is forgiving. If you move to stiffer stuff, it may not work     the same.
-   Do you want joints to spring back, or not?
-   Put a tangerine in the center of your robot. Does it fall? Then you     may need to go stiffer
-   How do you go stiffer?

## Common Kinematics

Series kinematics devices whose joints connect end-to end to create motion at the tip of something. Think your arm extending from body through shoulder down your upper arm to your elbow, along your lower arm to your wrist and all the way to your fingertip.

Parallel mechanisms are devices which connect to each other in a loop. Think the piston of a locomotive, the

Planar

Four-bar linkages

Four-Bar linkages are a class of linkages long studied and used in mechanical systems to trace complex prescribed paths. These systems are one DOF, or degree-of-freedom systems, because the motion of one link determines the motion of all others(we always ground one linkage to not move.)

Many interesting four-bar linkages have been designed. The interesting thing is that the design of these systems is determined by only four values(and really three if you think about it). The lengths of your four linkages are all that determine the motion of your output

There are several good ways to derive and solve for the motion of a four-bar linkage analytically. Later in this book we will go through an exercise for solving for the motion of a similar linkage using Python and scripting to solve the problem for us, with some caveats. But for now, I refer you to a good book if you want to solve it further. Needless to say, the derivation uses lots of sines and tangents.

Why do I like four-bar linkages? Because they are simple and can still create quite complex motion in one degree of freedom. Also, you see them in nature. The jaws of fish can be approximated by four-bar linkages, and through different species of the same genus/family, the variation in species, nich, and mieal is tied to a variation in morphology.

