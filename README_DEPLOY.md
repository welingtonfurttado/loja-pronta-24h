# Loja Pronta 24h — Deploy Guide

**Versão:** 1.0  
**Última atualização:** 2026-04-19  
**Contato:** welingtonfurttado@gmail.com

---

## Estrutura de arquivos

```
deploy/service_lp/
├── index.html                      ← página principal (HTML minificado)
├── assets/
│   ├── logo/
│   │   ├── logo_lp24_dark.svg      ← logo do header
│   │   └── favicon_lp24.svg        ← ícone da aba do navegador
│   └── profile/
│       └── welington_furtado.jpg   ← foto de perfil (adicionar manualmente)
└── README_DEPLOY.md                ← este arquivo
```

---

## 1. Como publicar no Netlify

### Opção A — Drag and Drop (mais simples)

1. Acesse [app.netlify.com](https://app.netlify.com) e faça login
2. Na tela inicial, clique em **"Add new site" > "Deploy manually"**
3. Arraste a pasta `deploy/service_lp/` para a área indicada
4. Aguarde o deploy (menos de 1 minuto)
5. Netlify gera uma URL como `https://lp24-xxxxx.netlify.app`

> Para usar um domínio próprio: vá em **Site settings > Domain management > Add custom domain**

### Opção B — Via GitHub (recomendado para atualizações frequentes)

1. Crie um repositório no GitHub com os arquivos desta pasta
2. No Netlify: **"Add new site" > "Import an existing project"**
3. Conecte ao repositório GitHub
4. Configure:
   - **Branch:** `main`
   - **Publish directory:** `/` (raiz do repositório)
5. Clique em **Deploy site**

> Cada push ao repositório atualiza o site automaticamente.

---

## 2. Como atualizar o conteúdo

Todos os textos estão no arquivo `index.html`. Abra em qualquer editor de texto.

### Textos principais por seção

| Seção | O que editar | Como encontrar |
|-------|-------------|----------------|
| Hero | Título e subtítulo | Buscar por `id="hero"` |
| Como funciona | Passos 01, 02, 03 | Buscar por `id="how"` |
| O que você recebe | Lista de entregáveis | Buscar por `id="deliverables"` |
| Benefícios | Cards de vantagens | Buscar por `id="benefits"` |
| Garantia | Texto da garantia | Buscar por `id="guarantee"` |
| Quem está por trás | Bio e nome | Buscar por `id="about"` |
| FAQ | Perguntas e respostas | Buscar por `id="faq"` |
| CTA Final | Chamada para ação | Buscar por `id="cta-final"` |

### Alterar o preço

Busque por `R$197` no arquivo e substitua pelo valor desejado.

### Alterar o nome exibido

Busque por `Welington Furtado` e substitua onde necessário.

---

## 3. Como substituir a foto de perfil

1. Prepare a foto:
   - Formato: **JPG**
   - Tamanho recomendado: **400x400px** ou maior (quadrada)
   - Tamanho do arquivo: máximo **200KB**
   - Foco no rosto (parte superior da imagem)

2. Renomeie o arquivo para:
   ```
   welington_furtado.jpg
   ```

3. Salve dentro da pasta:
   ```
   assets/profile/welington_furtado.jpg
   ```

4. Republique o site (no Netlify, basta fazer novo drag and drop ou push ao GitHub).

> Se a foto não carregar, o site exibe uma silhueta automaticamente — não quebra o layout.

---

## 4. Como alterar o número do WhatsApp

O número atual é **(41) 99835-3581**. Para trocar:

### Passo 1 — Abra o `index.html` em um editor de texto

### Passo 2 — Busque pela string:
```
wa.me/5541998353581
```

### Passo 3 — Substitua pelo novo número no formato internacional:
```
wa.me/55DDNÚMERO
```

Exemplo para o número **(11) 98888-7777**:
```
wa.me/5511988887777
```

### Passo 4 — Atualizar a mensagem automática (opcional)

Junto ao link há um parâmetro `?text=`. Para alterar a mensagem:

1. Escreva a mensagem desejada
2. Codifique em URL (use [urlencoder.org](https://www.urlencoder.org))
3. Substitua o texto após `?text=`

**Mensagem atual (decodificada):**
```
Olá, vi sua página e quero saber mais sobre a criação de loja online.
```

### Passo 5 — Salvar e republicar

---

## 5. Checklist antes de publicar

- [ ] Foto de perfil salva em `assets/profile/welington_furtado.jpg`
- [ ] Número do WhatsApp correto em todos os botões
- [ ] Preço atualizado (`R$197` ou valor atual)
- [ ] Email de contato correto no botão CTA final
- [ ] Testado no celular antes de publicar

---

## 6. Ferramentas gratuitas recomendadas

| Ferramenta | Uso | Link |
|------------|-----|------|
| Netlify | Hospedagem gratuita | netlify.com |
| Squoosh | Comprimir fotos JPG | squoosh.app |
| URL Encoder | Codificar mensagem WhatsApp | urlencoder.org |
| PageSpeed Insights | Verificar performance | pagespeed.web.dev |

---

*Loja Pronta 24h — Welington Furtado · Curitiba, PR*
