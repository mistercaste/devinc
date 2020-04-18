# DevInc

A Development Incubator for test and sample purposes.

- GIT Clone
- Configure your credentials
- Run Docker Compose
- Start playing with your new DevOps tools against DevInc! `;-)`

DevInc generates a best-practices ready stack to test CI/CD platforms.


## Kickstart
1. Clone *DevInc*
2. Put a _Java Key Store_ <code>jenkins.jks</code> in the main folder

> TIP - you can generate a self-signed one (the password is the value for `HTTPS_CERTIFICATE_PASSWORD`):
````
    keytool -genkey -keyalg RSA -alias tomcat -keystore selfsigned.jks -validity <days> -keysize 2048
````

3. Create a `.env` file containing your passwords in the main folder

> Sample content of file .env
````    
    HTTPS_CERTIFICATE_PASSWORD=******** (see above)
    GITHUB_USERNAME=********
    GITHUB_PASSWORD=********
    GITHUB_TOKEN_READONLY=********
````
   
4. Run: <code>docker-compose up -d</code>
5. Enjoy testing your new DevOps tools against DevInc! `:)`
