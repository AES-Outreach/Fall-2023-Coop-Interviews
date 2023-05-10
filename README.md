<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/AES-Outreach/Fall-2023-Coop-Interviews">
    <img src="outstem_logo_icon.svg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">OutStem Fall 2023 Coding Challenge</h3>

  <p align="center">
    Welcome to the OutStem coding interview.
  </p>
</p>

# OutStem Front-end Challenge

Welcome to the OutStem front-end challenge. Submission instructions are listed below. The deadline to submit this challenge is **Tuesday May 23rd, 9:00 AM**. We would like to emphasize that we are looking for effort, and that the challenge is just part of our discussion with you during the interview, so don’t worry if your solution is *hacky* or even if it doesn’t work, we want to see it!

## The Challenge

The challenge is to build a fun card game app, where users will be given cards from a [standard deck of playing cards](https://en.wikipedia.org/wiki/Standard_52-card_deck), and make guesses about the next card that will be drawn. 

The design and layout of the website is totally up to you, though you will be judged on the look, feel, and usability of your application, so do your best to respect best practices in web design.

For this challenge, we will be using the [Deck of Cards API](https://www.deckofcardsapi.com/), which creates a deck of cards for you, gives you a `deck_id`, and keeps track of which cards are left as you draw cards.

## Goals

*The styling for this challenge is up to you, feel free to use any UI libraries*

This challenge has multiple goals that increase in level of difficulty, implement as many of these goals as you are able to.

### Goal 1
Fetch a new deck of cards from the API, and print the response to the console

URL: `https://www.deckofcardsapi.com/api/deck/new/`

Example Response:
```json
{
    "success": true,
    "deck_id": "3p40paa87x90",
    "shuffled": false,
    "remaining": 52
}
```


### Goal 2

Ask the user if the next card will be Red or Black. You can use any input element for this, ex input, buttons, dropdown

Once they input their answer, draw a card from your deck using the API:

URL: `https://www.deckofcardsapi.com/api/deck/<<deck_id>>/draw/?count=1`

Example Response:
```json
{
    "success": true, 
    "deck_id": "kxozasf3edqu", 
    "cards": [
        {
            "code": "5S", 
            "image": "https://deckofcardsapi.com/static/img/5S.png", 
            "images": {
                          "svg": "https://deckofcardsapi.com/static/img/5S.svg", 
                          "png": "https://deckofcardsapi.com/static/img/5S.png"
                      }, 
            "value": "5", 
            "suit": "SPADES"
        }
    ], 
    "remaining": 50
}

```

### Goal 3

Once a rating has been submitted, load a new dog image and reset your form elements.

### Goal 4

Add a section to your app where you can review the history of your dog ratings with both the picture and rating.

Note: this does not require a database, you can use a simple client side cache that only needs to persist until the page is refreshed.

### Goal 5

Add sorting to your ratings history by highest rated and lowest rated.

### Goal 6

Add an option to filter the random dogs being provided by breed, using the list of dog breeds in the [provided file](dog-breeds.txt).

Use the [random by breed](https://dog.ceo/dog-api/documentation/breed) endpoint of the API for this.

`https://dog.ceo/api/breed/${BREED_HERE}/images/random`

## Your solution

Here are the requirements for your solution.

1. You can complete this challenge using any front end framework of your choice, however, we prefer to see you do this challenge in JavaScript/TypeScript and Angular.
2. Your solution submission should indicate which goals you've achieved
4. You must submit your solution in a GitHub repository or a Repl.it. **Please make sure your project/repository is public and accessible by us.**

## Evaluation 

You will be evaluated on:
- Completeness: did you complete the features?
- Correctness: does the functionality act in sensible, thought-out ways?
- Maintainability: is it written in a clean, maintainable way?
- Best Practices: does your solution use Javascript/TypeScript's and your chosen framework's best practices
- User Friendly UI: does your solution anticipate what users might need to do and have elements that are easy to access?

## Submission

Please submit your solution in the 2023 Fall interview GitHub repository via GitHub Issue.

1. Navigate to the following link (https://github.com/AES-Outreach/Fall-2023-Coop-Interviews/issues/new/choose) or:
   1. Navigate to the challenge repository
   2. Click **Issues**
   3. Click **New Issue**
2. Click **Get Started** for Solution Submission
3. Change `YOUR_NAME` to your full name in the title field
4. Fill out the form
5. Click **Submit New Issue**
6. Done! Thank you for completing the challenge, we look forward to discussing your solution with you during the interview. 🎉

If you have any questions, you can email Ivana Erlich at ierlich@uottawa.ca


## Bonus Challenges

- Make your UI responsive, that is usable on all screen sizes
- Implement any other features provided by the API

