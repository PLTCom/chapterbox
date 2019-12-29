bigchonk-chapterbox
# SRA Chapterbox
#### Creating the infrastructure for a chapter in a single package.

## Components

This is the "modern" version of SRA Chapterbox. The "lite" version of this repo is by no means antiquated-but is built to be as light and resource-efficent as possible on time-tested technologies.

This repo is built with the modern web in mind-most of the components were built for the web. It's slightly more resource intensive, but will operate smoothly with other components in the package and will be supported for the foreseeable future.

### Bash Daemon
This particular repo starts with a bash shell daemon written to listen for file changes in two of the
main configuration files, turnserver.conf (for the TURN server) and homeserver.yaml (for the matrix configuration).

After writing the daemon, turnserver.conf and homeserver.yaml will be copied to this repo while leaving their live copies in tact. Changes made to these two files in the repo will be pushed to their respective directories via githook. When these files are changed, the bash daemon will restart the servers, allowing the code to be changed without access to the server itself.  

### Nextcloud with Groupware and OnlyOffice
Nextcloud is the base of the repo, providing a container for most of the other webapps. The matrix client runs in a tab across the top with other (optionally configurable) groupware like email and shared calendar. 

Nexcloud also comes configured with OnlyOffice. OnlyOffice offers an open-source alternative to Google Docs, allowing you to collaborate with other members of your chapter without compromising your privacy. With OnlyOffice and Nextcloud, your docs never leave your ecosystem.

### Keycloak
Keycloak is a web-based authentication client written in Java. It can provide Oauth tokens and SAML

### Matrix (with COTURN)
