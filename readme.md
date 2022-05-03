# FEEGOW

### AMBIENTE DE DESENVOLVIMENTO (Apache 2.4, PHP 7.2 e MySQL 5.7)

- XAMPP 7.2.34 [download](https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/7.2.34/xampp-windows-x64-7.2.34-2-VC15-installer.exe/download)
- MySQL 5.7 (.zip) [download](https://dev.mysql.com/downloads/file/?id=510458)
- HeidiSQL [download](https://www.heidisql.com/download.php)
- Git [download](https://git-scm.com/download/win)
- Composer [download](https://getcomposer.org/download/)
- NodeJS [download](https://nodejs.org/en/download/)

#### PASSO A PASSO PARA TROCAR O MARIADB PELO MYSQL5.7 NO XAMPP

> **ATENÇÃO! Este procedimento é indicado para instalações novas do XAMPP! Caso esteja fazendo em uma antiga e/ou que já
possua alguma base de dados, não esqueça de fazer os backups necessários**

- Instale o XAMPP
- Renomeie a pasta "C:\xampp\mysql" para "C:\xampp\mariadb" (ou exclua a pasta  "C:\xampp\mysql")
- Crie uma nova pasta "C:\xampp\mysql" vazia
- Extraia o conteúdo do arquivo "mysql-5.7.38-win32.zip" para a pasta "C:\xampp\mysql"
- Crie o arquivo "C:\xampp\mysql\bin\my.ini" com o conteúdo abaixo:

```
# c:/xampp/mysql/bin/my.ini
[mysqld]
# set basedir to your installation path
basedir=c:/xampp/mysql
# set datadir to the location of your data directory
datadir=c:/xampp/mysql/data
```

> **ATENÇÃO:** Lembre-se de que este tutorial é indicado para instalações novas do xampp. Caso esteja fazendo em uma
> instalação antiga e/ou que já possua alguma base de dados, não esqueça de fazer os backups necessários de dados antes
> da próxima etapa!

- Esvazie a pasta "C:\xampp\mysql\data"
- Abra o prompt de comando com privilégios de administrador
- Execute o seguinte comando:

```
c:\xampp\mysql\bin\mysqld --initialize-insecure
```

- Abra o Painel de Controle do Xampp
- Inicie o Apache e o MySQL

> NOTA: Inicie o Painel de Controle do Xampp como administrador caso queira instalar o Apache e o MySQL como serviços do
> Windows.

![img_1.png](img_1.png)

Pronto, o Xampp agora vai iniciar o MySQL na versão 5.7.38.
![img_2.png](img_2.png)
