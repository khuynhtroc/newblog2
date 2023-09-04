<template><div><h1 id="contribution-guides" tabindex="-1"><a class="header-anchor" href="#contribution-guides" aria-hidden="true">#</a> Contribution Guides</h1>
<p>This repository employs a <a href="https://en.wikipedia.org/wiki/Monorepo" target="_blank" rel="noopener noreferrer">monorepo<ExternalLinkIcon/></a> setup with <a href="https://pnpm.io/workspaces" target="_blank" rel="noopener noreferrer">pnpm workspaces<ExternalLinkIcon/></a>. It hosts theme Gungnir and a number of plugins for <a href="https://v2.vuepress.vuejs.org/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a>.</p>
<p> </p>
<h2 id="pre-requirements" tabindex="-1"><a class="header-anchor" href="#pre-requirements" aria-hidden="true">#</a> Pre-requirements</h2>
<ul>
<li><a href="http://nodejs.org/" target="_blank" rel="noopener noreferrer">Node.js<ExternalLinkIcon/></a> <strong>version 14+</strong></li>
<li><a href="https://pnpm.io/" target="_blank" rel="noopener noreferrer">pnpm<ExternalLinkIcon/></a> <strong>version 7+</strong></li>
</ul>
<p> </p>
<h2 id="development" tabindex="-1"><a class="header-anchor" href="#development" aria-hidden="true">#</a> Development</h2>
<p>Clone the repo and install dependencies:</p>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">pnpm</span> <span class="token function">install</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div><p>Start watching source files:</p>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">pnpm</span> dev
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div><p>Open another terminal, and start developing the documentation site:</p>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">pnpm</span> docs:dev
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div><p>Main tools that used in this project:</p>
<ul>
<li><a href="https://www.typescriptlang.org/" target="_blank" rel="noopener noreferrer">TypeScript<ExternalLinkIcon/></a> as the development language</li>
<li><a href="https://eslint.org/" target="_blank" rel="noopener noreferrer">ESLint<ExternalLinkIcon/></a> + <a href="https://prettier.io/" target="_blank" rel="noopener noreferrer">Prettier<ExternalLinkIcon/></a> for code linting and formatting</li>
</ul>
<p> </p>
<h2 id="license" tabindex="-1"><a class="header-anchor" href="#license" aria-hidden="true">#</a> License</h2>
<p>By contributing to Gungnir, you agree that your contributions will be licensed under its <a href="LICENSE">Apache-2.0</a> (theme) / MIT (plugins) license.</p>
</div></template>


