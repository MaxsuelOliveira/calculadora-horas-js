# 🚀 API Conversor de Unidades de Tempo

Uma aplicação completa **full-stack** para conversão de unidades de tempo com interface moderna e responsiva.

## ⚡ Status do Projeto

✅ **Backend**: Implementado e funcional  
✅ **Frontend**: Completamente reconstruído com UX/UI moderna  
✅ **Integração**: Full-stack com todas as rotas RESTful  
✅ **Design**: Responsivo, intuitivo e sem necessidade de scroll  
✅ **Documentação**: Swagger/OpenAPI 3.0

---

## 📦 Tecnologias Utilizadas

### Backend

- **Node.js** + **Express**
- **SQLite** com biblioteca sqlite
- **Swagger/OpenAPI 3.0** para documentação interativa
- **CORS** habilitado

### Frontend

- **HTML5** semântico
- **CSS3** com Flexbox/Grid e animações 3D
- **JavaScript vanilla** (Fetch API)
- **LocalStorage** para persistência de sessão
- **Sem dependências externas**

---

## 🎯 Funcionalidades

### Conversão Multi-direcional

- ✅ Converter **em qualquer unidade** (horas, minutos, segundos, semanas, meses, anos, dias)
- ✅ Todos os campos são funcionais e atualizáveis
- ✅ Conversão em tempo real conforme você digita
- ✅ Suporte a números positivos inteiros

### Backend & Data

- ✅ Criar usuários temporários
- ✅ Salvar histórico de conversões
- ✅ Visualizar histórico por usuário
- ✅ Deletar conversões
- ✅ Persistência de dados em SQLite
- ✅ API RESTful completa

---

## 🚀 Como Rodar Localmente

### 1. Clonar o Repositório

```bash
git clone https://github.com/MaxsuelOliveira/web-calcular-horas.git
cd web-calcular-horas
```

### 2. Instalar Dependências para o backend

```bash
npm install
```

### 3. Iniciar o Backend

```bash
node ./backend/server.js
```

**Saída esperada:**

```plaintext
Servidor rodando na porta 3001
Database conectado em ./database.db
```

### 4. Acessar a Aplicação

- **Aplicação Web**: `http://localhost:3001`
- **Documentação Swagger**: `http://localhost:3001/api-docs`
- **API Base**: `http://localhost:3001/api`

---

## 📡 Endpoints da API

### Usuários

```plaintext
POST   /api/users/temp              → Criar usuário temporário
GET    /api/users/{id}              → Buscar informações do usuário
```

### Conversões

```plaintext
POST   /api/conversions             → Criar nova conversão
GET    /api/conversions/{id}        → Buscar conversão específica
GET    /api/conversions/user/{userId} → Histórico completo do usuário
PUT    /api/conversions/{id}        → Atualizar conversão
DELETE /api/conversions/{id}        → Deletar conversão
```

---

## 🗂️ Estrutura do Projeto

```plaintext
api-calcular-horas/
├── app/
│   ├── index.html              (Splash screen)
│   ├── app.html                (Interface principal)
│   ├── css/
│   │   └── style.css           (Todos os estilos - 881 linhas)
│   └── js/
│       ├── main.js             (Lógica do splash screen)
│       └── app.js              (Lógica da aplicação principal)
├── backend/
│   ├── server.js               (Servidor Express)
│   ├── app.js                  (Configuração Express)
│   ├── database/
│   │   └── db.js               (Conexão SQLite)
│   ├── docs/
│   │   └── swagger.json        (Documentação Swagger)
│   ├── models/
│   │   ├── crud.js             (Operações gerais do banco)
│   │   ├── conversion.js       (Lógica de conversão)
│   │   └── user.js             (Lógica de usuário)
│   └── routes/
│       ├── conversion.js       (Rotas de conversão)
│       └── user.js             (Rotas de usuário)
├── package.json
├── README.md
└── UPDATE_SPLASH_SCREEN.md
```

## 📖 Como Usar

### 1. **Iniciar Sessão**

