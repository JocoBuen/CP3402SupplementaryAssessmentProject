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

1. Make an account at [Microsoft Azure](https://azure.microsoft.com/en-au/free/search/?ef_id=_k_EAIaIQobChMIyLTzpvSpgAMV-mwPAh0upAszEAAYASAAEgLcavD_BwE_k_&OCID=AIDcmmxbrcqs76_SEM__k_EAIaIQobChMIyLTzpvSpgAMV-mwPAh0upAszEAAYASAAEgLcavD_BwE_k_&gad=1&gclid=EAIaIQobChMIyLTzpvSpgAMV-mwPAh0upAszEAAYASAAEgLcavD_BwE)
2. Go to [Create Wordpress on App Service - Microsoft Azure](https://portal.azure.com/#create/WordPress.WordPress)
3. In the Basics tab, under `Project Details`, select the correct subscription and click on Create new to create a new Resource group. Give a name to identify your resource group and click on OK.
4. Under Hosting Details, select a region you wish to serve your application from. Give a unique name to your app. If the name is not unique, you will see an error message: The app name _website_name_ is not available.
5. Under `Hosting Plans`, the Standard hosting plan is selected by default. Should you need to change the plan, click on Change Plan. Choose your desired plan from the plan picker side bar.
6. Under `WordPress setup`, select the site language, provide an admin email address, username, and password for the WordPress website.
7. You can directly click on `Review + create` and go to the Review + Create tab or you can click on `Next: Advanced >`.
8. In the `Advanced` tab, you can opt for advanced features: Azure CDN or Azure AFD, and Azure Blob Storage. We recommend that you select Azure CDN and Azure Blob storage. If you select Azure AFD, you will need to either select an existing AFD profile or create a new one.
9. On the `Review + create` tab, you can see all the details of the web application. Click on `Create`.
10. Wait for the deployment to finish. Then click on `Go to resource`.
11. In the App Service Window, find the URL and go to the website.
12. You will land on the homepage of your WordPress website.
13. Add /wp-admin to your URL. In this example, https://wpwebsitename.azurewebsites.net/wp-admin This will take you to the Admin page. In the Admin page, enter your credentials that you had set in Step 5.
14. You are now in the WordPress Admin Dashboard! Happy WordPress-ing!