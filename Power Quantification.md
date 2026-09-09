# Power Quantification
As I take part in the governing bodies of some non-profit organizations with very ambitious presidents and board members, I thought it would be convenient to understand which projects are profitable for these organizations. But... Why make money from an organization if no one takes advantage of it? That means money is not what we actually seek in a "project's profit". But... Then, what do we seek? What could compound and let us (and our successors) grow endlessly and have a payback for each member? Power... maybe. I might lose a bet on this... I hope I don't.

## Definition of power/influence/whatever you want to call it
The **influence of a person over another** is the capacity of the first person to force the second one into doing something that results in a loss for the second person, without the second person being able to claim anything in exchange.

<b><i><u>Note:</u></i></b> In this case, a **person** is a physical person or a legal entity (i.e., an organization).

<b><i><u>Note 2:</u></i></b> This definition is based on various [definitions](https://dictionary.cambridge.org/dictionary/english/power) provided by the Cambridge Dictionary.

## First thoughts
How could I quantify something this abstract? It is not like I can use an "influmeter" (hahaha, like a thermometer -> influmeter. I know it is a very bad joke, my apologies). So my first approach is to assign a binary value if the condition is met; this way, the more dominant relations a person has, the more powerful they are... Therefore, power might be quantified as...
$$
PowerOfFirst = \sum(Seconds)
$$
But that misses something... Sometimes a person is not fully powerful over another. What happens if First can force Second into doing some things in specific scenarios, but can't force them to do just anything in any scenario?! Is that still called power? So a question comes to mind... Can I quantify power between individuals?

<b><i><u>Note:</u></i></b> I will be switching between power and influence depending on how I need to use the word, but they mean the same to me in this writing.

<b><i><u>Note 2:</u></i></b> From now on, if I refer to "First" and "Second", I am referring to the [[Power Quantification#Definition of power/influence/whatever you want to call it|definition]] I have provided.

## Quantifying power relations
So, as I want better precision than just the number of (forced or not) followers, I need to quantify how much power a person has over another... So, I'd need to count how many decisions are taken due to First's interests?
$$
PowerOfFirstOverSecond = \sum(Second'sDecisionsDueToFirst)
$$
Therefore, power might be quantified as... 
$$
P = \sum_{S}(\sum{D})
$$
Where:
- P = Power of First.
- S = Iterator through Seconds related to First.
- D = Decisions taken by S due to First's interests.

But... What happens when First can't influence Second's decisions but rather their image, prestige, or whatever else is not directly attached to Second's decisions? Who is in power now? How much power is being exercised? Is counting Second's decisions due to First's interests enough?
