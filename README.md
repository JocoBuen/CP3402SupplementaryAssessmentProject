# CP3402 Supplementary Assignment - U3A Townsville website

Included in this repo are all the essential files for the project’s website. This project outlined the creation of a well-designed, intuitive website for the client, the ‘U3A - Townsville’. Within this README file is a brief overview of the use of the Neve - child theme to create the custom WordPress theme.

## About the Neve Theme

Neve Theme is part of the family created by Themeisle in Wordpress. The Neve theme have features that is suitable for the target audience, the features are fast and lighweight, flexible and easy to use, easy to setup and sleek designs, and with reliable updates for future enhancements.

## About the Neve-child Theme

The child theme we have developed for our website contributes several important changes to the overall design and functionality. Firstly, it introduces a custom color scheme that aligns with our brand identity, creating a more cohesive and visually appealing user experience. Additionally, the child theme modifies the header layout to include a new logo and navigation menu, enhancing the website's navigation and branding.

Furthermore, the child theme alters the typography across the site, using more readable fonts to improve accessibility and user engagement. It also implements responsive design elements, ensuring that the website adapts seamlessly to different screen sizes and devices, making it mobile-friendly for our users.

Regarding further changes to the child theme, we recommend making updates and adjustments primarily within the child theme's stylesheet (style.css). This is where additional CSS rules can be added or modified to adjust the layout, colors, and other visual aspects of the website.

## Local Development - Docker Desktop

Docker Desktop is a cutting-edge local development solution for WordPress projects. By leveraging container technology, Docker enables you to create lightweight, self-contained environments that encapsulate your entire WordPress setup, including the application, dependencies, and configuration. This means you can easily replicate the exact development environment across different machines, making collaboration and deployment a breeze.

Comparing to Vagrant:

While both Docker Desktop and Vagrant aim to simplify local development, Docker stands out with its efficiency and resource optimization. Unlike Vagrant, which relies on virtual machines, Docker uses containers, which consume fewer system resources and boot up much faster. This allows for quicker iteration and testing in the WordPress development process.

Additionally, Docker benefits from an extensive library of pre-built container images specifically tailored for WordPress, making setup and configuration more straightforward. On the other hand, Vagrant often requires custom virtual machine configurations, which can be more time-consuming and complex.

In summary, Docker Desktop offers a streamlined and lightweight approach to developing WordPress projects locally, providing increased speed, efficiency, and simplicity compared to Vagrant's virtual machine-based workflow.

## Making Changes to the Website - Local, Testing, and Deployment Process

### Local Development Environment Setup

1. Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop/)
2. Create your [docker-compose](https://gist.github.com/erikyuzwa/7411752ddcb95b09434aa88f38d91630) file
3. Create your .env file that you will use in the docker-compose
4. Install Wordpress once a container was created from your docker
5. Open Wordpress Admin dashboard by adding `/wp-admin/`
6. Login with the credentials you created when you installed Wordpress

### Making New Changes

1. Use a code editor to modify the website's files in your local development environment.
2. Test the changes locally to ensure they work as intended on your computer.
3. Make use of descriptive comments in the code to document changes and their purpose.

### Production Environment Setup

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

### Deployment to Production

1. Once the changes are thoroughly tested and approved, merge the development branch into the main branch in the version control system.
2. Pull the latest version of the main branch on the production server.
3. Apply the changes on the production server, either through Git pull or by uploading the modified files.
4. Clear caches and ensure all necessary configurations are in place.

### Version Control and Documentation

1. Ensure that all changes made are well-documented in the version control system, including commit messages and detailed comments.
2. Maintain a changelog to keep track of all updates and improvements to the site.
3. Update the website's documentation to reflect any significant changes or new features.