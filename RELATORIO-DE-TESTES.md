# Relatório de testes pré-publicação

## Testes locais executados

- [x] `index.html` gerado como página única, sem `testes.html`.
- [x] Removidos o link superior direito de certificações, o texto "Aprendizado contínuo", a descrição de formação complementar, o rodapé com contato e o nome/cargo repetidos no rodapé.
- [x] Seis cursos/cartões cadastrados.
- [x] Quatro QR Codes recriados e decodificados por leitor QR local; o conteúdo lido corresponde exatamente ao destino definido para cada cartão.
- [x] Nenhum QR Code de validação foi criado para os módulos Microsoft Learn.
- [x] Os PDFs ausentes não geram links clicáveis quebrados: o cartão mostra "PDF A ADICIONAR" até detectar o arquivo no diretório `certificados/`.
- [x] IDs e códigos informados aparecem no cartão e podem ser copiados.
- [x] Sintaxe JavaScript aprovada com `node --check`.
- [x] Estrutura HTML lida por parser HTML (lxml).
- [x] Busca no conteúdo do projeto não encontrou o CPF informado no texto do certificado.

## Destinos dos QR Codes

| Curso | Destino codificado | Resultado do teste local |
|---|---|---|
| IBM SkillsBuild | URL individual da Credly enviada pelo titular | QR decodificado; destino corresponde à URL fornecida |
| Cisco | URL individual da Credly enviada pelo titular | QR decodificado; destino corresponde à URL fornecida |
| ENAP | Portal oficial de validação EV.G | QR decodificado; portal acessível e solicita código |
| IFRS | Verificador de certificados Aprenda Mais | QR decodificado; portal acessível e solicita código e pergunta de segurança |

## Limites da verificação externa

- A abertura das duas páginas individuais da Credly não pôde ser confirmada nesta sessão de navegação. Os links e QR Codes usam exatamente os endereços que o titular forneceu. Faça o teste final com a câmera de um celular e confirme que a Credly exibe o nome da credencial e o emissor.
- A página EV.G foi aberta e informa que a validação é feita pelo código, sem necessidade de login ou cadastro. Não foi enviado o formulário com o código; portanto, a autenticidade individual do certificado não foi confirmada nesta etapa.
- A página de verificação Aprenda Mais foi aberta. Ela apresenta campos para código e pergunta de segurança. O formulário não foi submetido; portanto, a autenticidade individual do certificado não foi confirmada nesta etapa.
- As páginas oficiais dos dois módulos Microsoft Learn estão acessíveis, mas são páginas de treinamento, não páginas públicas que provem a conclusão individual.
- Nenhum PDF de certificado foi enviado junto com os materiais disponíveis nesta conversa. Por isso, os links de PDF permanecerão desativados até o envio dos arquivos verdadeiros.

**Conclusão:** a página está pronta para ser enviada ao GitHub, mas não é correto afirmar que todos os certificados foram autenticados online antes de submeter seus códigos nos respectivos verificadores e adicionar os PDFs originais.
