<template><div><h1 id="gungnir-v2" tabindex="-1"><a class="header-anchor" href="#gungnir-v2" aria-hidden="true">#</a> Gungnir V2</h1>
<p><a href="https://www.npmjs.com/package/vuepress-theme-gungnir/v/next" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/npm/v/vuepress-theme-gungnir/next.svg?style=flat-square&amp;logo=npm" alt="npm"><ExternalLinkIcon/></a> <a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Docs-Gungnir-26A2FF?style=flat-square" alt="docs"><ExternalLinkIcon/></a> <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-green?style=flat-square" alt="license"></a> <a href="https://github.com/vuepress/awesome-vuepress/blob/main/v2.md#themes" target="_blank" rel="noopener noreferrer"><img src="https://cdn.jsdelivr.net/gh/sindresorhus/awesome@a7b5b7805ecc00b3396acb35022cf6e2c0699e03/media/badge-flat.svg" alt="awesome-vuepress"><ExternalLinkIcon/></a></p>
<p>A blog theme for <a href="https://v2.vuepress.vuejs.org/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a>, <strong>WIP</strong>.</p>
<p><strong>Gungnir</strong> is the spear of the god Odin in Norse mythology.</p>
<p><img src="https://raw.githubusercontent.com/Renovamen/vuepress-theme-gungnir/main/docs/.vuepress/public/img/docs/gungnir.jpg" alt="preview"></p>
<p> </p>
<h2 id="features" tabindex="-1"><a class="header-anchor" href="#features" aria-hidden="true">#</a> Features</h2>
<ul>
<li>Simple and beautiful</li>
<li>Responsive design</li>
<li>Multi-level navigation</li>
<li>Switchable cover images for home page</li>
<li>Dark and light mode: system theme detection with a theme-switcher to set the theme as per the user preference</li>
<li>Search</li>
<li>Table of contents</li>
<li>Full screening the code blocks (inspired by WordPress theme <a href="https://github.com/mashirozx/Sakura" target="_blank" rel="noopener noreferrer">Sakura<ExternalLinkIcon/></a>)</li>
<li>Tex support (<a href="https://github.com/KaTeX/KaTeX" target="_blank" rel="noopener noreferrer">Katex<ExternalLinkIcon/></a>)</li>
<li>Draw charts and graphs in Markdown easily: <a href="https://www.chartjs.org" target="_blank" rel="noopener noreferrer">Chart.js<ExternalLinkIcon/></a>, <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">Mermaid<ExternalLinkIcon/></a></li>
<li>Markdown enhancements:
<ul>
<li>Footnote (<a href="https://github.com/markdown-it/markdown-it-footnote" target="_blank" rel="noopener noreferrer">markdown-it-footnote<ExternalLinkIcon/></a>)</li>
<li>Mark (<a href="https://github.com/markdown-it/markdown-it-mark" target="_blank" rel="noopener noreferrer">markdown-it-mark<ExternalLinkIcon/></a>)</li>
</ul>
</li>
<li>Analytics (<a href="https://analytics.google.com/" target="_blank" rel="noopener noreferrer">Google Analytics<ExternalLinkIcon/></a> and <a href="https://tongji.baidu.com/" target="_blank" rel="noopener noreferrer">Baidu Tongji<ExternalLinkIcon/></a>)</li>
<li>Comment (<a href="https://github.com/giscus/giscus" target="_blank" rel="noopener noreferrer">Giscus<ExternalLinkIcon/></a>)</li>
<li>RSS</li>
<li>Reading time</li>
<li>Multi-language support (English, Simplified Chinese)</li>
<li>Archive page with tags and links page</li>
</ul>
<p>TODO:</p>
<ul>
<li><a href="https://github.com/jwilber/roughViz" target="_blank" rel="noopener noreferrer">roughViz.js<ExternalLinkIcon/></a> and <a href="https://github.com/gera2ld/markmap" target="_blank" rel="noopener noreferrer">markmap<ExternalLinkIcon/></a></li>
</ul>
<p> </p>
<h2 id="installation" tabindex="-1"><a class="header-anchor" href="#installation" aria-hidden="true">#</a> Installation</h2>
<p>Please make sure you are using the latest version of VuePress (2.0.0-beta.49) and theme Gungnir.</p>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">pnpm</span> <span class="token function">install</span> <span class="token parameter variable">-D</span> vuepress vuepress-theme-gungnir@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div><p> </p>
<h2 id="documentation-live-demos" tabindex="-1"><a class="header-anchor" href="#documentation-live-demos" aria-hidden="true">#</a> Documentation &amp; Live Demos</h2>
<ul>
<li>Documentation: <a href="https://v2-vuepress-theme-gungnir.vercel.app" target="_blank" rel="noopener noreferrer">v2-vuepress-theme-gungnir.vercel.app<ExternalLinkIcon/></a></li>
<li>My blog: <a href="https://blog.zxh.io" target="_blank" rel="noopener noreferrer">blog.zxh.io<ExternalLinkIcon/></a></li>
</ul>
<p> </p>
<h2 id="plugins" tabindex="-1"><a class="header-anchor" href="#plugins" aria-hidden="true">#</a> Plugins</h2>
<p>This repository also contains the following plugins:</p>
<ul>
<li><a href="packages/plugins/giscus">plugin-giscus</a>: use <a href="https://github.com/giscus/giscus" target="_blank" rel="noopener noreferrer">Giscus<ExternalLinkIcon/></a> (a comments system powered by <a href="https://docs.github.com/en/discussions" target="_blank" rel="noopener noreferrer">GitHub Discussions<ExternalLinkIcon/></a>) in Vuepress 2</li>
<li><a href="packages/plugins/katex">plugin-katex</a>: <a href="https://katex.org/" target="_blank" rel="noopener noreferrer">KaTeX<ExternalLinkIcon/></a></li>
<li><a href="packages/plugins/chart">plugin-chart</a>: <a href="https://www.chartjs.org" target="_blank" rel="noopener noreferrer">Chart.js<ExternalLinkIcon/></a></li>
<li><a href="packages/plugins/mermaid">plugin-mermaid</a>: <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">Mermaid<ExternalLinkIcon/></a></li>
<li><a href="packages/plugins/reading-time">plugin-reading-time</a>: word count and reading time</li>
<li><a href="packages/plugins/baidu-tongji">plugin-baidu-tongji</a>: <a href="https://tongji.baidu.com/" target="_blank" rel="noopener noreferrer">百度统计<ExternalLinkIcon/></a></li>
<li><a href="packages/plugins/rss">plugin-rss</a>: RSS</li>
<li><a href="packages/plugins/code-enhance">plugin-code-enhance</a>: full-screen and <s>copy</s> button for code blocks</li>
<li><a href="packages/plugins/search">plugin-search</a>: edit <a href="https://github.com/vuepress/vuepress-next/tree/main/packages/%40vuepress/plugin-search" target="_blank" rel="noopener noreferrer">@vuepress/plugin-search<ExternalLinkIcon/></a> to make it compatible with Gungnir</li>
</ul>
<p> </p>
<h2 id="changes-v0-v2" tabindex="-1"><a class="header-anchor" href="#changes-v0-v2" aria-hidden="true">#</a> Changes (v0 -&gt; v2)</h2>
<ul>
<li>With the power of <a href="https://v2.vuepress.vuejs.org/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a>, <a href="https://v3.vuejs.org/" target="_blank" rel="noopener noreferrer">Vue 3<ExternalLinkIcon/></a>, <a href="https://vitejs.dev/" target="_blank" rel="noopener noreferrer">Vite<ExternalLinkIcon/></a> and <a href="https://webpack.js.org/" target="_blank" rel="noopener noreferrer">Webpack 5<ExternalLinkIcon/></a>, written using <a href="https://v3.vuejs.org/guide/composition-api-introduction.html" target="_blank" rel="noopener noreferrer">Composition API<ExternalLinkIcon/></a>, of course</li>
<li>Stylus -&gt; SCSS</li>
<li>Drop external fonts to increase load speed</li>
<li>Built-in comments system: move from <a href="https://github.com/meteorlxy/vssue" target="_blank" rel="noopener noreferrer">Vssue<ExternalLinkIcon/></a> (doesn't support VuePress 2 yet) to <a href="https://github.com/giscus/giscus" target="_blank" rel="noopener noreferrer">Giscus<ExternalLinkIcon/></a></li>
</ul>
<p> </p>
<h2 id="contribution" tabindex="-1"><a class="header-anchor" href="#contribution" aria-hidden="true">#</a> Contribution</h2>
<p>See <RouterLink to="/packages/theme/CONTRIBUTING.html">Contributing Guide</RouterLink>.</p>
<p> </p>
<h2 id="other-versions" tabindex="-1"><a class="header-anchor" href="#other-versions" aria-hidden="true">#</a> Other Versions</h2>
<p>No further update expected for the following previous versions:</p>
<ul>
<li><a href="https://github.com/Renovamen/vuepress-theme-gungnir/tree/v0" target="_blank" rel="noopener noreferrer">VuePress 1 theme<ExternalLinkIcon/></a></li>
<li><a href="https://github.com/Renovamen/jekyll-theme-gungnir" target="_blank" rel="noopener noreferrer">Jekyll theme<ExternalLinkIcon/></a></li>
</ul>
<p> </p>
<h2 id="license" tabindex="-1"><a class="header-anchor" href="#license" aria-hidden="true">#</a> License</h2>
<p>VuePress theme Gungnir is <a href="https://www.apache.org/licenses/LICENSE-2.0" target="_blank" rel="noopener noreferrer">Apache License 2.0<ExternalLinkIcon/></a> licensed, see the <a href="LICENSE">LICENSE</a> file for details.</p>
<p>Plugins are licensed by MIT.</p>
</div></template>


