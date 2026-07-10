# Laborat-rio-2---reconhecimento-de-rede-com-Nmap
Criação do primeiro laboratório de Pentest utilizando Kali Linux e Metasploitable 2.  Foram configuradas duas máquinas em uma rede interna do VirtualBox, definidos endereços IP manualmente e realizado um escaneamento com Nmap para identificação de portas abertas, serviços e versões.
# Laboratório 2 - Reconhecimento de Rede com Nmap

## Objetivo

Configurar uma rede interna entre o Kali Linux e a Metasploitable 2 e realizar o reconhecimento inicial da máquina alvo utilizando o Nmap.

---

## Ambiente

- VirtualBox
- Kali Linux
- Metasploitable 2
- Rede Interna (LAB_NET)

---

## Configuração da Rede

Como a rede interna não possui servidor DHCP, foi necessário configurar manualmente os endereços IP.

### Kali Linux

IP: 10.10.10.10

### Metasploitable 2

IP: 10.10.10.20

Após a configuração foi realizado um teste de conectividade utilizando o comando ping.

---

## Comandos Utilizados

Verificar interface de rede

```bash
ip a
```

ou

```bash
ifconfig
```

Configurar IP

```bash
sudo ifconfig eth0 10.10.10.10
```

Escanear a máquina alvo

```bash
nmap -sV 10.10.10.20
```

---

## Explicação dos comandos

### ip a

Mostra todas as interfaces de rede e seus respectivos endereços IP.

---

### ifconfig

Exibe informações detalhadas da interface de rede.

Também pode ser utilizado para configurar endereços IP manualmente.

---

### nmap -sV

Realiza um escaneamento da máquina alvo identificando:

- portas abertas
- serviços
- versões dos serviços

A opção **-sV** solicita que o Nmap descubra a versão dos serviços encontrados.

---

## Resultados

O Nmap identificou diversos serviços ativos, entre eles:

- FTP
- SSH
- Telnet
- HTTP
- Samba
- MySQL
- PostgreSQL
- Tomcat

Essas informações serão utilizadas nos próximos laboratórios para análise de vulnerabilidades e exploração controlada.

---

## O que aprendi

- Configurar uma rede interna no VirtualBox.
- Configurar IP manualmente.
- Testar conectividade entre máquinas.
- Utilizar o Nmap para reconhecimento.
- Identificar portas abertas.
- Identificar versões dos serviços.
- Entender a importância da fase de enumeração em um Pentest.


