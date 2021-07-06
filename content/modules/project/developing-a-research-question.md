---
title: Developing a Research Question
type: submodule
---

#  Developing a Research Question

## Introduction

Robotics as a field is highly multi-disciplinary. Even within that field, designing a robot requires knowledge and input from a variety of domains, including biology,  materials,  mechanics, mechanical design,dynamics, CAD, manufacturing, optimization, control, etc.  Because of its highly interdisciplinary nature, as new knowledge emerges from any of its connected fields, there is an opportunity to innovate.  Designing  novel and innovative  robots requires adapting new ideas from those neighboring fields, connecting them together, and remixing them with existing techniques, in order to realize new modes of locomotion or achieve higher performance.

This is where research comes in.  The goal of research is to help us understand the underlying mechanisms that connect these concepts together.   Unlike industry, that may be more focused on applying the output of knowledge to solve an applied problem, research often helps us make connections and understand relationships between concepts

## Research Questions

Research questions are at the heart of this process.  There can be big research questions or small research questions.  In fact, the biggest research questions, the answers to life, the universe, and everything ^[Douglas Adams] are composed of a thousand small questions.

In fact, this class -- and my research in general -- focuses on a small set of research questions.  Research questions are at the heart of every paper and proposal I write.  Asking a good research question is important because as engineers and scientists, it is important to understand underlying connections between two disparate domains before trying to connect them together for an application.  

The biggest questions -- the answers to life, the secrets of intelligence, and our understanding of matter -- These by nature are open ended,  multifaceted and, in my opinion, have don't have a single answer.  But these are terrible questions to start with when opening up a new line of questioning.  Why?  

* They are too big.  You can't expect to answer them completely by yourself as a result of a single project.
* They don't provide a good starting point.  Where should you start to answer these questions
* They don't provide a good starting point.  Where should you start to answer these questions?
* They don't leverage your knowledge and abilities.  Ask a question you are both  interested in, but more importantly, ask a question you can answer!

On the other hand, questions like these can be broken down into smaller problems.  Take what I might consider the driving  question of much of my research:

> How can higher-acheiving robots be made more easily and more affordably by more people?

This remaines a poor starting point for new projects because it still fails by the same points above, except that maybe my expertise can go a long way towards answering that question, in the longer term.  Given my interests, how can I break that question up into smaller parts?

A good research question has the following characteristics:

### Achievable / Tractable

The question should focus your work towards an achievable goal.  It should be limited in nature and may even hint at the approaches you might use  to answer it.  Consider that for this class, an appropriate research question must be able to be answered in one semester.  
<!--The question itself should be focused, rational, and achievable.-->  

If, after some background reading and initial testing you find it's too broad, you should adjust and refocus your question.  This can be done using a number of techniques:

* **Be more specific.**  Are you talking about a solution for all robots in general, or for a class of robots?
* **Restricting yourself to a specific class of solutions.**  Maybe there are a hundred ways to answer a question.  How can one particular mechanism be leveraged to solve it?  For example, perhaps you want to improve the jumping performance of a legged robot.  How can you use beam theory to address it?  How can you use engineered nonlinearity?  How can you optimize your DC motors?  Each of those questions implies one path of many possible paths that you might take in solving the problem.  Defining that path is appropriate as long as you acknowledge that you are focusing in this way.
* **Adding constraints.**  Defining a framework within which you are answering a broader question is a good way of focusing your question.  Such a framework can be a legitimate constraint (like gravity) or more hypothetical.  If you can provide a good rationale for why that framework is important, then your question is still valid.  For example,  while a number of researchers have built  walking robots, have they made one out of cardboard?  Have they made one for less than $100?  Have they made it in an hour?  Have they designed it for walking on an asteroid?  Constraints can be useful for focusing your process of answering the question
* **etc.**  What other techniques can you think of that helps you focus your question on something more achievable?

