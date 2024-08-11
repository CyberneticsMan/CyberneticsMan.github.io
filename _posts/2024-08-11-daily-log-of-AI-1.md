---
layout: post
title: the AI journey begins
date: 2024-08-11 00:00:00
categories: AI
published: true
---

# The AI journey begins


This weeks subject was statistics and probability.

each day has its own question.

## Day 1

it was a basic question about solving a definite integral using pure python and the numpy library.

it wasn't too difficult but it was a good refresher.

## Day 2

The question was about a clumsy servant and a party of 238 guests. The clumsy servant is in charge of mens hats. all hats are the same. the servant mixes up the hats and gives them to the guests. what is the probability of each guest getting the correct hat?

this one was about doing a simulation of the problem and then calculating the probability of each guest getting the correct hat.

I did the simulation 10000 times and averaged the results.

like so:

```python
import numpy as np

def solve():
    number_of_guests = 238
    simulation_count = 10000
    results = []
    for _ in range(simulation_count):
        hats = np.arange(number_of_guests)
        np.random.shuffle(hats)
        results.append(np.sum(hats == np.arange(number_of_guests)))
    return int(np.mean(results).round())
```


## Day 3

The question was the Monty Hall Problem.

Following the start of my journey into the world of AI and machine learning, I was give the assignment to solve the Monty Hall Problem as a part of my homework. where there are 3 doors and behind one of them is a car and behind the other two are goats. The player picks a door and then the host opens one of the other two doors to reveal a goat. The player is then given the option to switch doors or stay with their original choice. The question is, is it better to switch doors or stay with the original choice?

-- Update: I was not turning into a percentage, lol.