Ao abrir [`http://localhost:3001`](http://localhost:3001), você será redirecionado para criar um usuário temporário.

### 2. **Converter Valores**

Escolha qualquer um dos 6 campos de resultado:

```plaintext
┌─────────────────────────────┐
│   CONVERSOR DE TEMPO        │
├─────────────────────────────┤
│  [0] Horas                  │
│  [0] Minutos                │
│  [0] Segundos               │
│  [0] Semanas                │
│  [0] Meses                  │
│  [0] Anos                   │
└─────────────────────────────┘
```

- **Digite um número** em qualquer campo
- **Os outros campos** se atualizam automaticamente
- **Passe o mouse** para editar com facilidade

### 3. **Salvar Conversão**

Após preencher um valor, clique **"💾 Salvar Conversão"** (aparece quando há valor).

### 4. **Visualizar Histórico**

Seu histórico aparece abaixo com:

- Valor original
- Data e hora
- Todos os resultados
- Opção de deletar

### 5. **Trocar Usuário**

Clique o botão **"🚪"** no canto superior direito para criar nova sessão.

---

## 🎬 Exemplo Prático

```plaintext
1. Abra http://localhost:3001
2. Será criado um usuário temporário automaticamente
3. Coloque o mouse sobre "Horas"
4. Digite: 48
5. Os outros campos se atualizam:
   - Horas: 48
   - Minutos: 2880
   - Segundos: 172800
   - Semanas: 0
   - Meses: 0
   - Anos: 0
6. Clique "Salvar Conversão"
7. Histórico é exibido abaixo
```

---

## 🔧 Configuração

### Variáveis de Ambiente

Crie um arquivo `.env` (opcional):

```env
PORT=3001
DATABASE_PATH=./database.db
NODE_ENV=development
```

### Porta Padrão

Se quiser usar outra porta, modifique em `.env`:

```javascript
const PORT = process.env.PORT || 3001;
```

---

## 📊 Dados Armazenados

### SQLite Database

### Tabela: users

```plaintext
id | name | createdAt
```

### Tabela: conversions

```plaintext
id | userId | days | horas | minutos | segundos | semanas | meses | anos | createdAt
```

---

## 🔐 Segurança

- ✅ CORS configurado
- ✅ Validação de entrada no backend
- ✅ IDs únicos para usuários
- ✅ Sem dados sensíveis armazenados
- ⚠️ **Nota**: Não é adequado para produção sem autenticação JWT

---

## 📱 Responsividade

| Dispositivo      | Suporte |
| ---------------- | ------- |
| Mobile (320px)   | ✅      |
| Tablet (768px)   | ✅      |
| Desktop (1024px) | ✅      |
| 4K (2560px+)     | ✅      |

---

## 🐛 Troubleshooting

### A aplicação não inicia

```bash
# Verifique se Node.js está instalado
node --version

# Reinstale dependências
rm -rf node_modules package-lock.json
npm install
```

### Porta 3001 já está em uso

```bash
# Mude a porta em backend/server.js ou use:
PORT=3002 node ./backend/server.js
```

### Erro no banco de dados

```bash
# Delete o arquivo de banco antigo
rm database.db

# Reinicie o servidor (criará novo)
node ./backend/server.js
```

## 👨‍💻 Autor

**MaxsuelDavid** - Desenvolvedor Full-Stack Web | JS | RPA in PY

---

## 📝 Licença

MIT License - Veja o arquivo LICENSE para detalhes

---

## 🤝 Contribuições

Contribuições são bem-vindas!

### Para contribuir

1. Fork o repositório
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

---

## 📞 Suporte

- 📧 Email: `olivieramaxsuellll@gmail.com`
- 🐙 GitHub Issues: [Abrir Issue](https://github.com/MaxsuelOliveira/web-calcular-horas/issues)
- 💬 Discussões: [Discussões do GitHub](https://github.com/MaxsuelOliveira/web-calcular-horas/discussions)

---

## 🎉 Destaques

- 🏆 Interface intuitiva e sem necessidade de documentação
- ⚡ Performance otimizada (0 dependências externas no frontend)
- 🎨 Design moderno com animações 3D
- 📱 Totalmente responsivo
- 🔄 Conversão bidirecional em tempo real
- 💾 Histórico persistent com SQLite

---

**Última atualização**: Março 3, 2026  
**Versão**: 2.1.0  
**Status**: Production Ready ✅

---

## 🌟 Se este projeto foi útil, considere dar uma ⭐ star
