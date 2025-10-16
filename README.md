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

Isso deve iniciar o processo de configuração e, quando aplicável, iniciar o servidor web que utiliza PHP.

## Instalação em Termux (Android)

No Termux, os nomes de pacotes podem variar. Um fluxo comum é:

```bash
pkg update && pkg upgrade -y
pkg install php openssh git wget -y
cd CamPhish
bash camphish.sh
```

## Observações importantes

* Se o script reclamar que "PHP não está instalado", confirme a versão do PHP com `php -v` e verifique se o binário está no PATH.
* Se o projeto requer módulos PHP adicionais (por exemplo `php-curl`, `php-mbstring`, `php-xml`), instale-os com `apt-get install php-curl php-mbstring php-xml` (ou o equivalente para sua distribuição).
* Se for executar em servidor remoto e precisar acessar via SSH, certifique-se que o servidor SSH esteja em execução (`systemctl status ssh` / `service ssh status`) e que portas necessárias estejam liberadas no firewall.

## Como adicionar imagens (captura pela câmera)

Se o seu projeto permite capturar fotos com a câmera e adicionar imagens, coloque aqui instruções específicas sobre:

* permissões necessárias (ex: permissões do navegador ou do app),
* endpoints para upload de imagens (se existir um backend PHP recebendo `multipart/form-data`),
* caminhos de armazenamento das imagens no servidor.

(Adapte esta seção conforme seu código: indique o arquivo responsável pelo upload, as rotas e exemplos de `curl` para enviar imagens.)

## Exemplo rápido de upload via `curl`

```bash
curl -X POST -F "photo=@/caminho/para/foto.jpg" https://seu-servidor/exemplo_upload.php
```

## Segurança

* Nunca aceite uploads sem validar o tipo MIME e extensão do arquivo.
* Verifique o tamanho máximo do arquivo e filtre extensões perigosas.
* Evite gravar arquivos diretamente com o nome enviado pelo usuário — gere nomes únicos (hash + timestamp).
* Se usar o servidor PHP embutido para testes (`php -S 0.0.0.0:8080`), lembre-se: é somente para desenvolvimento, não para produção.

## Licença

Adicione aqui a licença do seu projeto (ex: MIT, GPL, etc.).

---

Se quiser, eu posso:

* gerar uma versão curta para mostrar diretamente no GitHub (com emojis e estilo),
* adaptar o texto para um README `README.md` já existente (fazer um diff),
* criar exemplos de código PHP para o endpoint de upload.

Diga qual opção prefere e eu já edito aqui mesmo.
