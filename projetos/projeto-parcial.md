<div align="center">

<h1>🌐 Projeto Parcial</h1>
<h2>Portal da Escola em Rede</h2>
<p><strong>Construa sua área do portal, conecte-a às áreas dos colegas e investigue o que acontece quando um acesso falha.</strong></p>
<p><code>Figma</code> • <code>React + Vite</code> • <code>Cliente e servidor</code> • <code>IP e portas</code> • <code>HTTP</code> • <code>Comunicação entre equipes</code></p>

</div>

---

## 🎯 Situação-problema

A escola deseja reunir informações sobre disciplinas, projetos, notícias e orientações em um portal que funcione na **rede da escola sem depender de conexão com a internet**. A turma construirá uma primeira versão desse espaço.

Primeiro, a turma planejará no Figma um padrão compartilhado para as telas. Depois, cada equipe desenvolverá sua área com React + Vite e a disponibilizará em seu computador. Os links conectarão as áreas em um único percurso de navegação.

Para isso funcionar, será necessário conversar com outras equipes, descobrir os endereços corretos e testar os acessos. Um link pode estar digitado incorretamente, um servidor pode estar parado ou um computador pode estar sem conexão. A equipe deverá reunir evidências antes de concluir o que aconteceu.

> [!IMPORTANT]
> O portal terá **pelo menos 16 áreas no conjunto da turma**. Cada equipe será responsável por **uma área**, e todos os integrantes deverão participar. Esta primeira versão será um protótipo navegável. Futuramente, o portal poderá permitir registro de chamadas e gestão de informações e notícias por estudantes e professores. Autenticação, banco de dados, permissões e chamadas reais ficam para uma evolução posterior.

## 💡 Onde isso aparece no dia a dia

Quando você abre um sistema escolar, consulta uma loja ou usa um aplicativo, um programa pode enviar pedidos a outro computador para receber páginas ou dados.

Neste projeto, vocês estarão dos dois lados: oferecendo um serviço e usando os serviços dos colegas. A experiência ajuda a compreender por que um sistema pode funcionar no computador de quem o desenvolveu e falhar quando outra pessoa tenta utilizá-lo.

## 🧭 Visão geral

| Item | Combinado do projeto |
| --- | --- |
| 🏫 Produto coletivo | Portal com pelo menos 16 áreas conectadas |
| 💻 Desenvolvimento | Planejamento no Figma e implementação com React + Vite |
| 📋 Avaliação | Parcial de 10 pontos: 6 de desenvolvimento e 4 de apresentação |
| 🧰 Recursos | Figma, Node.js, React + Vite, editor, navegador e rede local |
| 📦 Repositório | `portal-escolar-xx`, utilizando o identificador da área |
| 📅 Apresentação | **30/09 ou data mais próxima** |

## 🏗️ As áreas do portal

Definam os responsáveis antes de começar para evitar assuntos repetidos. Os temas abaixo podem ser ajustados com o professor às disciplinas e necessidades da escola.

| Área | Tema sugerido | Primeira versão |
| --- | --- | --- |
| 01 | Início e apresentação da escola | Apresentação e catálogo de acesso às outras 15 áreas. |
| 02 | Cursos e formação técnica | O que se estuda e exemplos de aplicações. |
| 03 | Agenda escolar | Atividades e eventos com informações conferidas. |
| 04 | Guia do estudante | Orientações e perguntas frequentes. |
| 05 | Programação Web | Exemplos e recursos de aprendizagem. |
| 06 | Redes de Computadores | Conceitos e dicas de diagnóstico. |
| 07 | Desenvolvimento Mobile | Aplicativos e ideias de projetos. |
| 08 | Programação Orientada a Objetos | Conceitos apresentados com exemplos pequenos. |
| 09 | Banco de Dados | Como organizar e consultar informações. |
| 10 | Segurança da Informação | Cuidados com contas, arquivos e acesso. |
| 11 | Sistemas Embarcados | Componentes e projetos desenvolvidos. |
| 12 | Análise e Projeto de Sistemas | Necessidades dos usuários, requisitos e planejamento de funcionalidades. |
| 13 | Design de Interfaces e Usabilidade | Organização das telas, acessibilidade, navegação e facilidade de uso. |
| 14 | Qualidade e Teste de Softwares | Casos de teste, registro de falhas e verificação das correções. |
| 15 | Projetos da turma | Apresentação de trabalhos e do que eles resolvem. |
| 16 | Gestão de Startups | Identificação de problemas, soluções, público e validação de ideias. |

