# Making Decisions

To make proper decisions in programming, as in create different pathways to our instructions, it requires the following:

1. Creating Conditions
2. Evaluating Conditions
3. Events to occur depending on if a condition is true.

To simulate the following requirements, let's examine a `movie theatre pricing` situation.

```
// Movie Theatre Pricing

if you are an adult (17+), you pay $15.50.

if you are a child (17 and under), you pay $10.

if you are a senior (65+), you pay $12.
```

If we as a programmer were to create a `price checking program` , we would have to ask the user for their age, and the program should be able to generate with an appropriate pricing.

### Our Conditions

There are 3 conditions in this scenario:

1. Are they a senior?
2. Are they an adult?
3. Are they a child?

### Evaluation of the Condition

To determine which scenario they fall into, we must **compare their age against our threshold.**

1. They are a senior if their age is 65 or over
2. They are an adult if they are not a senior and their age is 18 or over
3. They are a child if they are not a senior or an adult, and their age must be 17 or under

### Events to Occur based on a Condition Being `true`

Possible Event #1  -> Their age is 65 or over; therefore, we output `price of $12.00`

Possible Event #2 -> Their age 18 to 64 inclusively; therefore, we output `price of $15.50`

Possible Event #3  -> Their age is 17 and under; therefore, we output `price of $10.00`

## How do we do this in Programming?

Conditions are created with `if statements`.

We compare values with `comparison operators`

We can combine multiple situations with `logical operators`

Both `comparison` and `logical operators` result to `Boolean values` (`true` or `false`) which forces the if statements to trigger their event code only if their related conditions are `true`.
