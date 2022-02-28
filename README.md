# Attune Web Site - Static - Hosted on GCP

With the elimination of Vin65 as our ecommerce hosting site, we moved our
website content to a static web hosting service.

Below describes how we set up the project and hosted the static content
for the Attune Wines web site.


### Google Project Data for this project:

|PROJECT_ID                |NAME             |PROJECT_NUMBER|
| ------------------------ | --------------- | ------------ |
|attune-web-site           |attune-web-site  |270521668189|


### Project Website
The project/website created to host the webservices was:

<https://attune-web-site.wm.r.appspot.com/>


### Building a static website in google
The following link explains how we got the base site up with static content:

<https://cloud.google.com/appengine/docs/standard/python/mapping-custom-domains>


### Connecting google site to your DNS
Having a site up and working - we used this page to hook up the DNS name to this site

<https://cloud.google.com/storage/docs/hosting-static-website>


### Our google projects area
Here is the google projects area where we connected DNS to our website

<https://console.cloud.google.com/appengine/settings/domains?project=attune-web-site&folder&organizationId=477930717646>

### Deploying updates of the website to the project
updated the data in the folder attune-web-site/www

go to the deployment folder:  attune-web-site (this houses app.yaml)

login to gcloud:  gcloud auth login

deploy the update:  gcloud app deploy

What you will see is:

Services to deploy:

    descriptor:      [C:\Users\ken\Dropbox\Attune\WebSite\20191216-Download\attune-web-site\app.yaml]
    source:          [C:\Users\ken\Dropbox\Attune\WebSite\20191216-Download\attune-web-site]
    target project:  [attune-web-site]
    target service:  [default]
    target version:  [20200827t192227]
    target url:      [https://attune-web-site.wm.r.appspot.com]

    Do you want to continue (Y/n)?

Answer Yes

you will see:

    Beginning deployment of service [default]...
                                                                  
       Uploading 54 files to Google Cloud Storage                 
                                                                  
    File upload done.
    Updating service [default].../

The reference document explaining how this is done:

<https://cloud.google.com/appengine/docs/standard/python/getting-started/hosting-a-static-website>