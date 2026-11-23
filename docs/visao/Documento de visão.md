<div align="center">
  
  # Documento de Visão 
  

## PetGestão — Sistema de Gestão para Organizações de Proteção Animal



| Campo | Detalhe |
| :--- | :--- |
| **Versão** | 1.0 |
| **Status** | Versão inicial para revisão da equipe |
| **Disciplina** | Desenvolvimento Web |
| **Professor** | Felippe Pires Ferreira |
| **Tecnologias principais** | Python, Django, HTML, CSS, JavaScript e banco de dados relacional. |

</div>


## 1. Contextualização do projeto

As organizações não governamentais (ONGs), abrigos e protetores independentes desempenham um papel fundamental na proteção, no resgate e no acolhimento de animais. Entretanto, a administração dessas iniciativas envolve uma série de processos e informações que precisam ser acompanhados continuamente, como o cadastro dos animais acolhidos, o controle de vacinas, medicamentos e consultas veterinárias, a gestão de doações e materiais, além da organização de voluntários e lares temporários.

Em muitas situações, esses registros encontram-se distribuídos em diferentes ferramentas, como planilhas, documentos físicos ou digitais, aplicativos de mensagens e redes sociais. Essa fragmentação dificulta a localização e a atualização dos dados, tornando mais complexo visualizar o histórico completo dos animais, identificar necessidades de reposição de insumos e acompanhar as responsabilidades da equipe.

Diante desse cenário, surge o PetGestão, uma aplicação web desenvolvida com o objetivo de centralizar as atividades administrativas dessas instituições em um único ambiente digital. A plataforma busca facilitar o gerenciamento das rotinas diárias, oferecendo recursos que promovem maior controle, organização dos processos e eficiência no acompanhamento das ações realizadas em prol dos animais.

## 2. Justificativa

A criação do PetGestão é motivada pela necessidade de oferecer um ambiente digital que facilite a organização administrativa e o acompanhamento das atividades realizadas por ONGs e protetores independentes. A proposta considera que essas instituições precisam administrar diferentes responsabilidades simultaneamente — envolvendo animais, cuidados veterinários, doações, estoques, voluntários e lares temporários —, muitas vezes utilizando ferramentas dispersas e que não estão integradas entre si.

Ao centralizar essas informações em uma única aplicação web, o sistema reduz a dispersão de dados e a dependência de múltiplos controles paralelos. Essa unificação facilita o acesso rápido aos registros, melhora a visualização do cenário operacional e auxilia diretamente na tomada de decisões da rotina institucional. Dessa forma, o projeto utiliza a tecnologia como instrumento de apoio à causa animal, otimizando a gestão para que as organizações possam dedicar mais tempo e atenção às atividades essenciais de acolhimento, proteção e cuidado dos animais.

## 3. Objetivos

### 3.1. Objetivo geral

Desenvolver uma aplicação web utilizando Python e Django para auxiliar a gestão de ONGs e protetores independentes, centralizando informações e oferecendo funcionalidades para administrar animais, cuidados veterinários, doações, estoques, voluntários e lares temporários.

### 3.2. Objetivos específicos

- Permitir o cadastro e o gerenciamento das organizações e de seus usuários.
- Centralizar o cadastro e as informações dos animais acolhidos.
- Registrar e acompanhar vacinas, consultas, medicamentos e tratamentos.
- Permitir o controle de doações recebidas e dos materiais disponíveis.
- Organizar o cadastro de voluntários, suas habilidades e disponibilidade.
- Permitir o acompanhamento dos animais encaminhados para lares temporários.
- Disponibilizar mecanismos de pesquisa e consulta dos registros.
- Gerar relatórios e indicadores relacionados às atividades das organizações.
- Disponibilizar uma API REST própria para acesso a informações selecionadas do sistema.
- Integrar a API ViaCEP para auxiliar no preenchimento de endereços durante os cadastros.
- Publicar a aplicação em ambiente acessível pela Internet, com configurações adequadas de segurança.

