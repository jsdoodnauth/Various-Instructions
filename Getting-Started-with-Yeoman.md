#Getting Started with Yeoman

### Install NodeJS
*	curl -sL https://deb.nodesource.com/setup_5.x | sudo -E bash -
*	sudo apt-get install -y nodejs
*	sudo apt-get install -y build-essential

### Setup Global NPM without SUDO 
*	mkdir "${HOME}/.npm-packages"
*	Create '~/.npmrc' and enter: 
		prefix=${HOME}/.npm-packages
*	In '.bashrc':


		NPM_PACKAGES="${HOME}/.npm-packages"

		PATH="$NPM_PACKAGES/bin:$PATH"

		# Unset manpath so we can inherit from /etc/manpath via the `manpath` command
		unset MANPATH # delete if you already modified MANPATH elsewhere in your config
		export MANPATH="$NPM_PACKAGES/share/man:$(manpath)"
		

*	npm config set prefix '~/.npm-packages'    <- This may error out, that's ok
*	source ~/.bashrc

### Update NPM
*	npm install -g npm@latest

### Verify version installation
*	node --version && npm --version
*	git --version

### Install Yeoman
*	npm install -g yo bower grunt-cli

### Confirm Installation
*	yo --version && bower --version && grunt --version

### If 'yo' not found, or issue with NODE_PATH

*	echo "export NODE_PATH=$NODE_PATH:/home/$USER/.npm-packages/lib/node_modules" >> ~/.bashrc && source ~/.bashrc

### Install Test tools
*	npm install grunt-karma karma karma-phantomjs-launcher karma-jasmine jasmine-core phantomjs --save-dev

### Install Generators
*	npm install --global generator-webapp
*	npm install --global generator-angular generator-karma

### Create App
*	mkdir [appName] && cd [appName]

### Run Yeoman Scaffolding
*	yo

### Setup from a Repo
*	git clone [repo url]
*	cd [repo]
*	npm install <- install Package dependences
*	bower install <- install Project dependences

### Fix issue with bower not pulling from git://
*	git config --global url."https://".insteadOf git://
*	