<!-- TODO:  Exercise: What other techniques can you think of to refocus a question to make it more achievable?-->

<!--
### Helps constrain your investigation. The question should have within it the means by which you should focus.
-->

### Novel

Through background reading of prior research, existing patents, and popular literature you should be relatively sure that the question hasn't already been answered.  Granted, if it's a good idea, other people may already be working on the problem, but if the main structure of the answer is already mapped out, then, unless you are reasonably sure you have something new to add, you will probably find that most of the most interesting questions within that subfield have already been asked and answered as well.
<!--but it shouldn't be a deep, old field with most of the structure within that question already answered by domain experts.  -->

Though it is hard to prove a negative, a five minute search on google scholar by a domain expert like your professor shouldn't come up with many highly cited results.  The toughest part is identifying the keywords that people within the field (if it already exists in a nascent form) already use.

Here are some ways to make a research question more novel 

* **Importing a new concept, material** What are the current trends in other fields?  Have they been applied to robotics yet?  Try swapping out a traditional approach for a new one. For example, instead of developing a traditional model for some phenomenon, based on experimental data and numerical analsis, can machine learning techniques be applied to solve a problem more efficiently?  Can you swap out a motor for a liquid crystal actuator?  Can you make your device entirely 3D printable?
    * Use new materials.  Instead of rubber, use hydrogels or LCA's.  Instead of metal links, try cardboard
    * Apply something used for sensing towards actuation, or actuation towards sensing.  
    * Use off-the-shelf components that are newly available.  Consider the myriad of new, small form factor sensors that have been developed for cell phones.  How can you integrate them to solve a problem?
* **Try a new approach to an existing solution.**  Some people solve a problem in a cosmetic manner and move on, never fully understanding exploiting the underlying phenomenon.  Searching through old robotics conferences reveals many cool ideas that were poorly implemented or not well understood.  How can you do it better?
    * Add a better model that more completely explains the phenomenon you're seeing and use that to build a better version.
    * Come up with an improved design of an existing robot.  Push the envelope through better engineering.
* **Looking at the problem more broadly.**  If you're too focused on one mechanism or technique, you may find -- after deeper searching -- that someone has explored that particular problem in depth.  Have they explored that class of problems more generally?  For example, many people have solved interesting problems using soft robots actuated with pneumatic bellows; what happens when you switch to soft materials that themselves can be actuated?  What new challenges can these materials address that were perhaps solved less gracefully with other soft robots? 
* **Other techniques...** How else do you make a concept more novel?

<!--TODO have students think of other ways to increase novelty-->

### Interesting, Timely, and Relevant

Your question should be interesting to the broader community.  How do you achieve this sweet spot of something that is interesting while at the same time being novel?  This is the challenge to research in general -- finding topics that are unexplored while at the same time of interest to the community.  If it is truly of interest, probably someone else is already thinking of your idea.  If someone else has solved it already, less can be learned from you re-examining the same question.  The only way to work through this is to proceed quickly and efficiently through your research, and to publish your results early and often. 

### Open-Ended

Most research questions should contain "how" or "why" phrases, and probe more fundamental relationships.  Why?  Yes/No questions are boring, and most of the time are not fundable.  Open ended questions are the bedrock of science, while application-focused projects are typically more goal-oriented.  Goal oriented questions are great in a number of scenarios, especially in military and industry-oriented projects, but to get funded by the National Science Foundation, your project needs "Intellectual Merit", which relates back to answering fundamental scientific questions of interest to the community.  So let's practice

#### Exercise: Turn this goal-oriented question to a more open-ended question

Use some of the techniques described above to refocus the given research questions to something more open-ended

| Goal-Oriented                                                                                       | Open-Ended                                                                                    |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| Can I make a jumping robot with liquid crystal actuators?                                           | What are the optimal material design parameters to increase the performance of jumping robots |
| How do I make the world's fastest robot?^[ Still goal oriented.  I said how, but I don't care why.] |                                                                                               |


