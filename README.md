# BORIS BIKES by Max and Jack | Makers Week 1

Create a program that creates a network of docking stations and bikes that anyone can do.

## Build Status

This program is a fork of crotcheycrows repo where challenges 1 through 9 (almost) were completed.

This fork will be used to progress the project beyond challenge 9 for the rest of the Wednesday.

## CHALLENGES COMPLETED
1. Setting up a project
- [x] Create a directory from the command line
- [x] Initialise a git repository within that directory
- [x] Create a README.md file from the command line
- [x] Write a clear README
- [x] Add the README.md to the staging area
- [x] Commit your changes with a clear message
- [x] Push the project to Github.

DONE#

2. From user stories to a domain model
- [x] Write down all the nouns in the User Stories
- [x] Write down all the verbs in the User Stories
- [x] Draw a table like the one above
- [x] Organise the nouns and verbs into Objects and Messages within the table
- [x]  Draw a diagram that shows how your Objects will use Messages to communicate with one another

DONE#

3. From a Domain Model to a Feature Test
- [x] Start irb (or any other REPL) from the Command Line
- [x] Set a variable docking_station equal to a new DockingStation object
- [x] Explain to your pair partner what the resulting error means.
  - error message essentially said that the constant did not exist and could not be found in the ruby language, the irb or any gems.

DONE#

4. Errors are good
- [x] Write down the type of error
  - uninitalized constant
- [x] Write down the file path where the error happened
  - /Users/jackmccarthy/.rvm/rubies/ruby-2.7.2/bin/irb:23:in <main>
- [x] Write down the line number of the error
  - Line 1 (in IRB)
- [x] Use the Ruby Documentation to find out what the error means
  - the Constant has not been defined
- [x] Suggest one way of solving the error.
  - Create a constant !

DONE#

5. From Feature Test to unit Test
- [x] Initialise RSpec within your project
- [x] Create a new spec file for your DockingStation object
- [x] Set up the spec file to describe a DockingStation
- [x] Run RSpec from the Command Line
- [x] Explain to your pair partner the difference between this error and the error you saw before.
  - No method created to release the bike

DONE#

6. Passing your first Unit Test

- [x] Create a new file for a Docking Station class, inside the /lib directory
- [x] Define a DockingStation class
- [x] Use require to include this file inside your spec file
- [x] Run RSpec from the Command Line
- [x] Explain to your pair partner the difference between what you see, and the error you saw before.

DONE#

7. Back to the feature

- [x] Start irb (or any other REPL) from the Command Line
- [x] Use require to include the file that contains the DockingStation class definition
- [x] Set a variable docking_station equal to a new DockingStation object
- [x] Explain to your pair partner why you do not see an error now, when you did before
- [x] Ask the docking_station instance to release_bike
- [x] Explain to your pair partner what the resulting error means.

DONE#

8. Back to the Unit

- [x] Add a test to your spec file that expects DockingStation instances to respond_to the method release_bike
- [x] Rewrite this test using RSpec's one-liner syntax
- [x] Run RSpec from the Command Line
- [x] Explain the error to your pair partner
    - *no method release_bike, so cannot find it*
- [x] Add a method release_bike to the DockingStation class
- [x] Run RSpec from the Command Line
- [x] Explain to your pair partner the difference between what you see, and the error you saw before.
  - we now have a method so it finds it and can run the test

DONE#

9. Building a bike
- [x] Start irb (or another REPL such as 💊 Pry)
- [x] Instantiate a DockingStation as docking_station
- [x] Ask docking_station to release a bike, and save the response to a variable bike
    - *Max fixed - changed docking station to create a new bike object.*
- [x] Ask the bike if it is working?
- [x] Explain the error to your pair partner
  - *unable to find method .working?, no Bike class*
- [x] Create a new spec file for a Bike class
- [x] Set up the spec file to describe the Bike class
- [x] Run RSpec from the Command Line
- [x] Fix the error you see, similarly to how you fixed the same error for DockingStation
- [x] Add a test to your bike_spec.rb file that expects Bike instances to respond_to the method working?
- [x] Make this test pass.

DONE#

10. Making Docking Stations Release Bikes
- [x]  Feature-test the feature you are building using irb
- [x]  Explain the error to your pair partner
- [x]  Add a test to your DockingStation specification that a) gets a bike, and then b) expects the bike to be working
- [x]  Make this test pass
- [x]  Feature-test the feature again.

DONE#

11.  Using Instance Variables

- [x] Write a feature test for docking a bike at a docking station
- [x] Write a unit test for the method you need to
  add to DockingStation to make docking possible
  - *When unit test run, .doc_bike return the bike id to us*
- [x] Pass both tests
- [x] Use an instance variable with attr_reader to do
  a full test-implementation cycle for the second User Story above
    - *added tests which docked a bike, checked bike was included in the bikes array, and inspected the bikes array*

As a member of the public
So I can return bikes I've hired
I want to dock my bike at the docking station

objects ------- messages

user            
bike             is_returned?
dockings station docks.bike

As a member of the public
So I can decide whether to use the docking station
I want to see a bike that has been docked

objects -------- messages

user
docking station  List.bikes
docking_station.List specific_bike

DONE#

12. Raising Exceptions

- [x] Feature test the feature you are building using irb
- [x] Use {} and raise_error syntax in your RSpec unit test to
  test exception raising
- [x] Use the fail or raise keyword to raise an exception in your
  code (not your tests)
- [x] Make the test pass by raising an exception
- [x] Explain why you use curly braces in the RSpec error handling
  syntax to your partner
- [x] Feature-test the feature again.

As a member of the public,
So that I am not confused and charged unnecessarily,
I'd like docking stations not to release bikes when there are none available.

Object ------------------ Message

User
docking_station.bike       true?     OR     false
docking)station            release_bike?    error

DONE#

13. Limiting Capacity

- [ ] Deliver the feature above in a Test-Driven manner

As a maintainer of the system,
So that I can control the distribution of bikes,
I'd like docking stations not to accept more bikes than their capacity.

objects ---------------- Message
Maintainer
docking_station.bike == 1
docking_station.dock_bike fail

Write RSpec tests that expect errors
Use fail or raise to raise an error
Use a 'guard condition'
