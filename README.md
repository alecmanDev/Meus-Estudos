# Meu Estudo — Concurso

App de estudos (ciclo, pomodoro, simulados, concursos) que roda no navegador do celular e do notebook,
funciona offline e pode ser instalado com ícone próprio.

## 1. Publicar no GitHub Pages

Este repositório já contém o app pronto (`index.html`, `manifest.webmanifest`, `sw.js` e a pasta `icons`).
Para colocá-lo no ar (uma vez só):

1. No GitHub, abra o repositório e vá em **Settings → Pages**.
2. Em *Build and deployment*, escolha **Deploy from a branch**, branch **main**, pasta **/(root)** e clique em **Save**.
3. Espere 1 a 2 minutos. O endereço aparece nessa mesma tela:
   `https://alecmandev.github.io/Meus-Estudos/`

O repositório precisa ser **público** para o GitHub Pages gratuito — só o código do app fica público; seus dados
de estudo ficam apenas no seu aparelho (e na nuvem, se você ligar a sincronização).

## 2. Usar no celular e no notebook

- **Celular (Chrome):** abra o endereço → menu (⋮) → **Instalar app** (ou *Adicionar à tela inicial*).
- **Notebook (Chrome/Edge):** abra o endereço → ícone de instalar na barra de endereço (ou menu → *Instalar*).
- Depois da primeira abertura com internet, o app funciona sem conexão.

## 3. Levar seus dados do artefato do Claude para o app novo

Os dados ficam separados em cada navegador/aparelho. Para migrar uma vez:
1. No artefato do Claude: aba **Ciclo → Backup dos dados → Exportar dados**.
2. No app novo: aba **Ciclo → Backup dos dados → Importar arquivo** (ou cole o texto em
   *Importar colando o texto do backup*).

## 4. Sincronizar PC e celular automaticamente

O app tem sincronização em tempo real entre aparelhos (aba **Ciclo → Sincronização entre aparelhos**),
usando um projeto gratuito no Firebase (Google) já configurado dentro do app. Ela **não funciona** dentro
do link do Claude (bloqueado pelas regras de segurança de lá) — só no endereço publicado no GitHub Pages.

Como usar:
1. No primeiro aparelho, toque em **Criar código neste aparelho**. Anote o código de 6 caracteres.
2. No segundo aparelho, digite esse código em **Já tenho um código** → **Conectar**. Se já houver dados
   salvos nesse código, ele pergunta se quer trazer para este aparelho.
3. Dali em diante, qualquer mudança em um aparelho aparece automaticamente no outro em poucos segundos.
   Se você usar o app sem internet, as mudanças ficam guardadas como pendentes e são enviadas quando a conexão
   voltar. Se os dois aparelhos mudarem os dados antes de sincronizar, o app pergunta qual versão manter
   (nada é substituído em silêncio).
4. **Desconectar** só para de sincronizar aquele aparelho — os dados continuam na nuvem, e dá para
   reconectar com o mesmo código quando quiser.

Isso já está pronto para uso; não é preciso criar nada no Firebase para usar esta função — o projeto já
existe e está configurado no próprio `index.html`.

## 5. Atualizações

Quando houver uma versão nova do `index.html` (ou dos outros arquivos), envie para a branch **main** do repositório
(*Add file → Upload files*, com o mesmo nome, substituindo o antigo, e **Commit changes**). Em ~1 minuto a versão
nova fica no ar; o app pega a atualização na próxima vez que você abrir com internet. Seus dados não são apagados.

## 6. (Opcional) Gerar um APK

Com o endereço do app no ar, abra **pwabuilder.com**, cole o endereço e use *Package for stores → Android*
para baixar um APK. Instale no celular liberando "fontes desconhecidas". Esse APK abre o mesmo endereço,
então também se atualiza sozinho quando você atualiza o GitHub.

## Cuidados

- Não limpe os "dados do site/navegador" nem desinstale o app sem fazer backup antes.
- Faça backup de tempos em tempos (o app avisa quando passar de 7 dias).
- Se você ligar a Sincronização, seus dados passam a ficar guardados também na nuvem (Firebase), além do
  aparelho. Qualquer pessoa com o código de 6 caracteres consegue entrar nesse grupo — trate-o como uma
  senha simples e não o compartilhe à toa.
