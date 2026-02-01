FROM python:3.14-trixie

# Copy requirements
COPY requirements.txt /opt/requirements.txt

# Install Python dependencies
RUN set -e && \
    python -m pip install --upgrade --root-user-action ignore \
    pip \
    setuptools \
    wheel && \
    python -m pip install --root-user-action ignore -r /opt/requirements.txt

# Set default command
ENTRYPOINT ["python"]

# Labels
LABEL org.opencontainers.image.authors="Yishen Miao <mys721tx@gmail.com>"
LABEL org.opencontainers.image.version="1.12.0"
LABEL org.opencontainers.image.description="This image contains Scanpy and its \
    dependencies installed on top of the Python 3.14 Trixie image."