Outras opções para substituir um tema, mediante combinação: **Informática Básica** (arquivos e ferramentas digitais), **Lógica de Programação** (algoritmos, condições e repetições), **Arquitetura e Manutenção de Computadores** (componentes e diagnóstico) e **Planejamento de Carreira** (habilidades, objetivos e formação).

Cada área deverá ter um título, pelo menos dois parágrafos curtos ou duas seções úteis e identificação pelo nome dos integrantes da equipe. Registrem a fonte das informações quando houver pesquisa.

**A equipe 01 organiza o catálogo; cada outra equipe fornece seu título e endereço e verifica se o próprio link foi incluído corretamente.** A construção da página inicial também depende da colaboração da turma.

## 🎨 Primeiro passo — planejar no Figma

Antes de programar, construam um planejamento compartilhado da interface:

1. Definam cores, fontes, espaçamentos e aparência dos links e botões.
2. Combinem um cabeçalho, um menu e um rodapé comuns.
3. Criem uma tela inicial e um modelo de tela de conteúdo.
4. Planejem cada área a partir desse modelo e indiquem os caminhos de ida e volta.
5. Revisem juntos a legibilidade e a navegação antes de iniciar o desenvolvimento.

Exportem imagens das telas para consultar durante a implementação. O conteúdo de cada área será diferente, mas o visitante deverá reconhecer a mesma identidade visual.

> [!NOTE]
> O Figma colaborativo, a instalação das dependências e a postagem no GitHub usam internet na preparação. O objetivo de funcionar sem internet se aplica ao **portal executado na rede local**, depois de preparado. Os computadores precisam continuar conectados à rede da escola.

## 🔗 Como conectar os computadores

Imagine três servidores disponíveis na rede:

| Área | Endereço de exemplo |
| --- | --- |
| Início | `http://192.168.10.21:8000/` |
| Programação Web | `http://192.168.10.25:8000/` |
| Redes | `http://192.168.10.26:8000/` |

Esses endereços são ilustrativos. Usem os IPs reais identificados no laboratório.

```text
Navegador do visitante
  ├── abre o início no computador da equipe 01
  ├── segue um link para o computador da equipe 05
  └── segue outro link para o computador da equipe 06
```

Ao seguir um link para outra área, o navegador faz um novo pedido ao servidor indicado na URL. As páginas não precisam estar todas no mesmo computador.

### Navegação obrigatória

- A página inicial deverá oferecer acesso às outras 15 áreas.
- Cada uma das outras áreas deverá ter um link para o início e links para pelo menos duas áreas de outras equipes.
- Os textos dos links deverão indicar o destino, como “Redes de Computadores”.
- Os responsáveis deverão testar os links com as equipes de destino.

Exemplo dentro de um componente React:

```jsx
<nav aria-label="Áreas do portal">
  <ul>
    <li><a href="http://192.168.10.21:8000/">Início do portal</a></li>
    <li><a href="http://192.168.10.25:8000/">Programação Web</a></li>
    <li><a href="http://192.168.10.26:8000/">Redes de Computadores</a></li>
  </ul>
</nav>
```

> [!TIP]
> Um link como `/` continua no servidor atual. Para abrir a área de outro computador, informe a URL completa desse computador. Não use `localhost`, `127.0.0.1` ou `0.0.0.0` como endereço de um colega.

## 🗂️ Organização do projeto

Utilizem a estrutura React + Vite trabalhada em Programação Web. Exemplo:

