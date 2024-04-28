# Domain and ORM, authorizations

## Skills

- Domain and ORM 
  - Implementation of a complex domain model (DSLearn project) 
  - Seeding of a domain model with SQL 
- Authorizations
  - Custom service-level authorization 
  - Customized content for the logged-in user 
  - Refresh token 
  - Pre-authorization of methods

## TDD task

Implement the necessary features for the project tests to pass: https://github.com/devsuperior/bds05

### MovieFlix project overview

The MovieFlix system consists of a bank of movies, which can be listed and rated by users. Users can be both visitors (VISITOR) and members (MEMBER). Only member users can enter reviews into the system.

When accessing the system, the user must log in. Only logged-in users can browse the movies. Right after logging in, the user goes to the movie listing, which shows the movies in a paginated way, sorted alphabetically by title. The user can filter the movies by genre.

When selecting a movie from the listing, a details page is shown, where you can see all the information about the movie, as well as its ratings. If the user is a MEMBER, they can still register a review on this page.

A user has a name, email, and password, and the email is their username. Each film has a title, subtitle, an image, year of release, synopsis, and a genre. Member users can register reviews for the movies. The same member user can leave more than one review for the same movie.

### Conceptual model

![Figma](https://github.com/SofiaMFonseca/assets/blob/main/bds05/conceptual-model-bds05.png)

### What should I do to solve the task?

Basically, you must complete three steps:

- Implement the proposed conceptual model, with database seed. 
- Include the infrastructure of exceptions, validation, and security to the project. 
- Implement the endpoint shown below.

Endpoint that must be done:

-	Get the logged in user's profile: GET /users/profile
