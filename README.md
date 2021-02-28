## SISTEMA DE CADASTRO DE PESSOAS
  
### O sistema faz cadastro, Listagem de dados(falta finalisar).

## Tecnologia Ultilizada:

### Banco de dados: 
MYSQL
  
### Liguagem de Programação:
Java

### IDE: 
NetBeans   


### Validações :

O sistema conta com validações , que foram feita ultilizando Exceptions Personalizadas.
Dentre elas: Verifica o cadastro dos dados registrado no banco.  

Script da tabelas do banco:

CREATE TABLE `usuario` (
  `id` bigint(10) NOT NULL AUTO_INCREMENT,
  `nome` varchar(255) DEFAULT NULL,
  `sobrenome` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`id`)


CREATE TABLE `salas` (
  `idsala` bigint(10) NOT NULL AUTO_INCREMENT,
  `sala` varchar(255) DEFAULT NULL,
  `idusuario` bigint(10) DEFAULT NULL,
  PRIMARY KEY (`idsala`),
  KEY `fk_usuario` (`idusuario`),
  CONSTRAINT `fk_usuario` FOREIGN KEY (`idusuario`) REFERENCES `usuario` (`id`)

CREATE TABLE `espaco` (
  `idespaco` bigint(10) NOT NULL AUTO_INCREMENT,
  `nomeespaco` varchar(255) DEFAULT NULL,
  `idusuario` bigint(10) DEFAULT NULL,
  PRIMARY KEY (`idespaco`),
  KEY `fk_usuario1` (`idusuario`),
  CONSTRAINT `fk_usuario1` FOREIGN KEY (`idusuario`) REFERENCES `usuario` (`id`) 



