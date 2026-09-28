[README.md](https://github.com/user-attachments/files/32714551/README.md)
# Meu Estudo — Concurso

App de estudos (ciclo, pomodoro, simulados, concursos) que roda no navegador do celular e do notebook,
funciona offline e pode ser instalado com ícone próprio.

## 1. Publicar no GitHub Pages (uma vez só, pelo notebook)

1. Extraia o arquivo `meu-estudo-pwa.zip`. Vai aparecer a pasta `meu-estudo`.
2. No GitHub, clique em **New repository**. Nome sugerido: `meu-estudo`. Marque **Public**
   (o GitHub Pages gratuito exige repositório público — só o código do app fica público; seus dados de
   estudo ficam apenas no seu aparelho). Clique em **Create repository**.
3. Na página do repositório, clique em **uploading an existing file** (ou *Add file → Upload files*).
4. Abra a pasta `meu-estudo` no seu computador, selecione **tudo que está dentro dela**
   (`index.html`, `manifest.webmanifest`, `sw.js`, `README.md` e a pasta `icons`) e arraste para o GitHub.
   Clique em **Commit changes**.
5. Vá em **Settings → Pages**. Em *Build and deployment*, escolha **Deploy from a branch**,
   branch **main**, pasta **/(root)** e clique em **Save**.
6. Espere 1 a 2 minutos. O endereço aparece nessa mesma tela:
   `https://SEU-USUARIO.github.io/meu-estudo/`

## 2. Usar no celular e no notebook

- **Celular (Chrome):** abra o endereço → menu (⋮) → **Instalar app** (ou *Adicionar à tela inicial*).
- **Notebook (Chrome/Edge):** abra o endereço → ícone de instalar na barra de endereço (ou menu → *Instalar*).
- Depois da primeira abertura com internet, o app funciona sem conexão.

## 3. Levar seus dados do artefato do Claude para o app novo

Os dados ficam separados em cada navegador/aparelho. Para migrar:
1. No artefato do Claude: aba **Ciclo → Backup dos dados → Exportar dados**.
2. No app novo: aba **Ciclo → Backup dos dados → Importar arquivo** (ou cole o texto em
   *Importar colando o texto do backup*).
3. Para usar nos dois aparelhos com os mesmos dados, exporte em um e importe no outro.
   (Sincronização automática exigiria um serviço na nuvem — dá para adicionar depois.)

## 4. Atualizações

Volte ao Claude e peça as mudanças. Ele entrega um novo `meu-estudo-pwa.zip`. No repositório do GitHub:
*Add file → Upload files*, envie os arquivos novos com o mesmo nome (substituem os antigos) e clique em
**Commit changes**. Em ~1 minuto a versão nova fica no ar; o app pega a atualização na próxima vez que
você abrir com internet. Seus dados não são apagados.

## 5. (Opcional) Gerar um APK

Com o endereço do app no ar, abra **pwabuilder.com**, cole o endereço e use *Package for stores → Android*
para baixar um APK. Instale no celular liberando "fontes desconhecidas". Esse APK abre o mesmo endereço,
então também se atualiza sozinho quando você atualiza o GitHub.

## Cuidados

- Não limpe os "dados do site/navegador" nem desinstale o app sem fazer backup antes.
- Faça backup de tempos em tempos (o app avisa quando passar de 7 dias).
