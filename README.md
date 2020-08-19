# selenoid-ggr-docker-compose
Ggr + Selenoid + Selenoid UI 

The purpose of this repository is to create Aurokube's Ggr + Selenoid + Selenoid UI on the same instance with single docker-compose.yml file

Steps to install:
  - sudo apt-get install apache2-utils (this is needed for htpasswd working)
  - Create configuration directory:
`    mkdir -p /etc/grid-router/quota`
  - Create users.htpasswd file:
`    htpasswd -bc /etc/grid-router/users.htpasswd test test-password`
  - copy etc/grid-router-quota/text.xml to configuration directory
  - start containers:
`    docker-compose up --force-recreate -d