## 4. Público-alvo

- ONGs de proteção animal: instituições que precisam administrar animais acolhidos, doações, voluntários e demais atividades.
- Abrigos e instituições de acolhimento: organizações responsáveis pelo acompanhamento dos animais e de suas necessidades.
- Protetores independentes: pessoas que realizam atividades de resgate, acolhimento e proteção animal.
- Responsáveis pelas organizações: usuários que administram os registros, os acessos e as atividades da instituição.
- Voluntários e responsáveis por lares temporários: pessoas envolvidas nas atividades e nos cuidados dos animais, conforme as permissões definidas pela organização.

## 5. Stakeholders — Partes interessadas

As principais partes interessadas identificadas são:

- **ONGs e instituições de proteção animal:** organizações que utilizarão o sistema para administrar suas atividades e informações.
- **Protetores independentes:** pessoas que realizam atividades de resgate, acolhimento e proteção animal e que poderão utilizar a aplicação para organizar seus registros.
- **Administradores e responsáveis pelas organizações:** usuários responsáveis pelo gerenciamento da instituição e pelo controle dos acessos.
- **Voluntários:** pessoas que colaboram com as atividades das organizações e poderão ter suas informações e atividades administradas pelo sistema.
- **Responsáveis pelos lares temporários:** pessoas que recebem animais temporariamente e participam do acompanhamento de seus acolhimentos.
- **Equipe de desenvolvimento:** responsáveis pela análise, implementação, manutenção e evolução da aplicação.


## 6. Escopo do projeto

O PetGestão pretende disponibilizar um ambiente centralizado para auxiliar o gerenciamento das atividades administrativas das organizações de proteção animal.

O escopo inicial contempla os seguintes módulos:

### 6.1. Gestão de organizações

- Cadastro e gerenciamento de organizações.
- Autenticação e controle de acesso dos usuários.
- Separação das informações de cada organização, respeitando as permissões de acesso.

### 6.2. Cadastro e gerenciamento de animais

- Cadastro, consulta, alteração e exclusão de animais.
- Registro das características e da situação dos animais acolhidos.
- Consulta e pesquisa dos registros.
- Acompanhamento do histórico dos animais.

### 6.3. PetCare — Saúde e cuidados

- Registro de vacinas.
- Registro de consultas veterinárias.
- Controle de medicamentos e tratamentos.
- Acompanhamento de datas de retorno e próximos cuidados veterinários.
- Consulta ao histórico de saúde dos animais.

### 6.4. AjudaPet — Doações e estoque

- Cadastro e controle de doações recebidas.
- Identificação de doadores.
- Gerenciamento de produtos e materiais disponíveis em estoque.
- Registro de entradas e saídas de materiais.
- Identificação de produtos com estoque reduzido.

### 6.5. VoluntPet — Gestão de voluntários

- Cadastro e gerenciamento de voluntários.
- Registro de habilidades e disponibilidade.
- Organização de atividades e tarefas.
- Acompanhamento das atividades atribuídas aos voluntários.

### 6.6. Lar Temporário

- Cadastro de responsáveis por lares temporários.
- Registro dos animais encaminhados.
- Acompanhamento de datas de entrada e saída.
- Atualização da situação do acolhimento.
- Consulta ao histórico dos animais encaminhados.

### 6.7. Consultas e relatórios

- Consultas e pesquisas dos registros cadastrados.
- Apresentação de indicadores e dados consolidados.
- Geração de relatórios administrativos.
- Aplicação de filtros para consulta das informações.
- Possibilidade de visualização, exportação ou impressão dos resultados.

### 6.8. Integração externa

A aplicação prevê a integração com a API ViaCEP para consulta e preenchimento de informações de endereço a partir do CEP informado nos cadastros de organizações, responsáveis ou outros registros que necessitem de endereço.

