# NGINX_PASSOAPASSO
Passo a passo para instalação do Serviço NGNIX

#### 1. Introdução 
- Mencione os tópicos que serão abordados:
  - Instalação do NGinx.
  - Alteração da porta padrão.
  - Localização do diretório `www`.
  - Criação de uma página HTML simples.

---

#### 2. Instalação do NGinx
- Mostre como instalar o NGinx em um sistema baseado em Debian/Ubuntu:
  ```bash
  sudo apt update
  sudo apt install nginx
  ```
- Explique o que cada comando faz.
- Verifique se o NGinx está rodando:
  ```bash
  sudo systemctl status nginx
  ```

---

#### 3. Alteração da Porta Padrão
- Explique que a porta padrão do NGinx é a 80, mas que pode ser alterada por questões de segurança ou para evitar conflitos.
- Edite o arquivo de configuração do NGinx:
  ```bash
  sudo nano /etc/nginx/sites-available/default
  ```
- Localize a linha `listen 80;` e altere para outra porta, por exemplo, `listen 8080;`.
- Reinicie o NGinx para aplicar as mudanças:
  ```bash
  sudo systemctl restart nginx
  ```
- Teste o acesso ao servidor usando a nova porta (ex: `http://localhost:8080`).

---

#### 4. Caminho do Diretório `www`
- Explique que o diretório padrão do NGinx para arquivos HTML é `/var/www/html`.
- Mostre como acessar e listar os arquivos nesse diretório:
  ```bash
  cd /var/www/html
  ls
  ```
- Crie um arquivo HTML de exemplo:
  ```bash
  sudo nano /var/www/html/index.html
  ```

---

#### 5. Criando um Código HTML Simples
- No arquivo `index.html`, insira o seguinte código:
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TUX DICAS</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }
        h1 {
            font-size: 3rem;
            color: #333;
            font-weight: bold;
            margin-top: 20px;
        }
        p {
            font-size: 1.75rem;
            color: #666;
            text-align: center;
            margin-top: 20px;
        }
        .penguin-gif {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div>
        <h1>TUX DICAS</h1>
        <p>Aqui você encontra dicas e tutoriais sobre Linux e tecnologia!</p>
        <div class="penguin-gif">
            <img src="https://mysanrensei.wordpress.com/wp-content/uploads/2014/04/penguin-makes-himself-as-present.gif" alt="Pinguim andando">
        </div>
    </div>
</body>
</html>

  ```
- Salve o arquivo e feche o editor.
- Acesse o servidor no navegador para ver o resultado.

---

#### 6. Conclusão
- Recapitule o que foi feito no vídeo:
  - Instalação do NGinx.
  - Alteração da porta padrão.
  - Localização do diretório `www`.
  - Criação de uma página HTML simples.
- se inscreverem no canal e deixarem sugestões para os próximos vídeos.

