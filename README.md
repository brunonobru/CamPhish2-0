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

## Adicionando imagens de teste

Você pode adicionar uma foto de teste no README para mostrar como funciona a captura de imagens:

```markdown
![Foto de teste](https://play-lh.googleusercontent.com/g7fyKspePb-etgdff7NSZSfV4uWMQtCEir6dejMfsyQBzw0AlayloikSouOXVQj6Tva-=w240-h480-rw)
```

> Coloque sua imagem dentro da pasta `images` do projeto com o nome `teste.jpg`.

Exemplo de visualização:

![Foto de teste](https://via.placeholder.com/150)

## Segurança

* Nunca aceite uploads sem validar o tipo MIME e extensão do arquivo.
* Verifique o tamanho máximo do arquivo e filtre extensões perigosas.
* Evite gravar arquivos diretamente com o nome enviado pelo usuário — gere nomes únicos (hash + timestamp).
* Se usar o servidor PHP embutido para testes (`php -S 0.0.0.0:8080`), lembre-se: é somente para desenvolvimento, não para produção.

## Licença

Adicione aqui a licença do seu projeto (ex: MIT, GPL, etc.).
