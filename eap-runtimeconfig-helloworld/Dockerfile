FROM registry.redhat.io/jboss-eap-7/eap74-openjdk8-openshift-rhel7:7.4.1

# COPY JAR TO /deployments/ dir
COPY ./target/helloworld-ssl.war /deployments

EXPOSE 8443

USER root
RUN chown -R jboss:root $JBOSS_HOME && chmod -R ug+rwX $JBOSS_HOME
USER jboss
CMD $JBOSS_HOME/bin/openshift-launch.sh