### Modular

While the research question you ask should be rational, achievable, and focused in order to fit within the constraints of a single project or semester, your question should also be able to be assembled into a broader picture.  This helps you as a researcher create a unique narrative around which you can define your academic career.  This is useful for a number of reasons.  First, building up blocks of questions defines you as a domain expert.  People start to associate you with a sub-field, or field, and -- if it is interesting to the community -- you will probably become more sought out to speak, collaborate on proposals or papers, etc..  Second, it gives you a mastery of a research pipeline that allows you to ask newer, related questions better and faster.  Like the gravity in a black hole, the better you are at something, the better you become, and it accelerates.  Finally, having multiple pieces that you can fit together in a variety of ways allows you to reframe your expertise as the field evolves.  While some topics become "solved", if you can swap out one piece of your research for another, you can continue to remain relevant, even if some of your topics remain stale.  Who knows, maybe it will become popular again, if something new comes along and makes it relevant again?


In summary the process of asking new questions can help you build up a research portfolio that you can remix and reframe as needed.

### Leverages your own abilities.

This may be obvious, but you should ask research questions that are both interesting, and that you are best able to answer.  If you are a mechanical engineer asking a research question about game theory, you may fall into some of the above pitfalls of novelty, interest, and focus

### Demonstrates your expertise

Finally, a good research question also demonstrates you know enough about your field to make a novel, interesting, and relevant new contribution to the field.

## Relevant

And finally, the question you ask must be answerable with the topics you learn in _Foldable Robotics_.

* Do I use other types of transmissions to solve a tough problem?  How much of my design time am I spending on this
    * Gears, pulleys, belts, wheels, shafts, etc
* Do I use alternate manufacturing methods to achieve success?
    * 3D printing, traditional machining
* Is the contribution of the foldable mechanism nontrivial?
    * Does it transform input motion to output motion in a meaningful way?
    * Does the use of foldable techniques solve a key design problem?
    * Is the foldable portion a mechanism or just a structure? 



<!--
A good research question will also help constrain the problem by defining the framework for asking the question.  This is done by implying a thesis statement.  

Not so good:

"Why does the earth rotate?"

Better:

What role does gravity play in 

A good research question needs to contain a number of elements.
-->


<!--
### Novelty
 
Asking a good research question implies some sort of novelty -- maybe the question itself is new or you've selected a different mechanism by which to understand and contextualize it.  
-->

<!--
### It connects disparate things
### Pairing a Mechanism with a Phenomenon
-->

<!--

"How does curvature play a role in creating hysterisis in soft mechanisms?"

Implied here is that a mechanism has something to do with a phenomenon.

### "How"

### "Why"

### Examples

* What factors play a role in ...


* What role can curvature play in the generation of 
* 
-->









<!--













* Original Question
  * How do I actuate soft robots?
* Better
  * What X are best used with Y to generate Z in soft robots?
* Variations
  * What <dimensions> are best used with <pneumatics> to generate <high forces> in soft robots?
  * What <recipes> are best used with <hydrogels> to generate <fast response> in soft robots?
  * What <radii> are best used with <curved-crease mechanisms> to generate <forward swimming> in soft robots?
 
asdf

* How can curvature propogation be leveraged to actuate soft systems
* What shapes

* How can higher-acheiving robots be made more easily and more affordably by more people?
    * How can curvature -- and curvature play a role?
    * How can optimization and machine learning techniques identify new designs
    * How can stiffness and compliance be better integrated into the design process to 
    * How can higher fidelity models of nonlinear effects be used in the design process?
    * How can we automatically compute how to make new robots that are manufacturable
It is your job to identify a new one.
-->

<!--
## Exercise

Think of one of those fundamental questions.

### Example

* Why does life exist
    * It self propogates
      * How?
        * Instinct
        * Biology
    * Because it self-formed
        * How?
          * Evolutionary processes
          * The emergence of chemical       
-->



