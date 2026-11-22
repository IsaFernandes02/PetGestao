<div align="center">

# PetGestão

[![Status](https://img.shields.io/badge/status-[em_desenvolvimento]-yellow)]()
[![Versão](https://img.shields.io/badge/versão-[0.1.0]-blue)]()
[![Licença](https://img.shields.io/badge/licença-[acadêmica]-lightgrey)]()

**Instituição:** CEUB · **Curso:** ADS · **Disciplina:** Desenvolvimento Web · **Turma/Semestre:** 2026.02 · **Professor:** Felippe Pires Ferreira

</div>

> **Logotipo / assinatura visual:** [inserir `images/logo-petgestao.png` quando a identidade visual estiver pronta]


## Sumário

- [1. Descrição do projeto](#1-descrição-do-projeto)
- [2. Funcionalidades](#2-funcionalidades)
- [3. Demonstração](#3-demonstração)
- [4. Tecnologias utilizadas](#4-tecnologias-utilizadas)
- [5. Arquitetura](#5-arquitetura)
- [6. Organização dos diretórios](#6-organização-dos-diretórios)
- [7. Participantes](#7-participantes)
- [8. Como executar](#8-como-executar)
- [9. Configuração](#9-configuração)
- [10. Testes](#10-testes)
- [11. Uso de inteligência artificial](#11-uso-de-inteligência-artificial)
- [12. Contribuição e fluxo de trabalho](#12-contribuição-e-fluxo-de-trabalho)
- [13. Histórico de versões](#13-histórico-de-versões)
- [14. Limitações e próximos passos](#14-limitações-e-próximos-passos)
- [15. Licença, referências e contato](#15-licença-referências-e-contato)


## 1. Descrição do projeto

O **PetGestão** é um sistema web de gerenciamento e organização para ONGs e protetores independentes de animais. Ele reúne em um só ambiente informações sobre os animais, cuidados com a saúde, doações recebidas, voluntários e lares temporários.

Organizações de proteção animal costumam controlar essas informações em planilhas, anotações e ferramentas separadas, o que dificulta o acompanhamento. O PetGestão oferece um painel administrativo para cada organização cadastrada, no qual os dados podem ser registrados, consultados e gerenciados de forma mais organizada.

O projeto é independente do **Adote.Anim**, plataforma voltada à divulgação de animais para adoção. Os dois sistemas poderão ser usados em conjunto, mas um não depende do outro para funcionar.

### Objetivos

- **Objetivo geral:** desenvolver uma plataforma web que auxilie ONGs e protetores independentes na administração de suas atividades de proteção animal.
- **Objetivos específicos:**
  - Centralizar o cadastro dos animais para uso em todos os módulos;
  - Registrar e consultar os cuidados de saúde dos animais (PetCare);
  - Controlar doações e estoque de produtos (AjudaPet);
  - Organizar voluntários e suas tarefas (VoluntPet);
  - Acompanhar os animais em lares temporários (Lar Temporário);
  - Oferecer busca, relatórios e uma API REST própria.

### Público-alvo

- ONGs de proteção animal;
- Abrigos e instituições de acolhimento;
- Protetores independentes;
- Organizações que realizam resgates e cuidados de animais.



## 2. Funcionalidades

| Funcionalidade | Descrição | Status |
|---|---|---|
| Autenticação e perfis de acesso | Login e logout; perfis de administrador da plataforma e responsável pela ONG; cada organização acessa apenas os seus dados. | Planejada |
| Painel administrativo | Visão geral da organização: animais, vacinações pendentes, voluntários, doações e estoque. | Planejada |
| Animais | Cadastro centralizado, consulta, edição e exclusão. | Planejada |
| PetCare | Vacinas, consultas veterinárias, medicamentos e datas de retorno. | Planejada |
| AjudaPet | Doadores, doações financeiras e de materiais, entrada e saída de estoque, estoque baixo. | Planejada |
| VoluntPet | Cadastro de voluntários, habilidades, disponibilidade e tarefas. | Planejada |
| Lar Temporário | Pessoas acolhedoras, animais acolhidos, datas e situação do acolhimento. | Planejada |
| Busca | Pesquisa de animais, doações, voluntários e outros registros. | Planejada |
| Relatórios | Relatório com dados consolidados, visualizável e exportável ou imprimível. | Planejada |
| API REST própria | Disponibilização de dados selecionados dos animais em JSON. | Planejada |
| Consulta de CEP (ViaCEP) | Preenchimento automático de endereço no cadastro de organizações e lares temporários. | Planejada |

### Requisitos não funcionais

- **Segurança:** autenticação, controle de permissões, proteção das informações e HTTPS em produção.
- **Usabilidade:** interface responsiva para computador e celular.
- **Usabilidade:** interface responsiva para computador e celular; relatórios imprimíveis.
- **Disponibilidade:** aplicação publicada em URL pública durante o período de avaliação.

## 3. Demonstração

*Capturas de tela e protótipos serão adicionados quando disponíveis.*

| Tela | Descrição |
|---|---|
| [Login] | [descrição] |
| [Painel] | [descrição] |

**Protótipo:** [link do Figma ou outra ferramenta]  
**Vídeo de demonstração:** [URL, quando houver]


## 4. Tecnologias utilizadas

| Camada | Tecnologia | Versão |
|---|---|---|
| Linguagem | Python | [versão] |
| Backend | Django | [versão] |
| API | Django REST Framework | [versão] |
| Frontend | HTML5, CSS3 e JavaScript (Django Templates) | — |
| Banco de dados | PostgreSQL (a confirmar) | [versão] |
| API externa | ViaCEP | — |
| Versionamento | Git e GitHub | — |
| Outras ferramentas | [Ex.: Figma, draw.io, Postman] | — |


## 5. Arquitetura

[Descrever a arquitetura após a conclusão do documento em `docs/arquitetura/`: camadas, componentes e fluxo de dados.]

```text
[Usuário] → [Interface (Django Templates)] → [Backend Django / API REST] → [Banco de dados]
                                                     ↓
                                              [API externa: ViaCEP]
```

**Decisões relevantes:** [preencher conforme o documento de arquitetura]

### Endpoints principais

*Os endpoints serão definidos no contrato da API em `docs/api/`.*

| Método | Rota | Descrição |
| --- | --- | --- |
| `POST` | `/api/[recurso]` | [Ex.: criar um registro] |
| `GET` | `/api/[recurso]` | [Ex.: listar registros] |
| `GET` | `/api/[recurso]/{id}` | [Ex.: obter um registro] |
| `PUT` | `/api/[recurso]/{id}` | [Ex.: atualizar um registro] |
| `DELETE` | `/api/[recurso]/{id}` | [Ex.: remover um registro] |

**Documentação completa da API:** [link do Swagger/OpenAPI, quando publicado]


## 6. Organização dos diretórios

```text
.
├── README.md                 # Documentação principal do projeto
├── .env.example              # Modelo de variáveis de ambiente (sem segredos)
├── requirements.txt          # Dependências do projeto
├── manage.py                 # Inicialização do Django
├── docs/                     # Documentação e artefatos técnicos
│   ├── README.pdf            # Índice da pasta docs/
│   ├── modelagem/
│   │   ├── casos-de-uso/
│   │   │   └── especificacoes-casos-de-uso.pdf
│   │   ├── classes/
│   │   │   └── diagrama-de-classes.pdf
│   │   └── banco-de-dados/
│   │       ├── diagrama-er.pdf
│   │       └── modelo-logico.pdf
│   ├── visao/
│   ├── arquitetura/
│   ├── api/
│   ├── prototipos/
│   ├── planejamento/
│   └── seguranca/
├── images/                   # Figuras da documentação geral
├── src/                      # Código-fonte da aplicação
│   ├── frontend/             # Interface com o usuário
│   └── backend/              # Aplicação Django, regras de negócio e API
├── tests/                    # Testes automatizados
└── scripts/                  # Scripts auxiliares de setup, build ou deploy
```

| Diretório / arquivo | Função |
|---|---|
| `README.md` | Apresentação do projeto e guia de navegação. |
| `.env.example` | Lista das variáveis necessárias, sem credenciais reais. |
| `docs/` | Documentação e diagramas das Fases 1 e 2. |
| `docs/modelagem/` | Casos de uso, classes e modelo de dados. |
| `images/` | Logotipo e imagens usadas na documentação geral. |
| `src/` | Código-fonte organizado por camada ou módulo. |
| `src/frontend/` | Interface do sistema. |
| `src/backend/` | Aplicação Django, regras de negócio e API. |
| `tests/` | Casos de teste e evidências de verificação. |
| `scripts/` | Scripts auxiliares de configuração e execução. |



## 7. Participantes

| Nome | Matrícula | Função no projeto |
|---|---|---|
| Isadora | 22505955 | Frontend — desenvolvimento da interface e integração com o backend. |
| Renata | [matrícula] | Backend — desenvolvimento da aplicação Django, regras de negócio, banco de dados e API. |

**Professor responsável:** Felippe Pires Ferreira


## 8. Como executar

### Pré-requisitos

- Git;
- Python [versão];
- [Banco de dados escolhido pelo grupo].

### Instalação e execução

```bash
# 1. Clonar o repositório
git clone [URL_DO_REPOSITORIO]
cd [NOME_DA_PASTA]

# 2. Criar e ativar o ambiente virtual
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Instalar dependências
pip install -r requirements.txt

# 4. Configurar variáveis de ambiente
cp .env.example .env
# edite o arquivo .env com as configurações locais

# 5. Criar as tabelas do banco
python manage.py migrate

# 6. Criar um usuário administrador
python manage.py createsuperuser

# 7. Executar a aplicação
python manage.py runserver
```

**Acesso local:** [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

### Implantação

- **Ambiente:** [serviço de hospedagem]
- **URL de produção:** [https://...]
- **Documentação da API:** [https://.../api/docs/]
- **Conta de teste:** [informar usuário de demonstração, sem dados reais]


## 9. Configuração

| Variável | Obrigatória | Descrição | Exemplo |
|---|---|---|---|
| `SECRET_KEY` | Sim | Chave secreta do Django. | `[gerar localmente]` |
| `DEBUG` | Sim | Modo de depuração (`False` em produção). | `True` |
| `ALLOWED_HOSTS` | Em produção | Domínios permitidos. | `meu-app.exemplo.com` |
| `CSRF_TRUSTED_ORIGINS` | Em produção | Origens HTTPS confiáveis. | `https://meu-app.exemplo.com` |
| `DATABASE_URL` | Sim | Conexão com o banco de dados. | `[formato conforme o banco escolhido]` |

*Confirme esta lista com o arquivo de configurações do projeto.* Credenciais reais devem ficar apenas no arquivo `.env`, que não é versionado.


## 10. Testes

```bash
python manage.py test
```

| Tipo | Ferramenta | O que verifica |
|---|---|---|
| Automatizados | Django Test Framework | [fluxos críticos e API] |
| Manuais | Roteiro em `tests/` ou `docs/` | [fluxos principais da interface] |

**Cobertura atual:** [não medida]


## 11. Uso de inteligência artificial

Este repositório segue a política de uso de IA da disciplina (semáforo pedagógico):

![Política de uso de IA — semáforo](images/semaforo.png)

| Situação | Significado |
| --- | --- |
| **Vermelho — uso proibido** | Atividades de autonomia intelectual (ex.: provas presenciais sem consulta). |
| **Amarelo — uso limitado** | IA pode ser ferramenta auxiliar, desde que haja declaração de uso. |
| **Verde — uso permitido** | Uso livre ao longo da atividade acadêmica. |

### Declaração de uso

*Preencha de forma honesta. Se não houve uso de IA, declare explicitamente.*

- **Houve uso de IA neste projeto?** Sim.
- **Ferramentas utilizadas:** Claude e ChatGPT.
- **Finalidade:** apoio na organização e revisão do README, esclarecimento de dúvidas, análise de materiais do projeto e auxílio técnico durante o desenvolvimento.
- **O que NÃO foi delegado à IA:** [ajustar conforme a realidade do grupo, respeitando as orientações da disciplina sobre elaboração das especificações, decisões do projeto e implementação].


## 12. Contribuição e fluxo de trabalho

### Branches

- `main`: versão estável para avaliação;
- `develop`: integração do grupo *(opcional)*;
- `feat/[nome]`: nova funcionalidade;
- `fix/[nome]`: correção de defeito;
- `docs/[nome]`: alterações só de documentação.

### Commits

Use mensagens curtas e no imperativo, por exemplo:

- `feat: adiciona cadastro de animais`
- `fix: corrige validação de data`
- `docs: atualiza instruções de execução`

### Passos sugeridos

1. Criar uma branch a partir de `main`.
2. Implementar e testar localmente.
3. Abrir um *pull request* para revisão da outra integrante.
4. Só então integrar à branch principal.

**Issues e quadro de tarefas:** [link do GitHub Projects ou similar]


## 13. Histórico de versões

| Versão | Data | Descrição |
|---|---|---|
| `0.0.1` | [2026-11-21] | Estrutura inicial do repositório. |


## 14. Limitações e próximos passos

### Problemas conhecidos

- [preencher ao longo do desenvolvimento]

### Roadmap

- [ ] Fase 1: documentação e arquitetura;
- [ ] Fase 2: implementação, publicação, segurança e apresentação.

**Fora do escopo inicial (versões futuras):**

- [ ] Notificações automáticas;
- [ ] Controle financeiro completo;
- [ ] Agendamento de consultas;
- [ ] Aplicativo para celular;
- [ ] Integração entre o PetGestão e o Adote.Anim por meio de APIs.


## 15. Licença, referências e contato

**Licença:** uso exclusivamente acadêmico.

Este material destina-se a fins educacionais.

### Documentação complementar

- **Índice da pasta `docs/`:** [`docs/README.pdf`](docs/README.pdf)
- **Apresentação:** [`docs/apresentacao.pdf`](docs/apresentacao.pdf)
- **Documento de visão:** `docs/visao/`
- **Casos de uso (diagrama + especificações):** [`docs/modelagem/casos-de-uso/especificacoes-casos-de-uso.pdf`](docs/modelagem/casos-de-uso/especificacoes-casos-de-uso.pdf) (`docs/modelagem/casos-de-uso/`)
- **Diagrama de classes:** [`docs/modelagem/classes/diagrama-de-classes.pdf`](docs/modelagem/classes/diagrama-de-classes.pdf) (`docs/modelagem/classes/`)
- **Modelo de dados (`docs/modelagem/banco-de-dados/`):**
  - Modelo conceitual (ER): [`docs/modelagem/banco-de-dados/diagrama-er.pdf`](docs/modelagem/banco-de-dados/diagrama-er.pdf)
  - Modelo lógico: [`docs/modelagem/banco-de-dados/modelo-logico.pdf`](docs/modelagem/banco-de-dados/modelo-logico.pdf)
- **Arquitetura:** `docs/arquitetura/`
- **Contrato da API e integração externa:** `docs/api/`
- **Protótipos e identidade visual:** `docs/prototipos/`
- **Planejamento:** `docs/planejamento/`

### Referências

- Django: [https://docs.djangoproject.com](https://docs.djangoproject.com)
- Django REST Framework: [https://www.django-rest-framework.org](https://www.django-rest-framework.org)
- ViaCEP: [https://viacep.com.br](https://viacep.com.br)

### Contato

Dúvidas sobre o projeto: [e-mail institucional do grupo ou issue no repositório]

**Agradecimentos:** Professor Felippe — Desenvolvimento Web.
