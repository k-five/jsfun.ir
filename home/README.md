<h1 align="center">jsfun.ir</h1>

<p>The main repository for <a target="_blank" href="http://jsfun.ir">jsfun.ir</a></p>
<p>Anyone can clone / fork and then add more posts to it.</p>
<p>Before doing it you will need <a target="_blank" href="https://github.com/k-five/nodepost">nodepost</a> application to handle dependencies.</p>

<h1 align="center">Instruction</h1>


 1. `git clone http://github.com/k-five/nodepost`
 2. `cd nodepost`
 3. again: `git clone https://github.com/k-five/jsfun.ir home`
 4. `rm -f database`
 5. `mv home/database .`
 6. `npm install`
 7. `./node-dev nodepost`
 8. open `localhost:1400`

This is what we did:

 1. we cloned the application (= nodepost) for managing our blog.
 2. then `cd` to **nodepost**.
 3. then cloning the blog we want which here is <a target="_blank" href="http://jsfun.ir">jsfun.ir</a>.
 4. removing the default **database** we no longer need it.
 5. Then adding **jsfun.ir**'s database to the application.
 6. Then install applicatoin dependencies using `npm`.
 7. Then running the nodepost application
 8. Finally see it live.

Or using `npm`

 1. `git clone https://github.com/k-five/nodepost` | clone the application
 2. `cd nodepost` | changing Working Directory
 3. `npm install jsfun.ir` | installing **jsfun.ir** blog
 4. `mv node_modules/jsfun.ir home` | moving+renaming it to Current Working Directory
 5. `rm -fr database` | deleting the default **database**
 6. `mv home/database .` | moving jsfun.ir's database to CWD
 7. `npm install` | installing dependencies
 8. `./node-dev nodepost.js` | run the application
 
The directory structure will be like this:

```bash
nodepost                    # nodepost application
├── build
├── database                # database we pulled out of jsfun.ir
├── database-manager
├── error-page
├── home                    # jsfun.ir, which we renamed it to home
├── main-html
├── node_modules
├── path-manager
├── public
├── route-manager
├── script
├── src
├── test
└── vendor

14 directories
```

If everything goes well, we will get:

```bash
$ ./node-dev nodepost.js
ENOENT: no such file or directory, open '/var/www/html/ir/nodepost/database/stat.json'
Create: stat.json
ENOENT: no such file or directory, open '/var/www/html/ir/nodepost/database/route.dirs'
Create: route.dirs
Create: main-html/
posts.json md5: 21646e71bd20486f9e593a7bea55997c
route.dirs md5: 74e6f7298a9c2d168935f58c001bad88
Server is running at http://localhost:1400/
H-Link: ./home/database/posts.json
H-Link: ./home/database/user.json
Update: route.dirs ...
Update: route.link ...
Update: route.path ...
```
