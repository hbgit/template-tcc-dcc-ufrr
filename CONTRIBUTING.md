# Guia de Contribuição

Obrigado por seu interesse em contribuir com o projeto de **Template LaTeX para TCCs do DCC/UFRR**! Este repositório visa manter modelos padronizados e atualizados para Trabalhos de Conclusão de Curso conforme as normas estabelecidas pelo departamento.

Siga as etapas abaixo para colaborar de forma eficiente.

## 🧾 O que está neste repositório?

* Templates LaTeX para diferentes tipos de TCC (artigo, monografia, relatório técnico, etc.);
* Padrões de formatação conforme normas institucionais;
* Arquitetura modular com estilo separado (`.sty`);
* Exemplos comentados para facilitar o uso pelos alunos.

---

## 📌 Requisitos para contribuir

Antes de enviar contribuições, certifique-se de que:

* Possuir ambienter de desenvolvimento básico em LaTeX;
* Conhecer os padrões exigidos pelo DCC/UFRR para TCCs;
* Você tem o [Git](https://git-scm.com/) instalado e sabe usar pull requests no GitHub.

---

## 🚀 Etapas para contribuir

1. **Faça um fork do repositório**

   * Clique em "Fork" no topo da página do projeto.

2. **Clone o seu fork**

   ```bash
   git clone https://github.com/seu-usuario/template-latex-dcc.git
   cd template-latex-dcc
   ```

3. **Crie uma nova branch**
   Nomeie a branch de forma descritiva:

   ```bash
   git checkout -b correcao-margens
   ```

4. **Implemente suas alterações**

   * Mantenha a organização modular do projeto;
   * Comente suas alterações se necessário;
   * Siga os padrões de nomenclatura e formatação já adotados.

5. **Faça commit das suas alterações**
   Escreva mensagens de commit claras e objetivas:

   ```bash
   git add .
   git commit -m "Corrige margens para modelo de monografia conforme nova norma"
   ```

6. **Envie sua branch para o GitHub**

   ```bash
   git push origin correcao-margens
   ```

7. **Abra um Pull Request**

   * Vá até o seu repositório forkado;
   * Clique em "Compare & pull request";
   * Descreva claramente o que foi alterado e por quê.

---

## ✅ Boas práticas

* Sempre confira as normas atualizadas do DCC antes de alterar estilos ou formatação;
* Faça testes com exemplos reais de TCCs;
* Evite incluir arquivos desnecessários (ex: `.log`, `.aux`, `.pdf`);
* Utilize `.gitignore` para evitar envio de arquivos temporários;
* Use a pasta `modelos/` para diferentes variantes (ex: `monografia/`, `artigo/`, etc.).

---

## 🛠 Sugestões de contribuição

* Correções de estilo e diagramação;
* Ajustes conforme normas atualizadas do DCC;
* Inclusão de novos modelos (ex: TCC em formato de artigo);
* Tradução ou melhorias na documentação do projeto;
* Testes de compatibilidade com diferentes compiladores LaTeX (ex: `pdflatex`, `xelatex`, `lualatex`).

---

## 📫 Dúvidas?

Abra uma [issue](https://github.com/hbgit/template-tcc-dcc-ufrr/issues) para relatar bugs, sugerir melhorias ou tirar dúvidas.

---

Agradecemos por colaborar com este projeto que visa facilitar a vida dos alunos e padronizar a produção científica no DCC/UFRR! 🎓

---