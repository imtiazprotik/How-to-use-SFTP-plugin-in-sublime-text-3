# How-to-use-SFTP-plugin-in-sublime-text-3
Here describe How anyone can use SFTP plugin in sublime text 3

## 1st Install Package in your Sublime Text
To install package copy the bellow code and go to sublime text > View > Show console > paste code > Enter

	import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)

### Now press Ctrl+Shift+Enter and Search sftp and install

## 2nd create a file in you computer with the sftp-config.json name & save below code

	{
	    // The tab key will cycle through the settings when first created
	    // Visit http://wbond.net/sublime_packages/sftp/settings for help
	    
	    // sftp, ftp or ftps
	    "type": "ftp",

	    "save_before_upload": true,
	    "upload_on_save": true,
	    "sync_down_on_open": false,
	    "sync_skip_deletes": false,
	    "sync_same_age": true,
	    "confirm_downloads": false,
	    "confirm_sync": true,
	    "confirm_overwrite_newer": false,
	    
	    "host": "109.199.97.128",
	    "user": "admin@be1stfitness.com",
	    "password": "quwyetr1!!23",
	    "port": "21",
	    
	    "remote_path": "/",
	    "ignore_regexes": [
	        "\\.sublime-(project|workspace)", "sftp-config(-alt\\d?)?\\.json",
	        "sftp-settings\\.json", "/venv/", "\\.svn/", "\\.hg/", "\\.git/",
	        "\\.bzr", "_darcs", "CVS", "\\.DS_Store", "Thumbs\\.db", "desktop\\.ini"
	    ],
	    //"file_permissions": "664",
	    //"dir_permissions": "775",
	    
	    //"extra_list_connections": 0,

	    "connect_timeout": 30,
	    //"keepalive": 120,
	    //"ftp_passive_mode": true,
	    //"ftp_obey_passive_host": false,
	    //"ssh_key_file": "~/.ssh/id_rsa",
	    //"sftp_flags": ["-F", "/path/to/ssh_config"],
	    
	    //"preserve_modification_times": false,
	    //"remote_time_offset_in_hours": 0,
	    //"remote_encoding": "utf-8",
	    //"remote_locale": "C",
	    //"allow_config_upload": false,
	}

Now put your host, user, password and port and work.