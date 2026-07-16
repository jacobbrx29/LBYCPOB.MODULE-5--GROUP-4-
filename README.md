# LBYCPOB Module 5A — Applied OOP & Design

This repository contains the group activities for **LBYCPOB Module 5A: Applied Object-Oriented Programming and Design (Part I: Spring Boot)**. The module focuses on migrating and developing Java applications as web applications using Spring Boot while applying object-oriented design, layered architecture, dependency injection, validation, design patterns, UML modeling, and version control.

## Course Information

- **Course:** LBYCPOB — Object-Oriented Programming Laboratory
- **Section:** E22
- **Module:** Module 5A — Applied OOP & Design
- **Framework:** Spring Boot
- **Laboratory Instructor:** Dr./Engr. Cesar Llorente

## Group Members

- Chase Carmelo B. Capili
- Rone Jacob G. Medina
- Emer Gabriel C. Vales

## Repository Contents

```text
LBYCPOB-Module-5A/
├── grade-tracker-web-app/
├── hangman-web-app/
├── pokemon-card-collection-web-app/
├── socialnet-profile-manager/
├── docs/
│   ├── screenshots/
│   ├── uml-class-diagrams/
│   ├── uml-sequence-diagrams/
│   └── deliverables/
└── README.md
```

> Folder names may be adjusted to match the actual names used in the repository.

## Activities

### 1. Code Reading and Migration: Grade Tracker Web App

The Grade Tracker activity migrates the previous console-based grade tracker into a Spring Boot and Thymeleaf web application.

#### Main Features

- Add student records through a web form
- Validate student names, ID numbers, and grade inputs
- Store and display multiple student records
- Calculate weighted grades and equivalent rankings
- Generate a complete student grade report
- Display class statistics
- Identify the highest and lowest grades
- Compute the class average
- Verify whether a student ID exists
- Use a `StudentFormDTO` to separate form input from the main `Student` model
- Display an About or identification section in the application

#### Main Concepts Applied

- Model–View–Controller architecture
- Data Transfer Object pattern
- Form validation
- Dependency injection
- Service and repository layers
- Separation of concerns
- UML class and sequence diagrams

---

### 2. Hangman Web App

The Hangman activity migrates the previous console-based Hangman game into a browser-based application using Spring Boot and Thymeleaf.

#### Main Features

- Start a new Hangman game
- Select a word from a classpath word-list resource
- Display the hidden word and Hangman drawing
- Accept letter guesses from the player
- Track correct and incorrect guesses
- Detect winning and losing game states
- Store the current game state in the user session
- Record and display game statistics
- Support repeated games
- Display an About or identification section

#### Main Concepts Applied

- MVC and layered architecture
- Session-based state management
- Repository abstraction for word files
- Service layer for game rules
- Classpath resource handling
- Records or value objects for statistics
- Dependency injection
- UML class and sequence diagrams

---

### 3. Pokémon Card Collection Web App

The Pokémon Card Collection activity creates a Spring Boot web application that loads Pokémon information from a CSV resource and displays the data as visual Pokémon cards.

#### Main Features

- Load Pokémon records from `pokemon_list.csv`
- Validate and skip malformed CSV records
- Include at least five Pokémon from different types
- Include at least two dual-type Pokémon
- Search for a Pokémon by name
- Display one random Pokémon
- Display all available Pokémon as a slideshow
- Remove a Pokémon from the current collection
- Display Pokémon sprites and type-based card backgrounds
- Show Pokémon attributes such as:
  - Name
  - Type
  - Weight
  - Height
  - Attack
  - Defense
  - Stamina
  - Computed power level
- Display an About or identification section

#### Main Concepts Applied

- Abstraction through `AbstractPokemon`
- Interface implementation through `PokemonOperations`
- Polymorphism
- Factory pattern through `PokemonFactory`
- Service layer and controller separation
- CSV file processing
- Defensive programming and input validation
- UML class diagrams

---

### 4. SocialNet Profile Manager App

The SocialNet Profile Manager is a Spring Boot web application for creating, viewing, editing, and managing social-network profiles. It uses Supabase for database persistence and image storage.

#### Main Features

- Add a new profile
- Search or look up an existing profile
- Delete a profile
- Display at least five profiles
- Display a profile's:
  - Name
  - Current status
  - Favorite quote
  - Profile image
  - Friends list
- Change the current status
- Update the favorite quote
- Upload or change the profile picture
- Add a friend
- Remove or unfriend a profile
- Display status messages for completed actions
- Apply error handling and exception handling
- Store profile and friendship data in Supabase PostgreSQL
- Store profile images in Supabase Storage

#### Main Concepts Applied

- Spring Data JPA
- PostgreSQL and Supabase
- CRUD operations
- Entity relationships
- Repository and service patterns
- Transaction management
- Multipart file upload
- Image compression and storage services
- Global error handling
- Environment-variable configuration


## Backup Files and Google Drive Access

Some project files included in this GitHub repository may be incomplete, corrupted, or unable to open properly after being downloaded. A complete backup of the Module 5A files is available through the Google Drive link below:

**Google Drive:**https://drive.google.com/drive/u/2/folders/161LlgvjhtYmhAKad-pWgJtNkAC6_6LAL 

