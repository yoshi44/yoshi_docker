from sjfloat/haskell_7.10.2

run sudo apt-get update
run echo "mysql-server mysql-server/root_password password root" | sudo debconf-set-selections && \
    echo "mysql-server mysql-server/root_password_again password root" | sudo debconf-set-selections && \
    sudo apt-get -y install mysql-server
run sudo apt-get -y install libghc-pcre-light-dev
run sudo apt-get install libmysqlclient-dev
run sudo apt-get install pkg-config
run sudo apt-get install git

run cd && git clone https://github.com/yoshi44/yesod-api.git
run cd ${HOME}/yesod-api && stack setup && stack install yesod-bin cabal-install --install-ghc
run cd ${HOME}/yesod-api && stack build

expose 4444

