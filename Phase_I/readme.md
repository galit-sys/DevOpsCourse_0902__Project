# NEW Web description:

A very base "Hello World" web site based on python flask module

How to Run:
# Build the image
docker build -t galitoshri/webapp:1.1 .

# Run the container 
docker run -p 5000:5000 -d galitoshri/webapp:1.1

# Run the app
Open Browser on http://localhost:5000

# Run with mount
docker run -d -p 5000:5000 -v $(pwd):/app galitoshri/webapp:1.1

