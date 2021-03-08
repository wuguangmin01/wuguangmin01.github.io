# How to Build a Document Using Github Pages and Hugo 
 

### Prerequisites:

* Homebrew has been installed.
* Github account has been registered.
* A new Github repository has been created.

### Procedure:

Step 1. Open a terminal and run the following command to install Hugo.
 
	 
    brew install hugo
    
 Step 2. Run the following command to check whether Hugo is installed successfully and check the Hugo version.
	 
	hugo version
	 
	 

The following information is displayed, indicating that the installation is successful.
		 
    hugo v0.81.0+extended darwin/amd64 BuildDate=unknown
		 

Step 3. Run the following command to create a new website.

	 
	hugo new site techdoc
	 
Step 4. Run the following command to add a topic.

	
	cd /Users/wuguangmin/techdoc
	git init
	git submodule add git submodule add https://github.com/thingsym/hugo-theme-techdoc.git themes/hugo-theme-techdoc
	
Step 5.  Run the following command to add new data in the *config.toml* in the root directory.
	
	echo'theme = "hugo-theme-techdoc"' >> config.toml
	
> 	**Note:**
> 	
> 	The Theme configuration item refers to the name of the selected theme, which must be the same as the theme added in step 4. theme = "hugo-theme-techdoc".
> 	

Step 6. To change the information of the *config.toml*, the specific operation is as follows: Use the key combination **Command + Shift + G** in the **Finder**, enter /*Users/wuguangmin/techdoc* in the input box of the pop-up page, and find *config.toml*, right-click and select **Open > Text** Edit. Change the value of baseURL http://example.org/ to https://github.com/wuguangmin01/wuguangmin01.github.io.git/ and the value of title My New Hugo Site to Hailey's Techdoc Website, press and hold  **Command + S** to save.

Step 7. Run the following command to start the Hugo server.

	
	hugo server
	
	
  The following information is displayed, indicating that the server has started successfully.
 
	 
	Start building sites…
	
	               | EN
	-------------------+-----
	  Pages | 10
	  Paginator pages | 0
	  Non-page files | 0
	  Static files | 6
	  Processed images | 0
	  Aliases | 0
	  Sitemaps | 1
	  Cleaned | 0
	Built in 25 ms
	Watching for changes in /Users/wuguangmin/techdoc/{archetypes,content,data,layouts,static,themes}
	Watching for config changes in /Users/wuguangmin/techdoc/config.toml
	Environment: "development"
	Serving pages from memory
	Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
	Web Server is available at http://localhost:1313/wuguangmin01/wuguangmin01.github.io.git/ (bind address 127.0.0.1)
	Press Ctrl+C to stop
	 
Step 8. Use a browser to open the http://localhost:1313/wuguangmin01/wuguangmin01.github.io.git/ preview.

Step 9. According to the prompt on the website page, put the compiled   *_index.md* in the */user/wuguangmin/techdoc/content* directory.

Step 10. Run the following command in the */Users/wuguangmin/techdoc/public* directory to add a remote connection for the Git local library.

	
	git remote add origin git@github.com: git@github.com:wuguangmin01/wuguangmin01.github.io.git
	

Step 11. Run the following command to view the relationship between the Git local library and the remote library.

	 
	 cat.git/config
	
	 

The following information is displayed, indicating that the Git local library is successfully associated with the remote library.
 
	 
	[core]
	    repositoryformatversion = 0
	    filemode = true
	    bare = false
	    logallrefupdates = true
	    ignorecase = true
	    precomposeunicode = true
	[remote "origin"]
	    url =git@github.com:wuguangmin01/wuguangmin01.github.io.git
	 

Step 12. Run the following command, submit the modification to the local library through commit, and write a commit message to briefly describe the modification content.
	
	git status
	git add.
	git commit -m "Add a new post"
	 

Step 13. Run the following command to push the modification to the remote library.
 
	 
	git push -u origin master
	git status
	 

 
 

