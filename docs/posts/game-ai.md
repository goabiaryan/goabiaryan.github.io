---
title: "Developing A.I. using Games"
categories:
  - 2019
tags:
  - Agents
  - Machine Learning
---
**September 9, 2019** 

Intelligence is a highly abstract term that could mean several different things to several different people. In 2006, Shane Legg and Marcus Hutter decided to conduct a comprehensive literature review for the definition of intelligence in various disciplines. And thus, it paved the way for them to create a “complete” definition of intelligence finally presented in their 2007 paper [Universal Intelligence: A Definition of Machine Intelligence](https://arxiv.org/abs/0712.3329%0A). They defined it as -

> Intelligence measures an agent’s ability to achieve goals in a wide range of environments

### Various Kinds of Intelligence

While the above definition sound pretty general and obviously so. **A goal** can be anything — from moving from place A to place B — to — recognizing cat breeds from dog breeds — to — planning a birthday party.

While most earlier intelligence tests only tested for cognitive intelligence, for artificial intelligence- we have another equally important field of work to develop, often dealt in robotics, called Physical Intelligence. One can easily remark that physical intelligence can, in fact, be broken into a sequence of decisions combined with motor abilities for a machine.

All right, let’s take another example to mark the distinction- when we touch a hot saucepan we instantly pull our hand away, what kind of intelligence would you call it since it isn’t a goal-oriented intelligence? Maybe consciousness?! But then how do you define consciousness? Unfortunately given our own limited understanding of human cognition, defining it as consciousness is likely to send us spiraling down a never-ending *black hole* of what it means for something to be conscious or to have free will. Big, important terms. Poorly understood. But beyond the scope of this article.

So, for the sake of simplicity, let us call it physical intelligence i.e. our tendency to protect ourselves. **Bodies** by pulling our hand back or reproducing — **minds** by saying I give up when the going gets hard — **emotions** by distancing ourselves from the source of pain.

But, neither kind, cognitive or physical intelligence has yet been fully developed in only but biological organisms, and in varying degrees.

Coming to the next term in that definition, **the environment**. It’s obvious that goals can only be measured in a particular environment. Environments, thus, act as the deterministic bounds for these goals.

One of the most common domains where we explicitly seek, use and create environments is “Games” thus games become an excellent training ground for AI.

### Single Player Games

Some of the key environments for AI training today are single agent games where A.I. agents accomplish a per-determined goal for a reward (an actual reward or simply higher accuracy).

[Open AI’s Gym](https://gym.openai.com/) or [MuJoCo](http://www.mujoco.org/) is an excellent representation of many such environments where you can train your algorithm to perform for high accuracy on these games. There are some other open source implementations of these environments, for example, [RL-Baselines-Zoo](https://github.com/araffin/rl-baselines-zoo) or [RoboSchool](https://openai.com/blog/roboschool/) or [PyBullet Gym](https://github.com/benelot/pybullet-gym).

Though, using A.I. in Games isn’t a new phenomenon caused by the A.I. **outbreak** (*thanks Alex Net!*). A.I. has been long explored in the game domain. Among the key uses and implementations for A.I. in games earlier is developing new terrains, environments (esp. in rogue games) or defining the behaviors of NPCs (Non-Player Characters). Today, people in the game industry have now taken it a notch further by using AI to develop new game engines like [Angelina](https://twitter.com/angelinasgames).

### Key Algorithms for AI in Single Player Games

While it would be beyond the scope of this article to define all the algorithms in detail, some excellent resources on this topic are [Ian Millington’s Book on Artificial Intelligence for Games](https://www.amazon.com/Artificial-Intelligence-Games-Ian-Millington/dp/0123747317) and [Julian Togelius’ book on Artificial Intelligence and Games](https://www.amazon.com/Artificial-Intelligence-Games-Georgios-Yannakakis/dp/3319635182).

On the big picture level, these algorithms can be classified into three broad categories-

1. Movement Algorithms: This includes some of the most commonly known path-finding algorithms including Dijkstra or A* or Near-Optimal Hierarchical Path-finding (HPA) etc.
2. Decision Making Algorithms: These include, but aren’t limited to, decision trees, finite state machines (FSM), behavior trees, fuzzy state machines and Markov Systems.

The third category is the advanced State of the Art A.I. algorithms that we aren’t often seen in typical gaming industry implementations, though there are some exceptions we will discuss later.

Some of these key unexploited algorithms include-

- Monte Carlo Tree Search (MCTS)
- Evolutionary Algorithms (Random-Key Genetic Algorithms, Differential Evolution Algorithms etc)
- Deep Reinforcement Learning — Policy Gradient (PPO/TRPO), Q-Learning(DQN/HER) or Mixed Policy Optimization (DDPG/SAC)

However, mainstream tech companies and academic labs for AI and Robotics, have been developing, exploiting and extending various AI algorithms and implementing them on simpler custom-built environments.

However, one of the key limitations of using single-player games to model and develop A.I. in single-agent environments is the inability of these trained agents to achieve goals in different multi-agent environments, thus refuting Shane and Hutter’s definition of intelligence.

> Intelligence measures an agent’s ability to achieve goals in a wide range of environments.

### Multiplayer Games

Some of the most prominent and recent success of our A.I. advancement can be captured by their performance on multiplayer games including [Dota2](https://openai.com/five/) and [StarCraft](https://deepmind.com/blog/alphastar-mastering-real-time-strategy-game-starcraft-ii/).

This kind of environments often extend the capabilities of a single-player-environment-agent (SEA) to a multiplayer-environment-agent (MEA) by adding something extra to the mix. This extra is the tactical and strategic A.I. that includes way-point tactics, coordinated action and learning.

Multi-player games come in many flavors — small (Warframe), huge (Super Mario) or Open World Games (Sims 4, The Elder Scrolls V: Skyrim) and thus present a huge play-field for the research and development for A.I. algorithms.

### The World is a Simulation

While potentially a contrarian view, the key fascination for A.I. researchers in games stems from the ability to closely simulate the real world to understand and imitate human behaviors and actions.

But isn’t the goal to create machine learning algorithms that could compete and (or) cooperate with human beings? Yes, precisely.

While playing a game, you are inside a carefully simulated world where your actions and reactions have been pre-planned by the game designer and are hard-coded in advance. Thus, one could argue that most games are boxes of complete (and also constantly evolving for open-world games) information. Thus, it’s fair to say that if you can learn the rules you could win the game. However, the real world ain’t much different.

For years, the so-called capitalist companies have been studying human behaviors to influence human decisions. Companies like Apple and Zara use several variations of warehouses to study the effect of the music playing in their stores to the lighting and positioning of items in the store. Researchers from various backgrounds (business, psychology, economics, politics, finance, journalism — you name it) have for years studied how predictable humans are — including Jonah Berger, Dan & Chip Heath, Fiery Cushman, Dan Ariely, Charles Duhigg, Daniel Kahneman, Richard H. Thaler, Daniel M. Oppenheimer.

In fact, some of the most fascinating work in the field of complex human patterns can be contributed to the man who shocked the world, Stanley Milgram, who devised a simple Obedience experiment to answer the following question about Nazi Germany and Holocaust:

> Could it be that Eichmann and his million accomplices in the Holocaust were just following orders? Could we call them all merely accomplices?”

To someone who has never thought of his and other humans’ behaviours as predictable, manipulable patterns, questions like these might seem like philosophical questions. However, based on Milgram’s experiment, he reached a conclusive answer in his article [Perils of Obedience](https://is.muni.cz/el/1423/podzim2013/PSY268/um/43422262/Milgram_-_perils_of_obediance.pdf)

> Ordinary people are likely to follow orders given by an authority figure, even to the extent of killing an innocent human being. Obedience to authority is ingrained in us all from the way we are brought up. People tend to obey orders from other people if they recognize their authority as morally right and/or legally based.

This led him to the development of Milgram’s Agency Theory. Milgram’s Agency Theory suggests humans have two mental states:

1. Autonomous: In the Autonomous State we perceive ourselves to be responsible for our own behaviour so we feel guilty for what we do
2. Agentic: In the Agentic State we perceive ourselves to be the agent of someone else’s will; the authority figure commanding us is responsible for what we do so we feel no guilt.

As such, humans are predictable beings who live in a carefully planned predictable open-world. According to [Seanoe et. al.](https://royalsocietypublishing.org/doi/10.1098/rsif.2018.0395), the world we live in can also be interpreted as a biological (and, technological) evolution strongly tied to the generative potential tied through combinatorics that allows the system to grow and expand their available state spaces. Thus, many complex systems that presumably display Open-Ended Evolution, from language to proteins, share a common statistical property: the presence of [Zipf’s Law](https://www.wikiwand.com/en/Zipf%27s_law).

Though, according to another [study](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0029796) conducted by Thurner et. al. on human behavioural sequences in an online world, it suggested that on a collective societal level the time-series of particular actions per day can be understood by a simple mean-reverting log-normal model which explains the rarity of absolute autonomy.

To conclude, it won’t be wrong to say that we are merely agents with the two agencies (autonomous and agentic) in a multi-agent world.

There are two essential ingredients when simulating human-like multi-agent societies-

1. EvolutionThe environment or agent should be open-ended and constantly evolving.
2. CreativityThe idea of seeing [creativity as a search](https://www.researchgate.net/profile/Margaret_Boden/publication/209436199_Creativity_in_a_nutshell/links/5424477c0cf26120b7a732d4/Creativity-in-a-nutshell.pdf) in a space of potential search-space is not new; it has been discussed at length by, for example, the British philosopher Margaret Boden. In fact, J. Schmidhuber has also worked tirelessly to capture the idea of curiosity and creativity to devise a [Formal Theory of Creativity](http://people.idsia.ch/~juergen/creativity.html)

### But training AI on Games isn’t a good idea in the long run

Let us substitute the word “game” for the environment especially since we have established that the two mean the same in an agents’ world.

Now, the games or training environments for AI can be broadly classified into two categories which can be further divided into two sub-categories-

1. Static Environments
2. Dynamic Environments
    - Dynamic Determinate Environments
    - Dynamic Indeterminate Environments

While training and developing AI algorithms to perform well on static environments is a near-finish goal however developing A.I. that can achieve goals in dynamic environments is an area of research where we quickly hit various roadblocks, esp in dynamic indeterminate environments. In my opinion, there are three key contributors to the same-

First would be our inadequate understanding of complexity theory and chaos theory. One of the most interesting efforts that is being pursued in this direction is [Fractal AI](https://arxiv.org/abs/1803.05049).

Second is the lack of models. Most of our current AI models are data-hungry beasts that need huge computational resources. Some of the most interesting works in this direction pursued by the Game AI community are [Framing for Computational Creativity](http://www.possibilityspace.org/papers/iccc19.pdf) and by the causal inference community [The Book of Why](https://twitter.com/yudapearl)

The third is the problem of learning that includes transfer learning and lifelong learning. Some of the interesting works in this direction are [AutoML Research](https://www.automl.org/), [Meta-Learning](https://lilianweng.github.io/lil-log/2018/11/30/meta-learning.html) and Differential Evolution (check [Differential Plasticity](https://github.com/uber-research/differentiable-plasticity))

### Open-Endedness

One of the classical properties of Dynamic Indeterminate Spaces is their [open-endedness](https://www.oreilly.com/ideas/open-endedness-the-last-grand-challenge-youve-never-heard-of). Open-ended problems are hard to define and model thus are often abandoned due to the lack of definite metrics.

Another way of looking at this problem is through the lens of algorithmic complexity namely [Kolmogorov Complexity](https://www.wikiwand.com/en/Kolmogorov_complexity), [Attribute Substitution](https://www.wikiwand.com/en/Attribute_substitution), [Occam’s Razor](https://www.wikiwand.com/en/Occam%27s_razora) and [Adaptive Levin Search](http://people.idsia.ch/~juergen/mljssalevin/node5.html).

However, a few researchers who dabbled into this space have created quite a perspective shift. One such work is the paper [Exploiting Open-Endedness to Solve Problems Through the Search for Novelty](http://eplex.cs.ucf.edu/papers/lehman_alife08.pdf). Later, another excellent work in novelty-search which a few years later led to the development of [quality-diversity algorithms](https://www.frontiersin.org/articles/10.3389/frobt.2016.00040/full).

According to one of the first [papers](https://www.frontiersin.org/articles/10.3389/frobt.2016.00040/full) in Quality diversity (QDA) algorithms by Kenneth Stanley et. al., QDAs is a kind of learning algorithm (for example, novelty search with local competition and [MAP-Elites](http://jeffclune.com/publications/2019-06-20-ReWork-POET.pdf)) that try to balance the great dilemma in machine learning: **exploration vs. exploitation**. They aim to optimize for both quality and diversity simultaneously while aiming to fill a space of possibilities with the best possible example of each type of achievable behaviour. The result is this new class of algorithms that return an archive of diverse, high-quality behaviours in a single run.

Though, because of the digital nature of inheritance, there are inherent limits on the kinds of questions that can be answered using such an approach. In particular, according to an excellent paper by [Troy Day](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3284140/), even in extremely simple evolutionary systems, a complete theory accounting for the potential open-endedness of evolution is unattainable unless evolution is progressive.

However, in 1936, Turing adapted Godel’s Theory of Open-Endedness (also called Incompleteness) to computability to show that a general algorithm to solve the [halting problem](https://www.wikiwand.com/en/Halting_problem) for all possible program-input pairs cannot exist.

One of the rebuttals of Godel’s open-endedness problem has been presented in [Monads and Sets: On Gödel, Leibniz, and the Reflection Principle](https://www.semanticscholar.org/paper/Monads-and-Sets%3A-On-G%C3%B6del%2C-Leibniz%2C-and-the-Atten/1bc646d1c6b0494f8b65477f0dd4e36e54253948). In complexity theory, it can also be interpreted as the Reflection Principle applied to the [Wiener Process](https://www.wikiwand.com/en/Reflection_principle_%28Wiener_process%29).

So, if we were to agree with Godel and his theory of open-endedness, then how do we develop progressive environments thus leading to progressive search spaces and thus hopefully progressive quality-diversity search algorithms?

### Introducing PCG

Procedural content generation (PCG) is the programmatic generation of game content using a random or pseudo-random process that results in an unpredictable range of possible gameplay spaces.

But why games again? Didn’t we just establish that games are inadequate training environments?

Games make it easy to comparatively test and measure for novelty, delight and desirability in the newly created content.

Some of the interesting applications of procedural content generation for training A.I. agents have been seen in the games like [Obstacle Tower](https://arxiv.org/abs/1902.01378), [Capture the Flag](https://deepmind.com/blog/capture-the-flag-science/) etc. Though it would be interesting to see A.I. agents trained on games like The Shadow of Mordor, a game where NPCs remember their encounters with you and refer back to them in future fights to more accurately represent the real world.

Thus, PCG presents huge opportunities for the field of A.I. in general. However, one of the big problems would be while games present excellent training environments for training our A.I. agents in decision making for competition and cooperation. But one of the biggest challenges for these advanced A.I. algorithms would be coordination with humans due to the differences in evolution.

Despite our common biological roots and parallel evolutionary process, it has taken animals and humans only 200,000 years to adapt and evolve alongside each other.

Through these thousands of years of shared evolution, many animal species esp cats and dogs have become inseparable from human societies, not only terrestrially but also emotionally — a magnificent feat especially given the lack of a common language of expression and entirely different cognitive and physical abilities.

### The Way Ahead: Mixed-Initiative Games

This suggests that we could build A.I. systems where A.I. algorithms can collaborate with humans such that the AI can learn, provide suggestions and guess the intent of the human user to help him achieve common goals.

Some interesting works in this direction are [Mixed Initiative Game Design Platform Tangara](https://link.springer.com/chapter/10.1007/978-3-319-42716-4_11), [Quake III Arena](https://deepmind.com/blog/capture-the-flag-science/), [Sentinent Sketchbook](http://www.sentientsketchbook.com/) which is used by AI to second guess the designer’s intention, [Collaborative Language Grounding with Robots](http://www.cse.msu.edu/~jchai/), [Hierarchical Imitation](https://slideslive.com/38916832/beyond-demonstrations-learning-behavior-from-higherlevel-supervision) and [Intrinsic Social Motivation via Causal Influence in Multi-Agent Reinforcement Learning](https://www.media.mit.edu/publications/intrinsic-social-motivation-via-causal-influence-in-multi-agent-rl/)


<sup> * Acknowledgements: I would like to thank [Ian Danforth](https://twitter.com/iandanforth) for proofreading the article and providing useful feedback.</sup>

### Citation
```
  @article{abi2019,
  title = "Developing A.I. using Games",
  author= "Aryan, Abi",
  journal = "abiaryan.com"
  year = "2019"
  month = "Sept"
  url = "https://abiaryan.com/posts/game-ai/"
  }
```