# 🚀 Como fazer o deploy no GitHub Pages

## Passos para configurar o deploy:

### 1. Preparar o Repositório
```bash
# Na pasta do projeto
git init
git add .
git commit -m "Initial commit - Indicadores Seven Dashboard"
```

### 2. Criar Repositório no GitHub
1. Vá em https://github.com/new
2. Nome: `indicadores-seven` (ou outro nome de sua escolha)
3. Deixe público (necessário para GitHub Pages gratuito)
4. NÃO initialize com README (já temos um)

### 3. Conectar e fazer Push
```bash
# Substitua USERNAME pelo seu usuário do GitHub
git remote add origin https://github.com/USERNAME/indicadores-seven.git
git branch -M main
git push -u origin main
```

### 4. Configurar GitHub Pages
1. No repositório, vá em **Settings**
2. No menu lateral, clique em **Pages**
3. Em "Source", selecione **GitHub Actions**
4. Pronto! O deploy será automático a cada push

### 5. (Opcional) Configurar API Key do Gemini
Se usar funcionalidades de IA:
1. No repositório, vá em **Settings > Secrets and variables > Actions**
2. Clique em **New repository secret**
3. Nome: `GEMINI_API_KEY`
4. Valor: sua chave da API

### 6. Acessar o Site
Após o primeiro deploy (alguns minutos), seu site estará em:
`https://USERNAME.github.io/indicadores-seven/`

## ⚡ Atualizações Automáticas
Sempre que você fizer push para a branch `main`, o site será atualizado automaticamente!

## 🛠️ Deploy Manual (alternativo)
Se preferir fazer deploy manual:
```bash
npm run deploy
```

## ❗ Importante
- O nome do repositório deve coincidir com o `base` configurado no `vite.config.ts`
- Se mudar o nome do repositório, atualize também o `vite.config.ts`
- O GitHub Pages pode levar alguns minutos para refletir mudanças
