# Add your name & photo to the Germantown Codes website

The **Our Members** section of our [website](http://codepen.io/diptajbasu/pen/oxrZer) needs to be updated so the placeholder members are replaced with **real** members!

![Our Members](https://raw.githubusercontent.com/GermantownCodes/our-members/master/images/our-members.png)


If you'd like to have your name & photo included on our upcoming website, please follow the instructions below.

If you're new to Git / GitHub, check out our [recommended resources](https://www.facebook.com/notes/184961131858082/Git%20/%20GitHub%20resources/258232804530914/).


### 0. Join our GitHub organization
Please comment on this [Facebook thread](https://www.facebook.com/groups/free.code.camp.germantown.maryland/permalink/276279196059608/) with your GitHub username.


### 1. Fork the project
In GitHub, fork the [website project](https://github.com/GermantownCodes/website) to your personal GitHub account.


### 2. Open a CLI tool
Open your preferred Command Line Interface tool. This could be PowerShell, Cmder, etc. on Windows. Terminal, iTerm2, etc. on OSX. Gnome, Terminator, Konsole, etc. on Linux.


### 3. Select a directory
Navigate to the directory in your file system where you want to store the project locally. For example, if you want to store a local copy of the project on your Desktop (on a mac):

`$ cd ~/Desktop`


### 4. Clone the forked repo
Clone the forked repository to your local machine. **Note:** Be sure to copy the web URL (or SSH key / passphrase) from your personal forked copy of the repo. The link will contain your personal GitHub username in place of *diptajbasu* in the example link below.

`$ git clone https://github.com/diptajbasu/website.git`


### 5. Connect your local copy
Connect your local copy to the original repository. Group members (i.e., collaborators) will be making many updates to the project's main repo, which contains the master branch. You'll, in turn, want to pull in those updates to your local copy frequently to avoid merge conflicts. So, you should connect your local copy by adding the original repo as a remote.

It's a convention to call the original repository **upstream**.

`$ git remote add upstream https://github.com/GermantownCodes/website.git`


### 6. Review your remotes
You should now have 2 remote repos: 1) upstream (the group's original repo) and 2) origin (your forked copy). Let's confirm this.

`$ git remote`

You should see 2 remotes printed to the command line: **origin** and **upstream**


### 7. Enter your local copy
Enter your local copy of the project. The project folder you cloned onto your machine is called *website*.

`$ cd website`


### 8. Create a local branch
Create a local feature branch (a branch is a complete copy of the project), prefixed with your initials. For example, (My initials are **djb** and I want to create a branch that adds member **bio** information):

`$ git branch djb-add-member-bio`


### 9. Switch branches
Switch from the default master branch (your local copy of the master branch) you started in, over to the branch you just created (i.e., your new feature branch). For example:

`$ git checkout djb-add-member-bio`


### 10. Create a directory
Create a directory, named with your initials, within the src/data/members directory. For example:

`$ mkdir src/data/members/djb`


### 11. Create a JSON file
Create a JSON file, named with your initials, within the new directory you just created.

Add any information you'd like to share publicly on our website. The only required field is name, the rest are up to you. Our current UI design only displays your name, but (depending on interest) this may change in the future. It's perfectly acceptable to just include your name only.

Create the JSON file:

`$ touch src/data/members/djb/djb.json`

Add whatever data you'd like to share. Please follow guidelines from the [Google JSON Style Guide](https://google.github.io/styleguide/jsoncstyleguide.xml) for JSON data formatting. You may want to run your JSON through a linter like [JSON Generator](http://www.json-generator.com/).

Here's JSON from an example file (djb.json):

```javascript
{
  "name": "Dipta J. Basu",
  "location": "Germantown, Maryland",
  "bio": "I'm a data-driven web developer committed to advancing greater equality and opportunity.",
  "socialProfiles": {
    "freecodecamp": "https://www.freecodecamp.com/diptajbasu",
    "github": "https://github.com/diptajbasu",
    "codepen": "http://codepen.io/diptajbasu/",
    "facebook": "https://www.facebook.com/diptajbasu",
    "twitter": "https://twitter.com/DiptaJBasu",
    "dribbble": "https://dribbble.com/diptajbasu"
  },
  "professional": {
    "organization": "globalgiving.org",
    "role": "Front End Web Development"
  },
  "languages": [
    "HTML",
    "CSS",
    "JavaScript",
    "PHP",
    "SQL"
  ],
  "interests": [
    "nonprofits",
    "online fundraising",
    "online education",
    "learn to code movement",
    "writing",
    "screencasting",
    "vlogging",
    "teaching",
    "hiking",
    "travel",
    "minimalism",
    "cooking",
    "functional fitness training",
    "productivity",
    "fatherhood",
    "hackathons",
    "web development",
    "UI/UX"
  ]
}
```

### 12. Add a photo

Add a photo of yourself, named with your intitials, within the same directory as the JSON file.
Please use a square photo, at least 300 x 300, in .jpg or .jpeg format. For example: **djb.jpg**

![Dipta J. Basu](https://raw.githubusercontent.com/GermantownCodes/our-members/master/images/djb.jpg)


### 13. Stage your changes
`$ git add .`


### 14. Commit your changes
`$ git commit -m "Add bio information for Dipta J. Basu aka djb"`


### 15. Check master for updates
In the time that has passed since you forked the repo in GitHub, it's certainly possible that other contributors have updated master. So, let's pull in any changes from master and merge them into our feature branch.

`$ git checkout master`

`$ git pull upstream master`

`$ git checkout djb-add-member-bio`

`$ git merge master`


### 16. Push changes to your fork
`$ git push origin djb-add-member-bio`


### 17. Submit a Pull Request
Now that your fork reflects the changes you made (adding a JSON file and photo), when you visit your fork on GitHub (in my case: https://github.com/diptajbasu/website), you should see a green **Compare & pull request** button in the upper right-hand corner of the page. Clicking the green button takes you to an **Open a pull request** page which displays summary information detailing the differences between where you think changes should be applied (i.e., **base branch**) and what you think should be applied (i.e., **head branch**). You may leave a comment in the textarea (e.g., reference a blog post or collaborator that helped you out, etc.) or alert someone (e.g., *Hey @diptajbasu, could you check this out?*) if you wish. Click the green **Create pull request** button.


### 18. Post in Facebook
Now that you've submitted a pull request ("PR"), please alert the team by posting on our [Facebook group](https://www.facebook.com/groups/free.code.camp.germantown.maryland/), so a teammate can review. You should hear back within 48 hours with suggestions on what might need updating, or your PR may be accepted without the need for revision.


### 19. Synching
Now that your updates have been accepted and added to master, it's time to celebrate!

Once the party has calmed, you'll notice that both your fork and your local copy are now out of sync with master! As this first project with GitHub is relatively brief, we won't do a rebase and instead use a simplified workflow to finish up. The next time we use GitHub we'll rebase as it's a best practice and cleans up the PR process (and master's commit history) considerably.

For our simplified workflow, we'll merge our **bio info** branch into master locally, delete the **bio info** branch as we'll no longer need it, pull from master, and then push to our forked copy on GitHub to get it synched as well.

`$ git checkout master`

`$ git merge djb-add-member-bio`

`$ git branch -d djb-add-member-bio`

`$ git pull upstream master`

`$ git push`

Now, upstream, origin and the local copy should all be in sync.
