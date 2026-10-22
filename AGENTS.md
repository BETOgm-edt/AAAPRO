# AAPRO — Agent Instructions

## 1. Missão obrigatória

O objetivo deste repositório é desenvolver o **AAPRO**, uma nova aplicação Android que unifique, de forma aprimorada e organizada, funcionalidades selecionadas do AAAD v2.8.5 e do AABrowser v3.3, investigadas por meio de engenharia reversa.

A prioridade técnica é utilizar ao máximo as capacidades pertinentes do **REA — Reverse Engineer Anything** para compreender os aplicativos de referência, reunir evidências, documentar seu funcionamento e orientar uma implementação independente.

O AAPRO NÃO é um aplicativo de academia, treinamento, musculação, dieta ou acompanhamento de exercícios.

Não transforme o projeto em outro tipo de aplicação. Não substitua seu objetivo por uma implementação genérica de Android.

## 2. Fontes oficiais de referência

- REA: https://github.com/morluto/rea
- AAAD v2.8.5: https://github.com/shmykelsa/AAAD/releases/tag/v2.8.5
- AABrowser v3.3: https://github.com/kododake/AABrowser/releases/tag/v3.3

Utilize as versões exatas indicadas para a análise inicial. Outras versões podem ser estudadas posteriormente, mas devem ser identificadas separadamente.

Consulte os repositórios originais, o código-fonte disponível, as releases, os APKs e a documentação pertinente. Não presuma que o código-fonte de um repositório representa integralmente o binário publicado.

## 3. Regra principal: investigar antes de implementar

Antes de criar ou modificar funcionalidades derivadas dos aplicativos de referência:

1. Inspecione o estado atual do repositório AAPRO.
2. Leia o README, a documentação em `docs/`, os planos existentes e as configurações de build.
3. Verifique se o REA está instalado, configurado e conectado ao agente utilizado.
4. Consulte a documentação e os recursos efetivamente disponíveis na versão instalada do REA.
5. Obtenha os artefatos de referência de fontes oficiais ou autorizadas.
6. Utilize os recursos de análise do REA apropriados ao tipo de artefato.
7. Registre as evidências obtidas e as limitações da análise.
8. Compare os resultados com o código-fonte disponível e a documentação original.
9. Elabore uma especificação funcional verificável.
10. Só então proponha e implemente o recurso correspondente no AAPRO.

Não execute rotinas de diagnóstico indiscriminadamente quando o REA já estiver configurado e funcional. Verifique os recursos existentes e execute apenas as etapas necessárias para a investigação atual.

Se o REA não estiver disponível, explique o impedimento, consulte as instruções oficiais de instalação e proponha o menor passo necessário para habilitá-lo. Não simule resultados de ferramentas que não foram executadas.

## 4. Utilização do REA

Utilize o REA como ferramenta central de investigação sempre que a tarefa depender de comportamento observado em APKs, binários, código descompilado ou execução do aplicativo original.

Quando aplicável, investigue:

- Manifesto Android, permissões e componentes declarados.
- Activities, Services, Receivers e Providers.
- Classes, métodos, chamadas e referências entre componentes.
- Recursos, strings, layouts e configurações.
- Dependências e bibliotecas relevantes.
- Fluxos de navegação e estados da interface.
- Requisições de rede e comportamento observável.
- Instalação, atualização, detecção e gerenciamento de aplicativos.
- Comportamentos relacionados à navegação web.
- Interações com o Android Auto, quando houver evidência disponível.
- Diferenças entre versões e entre código-fonte e binário publicado.

Use somente as ferramentas, os comandos e os parâmetros efetivamente suportados pela versão instalada do REA. Consulte os contratos das ferramentas e os guias oficiais antes de elaborar comandos específicos.

Para análise Android, instale e configure os pré-requisitos necessários, como JDK, JADX e ADB quando aplicáveis. Não suponha que todos estejam presentes no GitHub Codespaces.

A análise dinâmica exige um dispositivo ou emulador compatível e ferramentas apropriadas. Se esses recursos não estiverem disponíveis, execute a análise estática possível e documente as limitações.

Não conclua que uma funcionalidade funciona apenas porque encontrou uma classe, uma string ou um método com nome sugestivo.

## 5. Matriz de engenharia reversa

Mantenha documentação organizada em `docs/reverse-engineering/`.

Crie, no mínimo:

- `AAAD-2.8.5.md`
- `AABrowser-3.3.md`
- `FEATURE-COMPARISON.md`
- `EVIDENCE-LOG.md`
- `AAPRO-SPECIFICATION.md`

Cada investigação deve registrar:

- Aplicativo e versão analisados.
- Origem do artefato.
- Hash do arquivo analisado, quando disponível.
- Ferramentas e versões utilizadas.
- Pergunta investigada.
- Procedimento executado.
- Evidências relevantes produzidas pelo REA.
- Arquivos, classes, métodos ou componentes associados.
- Resultado confirmado.
- Hipóteses ainda não verificadas.
- Limitações técnicas.
- Consequências para a arquitetura do AAPRO.
- Próximos experimentos necessários.

Quando houver evidências suficientes, mantenha uma matriz de funcionalidades que indique a origem, o comportamento observado, o grau de confiança, a viabilidade técnica, as dependências e o estado da implementação.

## 6. Evidências e honestidade técnica

Classifique as conclusões como:

- **Confirmado:** sustentado por evidência direta e reproduzível.
- **Provável:** sustentado por indícios consistentes, ainda sem confirmação suficiente.
- **Desconhecido:** não foi possível determinar.
- **Não aplicável:** a funcionalidade não se aplica ao contexto investigado.

