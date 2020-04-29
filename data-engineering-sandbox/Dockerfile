FROM ubuntu:latest
MAINTAINER Flavien Jarry "flavien.jarry31@gmail.com"

RUN apt-get update && apt-get install -y vim python3 python3-pip git && pip3 freeze > requirements.txt && pip3 install jupyter && mkdir workspace && cd workspace && git config --global user.name "flavja" && git config --global user.email "flavien.jarry31@gmail.com"

WORKDIR workspace/
COPY . workspace/
RUN git clone https://github.com/flavja/FormationPython.git myGit
EXPOSE 8000
CMD ["jupyter", "notebook", "--port=8080", "--no-browser", "--ip=0.0.0.0", "--allow-root"]
