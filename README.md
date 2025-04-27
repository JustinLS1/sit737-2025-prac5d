# sit737-2025-prac5d

Step 1: Use credentials that has been given through school mail inbox durting first week

Step 2: Go to google cloud platform

Step 3: Login with school email and use the guide provided in email "Getting started with GCP"

Step 4: Create container registry under CI/CD in all products on GCP

Step 5: Install the needed APIs for it

Step 6: It navigates to Artifact Registry and create a repository "sit737-2025-prac5d" for the images to sit in

Step 7: Clone the 5.1p task into a new repo "sit737-2025-prac5d"

Step 8: I did a lot of research on how to do this task and used this "https://cloud.google.com/artifact-registry/docs/docker/store-docker-container-images?authuser=1&_gl=1*nmw465*_ga*MTQ5ODcwMDc4OS4xNzQzNzg0MDE4*_ga_WH2QY8WWF5*MTc0NTc1MzA5Ny4yLjEuMTc0NTc1Njg2MS42MC4wLjA.#console" as my guide for the task.

Step 9: Since I made the repo already in GCP, I proceeded to building a new image into local docker desktop "sit737-2025-prac5d:latest"

Step 10: I ran the image to check whether the image was working as expected and it was running using local image

Here is where I got stumped a bit. I had originally used australia-southeast2 as my region when buiilding the repo but i was getting all sorts of errors and just followed the guide which used us-west1 (Oregon) to remove any headaches

Step 11: I had to install gcloud CLI for docker and GCP to communicate with each other

Step 12: I had to login my account to gcloud CLI using "gcloud auth login"

Step 13: It showed that i had logged into my GCP by providing my project ID

Step 14: I had to set the authentication to docker repo using "gcloud auth configure-docker us-west1-docker.pkg.dev"

Step 15: After building the image, I had to tag it with the repo name "docker tag sit737-2025-prac5d:latest us-west1-docker.pkg.dev/sit737-25t1-sutanto-2e72199/sit737-2025-prac5d/sit737-2025-prac5d:latest"

Step 16: After tagging the image, I pushed the image into GCP using "docker push us-west1-docker.pkg.dev/sit737-25t1-sutanto-2e72199/sit737-2025-prac5d/sit737-2025-prac5d:latest"

Step 17: After the image is inserted into GCP and artifact registry, next to do is to run it from that repo

Step 18: To test the image in GCP, I used "docker run -d -p 3000:3000 --name sit737-2025-prac5d us-west1-docker.pkg.dev/sit737-25t1-sutanto-2e72199/sit737-2025-prac5d/sit737-2025-prac5d" to run it

Step 19: After running the command, the localhost:3000 is outputting all functions while pulling the image from GCP

All screenshots are in the submitted document.