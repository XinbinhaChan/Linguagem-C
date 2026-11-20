# 🖨️ Integração C com Impressora Elgin i9

## 📘 Sobre o Projeto

O projeto **Integração C com Impressora Elgin i9** consiste no desenvolvimento de uma aplicação em linguagem C capaz de realizar a comunicação e controlar as funcionalidades da impressora térmica Elgin i9 por meio de uma biblioteca DLL fornecida pela fabricante.

O programa oferece uma interface de menu interativo que permite configurar conexões, realizar impressões de diferentes formatos e executar comandos diretamente na impressora.

O trabalho foi desenvolvido por alunos para a disciplina de **Construção de Algoritmos e Programação**.

### ⚙️ Funcionalidades

- Configuração e gerenciamento da conexão com a impressora.
- Impressão de textos personalizados.
- Geração e impressão de QR Codes.
- Impressão de códigos de barras.
- Impressão de arquivos XML SAT e XML de Cancelamento SAT.
- Abertura de gaveta de dinheiro.
- Emissão de sinais sonoros.

---

## 🧰 Tecnologias Utilizadas

- **Linguagem:** C.
- **IDE:** Visual Studio Code (VSCode).
- **Compilador:** MinGW (32 ou 64 bits).
- **Biblioteca:** E1_Impressora01.dll.
- **Equipamento:** Impressora térmica Elgin i9.

---

## 📁 Estrutura do Projeto

```text
Projeto/
│
├── .vscode/                  # Configurações do VSCode
│
├── Output/                   # Bibliotecas e dependências
│
├── E1_Impressora01.dll       # Biblioteca de comunicação
├── XMLSAT.xml                # Arquivo XML para impressão SAT
├── CANC_SAT.xml              # Arquivo XML de cancelamento SAT
├── main.c                    # Código-fonte principal
└── README.md                 # Documentação do projeto
```

**Importante:** A DLL `E1_Impressora01.dll` e os arquivos XML devem estar na mesma pasta de onde o executável será iniciado.

---

## ⚙️ Compilação e Execução

### 1. Baixar o Projeto

1. Acesse o repositório no GitHub.
2. Clique no botão **Code**.
3. Selecione **Download ZIP**.
4. Extraia o conteúdo do arquivo baixado.

### 2. Abrir o Projeto

1. Abra o Visual Studio Code.
2. Selecione **File → Open Folder**.
3. Escolha a pasta do projeto.
4. Abra o arquivo `main.c`.

### 3. Configurar a DLL

O projeto utiliza a biblioteca `E1_Impressora01.dll`, que precisa ter a mesma arquitetura do compilador utilizado.

- **32 bits (x86):** Utilize a DLL localizada na pasta `x86`.
- **64 bits (x64):** Utilize a DLL localizada na pasta `x64`.

A DLL escolhida deve ser renomeada para `E1_Impressora01.dll` e colocada na mesma pasta do executável.

**Atenção:** Não utilize uma DLL de 32 bits com um compilador de 64 bits, ou vice-versa, pois isso impedirá o carregamento da biblioteca.

### 4. Compilar o Programa

Abra o terminal integrado do VSCode (`Ctrl + '`).

Para compiladores MinGW de 32 bits:

```bash
gcc main.c -o impressora.exe
```

Para compiladores MinGW de 64 bits, utilize o GCC correspondente à arquitetura x64:

```bash
gcc main.c -o impressora.exe
```

### 5. Executar o Programa

Após a compilação, execute o programa pelo terminal:

```bash
./impressora.exe
```

Certifique-se de que a DLL e os arquivos XML necessários estejam disponíveis na pasta de execução.

---

## 🔐 Login de Teste

Para acessar as funcionalidades do programa, é necessário realizar a autenticação.

Utilize as seguintes credenciais:

| Campo | Credencial |
|---|---|
| **Login** | admin |
| **Senha** | 1234 |

**Observação:** O programa permite até 3 tentativas de autenticação. Caso todas sejam realizadas incorretamente, a aplicação será encerrada.

---

## 📋 Opções do Menu

Após realizar o login, o usuário terá acesso às seguintes funcionalidades:

| Opção | Funcionalidade | Descrição |
|---|---|---|
| **1** | Configurar Conexão | Define o tipo de conexão, modelo da impressora, porta e parâmetros adicionais. |
| **2** | Abrir Conexão | Estabelece a comunicação com a impressora. |
| **3** | Fechar Conexão | Encerra a comunicação com a impressora. |
| **4** | Imprimir Texto | Permite digitar um texto e definir a quantidade de cópias. |
| **5** | Imprimir QR Code | Gera e imprime um QR Code a partir de um conteúdo informado. |
| **6** | Imprimir Código de Barras | Realiza a impressão de um código de barras de teste. |
| **7** | Imprimir XML SAT | Lê e imprime o conteúdo do arquivo XMLSAT.xml. |
| **8** | Imprimir XML Cancelamento SAT | Lê e imprime o arquivo CANC_SAT.xml. |
| **9** | Abrir Gaveta (Elgin) | Aciona a abertura da gaveta por meio do comando específico da Elgin. |
| **10** | Abrir Gaveta | Aciona a abertura da gaveta utilizando outro comando da biblioteca. |
| **11** | Sinal Sonoro | Emite sinais sonoros pela impressora, permitindo definir a quantidade de avisos. |
| **0** | Sair | Encerra o programa e fecha a conexão, caso esteja aberta. |

**Importante:** Para utilizar as funcionalidades de impressão, abertura de gaveta e sinal sonoro, é necessário estabelecer a conexão com a impressora primeiro.

---

## 🧪 Testes

O programa contempla testes das seguintes funcionalidades:

- Verificação do carregamento da DLL.
- Autenticação de usuário.
- Configuração e abertura da conexão USB.
- Fechamento da conexão.
- Impressão de textos e múltiplas cópias.
- Geração de QR Codes.
- Impressão de códigos de barras.
- Impressão de documentos XML SAT.
- Acionamento da gaveta.
- Emissão de sinais sonoros.

---

## 📚 Documentação Adicional

- Manual da impressora **Elgin i9**.
- Documentação do **SDK Elgin**.
- Documentação da biblioteca **E1_Impressora01.dll**.

---

## 👥 Autores

*Em ordem alfabética:*

- Matheus Maximiano Prado da Silva
- Matheus Navarro Wenceslau
- Yago Vidal Oliveira de Almeida