O dado retornado deverá ser utilizado no preenchimento das informações cadastrais, tornando a integração parte de um fluxo real da aplicação.

### 6.9. API REST própria

O sistema deverá disponibilizar uma API REST própria para a disponibilização de informações selecionadas, utilizando endpoints definidos, métodos HTTP e respostas no formato JSON.

### 6.10. Interface e publicação

- Desenvolvimento de uma interface responsiva.
- Aplicação de uma identidade visual consistente.
- Disponibilização da aplicação em ambiente web.
- Acesso ao sistema por meio de navegadores de Internet.

## 7. Fora do escopo

O PetGestão tem como finalidade auxiliar a organização administrativa das instituições, não sendo responsável pela execução direta das atividades de proteção animal.

Não fazem parte do escopo inicial:

- Realização de resgates ou transporte de animais.
- Atendimento veterinário, diagnóstico ou prescrição de medicamentos.
- Execução de procedimentos médicos.
- Processamento de pagamentos ou transferências financeiras.
- Plataforma pública de adoção e divulgação de animais.
- Chat em tempo real entre organizações e usuários.
- Aplicativo móvel nativo.
- Integração automática com todas as redes sociais e aplicativos de mensagens.
- Controle de serviços prestados por clínicas veterinárias externas.
- Automação de campanhas de arrecadação de recursos.

Funcionalidades adicionais poderão ser avaliadas para versões futuras, conforme as necessidades identificadas e a viabilidade de implementação.

## 8. Funcionalidades

### 8.1. Requisitos funcionais
|ID  | Requisito |
|---|---|
| RF01  | Cadastrar, consultar, alterar e excluir organizações.|
| RF02  | Cadastrar e gerenciar usuários e seus respectivos acessos.|
| RF03  | Cadastrar, consultar, alterar e excluir animais.|
| RF04	| Registrar e atualizar as informações e a situação dos animais.|
| RF05	| Registrar vacinas, consultas, medicamentos e tratamentos dos animais.|
| RF06	| Consultar o histórico de saúde e os próximos cuidados dos animais.|
| RF07	| Cadastrar e consultar doadores e doações recebidas.|
| RF08	| Cadastrar e gerenciar produtos e materiais em estoque.|
| RF09	| Registrar entradas e saídas de produtos e identificar estoque reduzido.|
| RF10	| Cadastrar e gerenciar voluntários.|
| RF11	| Registrar habilidades, disponibilidade e atividades dos voluntários.|
| RF12	| Cadastrar responsáveis por lares temporários e acompanhar os acolhimentos.|
| RF13	| Consultar e pesquisar animais e demais registros cadastrados.|
| RF14	| Gerar relatórios e indicadores administrativos com filtros.|
| RF15	| Consultar endereços por CEP utilizando a API ViaCEP.|
| RF16	| Disponibilizar uma API REST própria para consulta de informações selecionadas.|
| RF17	| Restringir o acesso às informações conforme as permissões dos usuários e da organização.|

### 8.2. Requisitos não funcionais

- Segurança: armazenamento seguro de senhas, controle de acesso, proteção de credenciais e validação dos dados recebidos.
- Usabilidade: interface organizada e intuitiva, facilitando a utilização por pessoas com diferentes níveis de familiaridade tecnológica.
- Responsividade: aplicação adaptável a computadores, tablets e celulares.
- Confiabilidade: tratamento de erros e falhas durante as operações e integrações externas.
- Integridade: manutenção da consistência dos registros e dos relacionamentos entre as informações.
- Desempenho: consultas e operações realizadas em tempo adequado, considerando o volume de dados da aplicação.
- Disponibilidade: aplicação publicada e acessível durante o período de avaliação.
- Manutenibilidade: código organizado em módulos, com estrutura que facilite correções e futuras melhorias.
- Privacidade: acesso às informações limitado aos usuários autorizados, respeitando a separação entre organizações.

