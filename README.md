# ITIS_6177_Final_Project- Computer Vision API - Optical Character Recognition

A simple OCR Application using Computer Vision API. OCR(Optical Character Recognition) converting images with printed or handwritten text into machine-encoded text.

Application URL:- http://147.182.218.164:3000/


To create an API on Microsoft Azure:

1. Create an account and log in to the Azure portal.
2. Create a new resource to manage the API.
3. Choose a specific API, such as Computer Vision API.
4. Link the API to the resource created in step 2.
5. Obtain the unique API Keys and endpoints to access the API.
6. The API endpoints that are leveraged are POST Read and GET Read Result(Explained further)


Prerequisites for the Project.
1. An Azure subscription
2. Node.js
3. Create your Azure subscription, create a Computer Vision resource in the Azure portal to get your key and endpoint. You will need the key and endpoint from the resource you create to connect your application to the Computer Vision service. 
4. Paste the API_KEY in the .env file so that it is not exposed in your server-side code.
5. Endpoints:-
curl -v -X POST "https://eastus.api.cognitive.microsoft.com/vision/v3.2/read/analyze"
curl -v -X GET "https://eastus.api.cognitive.microsoft.com/vision/v3.2/read/analyzeResults/{Operation ID}"

Testing the Application on UI:-
1. Go to the browser. Hit the URL http://147.182.218.164:3000/
2. Enter the image url in the Text Box. Click Submit. Example:- https://images.pexels.com/photos/2681319/pexels-photo-2681319.jpeg?cs=srgb&dl=pexels-ivan-bertolazzi-2681319.jpg&fm=jpg
3. Click on Extract Text.
4. Example images: 
https://images.pexels.com/photos/2681319/pexels-photo-2681319.jpeg?cs=srgb&dl=pexels-ivan-bertolazzi-2681319.jpg&fm=jpg

https://blog.hubspot.com/hs-fs/hubfs/quotes-on-life-14-maya-angelou.jpg?width=650&height=545&name=quotes-on-life-14-maya-angelou.jpg

https://algodocs.com/assets/img/articles/2021-10-14/handwritten-text-1.jpg


Testing on Postman:-
1.	Copy the url of the application http://147.182.218.164:3000/in Postman. Select the post request. In headers add Ocp-Apim-Subscription-Key : “your-subscription-key” and Content-Type: “Application/json”. In body, select x-www-form-urlencoded, add image as key and in value – image url. Click on send.
2.	If Image is supported, you will see 200 response. You can get the ID which will required for GET request in ‘action’ inside form in response body.
3.	Change the request type to GET and copy the ID in http://147.182.218.164:3000/:id 
example:- http://147.182.218.164:3000/ee989055-6529-4af9-a16a-c86ed43300fd

How to run the project locally.
1. Create an Computer Vision Azure Resource and get the API_KEY.
2. git clone https://github.com/tpatil6uncc/ITIS_6177_Final_Project.git
3. npm install
4. paste your API_KEY in .env file.


