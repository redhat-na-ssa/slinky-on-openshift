ARG PARENT_IMAGE=scratch
FROM ${PARENT_IMAGE}

RUN <<EOR
# Install hpc dev env
set -xeuo pipefail
dnf -q makecache --refresh
# https://spack.readthedocs.io/en/latest/getting_started.html
dnf -q -y group install "Development Tools"
dnf -q -y install libtool gcc-gfortran gcc-toolset-12 \
    python3 procps-ng git vim-enhanced hostname man-db hwloc iproute
dnf clean all
EOR
