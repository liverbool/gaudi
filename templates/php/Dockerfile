FROM stackbrew/debian:wheezy

[[ updateApt ]]
[[ addUserFiles ]]

WORKDIR [[ .Container.GetFirstMountedDir ]]

# Install PHP 5.6
RUN apt-get -y -f install php56 php56-mysql php56-mcrypt php56-curl curl php56-intl

# Add custom setup script
[[ beforeAfterScripts ]]

CMD [[ if (.Container.HasAfterScript) ]] /bin/bash /root/after-setup.sh && [[end]] /bin/bash
