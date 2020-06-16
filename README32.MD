## React Testing
Snapshots - Make assertions on the exact rendered markup (with content) at any state of the application.
Render Testing - Similar to snapshots, but allows for jQuery-like inspection of the virtual DOM tree
Shallow Testing - Executes and renders the called/container component, but does not compose children.
Mounting - Executes the full component and children. Allows for inspection of rendered Virtual DOM as well as the current state

## Deployment
React in development mode uses a node service to create a live website that refreshes as you write code. This is NOT what actually gets deployed when you want your React website to go live. React, remember is an index.html file that uses Javascript to render components in the browser. The node server is only there to aid in your development.



### 1. Deploying to GitHub Pages
Enable GitHub Pages on your domain, using the gh-pages branch
Create a Personal Access Token in your GitHub account
Add this token as a “Secret” called PERSONAL_TOKEN in the repository housing your react app
Add the react workflow .yml file to your repository (in .github/workflows)
This will initiate a GitHub Action whenever you push (or merge) code into your repository. This action will run the build command for you, create a new branch called gh-pages and deploy your React static files to that branch, which you can then view at the Github Pages link provided to you

### 2. Deploying to AWS (s3)
Create a new Bucket
Storage containers for static assets
Essentially, these are “folders”
Objects
These are the things in the buckets (your files)
Upload the contents of your React application build folder to your bucket
Set up to serve websites
Properties Tab “Static Web Hosting” option

### 3.Deploying to AWS Amplify
Create a new Amplify Workflow
Point the workflow at your GitHub repository (master branch)
Merge your code to master on GitHub
That’s it … Amplify will monitor your repository for changes, pull, build, and deploy your React app automatically
Eventually, there’s a usage charge for the service, depending on your traffic level
Deploying to Netlify
Create a netlify.com account
Create a new application
Point the application at your GitHub repository (master branch)
Merge your code to master on GitHub
That’s it … Netlify will monitor your repository for changes, pull, build, and deploy your React app automatically
