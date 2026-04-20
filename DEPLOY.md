# Deploy no Vercel via GitHub

## 1. Subir o código no GitHub
No editor da Lovable: **Connectors → GitHub → Connect project → Create Repository**.
Pronto — todo commit feito na Lovable é sincronizado automaticamente com o repo.

## 2. Importar no Vercel
1. Acesse https://vercel.com/new
2. Selecione o repositório criado
3. O Vercel detecta **Vite** automaticamente (já configurado em `vercel.json`):
   - Build Command: `npm run build`
   - Output Directory: `dist`
   - Install Command: `npm install`
4. Clique em **Deploy**

## 3. Variáveis de ambiente
Este projeto não usa backend nem variáveis de ambiente — nada a configurar.

## 4. Domínio personalizado
Em **Settings → Domains** no Vercel, adicione seu domínio e siga as instruções de DNS.

## 5. Atualizações
Cada push para a branch `main` (via Lovable ou Git) gera um novo deploy automático no Vercel.

---

### Arquivos relevantes para o deploy
- `vercel.json` — config do Vercel + SPA fallback (rotas funcionam ao recarregar)
- `.nvmrc` — fixa Node 20
- `package.json` — script `build` já configurado
- `vite.config.ts` — build do Vite
