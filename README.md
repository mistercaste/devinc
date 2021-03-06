# DevInc

A Development Incubator for test and sample purposes.

- GIT Clone
- Configure your credentials
- Run Docker Compose
- Start playing with your new DevOps tools against DevInc! `;-)`

DevInc generates a best-practices ready stack to test CI/CD platforms.

## Requirements

* [docker 19.00](https://docs.docker.com/get-docker)
* [docker-compose 1.25](https://docs.docker.com/compose/install)

## Kickstart
1. Clone _DevInc_
2. Put a _Java Key Store_ <code>jenkins.jks</code> in the main folder

**NOTE**
You can generate a self-signed one. The password is the value for `HTTPS_CERTIFICATE_PASSWORD`

````shell script
    keytool -genkey -keyalg RSA -alias tomcat -keystore selfsigned.jks -validity <days> -keysize 2048
````

3. Create a `.env` file containing your passwords in the main folder

````shell script
    HTTPS_CERTIFICATE_PASSWORD=********
    GITHUB_USERNAME=********
    GITHUB_PASSWORD=********
    GITHUB_TOKEN_READONLY=********
````
   
4. Run: <code>docker-compose up -d</code>
5. Enjoy testing your new DevOps tools against DevInc! `:)`


#### Disclaimer
Despite focusing on the DevOps best practices, _DevInc_ is not intended for using in production systems. Use at your own risk!