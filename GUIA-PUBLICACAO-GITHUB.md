# Publicar o portfólio no GitHub Pages

Este projeto usa um único arquivo principal (`index.html`). O diretório `certificados/` guarda os PDFs.

## 1. Preparar a pasta
1. Baixe e extraia o arquivo ZIP do projeto.
2. Abra a pasta `portfolio-certificacoes`.
3. Confira se `index.html` está diretamente dentro dessa pasta, e não dentro de outra pasta duplicada.
4. Não altere o nome `index.html`. O GitHub Pages usa esse arquivo como entrada do site.

## 2. Visualizar localmente antes de publicar

1. Abra um terminal/PowerShell dentro da pasta `portfolio-certificacoes`.
2. Execute `py -m http.server 8000` (se o comando `py` não existir, tente `python -m http.server 8000`).
3. Abra `http://localhost:8000` no navegador.
4. Para encerrar o servidor, volte ao terminal e pressione `Ctrl+C`.

Use um servidor local em vez de abrir o arquivo com duplo clique: assim o navegador consegue verificar se os PDFs existem na pasta.

## 3. Criar o repositório
1. Entre em https://github.com e faça login.
2. Clique em **New repository**.
3. Dê o nome `portfolio-certificacoes`.
4. Escolha **Public** (no GitHub Free, o Pages exige repositório público).
5. Clique em **Create repository**.

## 4. Enviar os arquivos
1. No repositório recém-criado, clique em **Add file → Upload files**.
2. Envie o conteúdo da pasta do projeto: `index.html`, `README.md`, `GUIA-PUBLICACAO-GITHUB.md`, `.nojekyll` e a pasta `certificados/` com `LEIA-ME.txt` e `.gitkeep`.
3. Confirme que `index.html` aparece na raiz do repositório.
4. Clique em **Commit changes**.

## 5. Ativar o GitHub Pages
1. No repositório, abra **Settings**.
2. No menu lateral, escolha **Pages**.
3. Em **Build and deployment**, selecione **Deploy from a branch** em **Source**.
4. Em **Branch**, selecione `main`.
5. Na pasta, selecione `/(root)`.
6. Clique em **Save**.

## 6. Abrir o site
O endereço ficará neste formato:

`https://SEU-USUARIO.github.io/portfolio-certificacoes/`

Para abrir diretamente a lista de cursos:

`https://SEU-USUARIO.github.io/portfolio-certificacoes/#certificacoes`

Substitua `SEU-USUARIO` pelo seu nome de usuário do GitHub. Depois de ativar o Pages, volte a **Settings → Pages** e clique em **Visit site** quando o endereço aparecer. A primeira publicação pode levar alguns minutos.

## 7. Adicionar os PDFs
1. Abra a pasta `certificados/` no repositório do GitHub.
2. Clique em **Add file → Upload files**.
3. Envie os PDFs usando exatamente os nomes abaixo (também listados em `certificados/LEIA-ME.txt`):

- `IBM-SkillsBuild-Cybersecurity-Fundamentals-2026.pdf`
- `Cisco-Networking-Basics-2026.pdf`
- `Microsoft-Entender-o-Microsoft-Entra-ID-2025.pdf`
- `Microsoft-Introducao-ao-Azure-Cloud-Shell-2025.pdf`
- `ENAP-SEI-Usar-4-0-2025.pdf`
- `IFRS-Redes-de-Computadores-2025.pdf`

4. Clique em **Commit changes**.
5. Recarregue o portfólio. Quando o arquivo existir, o cartão correspondente mostrará o botão/ícone para abrir o PDF.

## 8. Testar antes de compartilhar
- Abra o site no computador e no celular.
- Leia os QR Codes com a câmera do celular.
- Confirme se IBM e Cisco abrem suas páginas de credencial da Credly.
- No ENAP, abra o portal EV.G e informe o código exibido no cartão.
- No IFRS, abra o Aprenda Mais, informe o código e responda à pergunta de segurança apresentada.
- Teste cada botão de PDF depois de enviar os arquivos.

## Privacidade e autenticidade
- O site e os PDFs enviados ao repositório serão públicos.
- O certificado IFRS informado para este projeto contém CPF. Não publique o PDF original sem revisar esse dado. Antes de ocultar o CPF, confirme se o PDF tem assinatura digital incorporada, pois uma edição pode afetar a validação; se houver dúvida, deixe o PDF privado e use o código/portal de validação no site.
- Não publique PDFs com CPF, endereço, telefone, assinatura manuscrita ou outros dados que não sejam necessários para validar a formação.
- QR Code não substitui a validação no portal: no ENAP e no Aprenda Mais, o visitante ainda precisará informar o código ou responder ao desafio de segurança.
- Os módulos Microsoft Learn não têm, nos dados fornecidos, uma credencial pública individual de validação. O cartão oferece o conteúdo oficial do módulo e espaço para o PDF de conclusão, se você tiver esse documento.

## Atualizações futuras
Mantenha o mesmo repositório e o mesmo `index.html`. Para novos cursos, atualize o array `credentials` no próprio HTML e coloque o PDF correspondente em `certificados/`. O endereço do GitHub Pages não muda.
