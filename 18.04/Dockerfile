FROM ubuntu:18.04
RUN useradd -ms /bin/bash tina
RUN passwd -d tina
RUN usermod -a -G sudo tina
RUN apt-get update \ 
 && apt-get install --no-install-recommends git-core python build-essential libncurses5-dev zlib1g-dev libssl-dev gawk unzip wget bc lsof  busybox lib32z1 lib32z1-dev lib32stdc++6 gpgv2 sudo openssl file rsync -y \
 && apt-get upgrade -y \ 
 && rm -rf /var/lib/apt/lists/*
USER tina
WORKDIR /home/tina
CMD [ "/bin/bash" ]