```text
portal-escolar-xx/
├── public/                 # Recursos locais, se utilizados
├── src/
│   ├── assets/             # Imagens e fontes locais
│   ├── components/         # Componentes da interface
│   ├── App.jsx             # Área desenvolvida
│   ├── main.jsx            # Inicialização do React
│   └── index.css           # Estilos
├── index.html              # Entrada do Vite
├── package.json
├── package-lock.json
├── vite.config.js
├── .gitignore
└── README.md
```

O conteúdo será implementado em `App.jsx` e nos componentes. Mantenham a configuração fornecida em Web, incluindo o script `dev` que executa `vite`. O servidor será o próprio Vite; o arquivo `servidor.cjs` do exemplo anterior não será utilizado.

## 🪜 Desenvolver e disponibilizar

### 1. Implementar o planejamento e testar localmente

Depois do planejamento no Figma, implementem a área seguindo o padrão combinado. Na pasta que contém `package.json`, confiram `node --version`. Se as dependências ainda não estiverem instaladas, preparem o projeto com internet:

```bash
npm install
```

Para iniciar o teste no próprio computador:

```bash
npm run dev -- --host 127.0.0.1 --port 8000 --strictPort
```

Abram `http://127.0.0.1:8000/` e mantenham o terminal aberto. O Vite atualiza a página durante o desenvolvimento quando os arquivos são salvos.

### 2. Disponibilizar e trocar os endereços

Encerrem o processo anterior com `Ctrl+C` e iniciem:

```bash
npm run dev -- --host 0.0.0.0 --port 8000 --strictPort
```

`--host 0.0.0.0` permite receber pedidos pelas interfaces IPv4. `--strictPort` impede que o Vite troque de porta automaticamente se a 8000 estiver ocupada. Nesse caso, confiram o processo anterior ou combinem outra porta e atualizem os links. Computadores diferentes podem usar a mesma porta.

Para descobrir o endereço da interface conectada:

**Linux:**

```bash
ip -br address
```

**Windows:**

```powershell
ipconfig
```

Se o IPv4 for `192.168.10.26`, a URL será `http://192.168.10.26:8000/`. Não incluam o prefixo `/24` no endereço do navegador.

Compartilhem o título da área e a URL com os responsáveis pelo início e pelas áreas relacionadas. Se o IP mudar, avisem e repitam os testes. Nesta primeira versão, as áreas ficam distribuídas entre os computadores; uma hospedagem central na escola poderá ser planejada posteriormente.

### 3. Preparar o uso sem internet

- Guardem imagens, fontes, ícones e demais recursos necessários dentro do projeto.
- Não dependam de fontes por CDN, vídeos incorporados, APIs externas ou imagens de outros sites para exibir o conteúdo obrigatório.
- Links externos podem aparecer como referência, identificados como recursos que precisam de internet.
- Mantenham as dependências instaladas nas máquinas da demonstração.

> [!IMPORTANT]
> O Vite será usado na demonstração de desenvolvimento. Para uma instalação permanente na escola, será necessário gerar a versão de distribuição com `npm run build` e preparar sua hospedagem local. O servidor de desenvolvimento e `vite preview` não são a solução de produção do portal.

## 🧪 Testes e evidências

Observem as requisições no painel **Network/Rede** do navegador e registrem os resultados, incluindo falhas e correções. Não é necessário que o terminal do Vite mostre uma linha para cada acesso.

| Teste | Ação | Resultado esperado | Resultado observado |
| --- | --- | --- | --- |
| 1 | Abrir a própria área por `http://127.0.0.1:8000/`. | Interface e recursos carregados no próprio PC. | |
| 2 | Abrir a área de outro PC pela URL informada. | Conteúdo correto e requisições visíveis no navegador. | |
| 3 | Usar os links para duas áreas relacionadas. | Cada link chegar ao destino combinado. | |
| 4 | Sair do início, visitar uma área e voltar. | Navegação coerente e aparência padronizada. | |
| 5 | Recarregar e navegar sem internet, mantendo a rede local. | Conteúdo obrigatório funcionar entre os computadores. | |

A área inicial também deve conferir os 15 links do catálogo, com apoio dos responsáveis.

No teste sem internet, usem **Disable cache/Desativar cache** no painel Network, com as ferramentas abertas, e recarreguem as páginas para conferir os recursos. Se não houver condição para esse teste, registrem “não verificado” e combinem sua validação com o professor.

