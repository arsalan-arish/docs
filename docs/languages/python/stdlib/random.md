# random

- random.seed(10) # The default seed is random on time
- random.randint(a, b) # inclusive
- random.randrange(start, stop, step) # Random number from a range
- random.random() # like .randfloat(0, 1)
- random.uniform(a, b) # like .randfloat(a, b)
- random.choice(iterable) # returns a single choice
- random.shuffle(list) # Shuffles the list
- mylist = ["apple", "banana", "cherry", "wow"]  
random.choices(mylist, weights = [10, 1, 4, 2], k = 14) # returns a list of *k* randomly selected choices from the iterable, influenced by weights, and can be duplicable  
random.sample(mylist, k=2) # returns a list of *k* randomly selected choices from the iterable, non-duplicable, hence k must be less than len(mylist)  