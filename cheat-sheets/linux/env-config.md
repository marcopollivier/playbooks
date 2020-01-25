# Configurações Ambiente Linux

**Criar link simbolico**
```sh
ln -s /usr/lib/jvm/latest /usr/lib/jvm/jdk1.7.0_40/
```

**Local para configuração de atalhos em sistemas baseados no Ubuntu (não sei se é universal, mas acredito que sim)**
```
/usr/share/applications
```

**/etc/bash.bashrc**
```
#USADO PELO JAVA
export JAVA_HOME="/usr/lib/jvm/latest"
export PATH=$PATH:$JAVA_HOME/bin

#USADO PELO MAVEN
M2_HOME=/usr/local/maven
M2=$M2_HOME/bin
PATH=$M2:$PATH

#USADO PELO JRUBY
export JRUBY_HOME="/opt/softwares/jruby"
export PATH=$PATH:$JRUBY_HOME/bin

#Completar codigo para o Rails
source /home/contfausto/rails.bash


export SONAR_RUNNER_HOME=/opt/softwares/sonar-3.5.1/sonar-runner-2.2
export PATH=$PATH:$SONAR_RUNNER_HOME/bin
```

**/etc/environment**
```
http_proxy="http://USUARIO:SENHA@PROXY:PORTA/"
https_proxy="https://USUARIO:SENHA@PROXY:PORTA/"
ftp_proxy="ftp://USUARIO:SENHA@PROXY:PORTA/"
```

**/etc/apt/apt.conf**
```
Acquire::http::proxy "http://USUARIO:SENHA@PROXY:PORTA/";
Acquire::https::proxy "https://USUARIO:SENHA@PROXY:PORTA/";
Acquire::ftp::proxy "ftp://USUARIO:SENHA@PROXY:PORTA/";
```
