
# GitHub-OAuth-Application

This project is an Express application that uses [Passport](http://www.passportjs.org/) for authentication. It is configured to use the GitHub OAuth strategy, and can be used as a starting point for any Express project that requires authentication. 

## Installation

To install GitHub-OAuth-Application, clone the repository and run `npm install` in the root directory. 

### Variable Declarations

The following variables are declared in this project: 

 - `PORT`: The port number on which the server will listen (defaults to 3000).  
 - `GITHUB_CLIENT_ID`: The client ID of your GitHub app (loaded from `processs/.env`).  
 - `GITHUB_CLIENT_SECRET`: The client secret of your GitHub app (loaded from `processs/.env`). 

_Note: Instructions to generate GitHub client secret can be found [here](../starting_code/Set-Client-Secret.md)._ 


## Run 

Before running the project, create `.env` file and save your GitHub client ID and GitHub client Secret. 
  
To start the server, run `npm start`. To start the development server, run `npm dev`. 

### Dependencies 
* dotenv: ^10.0.0 
* ejs: ^3.1.6 
* express: ^4.17.1 
* express-partials: ^0.3.0 
* express-session: ^1.17.2 
* passport: ^0.4.1 
* passport-github2: ^0.1.12


### Package Imports

The following packages are imported and used in this project: 
- [Path](https://nodejs.org/api/path.html) - Used to work with file and directory paths 
- [Dotenv](https://www.npmjs.com/package/dotenv) - Used to load environment variables from a `.env` file 
- [Express](https://expressjs.com/) - Used to create the server and handle requests 
- [Express Partials](https://www.npmjs.com/package/express-partials) - Used to render partials in views 
- [Express Session](https://www.npmjs.com/package/express-session) - Used to store session data on the server side 
- [Crypto](https://nodejs.org/api/crypto.html) - Used for cryptographic operations 
- [Passport](http://www.passportjs.org/) - Used for authentication  
- [Path](https://nodejs.org/api/path.html) - Used to check if a path is absolute or not  
- [Passport GitHub2 Strategy](https://www.npmjs.com/package/passport-github2) - Used for authenticating with GitHub OAuth  

 
 ## Routes
This project contains the following routes:

- `/`: renders the `index` page with the user's information.
- `/account`: renders the `account` page with the user's information. It also ensures that the user is authenticated. 
- `/login`: renders the `login` page with the user's information. 
- `/logout`: logs out the user and redirects them to the home page. 
- `/auth/github`: authenticates a user using GitHub credentials. 
- `/auth/github/callback`: redirects a successful authentication to the home page, or a failed authentication to the login page.
