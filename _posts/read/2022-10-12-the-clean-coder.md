---
layout: post
title: "The Clean Coder Robert C. Martin"
category: read
---
My notes of the book The Clean Coder by Robert C. Martin.

I urge every developer to read this book.
The book contains practical advices on what it means to be a profesionnal developer.

<!--more-->

# 1. Professionalism

- __"the Boy Scout rule"__ : check in code cleaner than when you checked it out
  
- __Must be conversant with minimal knowledge__:
	- Design Patterns
	- Design principles
	- Methods (scrum, lean, structured design, structured analysis, ..)
	- Disciplines (TDD, OOD, continuous integration, ..)
	- Artifacts (UML, charts, diagrams, ...)
	  
- Musicians __master__ their __craft not by performing but by practicing__
  The daily job is not practice

- The best way to learn is to teach

- Do your __due diligence__ on the __business domain__

> 🔑 Key concept:  
> Treat Software the way a sculptor treats clay, continuously shape and mold it.

# 2. Saying No

- __Say no clearly__ when you can't say yes

- __Why__ is a lot __less important__ than __the fact__. No Need to provide too much details

- __"Trying" is a commitment__ and admitting that you are holding back
  Trying = extra effort = commit

- __Don't try to be a hero__

- __Never accept dropping disciplines__

- __Dropping disciplines creates problems__, it __NEVER solves them__ 

> 🔑 Key Concept :  
> Be clear and honest.  
> Dont' try to be a hero.  
> Never abandon your disciplines.

# 3. Saying Yes

> Commitment Equals:
> 1. __Say__
> 2. __Mean__
> 3. __Do__

- Know how to recognize __real commitment__
	- __"Need/Should"__, __"Hope/Wish"__, __"Let's.."__ Is __NOT commitment__
	- Is only __about YOU__=, not other	  
	- If the goal depends on someone else, __commit only to specific actions you have full control on__ that bring you closer to the end goal (or commit to finding those specific actions)
	  
- If you can't commit __raise a clear RED flag as soon as possible__

- __NEVER drop disciplines__

- Be __honest__ about your __own stamina and reserve__

- Explain __personal cost__ and __demande your free time if you overtime__

> Key Concept:  
> Professionals are not required to say yes to everything that is asked of them.  
> However, they should work hard to find creative ways to make "yes" possible.  
> When professionals say yes, they use the language of commitment so there is no doubt about what they've promised.

# 4. Coding

- Coding is a __marathon__, not a sprint
- Coding is a __creative activity__. Take care of your personal __creative input__
	__Creative Input = Creative Output__ (Read SF ?)

#### Typing blind
- __Typing blind__ is __about confidence__
	  __Exercise__ it and learn to __sense errors__ in your typing to __build confidence__

#### Focus
- Coding needs __concentration and focus__. It is a __challenging__ and __exhausting__ activity
- __Don't code__ if __TIRED__ or __DISTRACTED__, __settle your mind first__
- __Pair__ and __recall context__ to stay in focus

- You have to juggle competing __many factors__
	You code must:
	1. __Work__
	2. __Solve__ the customer __problem__
	3. __Fit__ into the __existing system__
	4. Be __readable__ by __other programmers__

#### The Zone
- __DON'T let yourself into the ZONE__
	Makes you loose big picture = bad decision = have to go back = loss of time
- __The ZONE__ is for practicing

#### Debug
- __DEBUG TIME = CODING TIME__

- __Reducing debug time__ is a responsibility.
	Adopt the right __disciplines__ (TDD)

#### Hope
- __Do NOT hope__ and let others hope
	Follow your __estimates__ (see chapter X)

- __DO NOT be tempted to rush__ and tell your boss you already considered it

#### Overtime
- Don't agree to __overtime__ unless:
	1. __you can personally afford it__
	2. __it is short term (< 2 weeks or less)__
	3. __your boss has a plan if the rush fails__

#### "Done"
- __Rationalize "Done"__, __never think "Done enough"__
	Ask business and testers for __acceptance tests__

### Work with others
- __Ask for help__ and give it
	Gives __new perspective__, __resets forces and focus__, awesome __learning__
- __Seek mentoring__ from seniors, don't wait for it

# 5. Test Driven Development (TDD)


