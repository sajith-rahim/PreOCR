FROM tesseractshadow/tesseract4re

RUN apt-get update && \
	apt-get -y upgrade && \
	apt-get -y install \
	python \
	python-pip

# Set the working directory to /app
WORKDIR /app

ADD ./requirements.txt /app/requirements.txt

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# expose port 8081
EXPOSE 8081
