Prerequisites
Before running the project, ensure you have the following installed on your system:

Java 17+
Maven
MongoDB (running locally or a cloud instance like MongoDB Atlas)
Postman (optional, for testing API endpoints)
🛠 Steps to Run
Clone the repository

sh
Copy
Edit
git clone https://github.com/your-username/your-repo.git  
cd your-repo
Configure MongoDB

If running MongoDB locally, ensure it is started on port 27017 (default).

If using a cloud database (MongoDB Atlas), update the connection string in application.properties or application.yml:

ini
Copy
Edit
spring.data.mongodb.uri=mongodb+srv://<username>:<password>@cluster0.mongodb.net/<dbname>?retryWrites=true&w=majority
Build the project

sh
Copy
Edit
mvn clean install
Run the application

sh
Copy
Edit
mvn spring-boot:run
or

sh
Copy
Edit
java -jar target/your-app-name.jar
Verify API is running

Open your browser or Postman and visit:
bash
Copy
Edit
http://localhost:8080/api/health
This should return a success message.
Using the API

Use Postman or a frontend client to interact with the endpoints.
API documentation (if applicable) will be available at:
bash
Copy
Edit
http://localhost:8080/swagger-ui.html
Stop the application

Press Ctrl + C in the terminal
If running as a background process, find the process ID and kill it:
sh
Copy
Edit
lsof -i :8080  # Find process  
kill -9 <PID>  # Kill process
