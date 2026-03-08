## The 4 reusable for loop patterns

## These are the ones you should memorize.

    1. Print pattern
    for item in group:
     print(item)

Use when you just want to see each value.

    2. Count pattern
    count = 0

    for item in group:
        if condition:
            count += 1

## Use when you want:
how many
count of values
number of matches

    3. Sum pattern
    total = 0

    for item in group:
        total += item

## Use when you want:
total
average
running sum

    4. Filter pattern
    result = []

    for item in group:
        if condition:
            result.append(item)

## Use when you want:
keep only some items
build a new list
clean data
One master template for many applications

## This is the best general template:

    group = [...]
    result = []

    for item in group:
        if condition:
            result.append(item)

    print(result)

## And this one for counting:

    group = [...]
    count = 0

    for item in group:
        if condition:
            count += 1

    print(count)

## And this one for summing:

        group = [...]
        total = 0

        for item in group:
            total += item

        print(total)
        How to write a for loop from scratch every time

## Use this exact thinking process.

Case A: I want to print each item

    1- Write the data
    2- Write for
    3- Choose a temporary item name
    4- Write in
    5- Write the group name
    6- Add :
    7- Indent
    8- Write what to do

Example:
    students = ["Ali", "Sara", "John"]
    for student in students:
        print(student)

## Case B: I want to count items

- Write the data
- Make counter = 0
- Start loop
- Check condition
- Increase counter
= Print final counter

Example:

    ages = [15, 22, 18, 30, 12]
    count = 0

    for age in ages:
        if age >= 18:
            count += 1
print(count)

## Case C: I want to make a new list

- Write the data
- Create empty list
- Start loop
- Check condition
- Append matching item
- Print new list

    Example:
    ages = [15, 22, 18, 30, 12]
    adults = []
    for age in ages:
        if age >= 18:
            adults.append(age)
    print(adults)

**Common mistakes**

* Mistake 1: Forgetting colon
Wrong:
for num in numbers
* Correct:

for num in numbers:

* Mistake 2: No indentation
Wrong:
    for num in numbers:
    print(num)

* Correct:

    for num in numbers:
        print(num)

* Mistake 3: Using the list name instead of item name

    Wrong:

    numbers = [1, 2, 3]

    for num in numbers:
        print(numbers)

* This prints the whole list each time.

* Correct:
    for num in numbers:
        print(num)

* Mistake 4: Forgetting to initialize counter or result

    Wrong:
    for num in numbers:
    count += 1

*Correct:

    count = 0
    for num in numbers:
        count += 1
    Practical interview version

**When asked to solve something, first decide which pattern it* is:**

    print?
    count?
    sum?
    filter?

**Then write the matching template.**
Example question:
“Count how many values are above 100.”

You should immediately think:

This is a count pattern.

count = 0

for value in data:
    if value > 100:
        count += 1

print(count)
You can remember it like this:

# 1. prepare
# 2. loop
# 3. condition if needed
# 4. update result
# 5. print final answer

    Example:
    numbers = [5, 12, 8, 20]
    count = 0
    for num in numbers:
        if num > 10:
            count += 1
    print(count)

Your simple mental sentence
Before writing a loop, say this in your head:
“For each item in my data, what do I want to do?”
That sentence will help you in almost every problem.
Practice set for you

| Goal                 | Template                                     |
| -------------------- | -------------------------------------------- |
| Print each item      | `for item in group:`                         |
| Count matches        | `count = 0` + loop + `count += 1`            |
| Sum values           | `total = 0` + loop + `total += item`         |
| Keep matching values | `result = []` + loop + `result.append(item)` |
