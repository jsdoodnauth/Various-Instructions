Getting Started with Yeoman

npm install --global npm

* Verify version installation
**	node --version && npm --version
**	git --version

* Setup Global NPM without SUDO 
**	mkdir "${HOME}/.npm-packages"
**	Create '~/.npmrc' and enter: prefix=${HOME}/.npm-packages
**	In '.bashrc':
	/************************************/
		NPM_PACKAGES="${HOME}/.npm-packages"

		PATH="$NPM_PACKAGES/bin:$PATH"

		# Unset manpath so we can inherit from /etc/manpath via the `manpath` command
		unset MANPATH # delete if you already modified MANPATH elsewhere in your config
		export MANPATH="$NPM_PACKAGES/share/man:$(manpath)"
	/************************************/
* Install Yeoman
**	npm install --global yo bower grunt-cli

* Confirm Installation
**	yo --version && bower --version && grunt --version

* Install Test tools
**	npm install grunt-karma karma karma-phantomjs-launcher karma-jasmine jasmine-core phantomjs --save-dev

* Install Generators
**	npm install --global generator-webapp
**	npm install --global generator-angular generator-karma

* Create App
**	mkdir <appName> && cd <appName>

* Run Yeoman Scaffolding
**	yo
