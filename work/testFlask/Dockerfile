#
# Format of Dockerfile
# [INSTRUCTION] [ARGUMENT]
# e.g. [RUN] [apt-get update]
#

# Layer 1. Base Ubuntu layer (~120MB~?)
# OS - Ubuntu 16.04
FROM ubuntu

# Layer 2. Changes in apt packages (306MB)
# Update apt repo 
# Install dependencies using apt
RUN apt-get update
# Install Python dependencies using pip
RUN apt-get install python -y
RUN apt-get install python3 -y

# Layer 3. Changes in pip packages (6.3MB)
# Install Flask using pip
RUN pip install flask
RUN pip install flask-mysql

# Layer 4. Source code (229B)
# Copy source code to /opt folder
COPY . /opt/source-code

# Layer 5. Update Entrypoint with "flask" command (0B)
# Run the web server using "flask" command
ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask run


