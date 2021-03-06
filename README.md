# BORED GAMES
=============

## OUR SOLUTION FOR YOUR BOREDOM!!
----------------------------------


<img width="1440" alt="Main Menu" src="https://user-images.githubusercontent.com/74437516/108554298-1f9b9580-72b1-11eb-80a5-982795f62c10.png">



**_**BORED GAMES** WILL HELP YOU:_**

1. FIND THE PERFECT GAME TO BUST THE BOREDOM WITH OUR QUIZ.  
2. KEEP A CATALOGUE OF ALL YOUR FAVORITES.  
3. MATCH YOU TO A RANDOM GAME...and more!  

 ### Table of contents
* General Info  
* Intro Video  
* Technologies
* Setup
* Code Examples
* Features
* To-Dos
* What Inspired Us
* Created By
* Shout Outs!

Bored Games is a CLI application that allows users to create a profile,  
discover games that match their preferences, and gives users the ability  
to save their favorite games. Take the Find Your Best Board Bud quiz  
and start your favorites list today!!!

**_Intro Video_**

To see [Bored Games in action](https://asciinema.org/a/trilahU71tqDnIIzJUpBbWot1)

**_Technologies_**

* Ruby - version 2.6.1
* ActiveRecord - version 5.2
* Sinatra - version 2.0
* Sinatra-activerecord - version 2.0
* SQLite3 - version 1.4
* TTY Prompt

**Setup**

To run this project, install it locally by cloning the GitHub repository and typing:


* *bundle install*
* *rake db:migrate && rake db:seed*
* *ruby runner.rb*


**_Code Examples_**

```
def sign_in 

        user_input = prompt.ask "What is your username?"
        found_user = User.find_by(username: user_input)
        if found_user
            @user = found_user 
            main_menu
        else
            puts "So Sorry Bud, that username doesn't exist. Let's sign you up!"
            sign_up
        end
    end
```
```
def find_all_favorites
        all_faves = Usergame.all.filter do |user_fav|
            user_fav.user == @user
        end
        named_faves = all_faves.map do |favorite|
            favorite.boardgame.name
        end
   end
```

**_Features_**

* Game compatability quiz.
* Game randomizer.
* View and edit catalogue.


<img width="1440" alt="BG3" src="https://user-images.githubusercontent.com/74437516/108554964-0fd08100-72b2-11eb-8333-5bfad0f5b6b1.png">

<img width="1440" alt="BG2" src="https://user-images.githubusercontent.com/74437516/108555061-355d8a80-72b2-11eb-8ba2-5901f9d89eb0.png">

**_To-do list:_**

* Refactor 
* Make code more abstract

**_To-do list:_**

* Refactor Refactor Refactor.
* Make code more abstract.


**_WHAT INSPIRED US_**

Boredom can be a real **kick in kiester**.
We love board games and the way they can be a real **boredom buster**.  
In search of a way to match a game to our needs as well as keep  
track of games we love or want to learn more about, we came up with  
the concept of **Bored Games**

**_CREATED BY_**

**ADAM KNOWLAND** - Strong with the logic force, he is.  
**MELL BASHAM** - The littlest ewok with a heart of gold.

**_SHOUT OUTS!_**

**SYDNEY G., SAM, AND ARIELLE** - FOR HELP WITH AUDIO  
**THE COACHES** - FOR SHOWING US HOW TO **RESPONSIBLY** USE THE FORCE