> __THREE LAWS OF TDD__:  
> 1. ***Write a failing unit test before any production code***
> 2. ***Write only part of a unit test if it is sufficient to fail***. Not compiling is failing.
> 3. ***Only write sufficient production code to pass the current failing test***
>   
> These 3 rules will lock you in  ***30 sec long cycles***.

- __Unit tests are documents__ (detailed docs)
	Lowest-level description of the system's design

- Unit tests __force good design__ (force functions decoupling)

- __After-the-fact tests are bad__ because you already know how to solve the problem

# 6. Practicing

- __Performance = Practice__
- Practice must be done __on your own time__
- You will get paid for for you practice at your work

- __Seek diversity in practice__
	User others languages than the ones you regularly use

- Consider __Open-Source__ projects
	They are the "pro-bono" work lawyers do to challenge themselves and show their skills 

#### Exercises:
- __KATA__: precise choreographed mouvement that simulates __one side of a combat__
	__Movement and decisions practice__ : programming KATAs __simulates solving problems__, the __solution is known__

- __WASA__: two-man kata. Aggressor vs defender.
> WASA: Programming ping-pong
> 1. Defender writes a unit test
> 2. Aggressor writes code to pass the test and writes a new unit test
> 3. Aggressor and defender exchange roles
> 
> The defender can write a unit test for a new problem whenever he chooses and has full control of how the test should be passed (by writing a unit test with any condition to pass inside it)

- __RANDORI__: free-form combat
	Like two-man kata but they are more than 2 participants and people take turn to write unit tests and code to pass

> Practice Ressources:  
> http:s//katas/sopftwarecraftmanship.org/  
> https://codekata.pragprog.com/  
> "The bowling game"  
> "Prime factors"  
> "Word Wrap"  

# 7. Acceptance Testing

- __Stakeholders__ and __programmers__ __collaboration__ in order to __define a shared definition of done__

- __ALWAYS AUTOMATED__

- __"late precision"__ principle
	Should be written as late as possible
	In agile, written __after features enter sprint__

- __Business__ will write __"happy paths"__
	Focus where features have business value

- __QA__ will write __"unhappy paths"__
	Boundary conditions, exceptions, corner cases

# 8. Testing Strategies

>[!quote] QA
>1. QA should find nothing
>2. QA is part of the team, work together
>3. QA identifies the **actual** behavior of the system

# Automation Pyramid
![Automation Pyramid](/assets/img/reading/the-clean-coder/automation-pyramid.png)

> Unit Tests:  
> 100% coverage true coverage (=asserts behavior)
>
> 🚀 Run speed: Fast (TDD: constantly ran)  
> 💰 Dev and testing cost: Low  
>
> - Way to __specify__ what you will write
> - Part of __Continuous Integration__

> Component Tests:  
> ~50% coverage
>
> 🚀 Run speed: Fast  
> 💰 Dev and testing cost: Low  
>
> - Individual components of the system
> - __Wraps component__
> - __Pass input__ and __gather output__
> - __Acceptance tests__ of business rules
> - Other parts of the __application are mocked__
> - Inside a __component testing environnement__

> Integration Tests:  
> ~20% coverage  
>
> 🚀 Run speed: Slow (periodical runs)   
> 💰 Dev and testing cost: Moderate  
>
> - Assemble __groups of components__
> - Test how well they __communicate__
> - __"Choreography tests"__
> - Ensure __architectural structure__
> - Run periodically
> - __NOT part of Continuous Integration__

> System Tests:  
> ~10% coverage  
>
> 🚀 Run speed: Slow (periodical runs)  
> 💰 Dev and testing cost: High  
>
> - Against __entire integrated system__
> - __Does not test business__
> - __Throughput__ and __performance__ tests
> - Written by __architects__ and __lead devs__

> Manual Exploratory Tests:  
> ~5% coverage
>
> 🚀 Run speed: Very Slow  
> 💰 Testing cost: Very High  
>
> - Done by QA
> - By hand, no automation, nor script
> - Check is __system behaves well under human operations__
> - Goal is to __creatively find peculiarities__

# 9. Time Management

- Your responsibility is __your project first__

# Meetings

- __Accept meetings__ only if your __participation is immediately and significantly necessary__ to the __job you are doing now__

