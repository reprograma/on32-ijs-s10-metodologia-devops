# GitFlow vs Trunk-Based

## GitFlow

<img src="../assets/git-flow.png" alt="CI" width="600"/>

É uma metodologia de modelo de branching que se tornou bastante popular por sua estruturação clara e por suportar um ciclo de desenvolvimento de software mais tradicional, com versões e releases definidos. Abaixo estão os principais aspectos do Git Flow:

### Caracteristicas:

#### Branches Principais:

* Main (ou Master): Representa a versão estável e lançada do software. Somente código que está pronto para ser lançado entra na branch main.

* Develop (ou Dev): É a branch onde o desenvolvimento principal ocorre. Funciona como uma "pré-release" onde o código é integrado e testado antes de ser mesclado na main.

#### Branches de Suporte:

* Feature Branches: Usadas para desenvolver novas funcionalidades. Elas partem da branch develop e são mescladas de volta nela quando a feature está pronta.
Nome típico: feature/nome-da-feature

* Release Branches: Criadas a partir de develop quando o software está pronto para uma nova release. Essa branch permite ajustes finais, como correções de bugs ou pequenas melhorias antes do lançamento.
Nome típico: release/x.x.x

* Hotfix Branches: Usadas para correções de emergência na branch main. Elas partem de main e, depois de aplicadas as correções, são mescladas de volta em main e develop.
Nome típico: hotfix/x.x.x

### Fluxo de Trabalho

* Início de uma nova feature: Cria-se uma branch a partir de develop.Desenvolvimento é feito na branch de feature.
Quando pronta, é mesclada de volta na develop.

* Preparação para um lançamento: Cria-se uma branch de release a partir de develop. Ajustes finais e testes são feitos na branch de release. Uma vez estável, a branch de release é mesclada em main e develop.

* Correção de um bug crítico (hotfix): Cria-se uma branch de hotfix a partir de main. A correção é aplicada e testada.
A branch de hotfix é mesclada em main (para o lançamento imediato) e develop (para garantir que a correção também exista no próximo ciclo de desenvolvimento).

### Vantagens e Desvantagens do GitFlow

#### Vantagens:

* Estrutura clara que facilita o gerenciamento de versões e releases.
* Adequado para equipes que fazem releases periódicos e previsíveis.

#### Desvantagens:

* Pode ser complexo e pesado para projetos com ciclos de release rápidos ou contínuos.
* Exige muita criação e mesclagem de branches, o que pode ser confuso para equipes menores ou menos experientes.

## Trunk-Based

<img src="../assets/Trunk-Based-Development.jpg" alt="CI" width="600"/>

É uma abordagem mais simplificada e ágil para o gerenciamento de branches. Nesta abordagem, o foco é em integrar o código frequentemente em uma única branch principal (trunk ou main), minimizando a necessidade de branches de longa duração.

### Caraceristicas:

* Uma Única Branch Principal: Todo o desenvolvimento é feito na branch principal (trunk ou main). Novas features e correções de bugs são integradas diretamente na Branch Principal.

* Feature Flags: Como o código é integrado frequentemente, recursos incompletos ou experimentais são frequentemente controlados por feature flags, permitindo que eles sejam ativados ou desativados sem a necessidade de criar branches separadas.

* Commits Frequentes e Pequenos: Mudanças de código são feitas em pequenos incrementos e integradas na trunk o mais rápido possível. Isso minimiza os conflitos de merge e facilita o teste contínuo.

* Integração Contínua: O processo de integração contínua (CI) é fundamental no Trunk-Based Development. Todo o código integrado na trunk deve passar por testes automatizados para garantir a estabilidade.

#### Fluxo de Trabalho:

* Início de uma nova feature: Pequenos commits são feitos diretamente na branch principal. Se a feature não estiver pronta para produção, ela é protegida por feature flags.

* Correção de bugs: correções de bugs são feitas diretamente na trunk e implantadas imediatamente.

* Release contínuo: Como o código é constantemente integrado e testado, o software pode ser liberado a qualquer momento.

### Vantagens e Desvantagens do Trunk-Based:

#### Vantagens:

* Simplicidade: Menos complexidade em comparação com o Git Flow, com menos branches para gerenciar.
* Agilidade: Ideal para equipes que fazem deploy contínuo ou têm ciclos de release muito curtos.
* Redução de conflitos de merge: Como o código é integrado frequentemente, há menos chances de conflitos complexos.

#### Desvantagens:

* Pode ser arriscado para equipes que não têm uma boa cultura de integração contínua e testes automatizados.
* Requer disciplina para garantir que o código integrado na trunk esteja sempre em um estado de alta qualidade.

### Quando Usar Cada Abordagem?

* GitFlow:

    Melhor para projetos que seguem um ciclo de release mais tradicional, com lançamentos programados e versões definidas.
    Útil em projetos onde a estabilidade da versão de produção é crítica e onde as equipes podem se dar ao luxo de trabalhar em branches separadas por longos períodos.

* Trunk-Based Development:

    Ideal para equipes ágeis que fazem deploys contínuos ou muito frequentes.
    Adequado para ambientes de desenvolvimento onde a integração contínua e os testes automatizados são bem estabelecidos.

Cada abordagem tem seus próprios méritos, e a escolha entre Git Flow e Trunk-Based Development deve ser baseada no estilo de trabalho da equipe, na complexidade do projeto e nas práticas de deploy e release adotadas pela organização.