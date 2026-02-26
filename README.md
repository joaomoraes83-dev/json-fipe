# API FIPE – JSON

API pública e gratuita para consulta de valores FIPE a partir de um arquivo JSON.

Este projeto utiliza **json-server** para disponibilizar os dados como uma API REST simples, permitindo consultas por **marca**, **modelo**, **ano**, **preço** e **mês de referência**.

Ideal para estudos, testes, projetos pessoais e aprendizado de consumo de APIs.

---

## 🌐 Base URL

Após o deploy no Render, a API fica disponível em:
https://json-fipe.onrender.com

GET /veiculos

---

## 🔎 Exemplos de consulta

### Buscar por marca

GET /veiculos?marca=Audi

### Buscar por marca e modelo

GET /veiculos?marca=Audi&modelo=A3 Sedan 1.4 TFSI Flex Tiptronic 4p

### Buscar por marca, modelo e ano

GET /veiculos?marca=Audi&modelo=A3 Sedan 1.4 TFSI Flex Tiptronic 4p&ano=2018

### Buscar por mês de referência

GET /veiculos?referencia=fevereiro de 2026

### Buscar por marca, modelo, ano e mês

GET /veiculos?marca=Audi&modelo=A3 Sedan 1.4 TFSI Flex Tiptronic 4p&ano=2018&referencia=fevereiro de 2026

---

## 💰 Preço

O campo `preco` é retornado em **centavos**, por exemplo:

```json
"preco": "9410900"

Para exibição em reais (R$), o valor deve ser convertido no consumo da API.
Exemplo de conversão em JavaScript:
JavaScript(Number(preco) / 100).toLocaleString("pt-BR", {  style: "currency",  currency: "BRL"});Mostrar mais linhas

📑 Estrutura do objeto
Exemplo de resposta da API:
JSON{  "marca": "Audi",  "modelo": "A3 Sedan 1.4 TFSI Flex Tiptronic 4p",  "ano": "2018",  "preco": "9410900",  "referencia": "fevereiro de 2026"}``Mostrar mais linhas

🛠️ Tecnologias utilizadas

Node.js
json-server
GitHub
Render (deploy)


⚠️ Observações importantes

Esta API é somente para consulta (GET)
Os dados são estáticos
Não há autenticação
O serviço gratuito do Render pode entrar em modo de repouso após período de inatividade


📄 Licença
Uso livre para fins educacionais, estudos e projetos pessoais.



``