> [!NOTE]
> No React + Vite, um caminho desconhecido pode retornar o HTML inicial com status 200. Digitar uma página inexistente não garante um 404. Confiram a resposta e o conteúdo real: receber 200, sozinho, não comprova que a área esperada apareceu.

## 🔎 Uma área não abriu. Como investigar?

| Verificação | Próxima ação |
| --- | --- |
| URL digitada | Conferir `http://`, IP, porta e caminho com a equipe responsável. |
| Servidor em execução | Pedir que a equipe confira o terminal e teste a página no próprio PC. |
| Endereço de escuta | Conferir o uso de `--host 0.0.0.0` e a porta indicada no terminal. |
| Conexão e IP atual | Verificar a interface conectada e comparar o IP atual com o link divulgado. |
| Comunicação entre computadores | Se o teste local funciona e o remoto não, investigar o caminho e possíveis restrições com o professor. |
| Interface incompleta | Observar no Network recursos que falharam e consultar erros no Console. |

Redes diferentes podem se comunicar quando existe roteamento e acesso permitido. Não concluam que “estar em outra rede” é a causa apenas pela aparência dos IPs. Também não concluam que o firewall é responsável só porque o navegador esperou e não recebeu resposta.

### Registro curto de investigação

Registrem um problema encontrado ou um teste bem-sucedido com uma hipótese de falha e o próximo teste.

| Campo | Preenchimento |
| --- | --- |
| Sintoma e URL testada | |
| Evidência observada | |
| Hipótese e próximo teste | |
| Correção ou comunicação realizada | |
| Resultado após o teste | |
| O que ainda não podemos afirmar | |

**Exemplo:** o link apontava para `:800`, mas a equipe informou `:8000`. Após conferir o terminal, corrigimos o link e a página abriu. Isso comprova o acesso testado àquele serviço; não comprova que todos os serviços ou a internet estão funcionando.

> [!IMPORTANT]
> Investiguem apenas as máquinas e os serviços da atividade. Não é preciso provocar falhas na rede escolar. Se o acesso entre computadores estiver bloqueado, registrem os testes e utilizem a alternativa indicada pelo professor. Um teste local não deve ser apresentado como prova de acesso remoto.

## ✅ Checklist da entrega

### Área e funcionamento

- [ ] A equipe produziu uma área com conteúdo próprio e identificação.
- [ ] O planejamento no Figma foi realizado antes do desenvolvimento.
- [ ] A interface segue o padrão visual combinado.
- [ ] A página abre por HTTP usando React + Vite.
- [ ] Os recursos obrigatórios estão preparados para uso sem internet.
- [ ] A equipe identificou IP, porta e caminho da sua URL.
- [ ] O servidor permaneceu disponível durante a rodada combinada de testes.

### Comunicação e navegação

- [ ] O endereço foi informado e conferido com as equipes envolvidas.
- [ ] A área está no catálogo da página inicial.
- [ ] A área possui retorno ao início e links para outras duas equipes, ou organiza os 15 destinos.
- [ ] Mudanças de endereço foram comunicadas e os links afetados foram revistos.
- [ ] Os links possuem nomes compreensíveis e podem ser acionados pelo teclado.

### Teste e compreensão

- [ ] A tabela contém o resultado dos cinco testes, incluindo falhas ou restrições encontradas.
- [ ] Existe um registro curto de investigação, com uma evidência e seu limite.
- [ ] Outra equipe participou da verificação.
- [ ] O README explica como executar e acessar a área.
- [ ] A equipe preparou a demonstração e a explicação do desenvolvimento.

## 👀 Revisão por outra equipe

| Verificação | Conferido | Precisa de ajuste |
| --- | :---: | :---: |
| A URL informada corresponde ao servidor e à porta usados. | ☐ | ☐ |
| O conteúdo exibido pertence à área esperada. | ☐ | ☐ |
| Os links levam às equipes indicadas. | ☐ | ☐ |
| Existe um percurso de volta ao início. | ☐ | ☐ |
| O teste pode ser acompanhado no painel Network do navegador. | ☐ | ☐ |
| A equipe diferencia observação de hipótese. | ☐ | ☐ |

