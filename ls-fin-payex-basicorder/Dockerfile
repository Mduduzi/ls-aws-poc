FROM image-registry.openshift-image-registry.svc:5000/ls-aws-poc/ace-server-prod 
#FROM cp.icr.io/cp/appc/ace-server-prod:latest

ENV LICENSE "accept"

# Copy the BAR files to ace-server bars directory
RUN mkdir -p /home/aceuser/ls/pes/custom/input
RUN mkdir -p /home/aceuser/ls/pes/custom/output

COPY bars /home/aceuser/bars

RUN ace_compile_bars.sh
