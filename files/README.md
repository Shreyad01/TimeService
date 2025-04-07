# SimpleTimeService
### Overview
SimpleTimeService is a lightweight Python microservice that returns the current timestamp and the IP address of the visitor in JSON format.
### Features
- Returns the current timestamp in UTC format.
- Captures the visitor's IP address.
- Runs as a non-root user inside a Docker container.

### Steps
- Create simple microservice in python
[simple_time_service.py](simple_time_service.py)

- Create requirements.txt file to store require files
  
  ![alt text](image1.png)


- write Dockerfile and install the dependencies 

  ![alt text](image2.png)

- Execute the *Simple_time_service.py* file.

  ![alt text](image3.png)

-Visit http://127.0.0.1:6000 in your browser or use curl http://127.0.0.1:6000

  ![alt text](image4.png)

- Build the docker image by running following command :

      docker build -t simpletimeservice .

  ![alt text](image5.png)
  ![alt text](image6.png)

- Run the container by using following command :
    
      docker run -p 6000:6000 simpletimeservice 

  ![alt text](image7.png)

- Access the Service by using following command :
        
        Visit http://localhost:6000/ in your browser or 
        use curl http://localhost:6000
  
   ![alt text](image4-1.png)

- Login to **DockerHub** by using username and password

       docker login 

    ![alt text](image8.png)
- Tag and push image to **DockerHub**
   
      docker tag simpletimeservice <your-dockerhub-username>/  simpletimeservice:latest

      docker push <your-dockerhub-username>/simpletimeservice:latest

   ![alt text](image9.png) 

