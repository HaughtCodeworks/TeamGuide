# The README Process

The README is a key piece of how we can work on many projects as a team and minimize the cost of onboarding and project switching. We know when we come onboard a new project that a strong README will be there to get us up and running as fast as possible. It is also helpful for external client developers who will inherit a project when we're finished with it. A well thought out README creates trust on the team that others have already paved the way and can identify all dependencies and requirements for a project to run.  This is especially important when you have a complex project with many externals components such as ElasticSearch and background worker processes.

The README includes everything you need to do to get an app up and running on your local environment. Our README process saves us time and makes sure we don’t forget any important steps. Our first step in starting a README is to delete all the boilerplate contents that the Rails generator puts in there. We use Markdown in our READMEs for good formatting on GitHub and Bitbucket. We start off with the project’s name at top, even though it’s implied by its placement at the root of your Rails app. Next, we put requirements for the app. Usually this is the version of Ruby, any required databases and other special services/libs that you may not have installed on your system. We don’t list gem dependencies in this area since Bundler handles that. The meat of the README will be the steps to get the app up and running. This includes steps like configuring your database.yml, copying and adjusting any special config, running bundle and any steps to seed or bootstrap your environment with necessary data. These are typically written out as shell commands so someone could copy and paste it into their prompt. Next, we like to include information on deploying the app along with basic data on where that is. This piece isn’t as necessary but we find it convenient. This is especially true when you have many different apps and some may be on Heroku while others are on other servers that may use Capistrano for deployment. If there are common tasks that we do, we call them out here. Perhaps you have some external service you infrequently pull down data from. Finally, if there are any special notes or tips that we want the team to know about this app, they go at the end.

We want our READMEs to be a clear step-by-step guide. Shell scripts that do too much for us can tend to fail since everyone's environment is different. When we are following setup instructions a step at a time, each developer knows what goes into setting up the project, and we have a better understanding of what happened if something goes wrong, rather than having one magical command run the setup for us. Developers new to the project update the README as they set up their machine if they find that the README is unclear or out of date. If anything is stale or inaccurate, they update it. If something isn’t clear or they have questions on it, we look to see if something needs to be clarified or not. If there is room for improvement, they make it better as they go. This process also helps flush out any implicit steps that needs to be defined. Though it takes some extra time for the README to be written and kept up to date, we truly believe it’s worth every minute spent on it.

---

## An Example README Template

# App Title

Brief app description

## Dev environment set-up

* Required installations
* Cloning the repo
* Installing dependencies
* Server instructions

## Developing new features

### Code Generators

### Running Tests

* Commands for running tests

### Building

* Any commands go here

### Deploying

Specify what it takes to deploy your app.

## Further Reading / Useful Links

----

## An Example README

# Solar Wind Load Calculator

This is the solar panel wind load calculation project.

## Developer set-up

Requires ruby 2.1 and postgresql 8.2 or higher.

    $ git clone git@github.com:CPPWind/solar_load_calc.git
    $ cd solar_load_calc
    $ bundle
    $ cp config/database_example.yml config/database.yml

Edit the development and test sections of config/database.yml to
reflect your preferred database, username, and password settings. Make
sure the database user has superuser permissions (or at least
drop/create) on the dev/test databases. This file is specific to the
local dev/test environment, so it is git ignored and should not be
checked in.

On Ubuntu, here's how you create a user called 'cpp' with password
'cpp'.

    $ sudo su postgres -c psql
    postgres=# CREATE ROLE cpp SUPERUSER LOGIN PASSWORD 'cpp';


## Database creation and initialization

This will create the dev database, load its schema, and run any seed
scripts. (The 'bundle exec' prefix may not be necessary in your
set-up, but it doesn't hurt to use it.)

    $ bundle exec rake db:setup

To drop the db and set it up again, use db:reset.

    $ bundle exec rake db:reset


## How to run the test suite

    $ bundle exec rake


## How to start a local dev server on port 3000

    $ bundle exec rails s


## How to start an interactive dev console

    $ bundle exec rails c


## Deployment instructions

TBD