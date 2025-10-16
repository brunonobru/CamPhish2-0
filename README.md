# CamPhish — Instruções de instalação e uso

> **Aviso rápido:** Esta ferramenta requer **PHP** para rodar o servidor web, além de **SSH** ou um link para servidor (se for utilizar em servidor remoto).

---

## Pré-requisitos

* Sistema Debian/Ubuntu/Kali ou Termux (Android).
* Acesso com privilégios de administrador (sudo/root) para instalar pacotes.
* Conexão com a internet para baixar dependências.

## Comandos de instalação (Debian / Kali / sistemas baseados em APT)

Abra um terminal e execute:

```bash
apt-get -y update
apt-get -y install php openssh-client git wget
```

> Observação: em algumas distribuições o pacote do `openssh` pode ter outro nome (`openssh-client` / `openssh-server`). Se precisar do servidor SSH (para conexões remotas), instale `openssh-server`.

## Instalação e execução do CamPhish

1. Navegue até a pasta do projeto:

```bash
cd CamPhish
```

2. Execute o script de instalação/execução (se houver):

```bash
bash camphish.sh
```

