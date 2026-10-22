# AAPRO — Android Auto Power & Research Optimizer

**Um projeto open source para investigar, integrar e aprimorar experiências de aplicativos relacionados ao Android Auto.**

> Status: Em desenvolvimento e fase de pesquisa
> Objetivo: Unificar funcionalidades inspiradas no AAAD e no AABrowser em uma aplicação Android organizada, moderna e adaptável.

---

## 1. Visão geral

O **AAPRO** é um projeto experimental de desenvolvimento Android que tem como objetivo estudar, reconstruir de forma independente e integrar funcionalidades relevantes de dois projetos existentes:

- [AAAD — Android Auto Apps Downloader](https://github.com/shmykelsa/AAAD/releases/tag/v2.8.5)
- [AABrowser — Android Auto Browser](https://github.com/kododake/AABrowser/releases/tag/v3.3)

A proposta é investigar como esses aplicativos funcionam, documentar suas arquiteturas e funcionalidades relevantes e desenvolver uma solução unificada, com uma experiência de uso mais consistente, uma interface moderna e uma estrutura de código organizada.

O projeto utiliza como referência complementar o [REA — Reverse Engineer Anything](https://github.com/morluto/rea), ferramenta que pode auxiliar agentes de IA na análise de aplicativos, binários e comportamento de software.

O AAPRO não pretende ser apenas uma cópia visual dos aplicativos de referência. A meta é compreender seus comportamentos relevantes, identificar limitações e desenvolver uma implementação própria, modular e passível de evolução.

## 2. Objetivos do projeto

### 2.1. Engenharia reversa e pesquisa

- Investigar as versões de referência do AAAD e do AABrowser.
- Documentar fluxos de utilização, componentes, permissões e comportamentos observáveis.
- Analisar arquivos APK e código disponível, respeitando as licenças e os direitos aplicáveis.
- Utilizar ferramentas de análise estática e dinâmica quando apropriado.
- Registrar evidências, limitações e dúvidas para evitar conclusões sem comprovação.
- Comparar as funcionalidades dos projetos originais antes de definir a implementação correspondente no AAPRO.

### 2.2. Unificação funcional

Desenvolver uma aplicação que reúna, em uma estrutura coerente, as funcionalidades selecionadas dos dois projetos.

A arquitetura deverá permitir separar os componentes de gerenciamento de aplicativos, navegação web, configurações e demais recursos que forem efetivamente identificados durante a pesquisa.

A integração será definida com base na análise técnica e na viabilidade de cada funcionalidade, sem presumir que todos os recursos dos aplicativos de referência possam ser reproduzidos.

### 2.3. Interface e experiência de uso

A interface deverá priorizar:

- Design moderno, limpo e consistente.
- Layouts adaptáveis a diferentes dimensões e densidades de tela.
- Navegação intuitiva, com hierarquia visual clara.
- Componentes reutilizáveis e manutenção simplificada.
- Acessibilidade, legibilidade e uso adequado de áreas de toque.
- Compatibilidade com os requisitos e as restrições de interface do Android Auto, quando aplicáveis.

A adaptação visual não deve ser confundida com compatibilidade automática com a projeção do Android Auto. Cada modalidade de execução deverá ser validada separadamente.

### 2.4. Inteligência e automação

A IA deverá atuar como ferramenta de apoio à engenharia de software, auxiliando em:

- Análise dos projetos de referência.
- Compreensão da arquitetura e dos fluxos de execução.
- Planejamento de módulos e implementação.
- Geração e revisão de código.
- Identificação de inconsistências e possíveis falhas.
- Elaboração de testes e documentação.
- Revisão contínua das decisões técnicas com base em evidências.

A IA não deverá ser considerada uma fonte infalível: conclusões, alterações e resultados de testes precisam ser verificáveis.

---

## 3. Projetos de referência

### AAAD — versão 2.8.5

Repositório e versão de referência:

[https://github.com/shmykelsa/AAAD/releases/tag/v2.8.5](https://github.com/shmykelsa/AAAD/releases/tag/v2.8.5)

O AAAD será estudado para identificar sua arquitetura, seu fluxo de gerenciamento e instalação de aplicativos, suas dependências, permissões e demais funcionalidades efetivamente disponíveis nessa versão.

A implementação no AAPRO dependerá dos resultados da análise e dos limites técnicos e jurídicos identificados.

### AABrowser — versão 3.3

Repositório e versão de referência:

[https://github.com/kododake/AABrowser/releases/tag/v3.3](https://github.com/kododake/AABrowser/releases/tag/v3.3)

O AABrowser será investigado para compreender sua arquitetura de navegação, interface, gerenciamento de conteúdo web, configurações e integração com o ambiente Android Auto, conforme suportado pela versão analisada.

### REA — ferramenta auxiliar de engenharia reversa

Repositório:

[https://github.com/morluto/rea](https://github.com/morluto/rea)

O REA poderá ser utilizado para auxiliar a investigação de binários, aplicativos e comportamento em execução por meio de ferramentas de análise e integração com agentes de IA.

Sua utilização dependerá dos requisitos de cada tarefa, das ferramentas disponíveis no ambiente e dos resultados que possam ser verificados.

---

## 4. Arquitetura pretendida

A arquitetura definitiva ainda deverá ser estabelecida após a auditoria do código existente e dos projetos de referência.

Como direção inicial, o AAPRO deverá buscar uma estrutura modular com responsabilidades bem definidas:

| Módulo                       | Responsabilidade pretendida                                                              |
| ---------------------------- | ---------------------------------------------------------------------------------------- |
| Interface                    | Navegação, telas, componentes visuais e estados da aplicação                             |
| Gerenciamento de aplicativos | Recursos relacionados ao gerenciamento de aplicativos, conforme viabilidade e permissões |
| Navegação web                | Funcionalidades de navegador identificadas na pesquisa                                   |
| Configurações                | Preferências, opções e personalização                                                    |
| Compatibilidade Android      | Permissões, ciclo de vida, versões do sistema e integrações suportadas                   |
| Testes                       | Verificação automatizada e validação de funcionalidades                                  |
| Documentação técnica         | Registro de decisões, arquitetura, evidências e limitações                               |

Essa divisão é uma proposta de arquitetura, não uma declaração de que todos esses módulos já estejam implementados.

A implementação deverá seguir os padrões recomendados para desenvolvimento Android e evitar dependências desnecessárias entre módulos.

## 5. Ambiente de desenvolvimento

O desenvolvimento será realizado prioritariamente em um ambiente remoto baseado em GitHub Codespaces.

### Ferramentas previstas

- Git e GitHub para versionamento.
- GitHub Codespaces para edição e execução de tarefas de desenvolvimento.
- Java ou Kotlin, conforme a estrutura Android adotada pelo projeto.
- Gradle para configuração e construção do aplicativo.
- Android SDK e ferramentas de compilação compatíveis com o ambiente.
- Agentes de IA para análise, programação, revisão e documentação.
- REA e ferramentas complementares de engenharia reversa, conforme necessidade.

As tecnologias efetivamente utilizadas deverão ser confirmadas pelos arquivos de configuração do repositório.

### Desenvolvimento remoto

O Codespaces permitirá executar tarefas como:

- Editar e revisar o código.
- Analisar arquivos e documentação.
- Executar tarefas Gradle.
- Automatizar verificações por meio do GitHub Actions.
- Gerar APKs quando as dependências e os recursos necessários estiverem disponíveis.
- Manter o trabalho versionado no GitHub.

Entretanto, a compilação bem-sucedida não comprova compatibilidade funcional com um veículo ou dispositivo Android Auto. Testes de integração e validação em hardware compatível poderão ser necessários.

## 6. Estratégia de IA sem custos

Uma das metas do projeto é minimizar o custo de desenvolvimento, utilizando serviços gratuitos, cotas incluídas e ferramentas open source sempre que possível.

A estratégia poderá incluir:

1. Agentes de IA conectados a APIs que ofereçam cotas gratuitas.
2. Provedores alternativos para reduzir a dependência de um único serviço.
3. Modelos e ferramentas locais ou open source, quando viáveis no ambiente.
4. Uso de scripts para automatizar análise, testes e documentação.
5. Execução de tarefas pesadas de forma controlada para evitar consumo desnecessário de recursos.

### Limitações de custo

O objetivo de custo zero é uma meta operacional, não uma garantia de disponibilidade ilimitada.

Cotas de APIs podem ser alteradas, exigir cadastro ou impor limites de uso. O GitHub Codespaces também possui limites de computação e armazenamento conforme o plano da conta.

O projeto deverá priorizar configurações que não exijam pagamento, evitar serviços pagos sem autorização explícita e documentar qualquer dependência de cotas gratuitas.

Nenhuma chave de API, senha ou token deverá ser armazenado diretamente no repositório.

## 7. Engenharia reversa responsável

A investigação dos aplicativos de referência deverá seguir um processo documentado:

1. Identificar e registrar a versão exata do aplicativo analisado.
2. Reunir fontes disponíveis, arquivos de referência e documentação.
3. Inspecionar os componentes e os comportamentos relevantes.
4. Registrar evidências e distinguir observações de hipóteses.
5. Mapear funcionalidades, dependências e limitações.
6. Definir uma implementação independente para os requisitos selecionados.
7. Criar testes para verificar a implementação.
8. Atualizar a documentação conforme os resultados forem confirmados.

A análise deverá respeitar as licenças dos projetos originais, os direitos autorais, as condições de distribuição e as leis aplicáveis.

O AAPRO não deverá incorporar código ou recursos proprietários sem autorização adequada, nem contornar mecanismos de segurança ou restrições de acesso de forma não autorizada.

## 8. Segurança e privacidade

O projeto deverá adotar boas práticas de segurança desde o desenvolvimento:

- Não versionar credenciais ou segredos.
- Solicitar apenas as permissões necessárias.
- Validar entradas e tratar erros de forma segura.
- Evitar downloads e execução de arquivos de origem desconhecida.
- Registrar dependências e avaliar riscos conhecidos.
- Documentar o comportamento de rede e o tratamento de dados pessoais.
- Separar configurações locais de configurações públicas do projeto.

Qualquer recurso que envolva instalação de aplicativos, acesso a arquivos, navegação web ou comunicação externa deverá ser avaliado de acordo com seu risco e suas permissões.

## 9. Estado atual

O estado real do projeto deverá ser confirmado pela inspeção do repositório e pelos resultados dos testes.

| Área                               | Situação                                          |
| ---------------------------------- | ------------------------------------------------- |
| Objetivo e referências             | Definidos pelo escopo inicial                     |
| Pesquisa dos aplicativos originais | Requer documentação e validação contínuas         |
| Arquitetura definitiva             | A definir com base na auditoria                   |
| Implementação funcional unificada  | A verificar no código atual                       |
| Interface adaptável                | A verificar em cada modalidade de uso             |
| Testes em Android Auto real        | Dependem de ambiente e hardware compatíveis       |
| Automação de compilação            | A confirmar pelos workflows existentes            |
| Estratégia de IA com custo zero    | Em planejamento e sujeita às cotas dos provedores |

Nenhuma funcionalidade deverá ser considerada concluída apenas por existir um arquivo, uma tela ou um APK compilado. A conclusão dependerá de critérios de aceitação e evidências verificáveis.

## 10. Roadmap

### Fase 1 — Auditoria

- [ ] Inspecionar a estrutura atual do AAPRO.
- [ ] Identificar a linguagem, o framework e as dependências existentes.
- [ ] Ler a documentação e os planos de implementação já disponíveis.
- [ ] Confirmar o estado real da compilação e dos testes.

### Fase 2 — Pesquisa dos projetos de referência

- [ ] Analisar o AAAD v2.8.5.
- [ ] Analisar o AABrowser v3.3.
- [ ] Registrar funcionalidades, fluxos e limitações.
- [ ] Elaborar uma matriz comparativa dos recursos.
- [ ] Documentar as evidências da engenharia reversa.

### Fase 3 — Arquitetura

- [ ] Definir os requisitos funcionais e não funcionais.
- [ ] Estabelecer os módulos e suas responsabilidades.
- [ ] Escolher e documentar as tecnologias.
- [ ] Definir critérios de compatibilidade e segurança.
- [ ] Criar uma estratégia de testes.

### Fase 4 — Implementação

- [ ] Desenvolver os módulos priorizados.
- [ ] Integrar os componentes aprovados na arquitetura.
- [ ] Construir uma interface consistente e adaptável.
- [ ] Tratar erros, permissões e situações excepcionais.
- [ ] Atualizar a documentação a cada entrega.

### Fase 5 — Validação

- [ ] Executar verificações estáticas e testes automatizados.
- [ ] Validar a compilação em ambiente limpo.
- [ ] Testar os fluxos funcionais implementados.
- [ ] Validar a integração em dispositivos compatíveis.
- [ ] Revisar segurança, dependências e documentação.
- [ ] Publicar artefatos e versões somente após as verificações necessárias.

---

## 11. Critérios de qualidade

O AAPRO deverá ser desenvolvido com foco em:

- Correção funcional demonstrável.
- Código legível, modular e sustentável.
- Interface consistente e acessível.
- Compatibilidade comprovada, sem promessas não verificadas.
- Testes reproduzíveis.
- Segurança e respeito à privacidade.
- Documentação técnica rastreável.
- Uso eficiente de recursos computacionais.
- Transparência sobre limitações, dependências e custos.

## 12. Contribuição

Contribuições são bem-vindas após a definição e publicação das diretrizes de contribuição.

Antes de propor alterações significativas:

1. Consulte a documentação existente.
2. Explique o problema ou requisito que pretende resolver.
3. Apresente evidências ou critérios de aceitação.
4. Evite incluir credenciais, arquivos pessoais ou artefatos não autorizados.
5. Documente testes executados e limitações conhecidas.

As contribuições deverão respeitar as licenças aplicáveis ao projeto e às suas dependências.

## 13. Licença

A licença do AAPRO ainda deverá ser definida e publicada pelos responsáveis pelo projeto.

Até essa definição, não se deve presumir que o código do AAPRO, do AAAD ou do AABrowser esteja automaticamente coberto pela mesma licença.

A utilização de código, bibliotecas, recursos gráficos ou outros materiais de terceiros deverá respeitar suas respectivas licenças e condições.

---

## 14. Objetivo final

O objetivo do AAPRO é transformar a pesquisa técnica sobre o AAAD e o AABrowser em uma aplicação Android unificada, organizada, moderna e sustentável.

O desenvolvimento será orientado por evidências, documentação, implementação incremental e testes verificáveis, utilizando agentes de IA como ferramentas de apoio e priorizando alternativas gratuitas sempre que tecnicamente viáveis.

**A prioridade é construir uma solução funcional e bem documentada, não apenas produzir código ou gerar um APK.**
