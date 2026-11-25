<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#050505">
  <meta
    name="description"
    content="Jadson Evangelista, barbeiro e educador. Agende seu horário ou acompanhe o lançamento do curso."
  >
  <title>Jadson Evangelista | Barber Educator</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link
    href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@500;600;700&family=Manrope:wght@400;500;600;700&display=swap"
    rel="stylesheet"
  >

  <style>
    :root {
      color-scheme: dark;
      --black: #050505;
      --graphite: #121212;
      --graphite-light: #1c1c1c;
      --line: #2a2927;
      --gold: #c2a878;
      --gold-dark: #8f7a52;
      --text: #ece8e1;
      --muted: #9b958b;
      --serif: "Cormorant Garamond", Georgia, serif;
      --sans: "Manrope", Arial, sans-serif;
      --content: 1120px;
    }

    * { box-sizing: border-box; }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 90px;
    }

    body {
      margin: 0;
      background: var(--black);
      color: var(--text);
      font-family: var(--sans);
      line-height: 1.65;
    }

    a { color: inherit; text-decoration: none; }
    button, input, select { font: inherit; }

    .wrap {
      width: min(var(--content), calc(100% - 40px));
      margin-inline: auto;
    }

    .eyebrow {
      color: var(--gold);
      font-size: .72rem;
      font-weight: 700;
      letter-spacing: .18em;
      text-transform: uppercase;
    }

    h1, h2, h3 {
      margin: 0;
      font-family: var(--serif);
      font-weight: 500;
      line-height: 1.05;
    }

    h1 { font-size: clamp(3.2rem, 8vw, 6.7rem); }
    h2 { font-size: clamp(2.5rem, 5vw, 4.2rem); }
    p { color: var(--muted); }

    .button {
      display: inline-flex;
      min-height: 50px;
      align-items: center;
      justify-content: center;
      padding: 0 22px;
      border: 1px solid var(--gold-dark);
      background: var(--gold);
      color: #14120e;
      font-size: .72rem;
      font-weight: 800;
      letter-spacing: .09em;
      text-align: center;
      text-transform: uppercase;
      transition: background .2s ease, transform .2s ease;
    }

    .button:hover {
      background: #d3bb8c;
      transform: translateY(-2px);
    }

    .button--outline {
      background: transparent;
      color: var(--text);
    }

    .button--outline:hover {
      background: var(--graphite-light);
    }

    .site-header {
      position: sticky;
      z-index: 10;
      top: 0;
      border-bottom: 1px solid rgb(42 41 39 / 75%);
      background: rgb(5 5 5 / 92%);
      backdrop-filter: blur(12px);
    }

    .header-inner {
      display: flex;
      min-height: 76px;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .brand {
      font-size: .75rem;
      font-weight: 700;
      letter-spacing: .12em;
    }

    .brand span {
      display: block;
      margin-top: 2px;
      color: var(--muted);
      font-size: .62rem;
      font-weight: 500;
      letter-spacing: .16em;
    }

    .header-cta { min-height: 42px; padding-inline: 16px; }

    .hero {
      display: grid;
      min-height: min(760px, calc(100svh - 76px));
      grid-template-columns: 1.05fr .95fr;
      align-items: center;
      gap: clamp(38px, 8vw, 100px);
      padding-block: 70px;
      animation: reveal .8s ease both;
    }

    .hero-copy { max-width: 650px; }
    .hero h1 { margin-top: 22px; }
    .hero-copy > p {
      max-width: 540px;
      margin: 24px 0 30px;
      font-size: 1rem;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .photo-placeholder {
      display: grid;
      min-height: 460px;
      place-items: center;
      border: 1px solid var(--line);
      background:
        radial-gradient(ellipse at 50% 35%, #20201e 0, transparent 55%),
        linear-gradient(145deg, #171715, #0b0b0b 70%);
      color: #777168;
      text-align: center;
    }

    .photo-placeholder span {
      padding: 20px;
      font-size: .7rem;
      letter-spacing: .15em;
      text-transform: uppercase;
    }

    .section {
      padding-block: clamp(78px, 11vw, 132px);
      border-top: 1px solid var(--line);
    }

    .course-grid {
      display: grid;
      grid-template-columns: 1fr .85fr;
      align-items: start;
      gap: clamp(40px, 8vw, 100px);
    }

    .tag {
      display: inline-block;
      margin-bottom: 22px;
      padding: 6px 10px;
      border: 1px solid var(--gold-dark);
      color: var(--gold);
      font-size: .66rem;
      font-weight: 700;
      letter-spacing: .15em;
    }

    .course-copy h2 { max-width: 650px; }
    .course-copy > p { max-width: 590px; margin: 22px 0; }

    .course-list {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
      margin-top: 28px;
    }

    .course-list span {
      padding: 8px 12px;
      border: 1px solid var(--line);
      color: var(--muted);
      font-size: .75rem;
    }

    .form-card {
      padding: clamp(22px, 4vw, 36px);
      border: 1px solid var(--line);
      background: var(--graphite);
    }

    .form-card h3 { margin-bottom: 8px; font-size: 2rem; }
    .form-card > p { margin: 0 0 22px; font-size: .88rem; }

    .field { margin-bottom: 15px; }

    .field label {
      display: block;
      margin-bottom: 7px;
      color: var(--text);
      font-size: .75rem;
      font-weight: 600;
    }

    .field input, .field select {
      width: 100%;
      min-height: 48px;
      padding: 10px 12px;
      border: 1px solid var(--line);
      border-radius: 0;
      outline: none;
      background: #0b0b0b;
      color: var(--text);
    }

    .field input:focus, .field select:focus { border-color: var(--gold-dark); }
    .form-card .button { width: 100%; margin-top: 4px; }

    .about-grid {
      display: grid;
      grid-template-columns: .8fr 1fr;
      align-items: center;
      gap: clamp(40px, 9vw, 110px);
    }

    .about-photo { min-height: 430px; }
    .about-copy h2 { margin: 14px 0 20px; }
    .about-copy p { max-width: 620px; }

    .pillars {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 28px;
    }

    .pillars span {
      padding: 9px 13px;
      border-left: 1px solid var(--gold-dark);
      background: var(--graphite);
      color: var(--text);
      font-size: .76rem;
    }

    .section-heading {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 20px;
      margin-bottom: 30px;
    }

    .section-heading h2 { margin-top: 10px; }

    .gallery {
      display: grid;
      grid-template-columns: repeat(4, 