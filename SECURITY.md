# Política de Segurança

## 🔐 Visão Geral

Este projeto consiste em **templates LaTeX padronizados para Trabalhos de Conclusão de Curso (TCC)** do Departamento de Ciência da Computação (DCC/UFRR). Embora o risco de segurança neste tipo de projeto seja baixo, tratamos com seriedade qualquer **comportamento inesperado**, **código malicioso embutido** ou **vulnerabilidades LaTeX** que possam comprometer a integridade, privacidade ou funcionalidade dos usuários finais.

---

## 🛡️ Escopo de Segurança

As seguintes situações são consideradas relevantes para a política de segurança deste repositório:

* Inclusão não autorizada de comandos LaTeX perigosos (ex: `\write18` quando não necessário);
* Inclusão de pacotes que habilitam execução de código arbitrário (ex: `shell-escape`);
* Comandos ou pacotes que possam comprometer a segurança durante a compilação;
* Macros que causem comportamento inesperado ou silenciosamente modifiquem conteúdo;
* Possíveis backdoors em arquivos `.sty` ou `.cls` do projeto;
* Inserção de links externos maliciosos em arquivos `.tex` ou `.bib`.

**Fora de escopo**:

* Problemas de formatação, estilização ou não conformidade com as normas acadêmicas (devem ser tratados via [issues](https://github.com/hbgit/template-tcc-dcc-ufrr/issues)).

---

## 🧑‍💻 Relatando Vulnerabilidades

Se você identificar uma possível vulnerabilidade no projeto:

1. **Não abra uma issue pública** diretamente.
2. Envie um e-mail detalhado para: `herbert.rocha@ufrr.br`
   (ou outro contato mantido pelos mantenedores).
3. Inclua:

   * Descrição clara da vulnerabilidade;
   * Passos para reproduzir;
   * Potencial impacto;
   * Sugestão (se aplicável).

Você receberá uma resposta em até **5 dias úteis**.

---

## 🔄 Processo de Correção

Após receber o relatório, seguiremos este fluxo:

1. **Análise e verificação técnica** do problema;
2. **Confirmação da vulnerabilidade** (com feedback ao relator);
3. **Correção local em uma branch isolada**;
4. **Divulgação responsável**, se necessário, com menção ao relator (caso deseje);
5. **Atualização dos arquivos afetados** e, se aplicável, das instruções de compilação.

---

## 🔐 Recomendações Gerais

Para segurança local ao utilizar este projeto:

* Evite compilar arquivos `.tex` de terceiros sem revisão manual;
* Utilize `latexmk` ou `pdflatex` com a flag `--no-shell-escape`, exceto se estritamente necessário;
* Revise dependências e pacotes utilizados antes de enviar seu trabalho para publicação ou submissão.

---

## 📄 Licença e Responsabilidade

Este projeto é distribuído **sem garantias de segurança absolutas**. Usuários devem manter suas instalações LaTeX atualizadas e adotar práticas seguras ao manipular arquivos `.tex`.

---