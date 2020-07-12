# WebPoint-Boilerplate
 
Run the following to initalize the repository on your computer:
```
npm install
```

When you are developing, run this command which lets you view the site (with hot reload) on a localhost server; it will give you the address to go to in your browser. If you add new files that it must track, you may have to stop the command and restart it:
```
npm start
```

Before you push, and often throughout development, run the following command. It will run linters over your Pug, SCSS, and JS (it will tell you if you programmed something in an invalid or improper way). If everything is good, they will not output anything. The linters are very picky. Please appease them before you push (you should have no linting errors before pushing unless explicitly told otherwise):
```
npm test
```

Once it is finally time to build and deploy, it may be prudent to create a production branch that has the most recent production build. To do so, use the following commands, but only if you're sure you're supposed to. Please replace [version number] with the actual version number you are at and the URL with the actual Git repo URL. You may need to authenticate if you have not recently authenticated:
```
npm run-script build
cd dist
git init
git add -A
git commit -m Deploy v[version number, like 1.0.0]
git push [URL, like https://github.com/agoldstein03/highlight-within-textarea] deploy
```