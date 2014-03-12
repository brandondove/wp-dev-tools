# WordPress Developer Tools

And so it begins...

### Tasks

1. Interact with Fixtures Server (database)
	1. Get local database
	2. Push local database to fixtures
	3. Sync local database with production
	4. Sync fixtures database with production
2. WordPress
	1. Set up correct version of WordPress with designated layout
	2. Upgrade WordPress to latest version (WP-CLI)
	3. Upgrade WordPress to arbitrary version (WP-CLI)
3. WordPress Plugins
	1. Set up plugins as submodules
	2. Upgrade plugins to specific version (WP-CLI)
4. WordPress Themes
	1. Set up themes as submodules
	2. Upgrade themes to specific version (WP-CLI)
5. Set Up/Interact with Centralized Git Repository (git/github/bitbucket/etc)
	1. Create new empty project (interactive shell)
6. Set Up Environment (local/staging/production)
	1. Apache or Nginx
	2. MySQL
	3. PHP
	4. Git
	5. Capistrano, SSH, or (s)FTP
7. Change Environment (local/staging/production)
	1. Apache or Nginx
	2. MySQL
	3. PHP
	4. Git
	5. Capistrano, SSH, or (s)FTP

### Assumptions

1. Developers will create, update, and delete code locally using git for version control.
2. When a developer is ready to show changes to the client, they will want to do so in a remote staging environment. They will push their changes to a centralized git repository, then run `cap staging deploy`.
3. When changes are blessed by the client, the developer will merge their changes into the master branch and deploy code to the production server. They will push their changes to a centralized git repository, then run `cap production deploy`.
4. Scotch is for shippers, drink Scotch.

### Configuration Options

1. WordPress Layout
	1. Standard (default)
	2. Subdirectory
2. Track WordPress
	1. Yes (default)
	2. No
3. Staging Server
	1. IP Address/Server Name
	2. Username
	3. Password
	4. Directory
	5. Deployment Method
		1. SSH
		2. (s)FTP
4. Production Server
	1. IP Address/Server Name
	2. Username
	3. Password
	4. Directory
	5. Deployment Method
		1. SSH
		2. (s)FTP

### Nice To Haves

1. Ignores files based on configuration (gitignore)
2. Automatically install and ignore MU plugins for local development
	1. Developer
3. Don't pass 404s through WordPress `RewriteCond %{REQUEST_URI} !.*\.(?:gif|jpe?g|png|pdf|mp3|avi|mpeg|bmp|mov)$`
