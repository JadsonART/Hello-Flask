# 🌐 Hello Flask - Projeto de Demonstração com Flask

Este projeto é uma aplicação web simples desenvolvida com o microframework **Flask**, que demonstra funcionalidades básicas como:

- Retorno de JSON  
- Templates com Jinja2  
- Manipulação de parâmetros na URL  
- Verificação de métodos HTTP (GET/POST)  
- Tratamento de erro 404 com página personalizada  

---

## 🚀 Tecnologias utilizadas

- [Python 3.x](https://www.python.org/)
- [Flask](https://flask.palletsprojects.com/)
- HTML + Jinja2 (motor de templates)

---

## 📁 Estrutura dos arquivos

```
├── Hello02.py          # Arquivo principal da aplicação Flask
├── hello.html          # Template para saudação personalizada
├── error.html          # Página customizada para erro 404
```

---

## 📌 Rotas e funcionalidades

### `/`
- **Descrição**: Retorna uma mensagem no formato JSON.
- **Resposta**: `{"mensagem": "Hello Json!"}`

---

### `/hello/` ou `/hello/<nome>`
- **Descrição**: Rota que renderiza uma saudação com o nome informado.
- **Parâmetro**: `nome` (opcional) — se não for informado, usa o valor padrão `"Jadson"`.
- **Template**: `hello.html`
- **Exemplos**:
  - `/hello/` → "Olá, Jadson!"
  - `/hello/Maria` → "Olá, Maria!"

---

### `/show/<int:id>`
- **Descrição**: Mostra o valor inteiro recebido como parâmetro.
- **Exemplo**: `/show/42` → "Valor recebido id = 42"

---

### `/login`
- **Métodos suportados**: `GET` e `POST`
- **GET**: Exibe um formulário HTML simples.
- **POST**: Retorna uma mensagem confirmando o envio via POST.
- **Formulário incluído na resposta HTML da rota GET**.

---

### Página de erro 404
- **Descrição**: Quando uma rota não é encontrada, o app retorna um HTML customizado.
- **Template usado**: `error.html`
- **Resposta**: Código HTTP 404 com mensagem amigável.

---

## ▶️ Como executar

1. Instale as dependências:
   ```bash
   pip install flask
   ```

2. Execute o app:
   ```bash
   python Hello02.py
   ```

3. Acesse via navegador:
   ```
   http://127.0.0.1:5000/
   ```

---

## 📄 Licença

Este projeto é apenas para fins educacionais e não possui licença específica.  
Sinta-se livre para reutilizar ou modificar.

---
