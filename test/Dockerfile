FROM openmicroscopy/omero-server:5.6
MAINTAINER ome-devel@lists.openmicroscopy.org.uk

RUN cd /opt/omero/server/ && \
    /opt/omero/server/venv3/bin/omego download -q --release 5.6 server --sym auto

USER root

RUN /opt/omero/server/venv3/bin/python -m pip install pytest

USER omero-server

ENTRYPOINT ["bash"]
