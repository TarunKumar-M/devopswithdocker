# Start with ubuntu 20.04 image
FROM ubuntu:20.04

# Set working dir to /tmp
WORKDIR /tmp

# Copy the script.sh file from this location to /tmp creating /tmp/script.sh
COPY script.sh .

# Install curl into the image
RUN apt-get update && apt-get install -y curl

# Add execute permission to script
RUN chmod +x script.sh

# When running docker run the command will be ./script.sh
CMD ./script.sh
