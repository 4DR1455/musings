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
I = \sum_{S}(\sum{D_{FS}})
$$

Where:
- $I$ = Absolute influence of First.
- $S$ = Iterator through Seconds related to First.
- $D_{FS}$ = Decisions taken by $S$ due to First's interests.

But... What happens when First can't influence Second's decisions but rather their image, prestige, or whatever else is not directly attached to Second's decisions? Who is in influence now? How much influence is being exercised? Is counting Second's decisions due to First's interests enough as a quantifying reference? I don't know... I guess it is, but I can't argue why... I can't argue why not either... I am at a dead end. Is someone reading? Just in case there is... What do you think?

Anyway, we have other problems to assess... Because these formulas assume every relation is equal... And it is not. 

## Weighting the Seconds

Let me explain: Having influence over my neighbor, a normal dude who has a normal life that can be summarized as *"working an average job, and hanging out with friends"*, gives me a very small amount of influence. But having influence over the EU president is a completely different story; I could probably access any big fish in Europe, probably push them into making some laws for me... Whatever, so... Different person, different influence... Therefore, influence might be quantified as...

$$
I = \sum_{S}\left(\sum(D_{FS}) \cdot \frac{\sum(D_{FS})}{\sum(D_{S})} \cdot I_{S}\right)
$$

Where:
- $I$ = Absolute influence of First.
- $S$ = Iterator through Seconds related to First.
- $D_{FS}$ = Decisions taken by $S$ due to First's interests.
- $D_{S}$ = Decisions taken by $S$.
- $P_{S}$ = Absolute influence of $S$.

### Weighting each decision

But... I have another idea... let me show you and then I'll explain:
Therefore, influence might be quantified as... (yeah sorry I had to do the show again)

$$
I = \sum_{S}(\sum(D \cdot I_{D}))
$$

Where:
- $I$ = Absolute influence of First.
- bla bla bla
- $I_{D}$ = The absolute amount of influence the decision is exercising.

So the previous formula: $I = \sum_{S}\left(\sum(D_{FS}) \cdot \frac{\sum(D_{FS})}{\sum(D_{S})} \cdot I_{S}\right)$ had the problem that each decision had the same importance... But they don't; I mean, asking for a tissue doesn't have the same impact on society as legalizing drugs. Different favors, different influence exercised.

Now we need to know how to quantify $I_{D}$, right? 

#### The society

Well, the way I can know how much influence a decision exercises... is by counting how many people are being affected by this decision... (yeah yeah, I know I am making the same mistakes, but let me iterate until I have nothing to quantify). Therefore, $I_{D}$ might be quantified as...

$$
I_{D} = \sum(\text{Seconds Affected By } I_{D})
$$

##### Impact spread

The formula lacks something... Affecting the president of a company is not the same as affecting my neighbor (the normal dude), is it? If you raise taxes or prices, the impact will spread through the clients of the company of the president... But my neighbor has to tank all the impact... And... the portion delegated from all people exercising influence over him.
But, this spreading... It doesn't matter who *"pays the price"*, the only thing that matters is *"the price being paid"*. Therefore, this does not change the equation. What shall be considered is...

##### Weighting impact

(I know... same thing as before... you told me... "You will want to weight it again!")

An oil tax raise affects someone who moves by bike differently than someone who moves by car. They spend different amounts of oil, so they feel the change differently... Different people, different impact... Therefore, $I_{D}$ might be quantified as...

$$
I_{D} = \sum_{S}(W_{S})
$$

Where:
- $I_{D}$ = (You already know that)
- $S$ = Number of Seconds affected by the decision.
- $W_{S}$ = The weight of the change that $S$ feels.

### Successes market
Again... Let's quantify $W_{S}$ I guess... Can we quantify it by money? I mean, a decision that has a heavy impact would make you spend a lot of money, or win a lot of money, so I must use the absolute value of money. But also, there are decisions someone takes for you that make you sad, or happy. How do I translate this into money? Maybe for the sad side, the amount of money it takes for you to get back into a stable state? So if you make \$200/day and it takes you 2 days to recover from your cat's death, the decision to kill your cat has a weight of \$400 on you. But what happens with the happiness side? If a K-pop idol decides to meet a random fan, it will make the fan so happy, and I would count that as the time of the K-pop idol. But if I meet the same K-pop idol, the weight won't be the same because I'm not really into it... This is so hard because it is so subjective... T_T 

How did we resolve the subjective value of things before? The market solved that... Therefore... we could invent a successes market in order to value the weight of successes! Let's imagine I make a decision; then I have to consider all the possible direct consequences of my decision among my influenced Seconds. Then, I would have to ask them to weight this consequence, asking the question: "How much money would you pay for that to happen again?" or "How much money would you pay to cancel that?" Then, I could get all these values and perform the calculus...

