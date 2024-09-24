# Template para os projetos desenvolvidos no SENAI-SP

---

## **Pré-requisitos**

- **Python instalado**: Certifique-se de que o Python 3.x está instalado em seu sistema.
- **Cookiecutter instalado**: Se ainda não instalou o Cookiecutter, faça isso com o seguinte comando:

```bash
  pip install cookiecutter
```

### Passo 1: Utilizar o Cookiecutter com a URL do GitHub
Você pode gerar um novo projeto diretamente a partir do repositório do GitHub usando o Cookiecutter.

Comando:
```bash
cookiecutter https://github.com/Unidade-de-Inteligencia-SENAI/template-senai.git
```

---

*Nota*: Se o repositório for privado, siga as instruções na seção "Repositório Privado" abaixo.

---

#### Passo 2: Fornecer as Informações Solicitadas
Após executar o comando, o Cookiecutter irá clonar o template e solicitará que você insira as informações necessárias definidas no arquivo cookiecutter.json do template.

Por exemplo:
```json
project_name [meu_projeto]: nome do meu projeto
```
*Ação*:
- Digite o nome do seu projeto e pressione Enter. Este nome será usado para nomear a pasta do projeto e em outros locais conforme definido no template.

---

#### Passo 3: Gerar o Projeto
O Cookiecutter irá criar uma nova pasta com o nome do projeto que você forneceu, contendo toda a estrutura definida no template.

---

#### Passo 4: Verificar a Estrutura do Projeto
Navegue até a pasta do seu novo projeto e verifique a estrutura de diretórios e arquivos.

Comandos:
```bash
cd nome_do_seu_projeto
ls -R
```
Estrutura Esperada:
```css
├── src/
│   ├── __init__.py
│   └── main.py
├── data/
├── requirements.txt
└── README.md
```

---

#### Passo 5: Instalar Dependências (Se Necessário)
Se o arquivo requirements.txt estiver presente e contiver dependências, instale-as usando:
```bash
pip install -r requirements.txt
```

---

## Informações Adicionais
*Repositório Privado*
Se o repositório template-senai for privado, você precisará autenticar-se para acessá-lo.

#### Opção 1: Usar SSH
Verifique se você tem acesso SSH configurado para o repositório corporativo.

Use o comando com a URL SSH:
```bash
cookiecutter git@github.com:Unidade-de-Inteligencia-SENAI/template-senai.git
```

### Opção 2: Usar Token de Acesso Pessoal
Gere um Token de Acesso Pessoal (PAT) no GitHub com permissão para acessar repositórios.

Use o comando com o token:
```bash
cookiecutter https://<seu_token>@github.com/Unidade-de-Inteligencia-SENAI/template-senai.git
```
*Nota*: Substitua <seu_token> pelo seu token real.

Importante: Tenha cuidado ao usar tokens em comandos, pois eles podem ser armazenados no histórico do terminal.

---

#### Clonar o Template Localmente
Caso tenha problemas ao acessar o repositório diretamente, você pode clonar o template para o seu computador e depois usar o Cookiecutter localmente.

- Passo 1: Clonar o Repositório
```bash
git clone git@github.com:Unidade-de-Inteligencia-SENAI/template-senai.git
```

- Passo 2: Usar o Cookiecutter Localmente
```bash
cookiecutter template-senai/
```
