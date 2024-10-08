# Day21 - 👉 Day 21 Challenge


<a href="https://www.youtube.com/watch?v=rfK_QXsf2PA" target="_blank">Dāvida video</a>

Test your family and friends on their multiplication knowledge (or just be really mean to people you know and ask them to work out their multiplication tables for 5,474,000,000....)

1. Prompt the user by asking for a multiplication table for the number of their choice.
2. Generate the multiplication table for 1 to 10 times that number and ask each math fact as a question (psst...that's a hint).
3. If the user gets the math correct, award them a point. If they get it wrong, do not give them any points.
4. At the end of the 10 rounds, show the user their score out of 10 for how many math facts they got correct.
5. Why not give users an emoji if they get all 10 math facts correct?

```python
Math Game!
Name your multiples: 7
1 X 7 = 7
Great work! 
2 X 7 = 14
Awesome!
3 X 7 = 54
Nope. The answer was 21. 
---
You scored 3 out of 10.
```

<details>
<summary>💡 Hint</summary>

- Use a variable when asking the user what multiplication facts they want to solve.
- Within the `for` loop, set up a variable, input statement, and `if` statements.
- Don't forget to include your counter and an `if` statement to say when to give a perfect score emoji.

</details>

## Solution (No Peeking!)


<details>
<summary>👀 Answer</summary>

```python
print("Welcome to Math Facts Game")
print()
print("How well do you know your math facts? Pick a number and I will give you 10 math facts to solve.")
print()

fact_family = int(input("Name your multiples: "))
print()

counter = 0
for i in range(1, 11):
  correct_answer = i*fact_family
  print(i, "x", fact_family)
  answer = int(input("> "))
  if answer == correct_answer:
    print("You got it right!")
    counter += 1
  else:
    print("That's not correct. It should have been", correct_answer)

if counter == 10:
  print("Wow! A perfect score! 🥳")
else:
  print("You got", counter, "out of 10 correct.")
```

</details>