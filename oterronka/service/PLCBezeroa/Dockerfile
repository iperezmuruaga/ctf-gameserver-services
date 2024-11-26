FROM ubuntu:latest
RUN sudo apt install python3.10-venv
RUN python3 -m venv /home/isard/Descargas/ctf-gameserver-services/oterronka/service/PLCBezeroa/VirtualPath
RUN source .venv/bin/activate
RUN get checkout master

RUN git clone git://github.com/pymodbus-dev/pymodbus.git
RUN cd pymodbus
RUN pip3 install -r requirements.txt

RUN cd 






