Epub.js Reader
================================

![Demo](http://fchasen.com/futurepress/epubjs-reader_moby-dick.png)

[Try it while reading Moby Dick](http://futurepress.github.com/epubjs-reader/)

About the Reader
-------------------------

[Epub.js](http://futurepress.github.com/epub.js/) library.


Getting Started
-------------------------

Open up [reader/index.html](http://futurepress.github.com/epubjs-reader/index.html) in a browser.

You can change the ePub it opens by passing a link to bookPath in the url:

`?bookPath=https://s3.amazonaws.com/epubjs/books/alice.epub`

Running Locally
-------------------------

Install [node.js](http://nodejs.org/)

Then install the project dependences with npm

```javascript
npm install
```

You can run the reader locally with the command

```javascript
node start
```

Builds are concatenated and minified using [gruntjs](http://gruntjs.com/getting-started)

To generate a new build run

```javascript
grunt
```

Or, to generate builds as you make changes run

```
grunt watch
```

Additional Resources
-------------------------

[Epub.js Developer Mailing List](https://groups.google.com/forum/#!forum/epubjs)

IRC Server: freenode.net Channel: #epub.js

Follow us on twitter: @Epubjs

+ http://twitter.com/#!/Epubjs

Other
-------------------------

EPUB is a registered trademark of the [IDPF](http://idpf.org/).


Run this:
[opc@instance-20221019-2131 epubjs-reader]$ sudo npm install pm2 -g
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.

changed 184 packages, and audited 185 packages in 5s

12 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
[opc@instance-20221019-2131 epubjs-reader]$ ls
Gruntfile.js  LICENSE       nohup.out     package-lock.json  README.md  tools
libs          node_modules  package.json  reader             src
[opc@instance-20221019-2131 epubjs-reader]$ pm2 start tools/serve
[PM2] Spawning PM2 daemon with pm2_home=/home/opc/.pm2
[PM2] PM2 Successfully daemonized
[PM2] Starting /home/opc/projects/futurepress/epubjs-reader/tools/serve in fork_mode (1 instance)
[PM2] Done.
┌────┬────────────────────┬──────────┬──────┬───────────┬──────────┬──────────┐
│ id │ name               │ mode     │ ↺    │ status    │ cpu      │ memory   │
├────┼────────────────────┼──────────┼──────┼───────────┼──────────┼──────────┤
│ 0  │ serve              │ fork     │ 0    │ online    │ 0%       │ 35.7mb   │
└────┴────────────────────┴──────────┴──────┴───────────┴──────────┴──────────┘
[PM2][WARN] Current process list is not synchronized with saved list. App app differs. Type 'pm2 save' to synchronize.

change GIT

[opc@instance-20221019-2131 epubjs-reader]$ git remote rename origin upstream
[opc@instance-20221019-2131 epubjs-reader]$ git remote add origin https://github.com/bogithub/epub-reader
[opc@instance-20221019-2131 epubjs-reader]$ git push origin master
Enumerating objects: 186, done.
Counting objects: 100% (186/186), done.
Delta compression using up to 2 threads
Compressing objects: 100% (111/111), done.
Writing objects: 100% (186/186), 2.56 MiB | 33.13 MiB/s, done.
Total 186 (delta 79), reused 159 (delta 67), pack-reused 0
remote: Resolving deltas: 100% (79/79), done.
To https://github.com/bogithub/epub-reader
 * [new branch]      master -> master


 git branch --set-upstream-to origin/master
Branch 'master' set up to track remote branch 'master' from 'origin'.
[opc@instance-20221019-2131 epubjs-reader]$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 650 bytes | 650.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/bogithub/epub-reader
   ec5d3d1..acfd2ca  master -> master


   git add . && git commit -a -m "commit" && git push