- __Leave a meeting respectfully__ if:
	- it's __bad use of your time__,
	- it's __boring__
	- if you __can no longer contribute__

> Stand-up meeting (agile daily): 
>- 📅Schedule: __Every day__
>- 🚀Goal: __Report__ yesterday's activity and __prepare__ the day
>- 📄Content:
>	- Each member answers __3 questions__:
>		1. What did I do yesterday ?
>		2. What am I doing today ?
>		3. What is in my way ?
> - ⏰Time management:
> 	- __20 secondes answer__ for each question

> Sprint planning meeting: 
>- 📅Schedule: At the __start of each sprint__
>- 🚀Goal: __Select backlog__ for next sprint
>- 📄Preparation:
>	- __Estimates__ should already be done
>	- __Assessment of business value__ should already be done
>	- __Acceptance/component tests__ should be done or at least __sketched out__
> - ⏰Time management:
> 	- __5% of total sprint time maximum__ (for a 40h sprint = 2h meeting)
> 	- If item discussion __takes too much time__, __schedule an other meeting with a subset of the team__
>

> Retrospective Meeting:  
>- 📅Schedule: At the __end of each sprint__
>- 🚀Goal: Discuss __what when write or wrong__ during the sprint and __demo to stakeholders__
> - 📄Preparation:
> 	- Quickly prepare what is going to be demonstrated
> 	- Prepare documents to share if needed
>- ⏰Time management:
>	- Scheduled __45 minutes before the end of the sprint's last day__
>	- __20 minutes retrospective maximum__
>	- __25 minutes demonstration__

#### Working with others
- If you __disagree__, __express it or you must engage in made choices__
- If an __argument must be settled__, present the __arguments in turn and vote__
- __*"Focus-mana"* is limited__, take time to __recharge it__
	Sleep, caffeine, de-focus to re-focus

### Personal time management
> Pomodoro Technique
>- Work and pause in cycles
>- Classic pomodoro:
>	- __4 cycles__ of __25 minutes work__ and __5 minutes pause__
>	- Take __30 minutes pause every 4 cycles__
>- Easy __productivity statistics__ by counting the __number of cycles__

> Common time wasting behaviors
>- Priority Inversion:
>	- ❌Behavior: Avoid the task with the true priority by falsely raising the priority of another task
>	- ✅Solution: Don't avoid scary work and keep you tasks priority in check
>- Blind alleys:
>	- ❌Behavior: Vested in a decision you wander down into a technical pathway that leads to nowhere
>	- ✅Solution: Always keep an open mind into other ideas. Learn to have the skill of quickly realizing you are in a blind alley and the courage to back out.
>- Upgradable code:
>	- ❌Behavior: Don't act when you see code that you could upgrade
>	- ✅Solution: Immediately act on code you could upgrade. Understand that the cost  will always be bigger later.

# 10. Estimation

# Different definitions
- For __business__: __estimation = commitment__
- For developers: __estimation = guess__ /= commitment
- A commitment is a __*distribution* of probabilities__

# PERT: Program Evaluation and Review Technique
> Triviate Analysis:  
> #### Input: 3 estimates for the task
> 1. __O__: Optimisic (<1% occurrence)
> 2. __N__: Nominal (greatest chance of occurrence)
> 3. __P__: Pessimistic (<1% occurance)
> 
> 
> #### Output: 2 computed value
> $$\mu \text{ : Expected Duration} = {O + 4N + P \over 6}$$
> $$\sigma \text{ : Standard Deviation} = {P - O \over 6} $$
> $$\text{ESTIMATE} = {\mu \over \sigma}$$
> A __proper estimation__ is composed of an __***Expected Duration*** and a ***Standard Deviation***__
>
>> Set of tasks
>> $$\mu_{set} = {\sum \mu_{task}}$$
>> $$\sigma_{set} = {\sum \sigma_{task}^2}$$

> Task Example:  
> $$\text{Input :} \qquad O = 1 \qquad P = 12 \qquad N = 3$$
> $$\text{Output :} \qquad \mu = {1 + 4*3 + 12 \over 6} = 4,2 \qquad \sigma = {12 - 1 \over 6} = 1,8$$
> $$\text{ESTIMATE :} = 4,2 / 1,8$$
> $$\text{The task will probably take 5 days (4,2)}$$
> $$\text{But could take 6 or 9 days (+1,8 or +1,8*2)}$$

