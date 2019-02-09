
## Project ##

Web app similar to the Airbnb one, based on the following user stories.<br/>

```
As a user
So that I can list properties
I need to be able to sign up
```
```
As a user
So I can access my account
I need to be able to sign in
```
```
As a user
So I can leave my account
I need to be able to sign out
```
```
As a user
So that I can have guests
I need to be able to list a new space
```
```
As a user
So I can have guests at multiple locations
I need to be able to list multiple spaces
```
```
As a user
So I can describe the space and price to my guests
I need to be able to put title, describe space and give £ per night
```
```
As a user
So guests know when they can stay
I need to be able to display a range of dates where the space is available
```
```
As a user
So that I can stay at a property
I need to be able to book
```
### To develop in the future

```
As a user
So that I can stay at a property
I need to be able to be approved by the owner
```
```
As a user
So that I can vet my guests
I want to have the option of approving or denying user requests to stay
```
```
As a user
So that I don’t double-book guests
I want to be able to block that date from being booked
```
```
As a user
So that I can keep the space open until it’s been booked
I want to be have the space open for booking until the guest approves
```

## Our approach ##

As we worked on this project, we made sure to follow the below:
1. [XP values](#xp-values) to guide your behaviour
2. The full [developer workflow](#development-workflow) (Creating issues, branching, reviewing, squirrelling, merging.
3. Keeping code quality and test coverage using *Rspec*, *Capybara*, *simpleCov*, *Rubocop*
4. Agile processes (diagram the process, morning stand up, afternoon retros, used Waffle to keep track of what each of us where working on and what tasks were still pending)

![Waffle board](https://github.com/AlinaGoaga/MakersBNB/blob/master/MakersBNB_waffle.jpeg)

We built our CRC Model based on the user story as following.<br/>

![CRC model](https://user-images.githubusercontent.com/43742795/51039457-44d75900-15ad-11e9-8328-28f7f9f5d4d1.png)

Due to the short time we had to build the app, we decided to prioritise our Minimum Viable Product by building our MVP as following :<br/>

1. User is able to sign_up
2. User is able to sign_out
3. User is able to sign_in
4. User is able to choose on their profile if they wish to list or book a property
5. In the case of list, the user is redirected onto the list page and is able to fill a form about the property they wish to list.
6. User is able to add the date of the availability for this property
7. User can see on their profile the list of properties that they have listed
8. In the case of book, user is redirected onto a book page, where they are able to enter the dates they wish to book a property
9. User clicks on search and a list of the available properties matching their dates is displayed
10. User is able to click on a property to book it and is redirected on a page where they can see a message letting them know that the owner will have to approve their booking.

The project has been built from this ![mockup](https://user-images.githubusercontent.com/43742795/51042620-a4853280-15b4-11e9-98e3-cc1a6ed273b5.png).

## How to use ##

### Set up ###

1. Clone the repo
```shell
$ git clone https://github.com/your-username/your-repositary.git
```

2. Cd into the *madcoders_makersbnb* directory :
```shell
$ cd madcoders_makersbnb
```
3. To install all the *gems* contained in the *Gemfile*, run *Bundle* :
```shell
$ bundle
```

### Database ###

1. If you do not have it already, install *psql* on your local machine. Connect to your database and the create the development and testing databases:
```shell
$ psql
admin= CREATE DATABASE makers_bnb_development;
admin= CREATE DATABASE makers_bnb_test;
```

2. Exit from psql and from the command line run the below instruction to create the tables:
```shell
$ rake db:auto_migrate
$ rake db:auto_migrate RACK_ENV=test
```

3. Connect to psql, you can connect to any of the databases by using the `\c databasename;` command.
Once you are connected to the database, you can list the tables using the `\dt` command.
```shell
$ psql
admin= \c makers_bnb_development;
makers_bnb_development= \dt
```
4. You can connect to a specific table by using the `SELECT * FROM tablename;`
```shell
makers_bnb_development= SELECT * FROM tablename;
```

### Run the tests ###

1. To run the tests:
```shell
$ cd madcoders_makersbnb
$ rspec
```

To check only one file at a time :
```shell
$ cd madcoders_makersbnb
$ rspec spec/file_name_spec.rb
```

2. Run rubocop to check the quality of the code:
```shell
$ cd madcoders_makersbnb
$ rubocop
```

## Run the app ##

On the command line, from the root directory *madcoders_makersbnb*, use the `rackup` command :
```shell
$ cd madcoders_makersbnb
$ rackup
```

## Authors ##

[Alina Goaga](https://github.com/AlinaGoaga)
[João Abbott-Gribben](https://github.com/joaoag)
[Celine Kaslin](https://github.com/CelineKaslin)

## Acknowledgements ##

Code from sign_in_sign up web app from [Edward Withers](https://github.com/dearshrewdwit) (this has been adjusted to fit the project's needs)
