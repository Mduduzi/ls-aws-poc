FROM cp.icr.io/cp/appc/ace-server-prod:latest

ENV LICENSE "accept"

# Copy the jms jar files to ace-server common classes directory
# COPY jars/* /opt/ibm/ace-11/common/classes/

# Copy the BAR files to ace-server bars directory
#COPY --chown=aceuser bars /home/aceuser/bars
COPY bars /home/aceuser/bars

RUN ace_compile_bars.sh

# Expose ports.  7600, 7800, 7843 for ACE; 9483 for ACE metrics
#EXPOSE 7600 7800 7843 9483