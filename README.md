# Hugo ENIB Template

# Build the Site Locally

To build and test the site locally on your machine, you need to have Hugo installed. If you don't have Hugo installed, please refer to the official Hugo documentation for installation instructions (https://gohugo.io/getting-started/).

## Steps to Build the Site

1. Clone the Repository. First, clone this repository (or your fork of it) to your local machine:

```
git clone https://github.com/[YourUsername]/[RepoName].git
cd [RepoName]
```

2. Run Hugo Server. Navigate to the root directory of the repository and start the Hugo server:

```
hugo server
```

This command will start a local web server. By default, you can view your site at http://localhost:1313.

3. View Your Site. Open your web browser and go to http://localhost:1313 to see your site in action.

## Create Publication list

The template contains a python script that automatically build a publication page from your google scholar profile.

* Go to your google scholar profile
* Select all your articles > Export CSV
* Put the csv file in the data folder of the hugo project
* Run `python generate.py`

The script will create a file named `index.md` in the `content/publications` folder.


# Deploy with GitHub Pages

This theme supports automatic deployment using GitHub Pages and GitHub Actions. This means that every time you push changes to your repository, GitHub Actions will automatically build your Hugo site and deploy it to GitHub Pages

## Setup Steps

1. Enable GitHub Pages on Your Repository
    * Go to your repository's settings.
    * Scroll down to the "GitHub Pages" section.
    * Select the source branch (commonly gh-pages) and folder (/root or /docs) where your site will be published from.

2. Use GitHub Actions Workflow. The Hugo site's repository contains a directory named .github, and within it, another directory named workflows. This directory contains a YAML file (e.g., main.yml) for the GitHub Action workflow. 

Commit and Push the Workflow File
Commit and push these changes to your repository. This action will trigger the workflow and deploy your site to 

3. Push your website on github. Each push will install Hugo, build your site, and deploy the public directory to the gh-pages branch.

Once the workflow successfully completes, your site will be accessible at https://[username].github.io/[repository-name]/.


# Contributing

Contributions to improve the ENIB Theme are welcome. Here's how you can contribute:

* Fork the repository.
* Create a new branch (git checkout -b feature-branch).
* Make your changes.
* Commit your changes (git commit -am 'Add some feature').
* Push to the branch (git push origin feature-branch).
* Create a new Pull Request.