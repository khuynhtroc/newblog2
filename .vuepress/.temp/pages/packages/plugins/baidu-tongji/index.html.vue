<template><div><h1 id="renovamen-vuepress-plugin-baidu-tongji-next" tabindex="-1"><a class="header-anchor" href="#renovamen-vuepress-plugin-baidu-tongji-next" aria-hidden="true">#</a> @renovamen/vuepress-plugin-baidu-tongji@next</h1>
<p><a href="https://www.npmjs.com/package/@renovamen/vuepress-plugin-baidu-tongji/v/next" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/npm/v/@renovamen/vuepress-plugin-baidu-tongji/next.svg?style=flat-square&amp;logo=npm" alt="npm"><ExternalLinkIcon/></a> <a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/baidu-tongji.html" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Docs-@renovamen/vuepress--plugin--baidu--tongji-26A2FF?style=flat-square" alt="docs"><ExternalLinkIcon/></a> <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-green?style=flat-square" alt="license"></a></p>
<p>Plugin <code v-pre>@renovamen/vuepress-plugin-baidu-tongji@next</code> for adding <a href="https://tongji.baidu.com" target="_blank" rel="noopener noreferrer">百度统计<ExternalLinkIcon/></a> to <a href="https://v2.vuepress.vuejs.org/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a>. It is edited from <a href="https://github.com/vuepress/vuepress-next/tree/main/packages/%40vuepress/plugin-google-analytics" target="_blank" rel="noopener noreferrer">@vuepress/plugin-google-analytics<ExternalLinkIcon/></a>.</p>
<p> </p>
<h2 id="install" tabindex="-1"><a class="header-anchor" href="#install" aria-hidden="true">#</a> Install</h2>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token comment"># pnpm</span>
<span class="token function">pnpm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-baidu-tongji@next
<span class="token comment"># yarn</span>
<span class="token function">yarn</span> <span class="token function">add</span> @renovamen/vuepress-plugin-baidu-tongji@next
<span class="token comment"># npm</span>
<span class="token function">npm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-baidu-tongji@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p> </p>
<h2 id="usage" tabindex="-1"><a class="header-anchor" href="#usage" aria-hidden="true">#</a> Usage</h2>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> baiduTongjiPlugin <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"@renovamen/vuepress-plugin-baidu-tongji"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">baiduTongjiPlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
      <span class="token string-property property">"id"</span><span class="token operator">:</span> <span class="token string">"your-tracking-code"</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p><code v-pre>id</code> is your tracking code offered by <a href="https://tongji.baidu.com" target="_blank" rel="noopener noreferrer">百度统计<ExternalLinkIcon/></a>.</p>
<p> </p>
<h2 id="license" tabindex="-1"><a class="header-anchor" href="#license" aria-hidden="true">#</a> License</h2>
<p><a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/plugins/baidu-tongji/LICENSE" target="_blank" rel="noopener noreferrer">MIT<ExternalLinkIcon/></a></p>
</div></template>


