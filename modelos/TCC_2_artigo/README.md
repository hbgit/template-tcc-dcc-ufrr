# Modelo de TCC em Formato de Artigo

Este modelo em LaTeX foi desenvolvido para atender às diretrizes da **Resolução CEPE/UFRR nº 133, de 24 de março de 2025**, com foco especial na *Seção 3.2 (Formato Artigo)*. Além disso, incorpora adaptações específicas definidas pelo **Departamento de Ciência da Computação (DCC)**.

## Estrutura dos Arquivos

A estrutura do projeto está organizada da seguinte forma:

* [`capas/`](./capas): Contém as páginas iniciais do TCC. Não é necessário alterá-las.
* [`estilo/`](./estilo/): Inclui arquivos responsáveis pela formatação e configuração do template.
* [`imagens/`](./imagens/): Diretório para armazenar as imagens utilizadas no TCC. Já inclui exemplos ilustrativos.
* [`secoes/`](./secoes/): Contém os arquivos de cada seção do TCC, organizados individualmente.
* [`tcc-1-main.tex`](./tcc-2-main.tex): Arquivo principal que organiza o TCC, realizando a inclusão das seções necessárias.

## Como Utilizar

- Clone ou baixe o modelo completo
- Edite os arquivos na pasta [secoes/](./secoes/) conforme necessário
- Adicione suas imagens na pasta [imagens/](./imagens/)
- Compile o arquivo principal tcc-1-main.tex, exemplo, pdflatex tcc-2-main.tex
- As configurações de estilo e capas são aplicadas automaticamente