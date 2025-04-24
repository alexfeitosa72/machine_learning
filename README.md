# machine_learning
Repositorio de ML para o PPCIC 2025


# 🛠️ Primeiros Socorros do Git

> ⚠️ Para usar este guia, certifique-se de que está na **pasta correta do seu projeto**!

---

## 🧼 1. Resetar o repositório Git local (sem apagar arquivos)

```bash
rm -rf .git
git init
```

---

## 🔗 2. Conectar ao repositório remoto correto

```bash
git remote add origin https://github.com/<usuario>/<repositorio>.git
```

✅ Dica: use `git remote -v` para verificar se a URL foi corretamente configurada.

---

## 📥 3. Puxar o `README.md` do remoto (sem sobrescrever seus arquivos)

```bash
git fetch origin
git checkout -b main origin/main
```

---

## 📝 4. Adicionar seus arquivos do projeto e comitar

```bash
git add .
git commit -m "Commit inicial do projeto local"
```

---

## 🚀 5. Enviar para o repositório remoto

```bash
git push -u origin main
```

---

## 🧯 Soluções rápidas para erros comuns

### ❌ Repository not found

- Verifique se o repositório realmente existe no GitHub.
- Confirme a URL com: `git remote -v`
- Corrija com:

```bash
git remote set-url origin https://github.com/<usuario>/<repositorio>.git
```

---

### 🔐 Erro de autenticação (repositório privado)

- Use token pessoal (PAT) em vez de senha na URL HTTPS, ou
- Configure acesso via SSH:

```bash
ssh-keygen -t ed25519 -C "seu-email@exemplo.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

---

## ✅ Dica Final

Quer evitar tudo isso? Clone o repositório **primeiro**, e só depois adicione os arquivos do seu projeto. Exemplo:

```bash
git clone https://github.com/<usuario>/<repositorio>.git
cd <repositorio>
# Agora copie seus arquivos aqui dentro.
```