Não invente resultados de REA, arquivos, métodos, logs, testes, permissões ou comportamentos.

Não afirme que um teste foi executado sem executá-lo. Não apresente hipóteses como fatos. Quando uma ferramenta falhar, registre o erro e prossiga apenas com alternativas tecnicamente justificadas.

Referencie caminhos de arquivos, métodos, resultados de ferramentas e comandos de reprodução sempre que possível.

## 7. Implementação do AAPRO

O AAPRO será uma aplicação nova, com arquitetura própria, que poderá integrar funcionalidades selecionadas de:

- Gerenciamento de aplicativos relacionado ao AAAD.
- Navegação web relacionada ao AABrowser.
- Outros recursos úteis do ecossistema Android Auto, desde que tecnicamente viáveis, autorizados e documentados.

A seleção de funcionalidades deverá resultar da investigação, não de suposições.

A arquitetura deverá ser modular, testável e sustentável. Escolha tecnologias com base no código existente, nos requisitos comprovados e na compatibilidade Android.

Não copie código, recursos ou materiais de terceiros sem verificar as respectivas licenças e condições de uso. Prefira uma implementação independente baseada no comportamento documentado quando isso for apropriado.

A compatibilidade com Android Auto deve ser validada de acordo com as categorias de aplicativos, APIs, requisitos de segurança e restrições de interface aplicáveis. Não presuma que qualquer aplicativo Android pode ser projetado livremente na tela do veículo.

## 8. Descoberta de recursos do ecossistema

Depois de analisar os dois aplicativos principais, investigue outros projetos relevantes do ecossistema Android Auto.

Para cada candidato:

1. Identifique o repositório oficial e a licença.
2. Determine qual problema resolve.
3. Avalie atividade, dependências, manutenção e compatibilidade.
4. Use REA se for necessário compreender um binário ou comportamento não explicado pelo código disponível.
5. Documente benefícios, riscos e requisitos de integração.
6. Não adicione recursos apenas por popularidade.

Priorize recursos que agreguem valor real, sejam tecnicamente viáveis e possam ser mantidos.

## 9. Preservação do repositório e do histórico

O repositório contém ou pode conter trabalho anterior que não corresponde ao objetivo do AAPRO.

Antes de remover, substituir ou reorganizar arquivos:

1. Verifique `git status`, branches, commits e arquivos modificados.
2. Identifique código, documentação, workflows e artefatos relevantes.
3. Preserve o trabalho existente em branch ou tag de arquivo quando necessário.
4. Não apague o histórico Git nem force-push sem autorização explícita.
5. Não remova arquivos úteis de infraestrutura só porque foram criados durante uma implementação incorreta.
6. Separe claramente o material legado do produto pretendido.
7. Registre a decisão de migração e valide o estado final.

Código de academia ou treinamento não pertence ao produto AAPRO. Deve ser isolado e removido da linha principal somente após a preservação e a auditoria adequadas.

## 10. Desenvolvimento com custo mínimo

Priorize ferramentas open source, serviços com cotas gratuitas e recursos já disponíveis no GitHub Codespaces.

Não presuma que APIs, modelos, dispositivos virtuais ou recursos de computação sejam ilimitados ou permanentemente gratuitos.

Antes de adotar um serviço, documente seus requisitos, limites e alternativas. Não habilite cobranças, contrate serviços ou utilize credenciais pagas sem autorização explícita.

Nunca grave tokens, senhas ou chaves de API em código, commits, logs ou documentação pública.

## 11. Processo de trabalho

Trabalhe em etapas pequenas e verificáveis:

1. Auditar.
2. Investigar com REA.
3. Documentar evidências.
4. Especificar o comportamento esperado.
5. Implementar uma mudança delimitada.
6. Executar verificações e testes.
7. Revisar diferenças no Git.
8. Atualizar a documentação.
9. Relatar o que foi concluído e o que continua pendente.

Evite reescrever o projeto inteiro de uma só vez.

Antes de mudanças extensas, apresente um plano com arquivos afetados, riscos, critérios de aceitação e estratégia de rollback.

Não destrua trabalho existente nem faça alterações irreversíveis sem autorização.

## 12. Definição de pronto

Uma funcionalidade só pode ser considerada concluída quando:

- O requisito está documentado.
- As evidências e a origem da decisão são rastreáveis.
- A implementação está integrada ao projeto correto.
- Os testes relevantes foram executados e seus resultados registrados.
- Os erros conhecidos e as limitações foram documentados.
- A documentação correspondente foi atualizada.

Um APK compilado, uma tela desenhada ou código gerado pela IA não são, isoladamente, prova de conclusão.

## 13. Primeira tarefa obrigatória para qualquer agente

Antes de desenvolver novas funcionalidades:

1. Audite o repositório atual.
2. Identifique e preserve o código de academia criado por engano.
3. Determine o estado real do build Android.
4. Verifique a instalação e a disponibilidade do REA.
5. Consulte os pré-requisitos da análise de APKs Android.
6. Planeje a investigação do AAAD v2.8.5 e do AABrowser v3.3.
7. Proponha uma estrutura de documentação de evidências.
8. Apresente um plano de recuperação do AAPRO sem apagar o histórico Git.

Não comece pela criação de novas telas. A prioridade inicial é compreender os aplicativos de referência e estabelecer uma base técnica confiável.

---

**Princípio central:** investigar com evidências, documentar o que foi descoberto e implementar somente depois de compreender o comportamento desejado. O objetivo é o AAPRO — nunca um aplicativo de academia.
