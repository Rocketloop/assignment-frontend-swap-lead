# Assignment - Front-End Lead (Angular)

The subject of this assignment is a small Angular application that acts as an interactive explorer for the characters from the movie franchise Star Wars.  If you are not familiar with Star Wars, don't worry, prior knowledge of the movies is not required to complete the assignment. The assignment is divided into two tasks that focus on your technical and project management skills respectively.

## Application Requirements

The main view of the application should display the list of characters with a filter section, that the user can use to filter the characters by certain criteria. Clicking on one of the characters from the list should open a detail view of the corresponding character. When the user changes the filter settings in the filter section, the list of characters should instantly adapt to only show characters that match the chosen filter settings. The data for the application should be queried from an open API called [SWAPI (Star Wars API)](https://swapi.co/) that should give access to all data that is needed to fullfill the requirements.

### Character List
The character list should be a simple list that displays the name of the character. Each list entry should be clickable and open the detail view for the selected character when the user clicks the list entry.

### Filter
The filter section should allow the user to filter the list of characters according to the following filter settings:

* The movie the character appeared in (i.e. show only characters that appeared in Episode IV: A New Hope)
* The character's species (i.e. show only characters that are human)
* A range of years that the character's birth year falls in (i.e. show only characters born between 30 BBY and 5 ABY, see API documentation for field `birth_year` at https://swapi.co/documentation#people)

All filter settings should be treated using an AND relationship, i.e. if the user chooses to filter by movie and species, only characters that appear in the given movie AND are of the specified species should be displayed.

### Character Details
The character details that are shown when the user selects a character from the character list should show a brief summary of the character, including the name of the character, the movie the character appeared in, the species of the character, and the spaceships associated with the character. For the character "Han Solo", for instance, the detail view should display the following information:

> **Name:** Han Solo  
> **Species:** Human  
> **Movies:** Episode IV, Episode V, Episode VI, Episode VII  
> **Spaceships:** Millenium Falcon, Imperial shuttle  

## Technical Task (2-4h)

For the technical task, you will need to create an Angular application that satisfies the requirements given in the previous section. 

### Project Setup
Please use the Angular CLI to set up the application. We should be able to start the application using the `npm start` command. The app should use the latest version of Angular (8.1 at the time of writing).

### SWAPI
The [Star Wars API](https://swapi.co/) should be used to complete this assignment. The most important endpoint will be the `/people` endpoint to query the characters to display in the character list (see https://swapi.co/documentation#people). As the SWAPI does not support filtering the data, it will be necessary to fetch all data and filter on the client side. Make sure not to send unneccessary API requests.

### External Libraries
You are allowed to use any external library to complete this task. You are also allowed to use UI libraries like Bootstrap or Angular Material. Please make sure that the application looks decent and consistent.

## Project Management Task (1-2h)

For the project management task, you will need to turn a high-level description of a new feature into technical requirements that can be given to a developer for implementation. This task tries to simulate a real-world change request by a customer.

### Change Request

> We have received feedback from our users that the list of characters is too long and it is hard to find the character that they are looking for. To make it easier to find a specific character, we want to add a search function to our app, so that the user can directly type in the name of the character they are looking for. The search field should be displayed somewhere prominently and should behave like a usual search field. We also need a page that shows the search results. Also, we should automatically show suggestions when the user types into the search field. If the user clicks a suggestion, it would be best, if we can directly link to the character page.

### Ticket Format

The requirements should be divided into Jira tickets that can be assigned to individual developers.

Please use the following format for the tickets:

> **Title:** Title of the ticket  
> **Description:** Description of the ticket