Please use the Google Drive copy whenever the files currently attached to or uploaded in this repository are incomplete, broken, missing resources, or cannot be opened successfully.

### Pokémon Web App File Availability

The complete **Pokémon Card Collection Web App** could not be uploaded directly to GitHub because its total file size exceeds the repository's supported upload limit. Its complete project folder, including the source code, resources, images, and other required files, is available through the Google Drive link provided above.

The Pokémon-related documentation, screenshots, UML diagrams, or selected source files may still be included in this repository when possible.

## Technologies Used

- Java 25
- Spring Boot 4.x
- Maven
- Spring Web MVC
- Thymeleaf
- HTML and CSS
- Spring Data JPA
- Jakarta Validation
- PostgreSQL
- Supabase Database and Storage
- Git and GitHub
- IntelliJ IDEA Ultimate

## Application Architecture

The applications generally follow a layered Spring Boot structure:

```text
src/
├── main/
│   ├── java/
│   │   └── ph/edu/dlsu/lbycpob/
│   │       ├── controller/    # Handles browser requests
│   │       ├── service/       # Contains business logic
│   │       ├── repository/    # Handles data access
│   │       ├── model/         # Domain objects and entities
│   │       ├── dto/           # Form and request data
│   │       ├── exception/     # Error-handling classes
│   │       └── Application.java
│   └── resources/
│       ├── static/            # CSS, JavaScript, and images
│       ├── templates/         # Thymeleaf HTML pages
│       └── application.properties
└── test/
    └── java/
```

Not every activity uses every package. Each project contains only the layers and components required by its features.

## Prerequisites

Install the following before running the projects:

- JDK 25 or later
- IntelliJ IDEA Ultimate
- Maven
- Git
- A modern web browser
- A Supabase account for the SocialNet Profile Manager

## Running an Application

Each activity is a separate Spring Boot project. Open or run only one project at a time because the applications use port `8080` by default.

### Using IntelliJ IDEA

1. Open the selected activity folder in IntelliJ IDEA.
2. Wait for Maven to download and index the dependencies.
3. Locate the class containing `@SpringBootApplication`.
4. Run the application's `main()` method.
5. Open the following address in a browser:

```text
http://localhost:8080/
```

### Using the Terminal

```bash
cd <activity-folder>
mvn spring-boot:run
```

To stop the application, press `Ctrl + C`.

## SocialNet Environment Variables

The SocialNet Profile Manager requires Supabase credentials. Configure the following environment variables before running it:

```text
SUPABASE_DB_URL
SUPABASE_DB_USERNAME
SUPABASE_DB_PASSWORD
SUPABASE_URL
SUPABASE_SECRET_KEY
SUPABASE_AVATAR_BUCKET
```

Do not commit real database passwords, secret keys, or private credentials to GitHub. Use environment variables or a local configuration that is excluded through `.gitignore`.

## Git and Version-Control Practices

The projects were developed using incremental Git commits. The repository follows these practices:

- Use descriptive commit messages
- Commit one manageable feature or change at a time
- Avoid commits containing more than 100 changed lines when possible
- Preserve the complete commit history
- Show each member's contribution through GitHub activity
- Avoid committing generated files, IDE caches, passwords, and secret keys

Example commit messages:

```text
Initialize Grade Tracker Spring Boot project
Add student model and form DTO
Implement grade computation service
Add Grade Tracker report and statistics pages
Implement Hangman game session state
Add Pokemon CSV loader and validation
Implement Pokemon search and random card features
Configure SocialNet profile persistence
Add friendship management and avatar upload
Update documentation and UML diagrams
```

## Documentation and Required Evidence

The repository may include the following supporting files inside the `docs` directory:

- Annotated source code
- Application run screenshots
- Screenshots of all required features
- UML class diagrams
- UML sequence diagrams
- Complete Git commit history
- GitHub contribution screenshots
- Answers to the activity guide questions
- Project file structures
- Final laboratory deliverables summary

## Spring Boot Annotations Used

Examples of annotations applied across the activities include:

- `@SpringBootApplication`
- `@Controller`
- `@GetMapping`
- `@PostMapping`
- `@Service`
- `@Repository`
- `@Entity`
- `@Id`
- `@Valid`
- `@Transactional`
- `@ControllerAdvice`
- `@ExceptionHandler`
- `@PostConstruct`

The exact annotations used depend on the requirements and architecture of each application.

## Learning Outcomes

Through these activities, the group practiced how to:

- Convert console applications into web applications
- Apply object-oriented analysis and design
- Organize code using layered architecture
- Use dependency injection to reduce coupling
- Separate presentation, business logic, and data access
- Validate user input using DTOs
- Apply abstraction, interfaces, and polymorphism
- Use design patterns to improve maintainability
- Read data from resource files
- Persist data through Spring Data JPA
- Connect a Spring Boot application to Supabase
- Create UML class and sequence diagrams
- Collaborate through Git and GitHub

## Academic Use

This repository was created for the LBYCPOB Object-Oriented Programming Laboratory course at De La Salle University. It is intended for academic documentation, demonstration, and submission purposes.
