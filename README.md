# MVP - Análise de Contratos

Este é um MVP simples de uma aplicação para upload de documentos, processamento com FastAPI e exibição de checklist em React.

## 🚀 Estrutura do Projeto

```
mvp-contratos/
│── backend/          # FastAPI backend
│   ├── main.py
│   ├── storage/      # onde os uploads ficam armazenados
│
│── frontend/         # React frontend
│   ├── src/
│   │   ├── App.jsx
│   │   ├── api.js
│   │   ├── components/
│   │   │   ├── UploadForm.jsx
│   │   │   ├── DocumentList.jsx
│   │   │   ├── ChecklistView.jsx
│   ├── package.json
│
│── README.md
```

## 🔧 Backend (FastAPI)

### Instalar dependências:
```bash
cd backend
pip install fastapi uvicorn pydantic
```

### Rodar servidor:
```bash
uvicorn main:app --reload
```
Servidor roda em `http://localhost:8000`

---

## 🌐 Frontend (React + Vite + Tailwind)

### Criar projeto com Vite (já configurado no zip):
```bash
cd frontend
npm install
npm install tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

### Configurar Tailwind em `index.css`:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Rodar servidor de desenvolvimento:
```bash
npm run dev
```
Frontend roda em `http://localhost:5173`

---

## ✅ Fluxo de uso

1. Acesse o frontend em `http://localhost:5173`
2. Faça upload de um documento (simulação).
3. O backend processa o documento (mock IA).
4. O checklist é exibido com status (pass / warn / fail).

---

## 📌 Próximos Passos

- Adicionar autenticação (JWT, login com usuários).
- Salvar resultados em banco de dados real (Postgres).
- Integrar com OCR real (Tesseract, AWS Textract, etc).
- Melhorar UI/UX (PDF viewer, highlights).
