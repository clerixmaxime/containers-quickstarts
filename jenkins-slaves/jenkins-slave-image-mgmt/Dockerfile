FROM registry.access.redhat.com/openshift3/jenkins-slave-base-rhel7

MAINTAINER Andrew Block <ablock@redhat.com>

LABEL com.redhat.component="jenkins-slave-image-mgmt" \
      name="jenkins-slave-image-mgmt" \
      architecture="x86_64" \
      io.k8s.display-name="Jenkins Slave Image Management" \
      io.k8s.description="Image management tools on top of the jenkins slave base image" \
      io.openshift.tags="openshift,jenkins,slave,copy"
USER root

RUN yum repolist > /dev/null && \
    yum install -y --enablerepo rhel-7-server-extras-rpms skopeo && \
    rpm -V skopeo && \
    yum clean all

USER 1001
