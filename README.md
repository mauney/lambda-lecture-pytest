
# Lambda Lecture (Pytest)

Exercises in automated testing in Python, for students at the Lambda School!

## Setup

Fork [this repo](_______) under your own control. Then download or clone it onto your local machine, and navigate into its root directory from the command-line:

```sh
cd lambda-lecture-pytest/
```

Create and activate a virtual environment (if you like that kind of thing):

```sh
conda create -n game-env python=3.7 # first time only
conda activate game-env
```

From within the virtual environment (if you're using one), install the "pytest" package:

```sh
pip install pytest
```

OK, after installing "pytest" you're ready to proceed with the exercises!

<hr>

## Game Exercise

For this first exercise, we'll be playing a simple game!

In the file called "app/game.py" there is an unfinished game of rock-paper-scissors. Play it:

```sh
python app/game.py
```

After playing the game one or more times, you'll realize it erroneously always results in a tie. Hey, that's not right! **Your objective is to fix the bug in the game's logic so it can properly determine the real winner**.

Before you move on to tackling this objective, take a minute to observe the contents of the test file called "test/game_test.py", and run it:

```sh
pytest test/game_test.py
```

You'll see an "AssertionError", which means the test is failing. **Your second objective is to make the tests pass, and expand the number of scenarios tested.**

Instructions:

  1. Uncomment the "TODO" on line 42, and replace it with: `winning_choice = determine_winner(user_choice, computer_choice)`.
  2. Incrementally update the logic inside the `determine_winner()` function, and manually test the game after each iteration by playing it to ensure it is working properly.
  3. As you are iteratively developing, notice what manual testing actions you are taking and find opportunities to automate those activities by iteratively running the game test file and revising / expanding its contents as necessary.









<hr>

## Data Exercise

For this exercise, we're going to issue an HTTP request to a stock market data API, and attempt to determine what the latest closing price is for the given stock symbol. To issue the requests, we'll be using a few packages, so install them now:

```sh
pip install requests python-dotenv
```

Run the parser script to see it issue the request and print the response data and the latest closing price:

```sh
python app/parser.py
```

After running the script one or more times, you'll realize it erroneously calculates the closing price. Hey, that's not right! **Your objective is to fix the bug in the game's logic so it can properly calculate the latest closing price**.

Before you move on to tackling this objective, take a minute to observe the contents of the test file called "test/parser_test.py", and run it:

```sh
pytest test/parser_test.py
```

You'll see one test is passing, but the other is failing. NOTE: There is no need to update the contents of the parser test file, because when you are finished tackling your objective, all tests should pass.

Instructions:

  1. Incrementally update the logic inside the `latest_closing_price()` function and re-run the parser test file until all its tests pass.
  2. After the tests are passing, try running the parser script again, and observe it should work with live data.
  3. Observe that you have developed the logic of the `latest_closing_price()` without issuing unnecessary HTTP requests!




<hr>

## [License](/LICENSE.md)