> Set of tasks example:  
>
> $$\mu_1 = 4,2 \qquad \mu_2 = 3,5 \qquad \mu_3 = 6,5 $$
> $$\sigma_1 = 4,2 \qquad \sigma_2 = 3,5 \qquad \sigma_3 = 6,5 $$
>
> $$\mu_{set} = 4,2 + 3,5 + 6,5 = 14$$
> $$\sigma_{set} = (1,8^2 + 2,2^2 + 1,3^2)^{1/2} \simeq 3,13 $$
> $$\text{The 3 tasks could probably take 14 days to be completed} (\mu)$$
> $$\text{But could take 17 or 20 days} (1 \sigma \; or \; 2 \sigma)$$

# Nominal estimate techniques
> Wideband delphi, "Flying Fingers" or "Planning Poker":  
> 1. Discuss the task
> 2. Blind estimation of each members
> 3. If the estimations are close, take the average
> 4. If there is significant differences in estimation by at least one member iterate with another discussion and vote until ALL estimations are close

> Affinity estimation:  
> 1. Teams members sort the tasks without showing their estimation nor talking to each other (shared list, usually on board)
> 2. Any card moved *n* times by any members is set aside for discussion
> 3. Discuss cards and replace until no more movement
> 4. Group tasks in buckets of estimate (traditionally in Fibonacci sequence buckets)

> Law of large numbers:  
> The sum of sub-tasks estimates is a good estimate for the parent task (apply to hard task and large estimates)


> Key concepts:  
> - Don't commit if you cant
> - Provide hard numbers
> - Provide probabilistic estimates: *Expected completion time* and *Variance*

# 11. Pressure

- The professional developer is __=calm and decisive under pressure__=
  As the pressure grows he __adheres to his training and disciplines__
  They are the __best way to meet the deadlines and commitments__ that are pressing on him

- The best way to stay calm under pressure is to __avoid the situations that cause pressure__

> Business commitments made for us:  
> We are __honor bound to help the business__ find a way to meet those commitments  
> We are __NOT honor bound__ to accept the commitments

> Be a professional:  
> Professionals will __always help the business find a way to achieve its goals__  
> But professionals __do not necessarily accept commitments made for them by the business__

> Staying Clean:  
> Professionals realize that "quick and dirty" is on oxymoron. __Dirty always means slow__ !

> Disciplines in time of crisis:  
> - Truly __believe__ in your disciplines
> - Choose disciples that you __feel confortable following in a crisis__.
> - Follow your disciplines __ALL THE TIME__
> - They are the __BEST WAY to avoid getting into a crisis__
> - Don't change your behavior __when the crunch comes__. Instead __follow them even more__.
>  
>  > Responds to crisis with more disciplines, not less  
>  > This is __not the time to question or abandon__ disciplines.
>  >
>  > If you follow TDD : __Write even more tests that usual__
>  > If you are a merciless refactor: __refactor even more__
>  > If you keep your functions small: __keep them even smaller__
>  >
>  > In tough times __rely on what you already know__, your __DISCIPLINES__

## Handling Pressure
> Don't Panic:  
> - The __worst thing__ you could do is __rush__ !
> - Rushing will only drive you deeper in the hole you might be in.
> - Instead, __slow down__. __Think the problem through__.
  
> Communicate:  
> If you are in trouble:
> 1. __Let your team and superior know__ that you are in trouble
> 2. __Tell them your best plans__ for getting out of trouble
> 3. __Ask__ them for their __input__ and __guidance__  
>
>__Avoid creating surprises__. They multiply pressure by ten, make people angry and less rational.

### Get Help
- PAIR !
- Offer to pair when you see someone else who is under pressure.

> Key Concepts:  
>- Manage your commitments and the commitments others might make for you
>- Follow your disciplines at all times and keep clean
>- Stay calm, communicate, follow your disciplines and get help

# 12. Collaboration

- Teams are __most effective__ when the team __members collaborate professionally__
  Being a __loner__ or a __recluse__ on a team is __unprofessional__

