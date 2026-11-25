# Jadson Evangelista | Barber Educator
## Documentação da landing page

Documento de referência do projeto: posicionamento, identidade visual, estrutura, textos, como editar e o que ainda falta.

---

## 1. Visão geral

**O que é:** landing page pessoal e link principal do Instagram.
**Posicionamento:** barbeiro que ensina o que vive na prática da profissão.
**Objetivos atuais (versão objetiva):**
1. Destacar o curso em pré-lançamento e capturar interessados.
2. Facilitar o agendamento de horário pelo WhatsApp.
3. Apresentar Jadson como barbeiro, com trajetória e trabalhos reais.

**Princípios de comunicação**
- Autoridade sem arrogância.
- Experiência sem ostentação.
- Conhecimento sem complicação.
- Evolução sem promessas milagrosas.
- Nada de números, títulos, cursos ou avaliações inventados.

---

## 2. Identidade visual

| Elemento | Definição |
|---|---|
| Preto profundo | `#050505` (fundo) |
| Grafite | `#121212`, `#1c1c1c` (blocos e campos) |
| Linhas | `#2a2927` |
| Champagne envelhecido | `#c2a878` (detalhes e botões), `#8f7a52` (contornos) |
| Texto | `#ece8e1`, secundário `#9b958b` |
| Tipografia de títulos | Cormorant Garamond (serifada, editorial) |
| Tipografia de texto | Manrope (sans, limpa) |

**Direção:** minimalista, masculina, premium, com espaçamento generoso e contraste alto. O dourado aparece só em detalhes pequenos (botões principais, tag de pré-lançamento, contornos).

**Animação:** apenas uma entrada suave na primeira dobra. Scroll suave. Respeita a configuração de movimento reduzido do aparelho.

---

## 3. Estrutura da página

### 3.1 Primeira dobra (hero)
- Identificação: JADSON EVANGELISTA · BARBER EDUCATOR
- **Headline:** "O que a cadeira me ensina, eu compartilho."
- **Subheadline:** "Barbeiro na rotina, educador na prática. Agende seu horário ou conheça meu curso."
- **CTA principal:** QUERO O CURSO (rola até a seção do curso)
- **CTA secundário:** AGENDAR NO WHATSAPP
- Foto de destaque (provisória, a trocar).

### 3.2 Curso em pré-lançamento
- Tag: PRÉ-LANÇAMENTO
- **Título:** "Conhecimento que transforma prática em evolução."
- **Texto:** "Estou desenvolvendo conteúdos e experiências educacionais para barbeiros que desejam evoluir profissionalmente. Cadastre seu interesse e seja avisado primeiro."
- Linha "Em construção" com as frentes planejadas (aulas, workshops, mentorias, materiais digitais).
- **Formulário:** nome, WhatsApp e fase da carreira (começando, já atendo clientes, trabalho em barbearia, tenho minha barbearia).
- **Botão:** QUERO ACOMPANHAR OS PRÓXIMOS LANÇAMENTOS
- **Funcionamento:** ao enviar, o WhatsApp abre com uma mensagem pronta contendo os dados da pessoa. Não depende de ferramenta externa.

### 3.3 Quem está por trás do curso
- Foto de Jadson trabalhando (provisória).
- Texto curto sobre a trajetória: começou conciliando outra profissão com a barbearia, primeiros clientes em casa, investimento em formação, entrada em barbearia profissional, aprendizado diário.
- Três marcas: Formação, Prática diária, Clientes reais.

### 3.4 Trabalhos
- Galeria de 8 imagens verticais (cortes, acabamentos, antes e depois, evoluções).

### 3.5 Agendamento
- Texto: "Atendimento com hora marcada. Chame no WhatsApp e escolha o melhor dia."
- Nome da barbearia, endereço e horários (a preencher).
- Botões: AGENDAR NO WHATSAPP, VER AGENDA ONLINE (só aparece se houver link) e INSTAGRAM.

### 3.6 Elementos fixos
- Cabeçalho com botão AGENDAR HORÁRIO.
- No celular, barra fixa inferior com AGENDAR e QUERO O CURSO.

---

## 4. Como editar

Tudo que muda no dia a dia fica no bloco `CFG`, no início do script do arquivo HTML.

```js
const CFG={
 whatsapp:"5517900000000",        // DDI + DDD + número, só dígitos
 instagram:"https://instagram.com/SEU_USUARIO",
 agendaOnline:"",                 // link de agenda online; vazio = botão some
 barbearia:"Nome da barbearia",
 endereco:"Endereço completo, cidade",
 horarios:"Terça a sábado, 9h às 19h",
 curso:["Aulas","Workshops","Mentorias","Materiais digitais"],
 fotos:[]                         // URLs das fotos de trabalhos (até 8)
};
```

**Para trocar as fotos:** substitua os espaços provisórios por imagens reais. A foto da primeira dobra e a da seção "Quem está por trás do curso" ficam no HTML. As da galeria entram pela lista `fotos`.

**Para lançar um curso:** troque a tag PRÉ-LANÇAMENTO por uma descrição real (nome, formato, o que o aluno recebe, valor, link de compra) e use o formulário como lista de espera ou remova-o.

---

## 5. Checklist de materiais

**Fotos**
- [ ] Retrato profissional (vertical, boa luz, fundo limpo)
- [ ] Foto trabalhando na cadeira
- [ ] 8 fotos de trabalhos (cortes e acabamentos)

**Dados**
- [ ] Número de WhatsApp para agendamento
- [ ] @ do Instagram
- [ ] Nome da barbearia, endereço e horários
- [ ] Link de agenda online, se usar um app
- [ ] Revisão do texto da trajetória com a sua história real

**Conteúdo do curso (quando definido)**
- [ ] Nome e formato
- [ ] Público-alvo
- [ ] O que o aluno aprende
- [ ] Data prevista e valor

---

## 6. Publicação e SEO

- **Título da página:** Jadson Evangelista | Barber Educator
- **Descrição:** "Jadson Evangelista, barbeiro e educador. Agende seu horário ou acompanhe o lançamento do curso."
- Mobile-first, responsiva e sem dependências pesadas (um único arquivo HTML).
- Para domínio próprio, hospede o arquivo em qualquer serviço de páginas estáticas e aponte o domínio.
- Depois de publicar, coloque o link na bio do Instagram.

---

## 7. Evolução planejada

A estrutura foi pensada para crescer sem refazer a página:
- Volta da **biblioteca de conteúdos** por categoria (técnica, fundamentos, processo, acabamento, rotina, carreira, gestão de tempo, experiência do cliente), com links para os Reels.
- Seção de **feedbacks reais** (clientes agora, alunos depois), sempre com autorização.
- Páginas ou blocos para **workshops, mentorias e materiais digitais**.
- Captura de leads integrada a uma ferramenta de e-mail ou CRM, se o volume crescer.

---

## 8. Pontos de atenção

- Todas as imagens atuais são provisórias.
- Não publicar depoimentos, números ou resultados que não possam ser comprovados.
- Pedir autorização antes de usar fotos de clientes.
- Testar o formulário e os botões de WhatsApp com o número real antes de divulgar.