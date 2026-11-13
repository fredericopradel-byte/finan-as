# Meu Financeiro — MVP 1.0

PWA sem dependências externas. Dados locais em IndexedDB. Interface adaptada para celular e desktop.

## Executar

Sirva esta pasta em `localhost` ou HTTPS. Exemplo: `python -m http.server 8080` e abra `http://localhost:8080`.
Para instalar no iPhone, hospede a pasta em GitHub Pages e use Safari > Compartilhar > Adicionar à Tela de Início.

## Recursos

- Painel mensal de receitas, despesas, patrimônio e categorias
- Contas correntes, poupança e investimentos, transferências internas, ajustes de saldo
- Contracheques com rubricas, conferência e receita líquida vinculada
- Tentativa experimental de extração local de PDFs com fluxos de texto simples; não é um leitor PDF completo e pode falhar com PDFs reais
- Projeção de juros compostos
- Backup/restauração JSON
- Service worker para acesso offline após primeira carga em HTTPS/localhost

## Limitações e próximos passos

- PDF: integrar uma biblioteca PDF.js **empacotada localmente**, com tratamento de tabelas, rubricas e fontes; a heurística atual não é confiável para importação automática.
- Segurança: adicionar criptografia do backup e bloqueio de acesso antes de inserir dados reais sensíveis em dispositivos compartilhados.
- Cartões: contas a pagar, faturas, parcelamentos e conciliação de pagamentos ainda não implementados.
- Não há sincronização entre dispositivos.
- Não é recomendado guardar contracheques com dados pessoais no campo de texto; os arquivos PDF não são persistidos.
