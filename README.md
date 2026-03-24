# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas linguagens Python, JavaScript, TypeScript e Java, e gera relatórios `HTML` como [este](https://andrehora.github.io/gitevo-examples/python/pandas.html).

Mais exemplos de relatórios podem ser podem ser encontrados em https://github.com/andrehora/gitevo-examples.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

> [!NOTE]
> Antes de instalar a ferramenta, é recomendado criar e ativar um [ambiente virtual Python](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#create-and-use-virtual-environments).

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
$ pip install gitevo
```

Execute a ferramenta no repositório selecionado utilizando o comando abaixo (ajuste conforme a linguagem do repositório).
Substitua `<git_url>` pela URL do repositório que será analisado:

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r javascript <git_url>

# TypeScript
$ gitevo -r typescript <git_url>

# Java
$ gitevo -r java <git_url>
```

Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

> [!NOTE]
> Essa etapa pode demorar alguns minutos pois o projeto será clonado e analisado localmente.

# Passo 3: Explorar o relatório de evolução de código

Após executar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), é gerado um relatório `HTML` contendo diversos gráficos sobre a evolução do código.

Abra o relatório `HTML` e observe com atenção os gráficos.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo
- Detalhar se as curvas estão de acordo com boas práticas
- Explicar grandes alterações nas curvas
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- etc.

Seja criativo!

# Instruções para o exercício

1. Crie um `fork` deste repositório (mais informações sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Adicione o relatório `HTML` no seu fork.
3. No Moodle, submeta apenas a URL do seu `fork`.

Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork:

1. Repositório selecionado: https://github.com/nodejs/node
2. Gráfico selecionado:
<img width="895" height="455" alt="image" src="https://github.com/user-attachments/assets/75287eff-2a19-4200-8ce7-8277c37b0c0a" />

3. Explicação:
   
O gráfico de "Variable declarations” mostra a quantidade no uso de const, var e let ao longo dos anos, e revela uma mudança na estratégia de programação do projeto.

Observando a evolução, o uso de const cresce de forma consistente de 2021 até 2026. Ele sai de cerca de 64 mil declarações e chega próximo de 98 mil, indicando que os desenvolvedores estão preferindo variáveis imutáveis sempre que possível. Isso é considerado uma boa prática, pois reduz efeitos colaterais e torna o código mais previsível.

Já o let também apresenta crescimento contínuo, embora mais moderado. Ele vai aumentando a cada ano, o que mostra uma permanência na estratégia da utilização dessa variavél, aumentando constantemente junto com as linhas de código, mas pode também ser o resultado de uma adoção gradual para casos onde a mutabilidade é necessária, substituindo o uso antigo do var.

Por outro lado, o var tem um comportamento interessante, visto que ele começa muito alto, sofre uma queda em 2022, tem um pico em 2023 e depois entra em uma tendência de queda até 2026. Esse padrão sugere que, embora ainda seja utilizado, o var está sendo progressivamente abandonado, mesmo sem ter encontrado uma lógica para o aumento significativo em 2023.

Essa transição é totalmente coerente com as boas práticas modernas de JavaScript, que recomendam evitar var por problemas de escopo e preferir const e let. O gráfico, portanto, indica uma evolução positiva na qualidade do código, o que contribui para um código mais seguro, legível e fácil de manter.



