# Solutions
--still broken.

## Bug 1: Pizzas aren't being displayed after creation

0. Asking Questions
What is expected: we expect after submission to be returned to the home page where it will great us with our pizza order rather than "No pizza orders to show!"

What is happening: We are greeted with a server error 500, indicating server overload, or an error in the application. In the terminal we get

I assume Part of the issue is looking at how  Enum works. All that enum is currently returning are class keys and not values. such as 
<enum 'PizzaSize'>
<enum 'CrustType'>
<enum 'ToppingType'>
and not
"Large"
"Thin"
"Pineapple"

1. Reading Code
While reading the code a set of get strings matched the names of variables. However size was missing an s to match it's variable so I added an s.
size to sizes on line 69

I also saw that we were appending all enumerated values from toppings were being added to PizzaToppings. Which doesn't make since if the user only  wants soy cheese on their pizza, so we check against the submitted items and the enumerated.
if statement on line 80

2. Research
Apparently I've never written a flask post get method before. I couldn't find anything in past code so my next steps should be to read more to improve my understanding of the code to better debug it.
