FROM image-registry.openshift-image-registry.svc:5000/ls-aws-poc/ace-server-prod 
#FROM cp.icr.io/cp/appc/ace-server-prod:latest

ENV LICENSE "accept"

#Use root user
USER root

# Copy the BAR files to ace-server bars directory
COPY bars /home/aceuser/bars
RUN mkdir -p /home/aceuser/ls/pes/custom/input && mkdir -p /home/aceuser/ls/pes/custom/output
RUN chmod -R ugo+rwx /home/aceuser

#Use ace user
USER 1000
RUN ace_compile_bars.sh

#Use root user
USER root
RUN  chmod -R ugo+rwx /home/aceuser

#Use ace user
USER 1000