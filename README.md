# Deploy ReactJS app to GitHub Pages
This repo contains step to step process on how to deploy react app to github pages

### Create Github repo
[Follow this link to create new repo](https://github.com/new)


### Add GitHub Pages dependency package
Install "gh-pages" package using the below command.

```
npm install gh-pages --save-dev
```

### Add homepage property to package.json file

```
homepage": "https://{username}.github.io"
```
![package.json example image](https://github.com/NSQ1point0/deploy-reactapp-to-github/blob/main/3%5B1%5D.png)


### Add deploy scripts to package.json file
Add both predeploy and deploy property scripts to the package.json file as below,

```
"predeploy": "npm run build",
"deploy": "gh-pages -d build"
```

The "predeploy" command is used to bundle the react application and the "deploy" command helps to deploy the bundled file.
![package.json deploy example image](https://github.com/NSQ1point0/deploy-reactapp-to-github/blob/main/4%5B1%5D.png)

### Create a remote GitHub repository
..* Initialize the Git using "git init" command.
..* Add it as remote using "git remote add origin your-github-repository-url.git" command.

### Deploy the Application to GitHub Pages
Now run the below command to deploy your react application to GitHub Pages.

```
npm run deploy
```

### Access deployed site

To get the published URL, 

..* Go to your GitHub Repo.
..* Click Settings menu.
