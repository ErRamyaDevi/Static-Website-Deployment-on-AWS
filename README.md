# Static-Website-Deployment-on-AWS

step 1: create a unique bucket and upload all the required files such as index.html,error.html,css,images for a static website into bucket.
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

