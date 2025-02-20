"# Web_hook" 

Step 1: Set up Node server
  1.Install Node.js and npm:
    Download and install Node.js from nodejs.org.
    
  2.Create a new Node.js project:
  
mkdir webhook-server
cd webhook-server
npm init -y

  3.Install Express:
  
npm install express body-parser

Step 2: Set Up React Frontend
 1.Create React app

npx create-react-app webhook-client
cd webhook-client

 2.Start the React app:
npm start

Step 3: Test the Webhook
Using Postman:
    Set the request method to POST.
    Enter the URL: http://localhost:3001/webhook.
Add a JSON body, e.g.:
    {
  "event": "user_signup",
  "user_id": 123,
  "email": "test@example.com"
}

Using curl:
curl -X POST http://localhost:3001/webhook \
-H "Content-Type: application/json" \
-d '{"event": "user_signup", "user_id": 123, "email": "test@example.com"}'


