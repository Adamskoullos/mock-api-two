# mock-api-two

Build a test mock api and deploy to Heroku for development use

This process is modelled from Ania Kubow's YouTube video: https://www.youtube.com/watch?v=FLnxgSZ0DG4 and takes advantage of `json-server`: https://github.com/typicode/json-server

## Process Overview

1. Create `db.json` and put some default data in there so when we test, we can clearly see if it's working
2. Install json-server on the machine globally: `npm install -g json-server`
3. Fire up the json-server: `json-server --watch db.json`
4. Make sure you have a Heroku account and activate and commit to GitHub
5. Initialise the project and create a package.json file: `npm init`
6. Add json server to the package.json file: `npm i json-server` so it is shipped when deployed to Heroku
7. Add `start` to scripts in package.json and add file `server.js`. This will act as a mini back-end on Heroku
8. Add a `.gitignore` so the `node_modules` will not be uploaded to GitHub
9. Make another commit to GitHub
10. Install/update Heroku CLI:
    - Mac: `brew tap heroku/brew && brew install heroku`
    - Linux: `sudo snap install --classic heroku`
11. Install Heroku globally on machine: `npm install -g heroku`
12. Make sure to be logged into heroku and create Heroku project: `heroku create projectName`

Once complete you will receive an end point ending with `herokuapp.com`, save this

13. Push the project to Heroku: `git push heroku main` (we are in the main branch)

Thats it You now have an endpoint that can be used for all crud operations!