**Equipe revisora:** ____________________

**Problema ou confirmação registrada:** ____________________

**Ação combinada com os responsáveis:** ____________________

## 📊 Avaliação — 10 pontos

| Parte | Critério | Máximo | Evidência para pontuação completa |
| --- | --- | :---: | --- |
| Desenvolvimento | Planejamento e interface | 2 | Planejamento conjunto no Figma, conteúdo útil e implementação do padrão visual. |
| Desenvolvimento | Funcionamento e integração | 2 | Serviço acessível no ambiente disponibilizado, links conferidos e recursos preparados para a rede local. |
| Desenvolvimento | Testes e documentação | 2 | Testes e investigação registrados, instruções claras e entrega organizada no GitHub. |
| Apresentação da equipe | Demonstração |  4| Mostrar a área, os acessos entre computadores e o resultado da verificação sem internet, ou a pendência validada pelo professor. |

Em cada critério: pontuação completa quando demonstrado, metade quando parcialmente demonstrado e zero quando ainda não há evidência. **A avaliação é da equipe: 6 pontos de desenvolvimento e 4 de apresentação.**

Se outro servidor estiver desligado ou houver uma restrição do laboratório, serão considerados os testes, a comunicação e a alternativa validada pelo professor. A equipe não perde automaticamente os pontos por uma condição fora de seu controle, mas precisa apresentar o que conseguiu verificar. Uma descrição no papel não substitui uma operação que ainda precisa ser demonstrada.

## ♿ Participação e apresentação

A contribuição pode ser demonstrada escrevendo conteúdo, editando um link, operando o terminal ou navegador, conferindo uma URL, organizando o desenho ou conduzindo um teste. Todos devem participar da produção e da verificação, com funções alternadas.

O uso de roteiro, leitura mediada ou outro apoio durante a apresentação não reduz automaticamente a nota.

## 📦 O que entregar

1. **Repositório no GitHub chamado `portal-escolar-xx`**, com o identificador combinado, código React + Vite, recursos locais, `package.json`, `package-lock.json` e README. Não enviem `node_modules`; mantenham essa pasta no `.gitignore`.
2. **Planejamento da interface:** link do Figma acessível ao professor e imagens exportadas das telas no repositório.
3. **README:** tema, nomes dos integrantes, preparação e execução, conexões, resultados dos testes e investigação.
4. **Apresentação da equipe em 30/09 ou data mais próxima**, demonstrando o desenvolvimento e o funcionamento.

Postar o código no GitHub não mantém o servidor ligado. Durante a demonstração, o portal depende dos computadores conectados e dos serviços em execução. A entrega no GitHub e o uso sem internet na escola são etapas diferentes.

## 🔒 Cuidados com o portal

- Identifiquem os autores pelo nome dos integrantes da equipe.
- Usem informações da escola que tenham sido conferidas e autorizadas para a atividade.
- Evitem senhas, dados fornecidos por IA, contatos pessoais, fotografias de pessoas sem autorização e capturas com dados de contas.
- Mantenham o catálogo de IPs reais no ambiente da aula. Para um registro público, usem exemplos identificados e ocultem dados desnecessários nas capturas.
- Representem funcionalidades futuras, como chamadas, apenas com dados fictícios nesta etapa.
- Encerrem somente o servidor da própria equipe com `Ctrl+C` ao final da aula.

## 📚 Para consultar

- [Vite — primeiros passos](https://vite.dev/guide/)
- [Vite — opções de execução](https://vite.dev/guide/cli)
- [React — componentes e interface](https://react.dev/learn)
- [MDN — links, URLs e caminhos](https://developer.mozilla.org/pt-BR/docs/Learn_web_development/Core/Structuring_content/Creating_links)
- [MDN — códigos de resposta HTTP](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Reference/Status)

---

<div align="center">

<p><strong>Uma área é responsabilidade de uma equipe. A navegação pelo portal depende da comunicação de toda a turma.</strong></p>

</div>
