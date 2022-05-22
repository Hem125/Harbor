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
