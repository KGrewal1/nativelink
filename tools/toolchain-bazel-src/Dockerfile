# Copyright 2022-2024 The NativeLink Authors. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

FROM ubuntu:22.04@sha256:f9d633ff6640178c2d0525017174a688e2c1aef28f0a0130b26bd5554491f0da

# Set shell to bash and enable pipefail
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# Get Ubuntu packages
# hadolint ignore=DL3015
RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
    gcc=4:11.2.0-1ubuntu1 \
    g++=4:11.2.0-1ubuntu1 \
    python3=3.10.6-1~22.04 \
    python3-minimal=3.10.6-1~22.04 \
    libpython3-stdlib=3.10.6-1~22.04 \
    curl=7.81.0-1ubuntu1.17 \
    ca-certificates=20230311ubuntu0.22.04.1 \
    git=1:2.34.1-1ubuntu1.11 \
    unzip=6.0-26ubuntu3.2 \
    openjdk-21-jdk=21.0.4+7-1ubuntu2~22.04 \
    zip=3.0-12build2 \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Find out whats missing:
# apt install npm
# npm install -g @bazel/bazelisk
# git clone https://github.com/adam-singer/bazel.git && cd bazel
# bazel build //src:bazel-dev
