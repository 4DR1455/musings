# Infuence Quantification
As I take part in the governing bodies of some non-profit organizations with very ambitious presidents and board members, I thought it would be convenient to understand which projects are profitable for these organizations. But... Why make money from an organization if no one takes advantage of it? That means money is not what we actually seek in a "project's profit". But... Then, what do we seek? What could compound and let us (and our successors) grow endlessly and have a payback for each member? Infuence... maybe. I might lose a bet on this... I hope I don't.

## Definition of influence
The **influence of a person over another** is the capacity of the first person to force the second one into doing something that results in a loss for the second person, without the second person being able to claim anything in exchange.

* **Note:** In this case, a **person** is a physical person or a legal entity (i.e., an organization).

* **Note:** This definition is based on various [definitions](https://dictionary.cambridge.org/dictionary/english/influence) provided by the Cambridge Dictionary.

## First thoughts
How could I quantify something this abstract? It is not like I can use an "influmeter" (hahaha, like a thermometer -> influmeter. I know it is a very bad joke, my apologies). So my first approach is to assign a binary value if the condition is met; this way, the more dominant relations a person has, the more influenceful they are. 

## Base of the formula
That sounds good, I mean... a person who can move two people (themselves + another) has more influence than one who can't... Therefore, influence might be quantified as...

$$
{InfluenceOfFirst} = \sum({Seconds})
$$

But that misses something... Sometimes a person is not fully influenceful over another. What happens if First can force Second into doing some things in specific scenarios, but can't force them to do just anything in any scenario?! Is that still called influence? So a question comes to mind... Can I quantify influence between individuals?

<b><i><u>Note:</u></i></b> I will be switching between influence and influence depending on how I need to use the word, but they mean the same to me in this writing.

<b><i><u>Note 2:</u></i></b> From now on, if I refer to "First" and "Second", I am referring to the definition I have provided.

## Quantifying influence inside relations
So, as I want better precision than just the number of (forced or not) followers, I need to quantify how much influence a person has over another... So, I'd need to count how many decisions are taken due to First's interests? That makes sense to me because when someone exercises influence over another, they don't need to be present; just the thought of them would make the Second act in favor of First, and that would be a decision made due to First. So the influence of First over Second is...

$$
InfluenceOfFirstOverSecond = \sum(Second'sDecisionsDueToFirst)
$$

## Weighted relations formula
Now, I can complement the previous absolute influence formula by giving a score to each relation... Therefore, influence might be quantified as... 

$$
P = \sum_{S}(\sum{D_{FS}})
$$

Where:
- $P$ = Absolute influence of First.
- $S$ = Iterator through Seconds related to First.
- $D_{FS}$ = Decisions taken by $S$ due to First's interests.

But... What happens when First can't influence Second's decisions but rather their image, prestige, or whatever else is not directly attached to Second's decisions? Who is in influence now? How much influence is being exercised? Is counting Second's decisions due to First's interests enough as a quantifying reference? I don't know... I guess it is, but I can't argue why... I can't argue why not either... I am at a dead end. Is someone reading? Just in case there is... What do you think?

Anyway, we have other problems to assess... Because these formulas assume every relation is equal... And it is not. 

## Weighting the Seconds
Let me explain: Having influence over my neighbor, a normal dude who has a normal life that can be summarized as *"working an average job, and hanging out with friends"*, gives me a very small amount of influence. But having influence over the EU president is a completely different story; I could probably access any big fish in Europe, probably push them into making some laws for me... Whatever, so... Different person, different influence... Therefore, influence might be quantified as...

$$
P = \sum_{S}\left(\sum(D_{FS}) \cdot \frac{\sum(D_{FS})}{\sum(D_{S})} \cdot P_{S}\right)
$$

Where:
- $P$ = Absolute influence of First.
- $S$ = Iterator through Seconds related to First.
- $D_{FS}$ = Decisions taken by $S$ due to First's interests.
- $D_{S}$ = Decisions taken by $S$.
- $P_{S}$ = Absolute influence of $S$.

### Weighting each decision
But... I have another idea... let me show you and then I'll explain:
Therefore, influence might be quantified as... (yeah sorry I had to do the show again)

$$
P = \sum_{S}(\sum(D \cdot P_{D}))
$$

Where:
- $P$ = Absolute influence of First.
- bla bla bla
- $P_{D}$ = The absolute amount of influence the decision is exercising.

So the previous formula: $P = \sum_{S}\left(\sum(D_{FS}) \cdot \frac{\sum(D_{FS})}{\sum(D_{S})} \cdot P_{S}\right)$ had the problem that each decision had the same importance... But they don't; I mean, asking for a tissue doesn't have the same impact on society as legalizing drugs. Different favors, different influence exercised.

Now we need to know how to quantify $P_{D}$, right? 

#### The society
Well, the way I can know how much influence a decision exercises... is by counting how many people are being affected by this decision... (yeah yeah, I know I am making the same mistakes, but let me iterate until I have nothing to quantify). Therefore, $P_{D}$ might be quantified as...

$$
P_{D} = \sum(\text{Seconds Affected By } P_{D})
$$

##### Impact spread
The formula lacks something... Affecting the president of a company is not the same as affecting my neighbor (the normal dude), is it? If you raise taxes or prices, the impact will spread through the clients of the company of the president... But my neighbor has to tank all the impact... And... the portion delegated from all people exercising influence over him.
But, this spreading... It doesn't matter who *"pays the price"*, the only thing that matters is *"the price being paid"*. Therefore, this does not change the equation. What shall be considered is...

##### Weighting impact
(I know... same thing as before... you told me... "You will want to weight it again!")

An oil tax raise affects someone who moves by bike differently than someone who moves by car. They spend different amounts of oil, so they feel the change differently... Different people, different impact... Therefore, $P_{D}$ might be quantified as...

$$
P_{D} = \sum_{S}(W_{S})
$$

Where:
- $P_{D}$ = (You already know that)
- $S$ = Number of Seconds affected by the decision.
- $W_{S}$ = The weight of the change that $S$ feels.

Again... Let's quantify $W_{S}$ I guess...