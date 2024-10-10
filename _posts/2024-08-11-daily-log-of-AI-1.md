---
layout: post
title: The AI Journey Begins
date: 2024-08-11 00:00:00
categories: AI
published: true
---

# The AI Journey Begins

This week's subject was statistics and probability. Each day has its own question.

## Day 1

It was a basic question about solving a definite integral using pure Python and the NumPy library. It wasn't too difficult but it was a good refresher.

## Day 2

The question was about a clumsy servant and a party of 238 guests. The clumsy servant is in charge of men's hats. All hats are the same. The servant mixes up the hats and gives them to the guests. What is the probability of each guest getting the correct hat?

This one was about doing a simulation of the problem and then calculating the probability of each guest getting the correct hat. I did the simulation 10,000 times and averaged the results, like so:

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

The question was the Monty Hall Problem. Following the start of my journey into the world of AI and machine learning, I was given the assignment to solve the Monty Hall Problem as a part of my homework. There are 3 doors and behind one of them is a car and behind the other two are goats. The player picks a door and then the host opens one of the other two doors to reveal a goat. The player is then given the option to switch doors or stay with their original choice. The question is, is it better to switch doors or stay with the original choice?

-- Update: I was not turning into a percentage, lol.
```
