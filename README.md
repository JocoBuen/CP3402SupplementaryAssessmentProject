# CP3402 Supplementary Assignment - U3A Townsville website

Included in this repo are all the essential files for the project’s website. This project outlined the creation of a well-designed, intuitive website for the client, the ‘U3A - Townsville’. Within this README file is a brief overview of the use of the Neve - child theme to create the custom WordPress theme.

## About the Neve Theme

Neve Theme is part of the family created by Themeisle in Wordpress. The Neve theme have features that is suitable for the target audience, the features are fast and lighweight, flexible and easy to use, easy to setup and sleek designs, and with reliable updates for future enhancements.

## About the Neve-child Theme

It is based from the parent theme Neve. Design modifications I made is for the CP3402 Supplementary Assignment Project. This child-theme is easy to use and well designed for third age people.

## Local Development - Docker Desktop

Local development systems that will be used include Docker and Git. The workflow mainly consists of cloning this project's repository into the files of a locally hosted website, before making changes on a feature-specific branch.

### Site Setup

1. Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop/)
2. Create your [docker-compose](https://gist.github.com/erikyuzwa/7411752ddcb95b09434aa88f38d91630) file
3. Create your .env file that you will use in the docker-compose
4. Install Wordpress once a container was created from your docker
5. Open Wordpress Admin dashboard by adding `/wp-admin/`
6. Login with the credentials you created when you installed Wordpress

### Theme Setup

1. Download and Install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
2. Download and Install [VS Code](https://code.visualstudio.com/download)
3. Navigate to your local site's root folder in the terminal of the VS Code
4. Navigate to `wp-content -> themes`
5. Clone the repository by typing `git clone https://github.com/JocoBuen/CP3402SupplementaryAssessmentProject.git`
    1. if using the theme for another purpose, clone a fork of this repository
6. Navigate to your Wordpress Admin Dashboard under `Appearance -> Themes`
7. Activate the theme `Neve-child`

## Live Production

This project uses Microsoft Azure for its live hosting. The primary workflow involves importing the theme and site content from the source local  development environments. The process of exporting is only done when migrating the site to a staging environment for the client.

### Site Setup

