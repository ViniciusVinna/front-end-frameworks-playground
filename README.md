# 🧪 &nbsp; Front-end Frameworks

<div align="left" width="100%">
  <p>
		Este repositório foi criado com o objetivo de conduzir análises de experimentos utilizando os principais frameworks / toolchains para desenvolvimento de front-end disponíveis no mercado: <strong><a href="https://pt-br.reactjs.org/">React</a></strong>, <strong><a href="https://vuejs.org/">Vue</a></strong> e <strong><a href="https://svelte.dev/">Svelte</a></strong>.
  </p>
</div>

<div align="left">

> Comparação entre os frameworks React, Vue e Svelte.
> Urls das aplicações publicadas no **Netlify**:

- [![Netlify Status](https://api.netlify.com/api/v1/badges/96fc5c62-93ac-48e2-8c4f-86ababaa42b0/deploy-status)](https://app.netlify.com/sites/vinna-react/deploys) [Netlify React](https://vinna-react.netlify.app)

- [![Netlify Status](https://api.netlify.com/api/v1/badges/286f8a07-28b8-48f1-b8c2-54d380f13b36/deploy-status)](https://app.netlify.com/sites/vinna-vue/deploys) [Netlify Vue](https://vinna-vue.netlify.app)

- [![Netlify Status](https://api.netlify.com/api/v1/badges/69e7c31c-d1cb-41b0-8f72-a49c2722abd4/deploy-status)](https://app.netlify.com/sites/vinna-svelte/deploys) [Netlify Svelte](https://vinna-svelte.netlify.app)

- [![Netlify Status](https://api.netlify.com/api/v1/badges/69e7c31c-d1cb-41b0-8f72-a49c2722abd4/deploy-status)](https://app.netlify.com/sites/vinna-svelte/deploys) [Netlify Svelte SSR](https://vinna-ssr.netlify.app/)

</div>

---

### Sumário

- [Frameworks/Toolchains - Inicialização Padrão](#frameworks-toolchains)
- [React vs Vue vs Svelte - SPA Benchmarking](#spa-benchmarking)
	- [Lighthouse Report](#lighthouse-report)
	- [Network Report](#network-report)

## 🥞 &nbsp; Frameworks/Toolchains - Inicialização Padrão <a name="frameworks-toolchains"></a>

Implementação padrão da página de inicialização dos respectivos frameworks, utilizando **vite** e **netlify** como solução de hosting das Single Page Applications.
<br />

<div align="center">
  <a href="https://vinna-react.netlify.app/" title="React" align="center">
    <img src="docs/images/react.svg" alt="React Logo" height="50" style="border: 5px solid transparent;"/>
  </a>

  <a href="https://vinna-vue.netlify.app/" title="Vue" align="center">
    <img src="docs/images/vue.svg" alt="Vue Logo" height="50" style="border: 5px solid transparent;"/>
  </a>

  <a href="https://vinna-svelte.netlify.app" title="Svelte" align="center">
    <img src="docs/images/svelte.svg" alt="Svelte Logo"  height="50" style="border: 5px solid transparent;"/>
  </a>
</div>

---

## 🏎️ &nbsp; React vs Vue vs Svelte - SPA Benchmarking <a name="#spa-benchmarking"></a>

Comparação entre os frameworks React, Vue e Svelte, **mobile-first**, **cache desabilitado** em modo anônimo.

---

### ​ Lighthouse Report <a name="lighthouse-report"></a>

> Critérios como acessibilidade, melhores práticas e SEO são relativos, uma vez que as páginas de welcome screen implementam boilerplates superficiais.

| Critério          | React  | Vue   | Svelte |
| ----------------- | ------ | ----- | ------ |
| Performance       | 99 🟢  | 96 🔻 | 99 🟢  |
| Acessibilidade    | 100 🟢 | 95 🔻 | 95 🔻  |
| Melhores Práticas | 100 🟢 | 92 🔻 | 100 🟢 |
| SEO               | 92     | 92    | 92     |

<div align="center">
    <img src="docs/images/benchmarking/react-lighthouse.png" alt="React Lighthouse" align="center" width="100%" style="border: 5px solid transparent;"/>
		<br />
    <img src="docs/images/benchmarking/vue-lighthouse.png" alt="Vue Lighthouse" width="100%" style="border: 5px solid transparent;"/>
		<br />
    <img src="docs/images/benchmarking/svelte-lighthouse.png" alt="Svelte Lighthouse"  width="100%" style="border: 5px solid transparent;"/>
		<br />
</div>

### ​ Network Report <a name="network-report"></a>

> Recursos como favicon, imagens e CSS foram ignorados por se tratarem de assets adicionais e diferentes entre as welcome screens de cada uma das soluções.

|       Critério (Tamanho)       |   React    |    Vue     |  Svelte   |
| :----------------------------: | :--------: | :--------: | :-------: |
|         Documento HTML         |  826 B 🔻  |  766 B 🟢  | 802 B 🟡  |
|       Javascript Bundle        | 44.9 kB 🔻 | 21.7 kB 🟡 | 2.7 kB 🟢 |
|      Nº de Requisições\*       |     5      |     5      |     5     |
|      Tamanho de Recursos       |  49.7 kB   |  35.1 kB   |  11.8 kB  |
| Tempo de Carregamento do DOM\* |   95 ms    |   785 ms   |  158 ms   |

<div align="center">
    <img src="docs/images/benchmarking/react-network.png" alt="React Network" align="center" width="100%" style="border: 5px solid transparent;"/>
		<br />
    <img src="docs/images/benchmarking/vue-network.png" alt="Vue Network" width="100%" style="border: 5px solid transparent;"/>
		<br />
    <img src="docs/images/benchmarking/svelte-network.png" alt="Svelte Network"  width="100%" style="border: 5px solid transparent;"/>
		<br />
</div>