## Programmers vs People
- Programmers tend to enjoy mild sensory deprivation and cocoon like immersion of focus

## Programmers vs Employers
> Pay attention to the ship you are sailing on.  
> The worst thing a programmer can do is to __bury himself in tech while the business is crashing and burning__ around him
> Keeping the business afloat is your job too !
>
> 1. Take time to __understand the business__
> 2. __Talk to users__ about the software they are using
> 3. __Talk to sales and marketing__ people about the problems and issues they have
> 4. __Talk to managers__ to understand the __short__ and __long-term goals__ of the team

## Programmers vs Programmers
> The team own the code, not individuals.  
> Worst symptoms of a dysfunctional team is when __each programmer builds a wall around his code__ and refuses to let other programmers touch it  
> It is far __better to break down all walls of code ownership__ and have the __team own ALL the code__
>
> - __Work with each other__ on as much of the system you can
> - __Learn from each other__ by working with each other __on other parts of the system__

### Pairing
> Two heads are better than one:   
> __Pairing__ is :  
> 1. The __most efficient way to solve problems__
> 2. The __best way to share knowledge__ with each other
> 3. The __best way to review code__ (the even best way is __collaborating in writing it__)
>
> All team members __should be able to play another position in a pinch__

### Working alone
> Working alone:  
> You __might think that you work better__ when you work __alone__  
> Does that mean that the __team works better__ when you work alone ?
> 1. It is __unlikely__ that you do work better when you work alone
> 2. It is __better to collaborate closely with others__ and to __pair__ with them a __large fraction of the time__

> Key Concept:  
> Programming is all about __working with people__

# 13. Teams and Projects

- It __makes no sense__ to tell a programmer to devote __half their time to project A__ and the __rest of their time to project B__
  __Different__ project __managers__, different __business analysts__, different __programmers__, different __testers__ : that __NOT a team__

> The Gelled Team  
> It __take time__ for a team to form:  
> 1. They learn __how to collaborate__ with each other
> 2. They __learn each other's quirks__, __strengths__ and __weaknesses__
>   
> A __Golden team__ will:
> 1. __Anticipate__ each other
> 2. __Cover__ for each other
> 3. __Demand the best__ from each other

> Team Composition: 
> The ratio of programmers to testers and analysts can vary but 2:1 is a good number
>  
>> Programmers:  
>	
>> Testers:  
>> Write __automated acceptance tests__  
>> - Focus: __Unhappy paths__: __failure__ and __boundary__ (what might go wrong)
>
>> Analysts:  
>> Develop the __requirements__ and write __automated acceptance tests__
>> - Focus: __Happy Paths__: __business value__
>
>> A Project Manager:  
>> __Tracks the progress__ of the team and makes sure the team __understands the schedules__ and __priorities__
>
>> Team Conscience:  
>> One of the team members may play a part-time role of coach or master and take responsibility for __defending the team's process__ and __disciplines__
>  They act as the team conscience __when the team is tempted to go off-process__ because of schedule pressure

### Fermentation
- It __takes time__ for a team to __work out differences__, __come to terms__ with each other, and really gel
- It is __ludicrous to break it apart__ just because a __project comes to an end__
- It's best to __keep that team together__ and just keep feeding it projects

### Which can first, the Team or the Project ?
- It is a __foolish approach to form a team around a project__
	Team members __need the time to learn to work together__
	A short project or working multiple project for a fraction of the time does not do that

- A __team that is gelled together__ can, as a team, __change its focus__ if needed and __relocate priorities quickly__.
  Because they __know each other__ and __how to work with each other__. They will __reorganize quickly and easily__.

> Key Concept:  
> Teams are harder to build than project  
> It is better to form a persistent team that move together from one project to the next and can take on more than one project at a time  
> A gelded team work together as an optimized engine and get project done

# 14. Mentoring, Apprenticeship, and Craftsmanship


- Craftsmanship is __handed from one person to another__. From elders to young and exchanged between peers.
- It a __contagion__, a mental virus, __caught__ by __observing others__
## 

## Unconventional Mentoring
- Learning from a well-written manual
- Learning by __observing people even__ when hey __don't want to__ or __don't care__ about mentoring

