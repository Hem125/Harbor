## Harbor
- ### first make sure that docker and docker compose are installed . 
![image](https://user-images.githubusercontent.com/103022040/169688594-745df4ab-42ce-4738-a3f1-67f5aeed8c18.png)
- ### config and add ip in daemon.json file
![image](https://user-images.githubusercontent.com/103022040/169689387-84637188-9edf-45d7-bc1b-5e64cf8942f6.png)
- ### start docker service
![image](https://user-images.githubusercontent.com/103022040/169689356-850cc4de-09c0-43b7-8b68-14ca0888bdbd.png)
- ### change to root user and run the following command
![image](https://user-images.githubusercontent.com/103022040/169691423-f4f63b85-4d2a-49b7-b441-39a1e9d37968.png)
- ### download the latest harbor installation package 
![image](https://user-images.githubusercontent.com/103022040/169691657-0470ba4d-e7cb-4edc-bb07-5d0f31691bd4.png)
- ### after file download unpack it with following command
![image](https://user-images.githubusercontent.com/103022040/169691737-43ba0185-b2ce-4407-ae8c-861b4262b3f7.png)
- ### after unzip go to harbor folder 
![image](https://user-images.githubusercontent.com/103022040/169691866-a62c0d53-95d5-4c43-a236-963183656385.png)
- ### copy harbor.yml.tmpl to harbor.yml
![image](https://user-images.githubusercontent.com/103022040/169691982-6afdab90-7a10-49ff-9272-373919e899a2.png)
- ### edit yml file
![image](https://user-images.githubusercontent.com/103022040/169692015-24d6d4c8-ad3a-4917-9104-4d788d77fc16.png)
- ### add the domain name and the path where we want to generate certificate
![image](https://user-images.githubusercontent.com/103022040/169692106-31cfcc99-ed46-480e-85b6-ba2e9db1b881.png)
- ### run the following command to install harbor
![image](https://user-images.githubusercontent.com/103022040/169692590-646f2339-30f5-4050-b740-f2f5b71811d1.png)
- ### after running the command harbor will be installed successfully
![image](https://user-images.githubusercontent.com/103022040/169692662-b7e0bf55-5255-45b7-bd61-58b8ae50f181.png)

### Harbor certificate
- ### run the following command to generate a CA certificate private key.
![image](https://user-images.githubusercontent.com/103022040/169692752-ee1ec8e5-8651-4e0d-bdb8-9f1aa631a58f.png)
- ### Generate the CA certificate. Adapt the values in the -subj option to reflect your organization
![image](https://user-images.githubusercontent.com/103022040/169692808-262ba4af-a9df-4188-a6b0-a1e5bfa4ef22.png)
- ### generate a private key for server certificate
![image](https://user-images.githubusercontent.com/103022040/169692851-272259cf-a96b-4f82-8dab-20e63f2859a6.png)
- ### Generate a certificate signing request (CSR).
![image](https://user-images.githubusercontent.com/103022040/169692886-a5e165de-932e-4f4b-b0ac-f7948faee18e.png)
- ### make change in host file and add domain with ip
![image](https://user-images.githubusercontent.com/103022040/169693008-3244d18f-df69-45ba-b328-f4c09276c670.png)

### Push and pull in Harbor
- ### run the docker compose up command to restart harbor service
![image](https://user-images.githubusercontent.com/103022040/169693047-4704ab69-5cc3-4ff6-8f7b-244cce1d00e1.png)
- ### login using following command
![image](https://user-images.githubusercontent.com/103022040/169693086-d064d35d-97d5-4430-a966-0d5d0bc37569.png)
- ### push using following command
![image](https://user-images.githubusercontent.com/103022040/169693124-1c872101-b376-42e4-99d8-191f96f8d5b5.png)
- ### we can verify by going in harbor ui interface
![image](https://user-images.githubusercontent.com/103022040/169693154-7d451a33-ad2b-44d2-82e1-49e4ece5f159.png)
- ### pull using following command
![image](https://user-images.githubusercontent.com/103022040/169693175-da31dba1-efeb-45da-8102-6235d0adebaf.png)

## *Jenkins Pipeline Integration to Harbor*
- ### go to jenkins and add a new pipeline 
![image](https://user-images.githubusercontent.com/103022040/169793826-85d16ae3-22de-4329-9e3c-2bad24356102.png)
- ### go to pipeline tab and write the script 
![image](https://user-images.githubusercontent.com/103022040/169952884-d07b15c2-dcc0-41ab-a3b2-7d3b24fd2c96.png)
- ### In the pipeline clone code from bit bucket
![image](https://user-images.githubusercontent.com/103022040/169801369-c1febae1-1c35-4e31-a837-f3da1509bc81.png)
- ### Build image using docker file and tag with a name
![tag harbor](https://user-images.githubusercontent.com/103022040/169952954-70e72baf-52d4-4214-b3f2-bc9651b02b87.JPG)
- ### Push the tag image to harbor repository 
![pushed harbor](https://user-images.githubusercontent.com/103022040/169801763-358d831e-921b-4cb8-a8e8-02c2f013b091.JPG)
- ### In the sudoers file give permission and open it with vi editor
![permission harbor](https://user-images.githubusercontent.com/103022040/169812492-12ffa425-ca1d-4490-b820-bb23932bb5ac.JPG)
- ### Change the highlighted line in vi editor 
![add edit line permission](https://user-images.githubusercontent.com/103022040/169802741-2ba571a0-f577-4e15-9d90-51e4ca4e1aa9.JPG)
- ### Go to pipeline and click on build now
![image](https://user-images.githubusercontent.com/103022040/169802808-3be0d19b-a813-48d9-9963-53059f75357b.png)
- ### Pipeline run successful 
![harbor pipeline](https://user-images.githubusercontent.com/103022040/169802936-831bf5d6-b57d-44b0-a929-89d570d56ac1.JPG)
- ### One can verify that in harbor ui with latest tag
![image](https://user-images.githubusercontent.com/103022040/169803257-4052a6cb-40c5-4216-9b00-1878f8a57aba.png)


