# Static-Website-Deployment-on-AWS

step 1: create a unique bucket and upload all the required files such as index.html,error.html,css,images in a structured order for a static website into bucket.

```
/website
 ┣ index.html
 ┣ about.html
 ┣ /css
 ┃   ┗ style.css
 ┣ /js
 ┃   ┗ app.js
 ┗ /images
     ┗ logo.png
```

![image](https://github.com/user-attachments/assets/e563a3d7-de4d-4a1b-9013-ca6e8d08cf21)

![image](https://github.com/user-attachments/assets/cef5f639-6f17-46bd-88f0-1e9f22ac75fa)

step 2: while creating bucket, we have to enable bucket versioning and turn off **block all public access** option

step 3: In Permission tab, apply bucket policy so that we can have required permissions alone to that bucket using Policy Generator. Just copy the satements and apply in bucket policy space.

![image](https://github.com/user-attachments/assets/27d856e0-dd4c-4bdf-bfff-0e7db22538d5)

step 4: Enable the **static website hosting** in properties column, and using **Bucket website endpoint** URL , you can access it in public.

![image](https://github.com/user-attachments/assets/d4416623-ef94-496d-9600-92138399da67)

First Page:
![image](https://github.com/user-attachments/assets/18dc4e85-5462-4f7e-b8c2-57b468f8b33e)

second Page:
![image](https://github.com/user-attachments/assets/64f2aa97-d02a-42a6-9060-6d5e403ae3ea)

Step 5: Creating CloudFront Distribution:

Created a cloudFront Distribution and set the S3 website endpoint as the origin.

![image](https://github.com/user-attachments/assets/b1af7786-e9b9-4f05-bc12-a556369cbd04)

![image](https://github.com/user-attachments/assets/f4c76bcb-21c0-4165-9f4f-0e59061dff89)

choose origin as specified bucket name and origin path as "/index.html"

step 6: Add AWS WAF(optional)

Integrated AWS WAF for security (optional).

![image](https://github.com/user-attachments/assets/278654e3-7a9c-4938-80d0-69e7926246c4)

Step 7: Review & create distribution

![image](https://github.com/user-attachments/assets/26c5eea2-4915-485d-9a3a-223f846c85bf)

Step 8: Deploying and Acessing Website Via CloudFront.

After deploying,  place the Generated Domain  **Distribution domain name** https://dzlorc2dsejjd.cloudfront.net globally.

![image](https://github.com/user-attachments/assets/04c59f29-feaf-4fd0-afbf-7e732d1ff53e)

![image](https://github.com/user-attachments/assets/5b09282f-b8a8-4744-8bac-09f08fe845c9)

![image](https://github.com/user-attachments/assets/5b240ed1-7eb6-443b-8bd8-ada9884cbede)

Tip: In Origin settings, you have to use website endpoint instead of bucket endpoint.

![image](https://github.com/user-attachments/assets/26fb993d-c4a8-406c-b5d5-6f6c3098dc79)

![image](https://github.com/user-attachments/assets/7971eb71-3eb0-476b-a2eb-87bb1056dc6d)

Protocol: HTTP Port:80


