# CodingDojo Challenge: Ninja Gold
## Goal: Create a simple game and implement the functionality below.

## Instructions:
Clone the git repository and do the following:
1. `cd` to the directory, e.g. `cd /<path>/<to>/ninja_gold`
2. Create a virtual environment (venv): `python3 -m venv venv`
3. Before coding / running any commands, start the venv: `. venv/bin/activate`
4. Within the venv, install Flask: `pip install Flask`
5. Run the app: `python app.py`

## Description:
For this assignment, you're going to create a mini-game that helps a ninja make some money! When you start the game, your ninja should have 0 gold. The ninja can go to different places (farm, cave, house, casino) and earn different amounts of gold. In the case of a casino, your ninja can earn or LOSE up to 50 golds. Your job is to create a web app that allows this ninja to earn gold and to display past activities of this ninja.

## Guidelines:
Refer to the provided wireframe; you will have the four forms appear when the user goes to **http://localhost:5000**, such as the following:

```
<form action="/process_money" method="post">
  <input type="hidden" name="building" value="farm" />
  <input type="submit" value="Find Gold!"/>
</form>
```

In other words, you want to include a hidden value in the form and have each form submit the form information to /process_money. Have /process_money determine how much gold the user should have. You should only have 2 routes -- '/' and '/process_money' (reset can be another route if you implement this feature).

## Miscellaneous:
- When you visit, "localhost:5000/" you are seeing the page we described above (in other words, we don't want to have to go to "/gold/index" or other URL to see this app).
- The forms are sent to "/process_money" and not any other URL.
- The activities are stored in the session. No need to store anything in the database.