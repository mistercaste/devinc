# DevInc

A Development Incubator for test and sample purposes.

- GIT Clone
- Configure your credentials
- Run Docker Compose
- Start playing with your new DevOps tools against DevInc! `;-)`

DevInc generates a best-practices ready stack to test CI/CD platforms.


#### Kickstart
Below you can find the steps to kickoff the platform command-line:

1. Generate a _Java Key Store_

> TIP - you can generate a self-signed one (password is the value of `HTTPS_CERTIFICATE_PASSWORD`):
````
    keytool -genkey -keyalg RSA -alias tomcat -keystore selfsigned.jks -validity <days> -keysize 2048
````

2. Create a `.env` file containing the passwords.

> Sample content of file .env
````    
    HTTPS_CERTIFICATE_PASSWORD=******** (see above)
    GITHUB_USERNAME=********
    GITHUB_PASSWORD=********
    GITHUB_TOKEN_READONLY=********
````
   
3. Copy the <code>jenkins.jks</code> _Java Key Store_ in the folder of docker-compose
4. Run: <code>docker-compose up -d</code>
5. Wait for Jenkins to be available at <code>https://\<HOST-IP\>:433</code>
6. Enjoy testing your new DevOps tools against DevInc! `:)`
