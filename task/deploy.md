-	add deploy task (just for developing deploy, separated from test task so it will be more flexible)

	-	su jenkins
		-	install rvm on server manually
			-	another way without installing rvm manually, see ruby-runtime, Rvm part of the following blog post
			-	http://blog.smlsun.com/2014/04/jenkins-plugins-nodejs.html#ruby-runtime-rvm
	-	New Item: choose "Freestyle project"
	-	Project name: [self pick]
	-	Source Code Management:
		-	choose Git
		-	Repository URL: [self pick]
		-	Credentials: select the key add in above 'set credentials' part
		-	Branches to build: */develop
			-	develop is a branch for developing, can be replaced with own branch
	-	Build Environment:
		-	check "Provide Node & npm bin/ folder to PATH"
	-	Build:

		-	Execute shell

			-	\`\`\` #!/bin/bash source ~/.bashrc #gem install bootstrap-sass npm install

			grunt  
			tar cvf zuru.tar .`
			*
			` #!/bin/bash (notice: add this line so that we can use "source" command below)\`\`\`* jenkins should install or compile needed packages and files before packing(tar) files

		-	Send files or execute commands over SSH

			-	SSH Server Name: [self pick]
			-	Transfer Set Source files: [self pick](ex: zuru.tar)
			-	Exec command:
				-	(ex: cd /srv/www/zuru/ && pm2 stop [app id] && tar xf zuru.tar && rm zuru.tar && rm -r .git && pm2 start app.coffee)
				-	[app id] should put id generated by pm2
				-	install pm2 manually (su jenkins, need to install nvm and node manually too):
					-	sudo npm install pm2 -g --unsafe-perm
					-	pm2 doc:
						-	https://www.npmjs.com/package/pm2

![enter image description here](https://lh3.googleusercontent.com/-bDHWBZnIyoY/VUCaM6KSWmI/AAAAAAAAP-k/SLepB0wTDvY/s0/Screen+Shot+2015-04-22+at+5.38.15+PM.png)

![enter image description here](https://lh3.googleusercontent.com/-MDY2VOzsdZg/VUCaRzWl4vI/AAAAAAAAP-w/5uQ1TdL5TP8/s0/Screen+Shot+2015-04-22+at+5.46.03+PM.png)
