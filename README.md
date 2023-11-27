# CircleW_AdvanceITSkillProgram-Assignment-T3-Class5
### Task3: Deploy Django Application on AWS

### Step1: Create a github repository and push Django project from local repository to newly created remote repository

Run following commands on local project to push on github:
- git init
- git remote add origin https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5.git
- git pull origin master --allow-unrelated-histories
- git push -u origin master

![image](https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5/assets/42076770/90fa9d3d-758a-4c79-8a0b-f8cf775ff49e)

### Step2: Create AWS EC2 instance and connect with it using SSH

- Instance created
  
![image](https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5/assets/42076770/95457043-5ae3-4e92-8ed8-67e659776489)<br>

- Connect with VM using SSH</br>

![image](https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5/assets/42076770/b25d5e62-23df-47b5-843d-62af518245c3)

###  Step3: Clone repository that contains Django project

Clone repository
- git clone https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5.git
  
![image](https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5/assets/42076770/48e24e47-a708-4c66-950d-52d5ee7bc5b5)

###  Step4: Install Pip and Django then Start Django server

Run following commands to install pip and django
- sudo apt install python3-pip
- pip3 install django
</br>

- In EC2 Instaces's security configuration add new inbound rule to allow incoming requests from anywhere on port 8001.

![image](https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5/assets/42076770/c5edce69-5bc2-4572-ae9c-87dfb98e2c85)

- In settings.py add "*" in ALLOWED_HOSTS

Run following commands to start Django server:
- python3 manage.py migrate
- python3 manage.py runserver 0.0.0.0:8001
</br>

- Server started successfuly
</br>

![image](https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5/assets/42076770/5d4aae93-1cac-41d9-9b61-5d995454bb69)

![image](https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5/assets/42076770/19056cfb-8df0-4e18-9538-701c422c326c)

### Step5: Deploy Django project using Docker
- Install Docker 'sudo apt install docker.io'
- Create docker-deploy.sh file that will automatically create docker image and run container
  ![image](https://github.com/ZuraizAhmedShehzad/CircleW_AdvanceITSkillProgram-Assignment-T3-Class5/assets/42076770/f444c899-0f84-4bb8-8612-e6e5e7527067)
 
