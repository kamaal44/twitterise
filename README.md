# Twitterise

Two objectives:

1. Have a new and diverse timeline over the time. We always follow people
similar to us, let's start with new ideas of different people. By default
Twitterise follows new 4 people during 5 days.

2. Increase the number of followers is a by product but following people maybe
they will follow you back.


## Instalation

    $ git clone git@github.com:arturoherrero/twitterise.git
    $ bundle install

You need to create a new [Twitter App][1] to work with the Twitter API. Also
it's necessary to create a `.env` file with the environment variables needed by
the Twitter client.

    TWITTER_CONSUMER_KEY="YOUR_CONSUMER_KEY"
    TWITTER_CONSUMER_SECRET="YOUR_CONSUMER_SECRET"
    TWITTER_ACCESS_TOKEN="YOUR_ACCESS_TOKEN"
    TWITTER_ACCESS_SECRET="YOUR_ACCESS_SECRET"


## Usage

Setup the database. Using SQLite all the information is self-contained in the
Twitterise directory.

    $ bin/setup

Run Twitterise.

    $ bin/twitterise

In order to automate the use of Twitterise is a good idea to run once per day.
To achieve this, insert a new line in crontab.

    $ crontab -e

    0 10 * * * bin/twitterise


[1]: https://apps.twitter.com/