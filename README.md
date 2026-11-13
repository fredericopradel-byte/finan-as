# Meu Financeiro v1.1 — atualização incremental

## Publicação

Extraia o ZIP e envie **os arquivos internos da pasta `meu-financeiro-v1.1` diretamente para a raiz** do repositório GitHub Pages `finan-as`, substituindo `index.html`, `sw.js`, `manifest.webmanifest` e `icon.svg`. Inclua `exemplos-c6.json`. Não apague dados do navegador. Faça **backup JSON antes de atualizar**.

## Novidades

- Aba C6 com importação de JSON normalizado e conferência dos totais de fatura.
- `exemplos-c6.json` contém 426 lançamentos extraídos das três faturas fornecidas (setembro, outubro e novembro de 2026), conciliados com R$ 7.393,16, R$ 6.137,87 e R$ 10.175,23.
- Categorização inicial por estabelecimento, com CMA como Saúde.
- Faturas importadas não duplicam ao importar o mesmo mês novamente; é possível excluí-las.
- Contracheque exige inserir líquido oficial e conferir a soma antes de salvar.
- Backup JSON inclui faturas; mantém dados existentes da versão 1.0.

## Limitações importantes

- **A leitura direta de PDFs complexos ainda não está pronta**: o PDF do C6 usa codificação de fontes que exige um motor de PDF completo (PDF.js empacotado localmente). O JSON fornecido foi extraído e validado neste desenvolvimento; novas faturas exigem extração externa ou texto copiado do PDF até integrarmos PDF.js.
- Categorias são heurísticas e ainda não têm editor de classificação. As datas das compras parceladas são preservadas como datas de compra, e o gasto é contabilizado no mês de vencimento para fluxo de caixa.
- Importações não modificam saldo bancário automaticamente: pagamentos de fatura não devem ser lançados como nova despesa. O saldo da conta corrente exige conciliação manual.
- O leitor de contracheque ainda não interpreta automaticamente o PDF militar com confiabilidade. O líquido oficial deve ser digitado e os valores revisados.
- Não há criptografia de dados nem sincronização entre dispositivos. Mantenha backups em local privado.
- Verificação: sintaxe JavaScript e conciliação dos três totais; não foi realizado teste funcional completo em Safari/iPhone.