## Evolution of a programmer
> Apprentices/Interns: 
> - __No autonomy__, very __closely supervised__ by journeymen
> - Takes __no tasks__ at all and simply __provide assistance__ to the journeymen
> - Very __intense pair-programming__
> - Until __foundational values are created__. Learning and reinforcing __disciplines__

> Journeymen: 
> - __Trained, competent and energetic__
> - Are __learning to work well in a team__ and __to become team leaders__ (masters)
> - Knowledgeable about __current technology__ but typically __lack experience with many diverse systems__
> - __Supervised__ by masters or other more senior journeymen
> - Work __closely supervised__ and __code is scrutinized__ until they __gain experience and autonomy__ and the supervision becomes less direct and more nuanced. Eventually transitioning into peer review.

> Masters: 
> - Programmers who have taken the __lead on more than one significant software project__
> - Typically __10+ years of experience__
> - Experience with __different kinds of systems__, __language__ and __operating systems__
> - Know how to __lead and coordinate multiple teams__, are __proficient designers__ and __architects__
> - __Maintain__ their technical role by __reading__, __studying__, __practicing__, __doing__ and __teaching__
> - The one that will be assigned __technical responsibility for a project__

- This description is idealized. __In most companies there is no technical supervision at all__
- Programmers get promotions and raises often because they are "there" and that is what you do with them
- Most of the time __elders do not take the time to teach the young__. That is __something that must change__

# What is a craftsman and craftsmanship ?
> Qualities: 
> - __Skill__
> - __Quality__
> - __Experience__
> - __Competence__
> - __Works quickly__
> - __Does not rush__
> - __Provides reasonable estimates__
> - __Meets commitments__
> - Knows when to __say no__
> - Tries hard to __say yes__
> - Is a __professional__

> Mindset: 
> - __Values__
> - __Disciplines__
> - __Techniques__
> - __Attitudes__
> - __Answers__


# A. Tooling

## IDE
- Were you write your code
- Has features to make development easier (auto completion, .. )
- Learn to use it properly and take time to customize it for you work.

## Continuous Build
- Hooks up to the __source code control system__
- When people check in code, it __automatically build and report the status of the team__
- If a __build fails__, it should stop the work and the __team should meet to quickly resolve__ the issue
  __Should not persist a day or more__
- Developers __run the continuous-build locally before they commit__

## Unit Testing Tools
- Features they should all support (and do):
	1. Should be __quick and easy to run tests__
	2. Should give you __clear visual pass/fail indication__
	3. Should give you a __clear visual indication of progress__
	4. Should __discourage individual test cases from communicating with each other__

## Component Testing Tools
- For __testing__ components at the __API level__
- Make sure that the behavior of a component is __specified in a language__ that the __business and QA people can understand__
- Ideally QA and business can write the specifications using the tool
- __Specifications are the Definition of Done__
  Completely unambiguous. __Done = All Tests Pass__

## Integration Testing Tools
- Component testing tools can also be used for many integration tests but are less than appropriate for tests that are driven through the UI
- __End-to-End tests__ are usually __not very many__ because __UIs are volatile__

## Unified Modeling Language (UML)/ Model Driven Architecture (MDA)
- The dream of models is to allow developers to leave behind the details of textual code and author systems in a __high-level language of diagrams__
- The __caveat__ is that modelling __does not includes details__ that the developers has to handle in his code

> Code for a teletype machine in the 70s:  
> ***Theses informations could easily be written into a model diagram:***
> - At the end of a line you need to go down to the next line (new line feed) (`\n`)
> - At the end of a line you need to go back to the start of the line (carriage return) `\r`
> - (Or simple "At the end of a line do a line return" which is common now since going to the next line and to the start of the line is shortened into the line return `\n`)
>
> ***This is the kind of __detail that wont be (shouldn't) be written into a model__:***
> - You need to wait some delay when you do theses 2 actions or text will be written at the wrong place
> - The __behavior__ of `\n` or `\r` is __interpreter specific__ (some interpret `\n\r` as two lines, some recognize `\n\r`, others `\r\n`)
> 
> Line endings are a common issue even today and __this kind of extra detail cannot be eliminated by a picture representation that diagrams are__

__The difference in the level of abstraction between code and diagrams is tiny at best.__

