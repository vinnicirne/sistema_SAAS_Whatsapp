# FRONTEND: URL_Frontend
# BACKEND: URL_Backend

# 
# INSTALAÇÃO AAPANEL VPS UNBUNTU 20.04  #

# 01) ``apt update && apt install uuid-dev libossp-uuid-dev -y && apt upgrade -y && reboot``

# 02) ``wget -O install.sh http://www.aapanel.com/script/install-ubuntu_6.0_en.sh && sudo bash install.sh aapanel``

# Do you want to install aaPanel to the /www directory now?(yes/n): yes

# Do you need to enable the panel SSl ? (yes/n): n

# 03) Instalar  NGINX 1.21.4 + ,  + Redis 7.0.11 e Linux Tools .
# 04) Instalar PM2 5.1 o Node sera instalado dentro do pm2 versão 14.21.3 // ATENÇÃOA VERSÃO DO NPM  9.6.2 ++
# 06) Instalar PostgreSQL Manager ( NÃO INSTALAR A VERSÃO APENAS O APP, SEGUIR PROCESSO ABAIXO)

# 07) Alterar o config do PostgreSQL para incluir a opção --with-uuid=ossp no ./configure (linha 95) do script localizado em      ``/www/server/panel/plugin/pgsql_manager/pgsql_install.sh ``

# 08) No PostgreSQL Manager, escolher a versão do PostgreSQL e mandar instalar

# 09) ABRA TERMINAL ``cd /usr/local/pgsql/contrib/uuid-ossp/``
 # ``make`` 

 # ``make install``

# ``ls –alh /www/server/pgsql/share/extension/``

# ``chown postgres.postgres  /www/server/pgsql/share/extension/uuid*``

# ``ls –alh /www/server/pgsql/share/extension/``

# 10) Upar e descompactar o .zip do seu Whaticket

# 11) Configurar .envs e dar

# 12) ``npm install --force && npm run build``

# 13) ``npm run db:migrate && npm run db:seed``

# 14) Ir no PM2 e criar os dois projetos (um para o backend e outro para o frontend)
# 15) Retirar o /dist/ da path do backend
# 16) Mapear ambos os projetos
# 17) Criar certificados SSL
# 18) Logar no Whaticket
##  ##ATENÇÃOA VERSÃO DO NPM  9.6.2 ##
## ========================================== ##
## CORRIGINDO WEBSOCKET ##
    proxy_set_header Upgrade $http_upgrade; 
    proxy_set_header Connection "Upgrade"; 
    proxy_http_version 1.1; 
## ============================================= ##
