# Calling Google Drive API with Service Account

This example shows the process for accessing Google APIs via a service account, abstracting the Google Drive API `/files` endpoint. Covered in this demo are signing JSON Web Tokens (RSA), exchanging the JWT for an Access Token, and storing that access token in ObjectStore. These token flows are accessed via the header configured in the HTTP Request config.

TODO: Add instructions for setting up configuration file with Google credentials

# Setup

## Google

TODO: Add instructions for GCP credentials

## Maven

This project utilizes the JWT DataWeave module located here: https://github.com/mulesoft-consulting/jwt-dw-module

In order to utilize this you will either need to manually install the package into your local maven (https://github.com/mulesoft-consulting/jwt-dw-module/packages/957660) or you can add the following to your maven settings.xml:

```xml
<profiles>
  <profile>
    <id>github-mulesoft-consulting</id>
    <activation>
      <activeByDefault>true</activeByDefault>
    </activation>
    <repositories>
      <repository>
        <id>github-mulesoft-consulting</id>
        <url>https://maven.pkg.github.com/mulesoft-consulting/*</url>
        <snapshots>
          <enabled>true</enabled>
        </snapshots>
      </repository>
    </repositories>
  </profile>
</profiles>
<servers>
  <server>
    <id>github-mulesoft-consulting</id>
    <username>USERNAME</username>
    <password>PERSONAL ACCESS TOKEN (just needs the read:packages scope)</password>
  </server>
</servers>
```