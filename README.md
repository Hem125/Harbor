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