## 9. Restrições
- Tecnologias: utilização de Python e Django no desenvolvimento do backend.
- Interface: utilização de HTML, CSS e JavaScript para a construção da interface web.
- Banco de dados: utilização de banco de dados relacional.
- API REST: implementação preferencialmente com Django REST Framework.
- Integração externa: utilização da API ViaCEP para consulta de endereços.
- Prazo: desenvolvimento condicionado ao calendário e às entregas da disciplina.
- Equipe: implementação de acordo com a divisão de atividades e a disponibilidade dos integrantes.
- Infraestrutura: necessidade de ambiente de hospedagem compatível com a aplicação e o banco de dados.
- Segurança: credenciais e informações sensíveis não poderão ser armazenadas diretamente no repositório público.

## 10. Premissas

- Os usuários terão acesso à Internet e a um navegador atualizado.
- As organizações serão responsáveis pelo fornecimento e pela atualização das informações cadastradas.
- Cada organização deverá acessar somente os registros para os quais possui autorização.
- Os usuários terão conhecimentos básicos para utilizar aplicações web.
- A API ViaCEP estará disponível para consulta durante a utilização do sistema.
- Quando a integração externa estiver indisponível, o sistema deverá tratar a falha sem comprometer as demais operações.
- A equipe terá acesso aos recursos necessários para desenvolvimento, testes e publicação da aplicação.
- Os dados utilizados na demonstração poderão ser fictícios, evitando a exposição de informações pessoais reais.

## 11. Riscos iniciais

| ID | Risco | Probabilidade | Impacto | Mitigação |
|---|---|---|---|---|
| R1 | Dificuldade em identificar todas as necessidades reais das organizações | Média | Alto | Pesquisar instituições e validar as funcionalidades com possíveis usuários. |
| R2 | Prazo insuficiente para implementar todos os módulos | Alta | Alto | Priorizar funcionalidades essenciais e organizar o desenvolvimento por etapas. |
| R3 | Falhas ou indisponibilidade da API ViaCEP | Média | Médio | Implementar tratamento de erros e permitir preenchimento manual do endereço. |
| R4 | Acesso indevido às informações de outras organizações | Média | Alto | Implementar autenticação, permissões e isolamento dos dados. |
| R5 | Cadastro de informações incorretas ou desatualizadas | Média | Médio | Implementar validações e permitir atualização dos registros. |
| R6 | Dificuldades na integração entre frontend e backend | Média | Alto | Definir previamente os contratos da API e realizar integrações progressivas. |
| R7 | Problemas durante a publicação da aplicação | Média | Alto | Realizar testes de hospedagem antecipadamente. |
| R8 | Perda de informações ou inconsistências no banco de dados | Baixa | Alto | Implementar medidas de integridade e procedimentos de backup. |
| R9 | Distribuição desequilibrada das atividades da equipe | Média | Médio | Definir responsáveis, acompanhar tarefas e manter contribuições identificáveis no GitHub. |

## 12. Critérios de sucesso

- Cadastro, consulta, alteração e exclusão dos registros previstos funcionando corretamente.
- Possibilidade de cadastrar e acompanhar os animais e seus históricos.
- Funcionamento dos módulos de saúde, doações, estoque, voluntários e lares temporários previstos para a versão entregue.
- Centralização das informações em um ambiente único.
- Consultas e pesquisas apresentando os registros correspondentes aos filtros utilizados.
- Relatórios administrativos apresentando informações consistentes.
- API REST própria funcional e documentada.
- Integração com a API ViaCEP funcionando em um fluxo real de cadastro.
- Controle de acesso e separação dos dados entre organizações funcionando adequadamente.
- Interface responsiva e compatível com os navegadores utilizados na avaliação.
- Aplicação publicada e acessível pela Internet.
- Documentação técnica atualizada e compatível com a implementação final.
- Tratamento adequado de falhas e erros nas operações da aplicação.