Now, the real world... We can't go and ask... What can we do? Let's see what people are paying for successes similar to what I would generate, and take this as a reference. It is an approach, yes, but it is the closest approach I can get through these late writings... Isn't it?

### An example:
I am the General Secretary of FIB Visiona, a student association meant to organize the annual career fair of the FIB (Barcelona School of Informatics). Let's calculate the influence that it has:

**The faculty:** (Yes, you will have to trust my numbers, and yes, I'm kinda guessing them, but hey, it is an example, not a real thing; the correctness of the numbers doesn't matter at all.)
- They include us in most of their business-college events ($W_{S} = 5\text{k}$€)
- They give us a permanent space in a building ($W_{S} = 10\text{k}$€)
- They do a public tender to buy our infrastructures ($W_{S} = 70\text{k}$€)
- They spend the time of their employees attending to us ($W_{S} = 5\text{k}$€)
- They do not buy brand positioning services ($W_{S} = 50\text{k}$€)

**The companies:** (You'll trust my guessed numbers again, right?) *(Value per company)*
- They spend their employees' time doing all the stuff to get into the fair ($W_{S} = 1.5\text{k}$€)
- They have less HR work to do ($W_{S} = 10\text{k}$€)
- They invite us to their events ($W_{S} = 5\text{k}$€)
- They find more synergies with other associations ($W_{S} = 20\text{k}$€) *(I'm counting lots of things going from technical screening, brand positioning, subscriptions, sponsorships, or even hiring)*

**Fira de telecos:** They are the annual career fair, and we let them exchange days so they don't do the fair the same day as another telecommunication engineering fair.
- Companies go to both fairs ($W_{S} = 60\text{k}$€) *(Yeah, they can't do the big thing we do 😎)*

Soooooooooo

We have an influence over the FIB of:

$$
I_{\text{FIB}} = 5\text{k} + 10\text{k} + 70\text{k} + 5\text{k} + 50\text{k} = 140\text{k€}
$$


We have an influence over each company of:

$$
I_{C} = 1.5\text{k} + 10\text{k} + 5\text{k} + 20\text{k} = 36.5\text{k}
$$

We have an influence over Fira de telecos of:

$$
I_{T} = 60\text{k}
$$

Overall, FIB Visiona's influence score is... 

$$
I_{\text{FV}} = 140\text{k} + 36.5\text{k} + 60\text{k} = 236,500
$$ 

I still can't know if that's a lot or ridiculous, but... It's a number!!
Note: different people will have different scales. Alphabet would find this number completely forgettable, but... For us it is a lot, because we sweat to make it higher!

## But... What does the internet say?

**Me:**

Quines teories per la quantificació de la influència existeixen? Respon amb una llista de les 3 millor valorades

Vull una teoria que escali la influència com si fos una magnitud, una cosa que tu realment poguessis medir, una cosa semblant a això:

https://github.com/4DR1455/musings/blob/main/Infuence%20Quantification.md

------------------------------------------------------------------------

**Gemini (Deep research mode):**

Here's my plan to tackle that topic. Let me know if you need to make changes.

---

**Me:**

Start research

---
**Gemini (Deep research mode):**

I've completed your research. Feel free to ask me follow-up questions or request changes.

Quantificació de la Influència

14 de set., 0:22

---

**Me:**

molt text, dona'm 1 nom i 1 formula per cada teoria

---

**Gemini:**

Aquí tens el nom i la fórmula clau de cadascuna de les 3 teories:

### 1. Teoria del Camp de Potencial Topològic

Mesura la magnitud d'influència total que un node irradia sobre el conjunt de la xarxa en funció de la seva massa i la distància geodèsica:

$$\Phi(v_j) = m_j \sum_{i=1}^{\vert{}V\vert{}} e^{-\left(\frac{d(v_i, v_j)}{\sigma}\right)^2}$$

### 2. Teoria de l'Entropia de Transferència

Mesura la taxa d'influència causal directa d'un procés sobre un altre restant la història prèvia del receptor (en bits d'incertesa eliminada):

$$T_{J \to I} = \sum p\left(i_{t+1}, i_t^{(k)}, j_t^{(l)}\right) \log_2 \left( \frac{p\left(i_{t+1} \mid i_t^{(k)}, j_t^{(l)}\right)}{p\left(i_{t+1} \mid i_t^{(k)}\right)} \right)$$

### 3. Teoria Axiomàtica del Valor Marginal (Valor de Shapley)

Mesura la contribució marginal neta i conservativa d'un individu sobre totes les coalicions o cascades possibles del sistema:

$$\phi_i(v) = \sum_{S \subseteq N \setminus \{i\}} \frac{\vert{}S\vert{}!(\vert{}N\vert{} - \vert{}S\vert{} - 1)!}{\vert{}N\vert{}!} \Big[ v(S \cup \{i\}) - v(S) \Big]$$

---

Let me translate my native language for you:

As I requested, it gives 3 theories: