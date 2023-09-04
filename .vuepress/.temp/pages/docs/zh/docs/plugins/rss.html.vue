<template><div><p>
  <a href="https://www.npmjs.com/package/@renovamen/vuepress-plugin-rss/v/next" target="_blank">
    <img src="https://img.shields.io/npm/v/@renovamen/vuepress-plugin-rss/next.svg?style=flat-square&logo=npm" style="display: inline; margin: 0 4px 0 0" alt="npm">
  </a>
  <a href="https://github.com/Renovamen/vuepress-theme-gungnir/tree/main/packages/plugins/rss" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-@renovamen/vuepress--plugin--rss-26A2FF?style=flat-square&logo=github" style="display: inline; margin: 0 4px 0 0" alt="github">
  </a>
  <a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/plugins/rss/LICENSE" target="_blank">
    <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" style="display: inline; margin: 0 4px 0 0" alt="license">
  </a>
</p>
<p><code v-pre>@renovamen/vuepress-plugin-rss</code> 插件，用于为 <a href="https://v2.vuepress.vuejs.org/zh/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a> 主题 Gungnir 提供 RSS 支持。修改自 <a href="https://github.com/youngtailors/vuepress-plugin-rss" target="_blank" rel="noopener noreferrer">youngtailors/vuepress-plugin-rss<ExternalLinkIcon/></a>。</p>
<div class="custom-container warning"><p class="custom-container-title">WARNING</p>
<p>该插件仅能保证在 VuePress 主题 Gungnir 上正常工作，在别的 VuePress 主题上可能会无效。</p>
</div>
<h2 id="安装" tabindex="-1"><a class="header-anchor" href="#安装" aria-hidden="true">#</a> 安装</h2>
<CodeGroup>
<CodeGroupItem title="PNPM" active>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">pnpm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-rss@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
<CodeGroupItem title="YARN" active>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">yarn</span> <span class="token function">add</span> @renovamen/vuepress-plugin-rss@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
<CodeGroupItem title="NPM">
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">npm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-rss@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
</CodeGroup>
<h2 id="配置" tabindex="-1"><a class="header-anchor" href="#配置" aria-hidden="true">#</a> 配置</h2>
<p>在 <code v-pre>.vuepress/config.js</code> 中配置插件：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> rssPlugin <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"@renovamen/vuepress-plugin-rss"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">rssPlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
      <span class="token literal-property property">siteURL</span><span class="token operator">:</span> <span class="token string">"https://zxh.io"</span><span class="token punctuation">,</span>  <span class="token comment">// 网站链接 （必须）</span>
      <span class="token literal-property property">title</span><span class="token operator">:</span> <span class="token string">"西伯利亚大恶龙的博客"</span><span class="token punctuation">,</span>  <span class="token comment">// 网站标题（可选，默认：`themeConfig.title`）</span>
      <span class="token literal-property property">description</span><span class="token operator">:</span> <span class="token string">"一个由 VuePress 和 Gungnir 强力驱动的博客"</span><span class="token punctuation">,</span>  <span class="token comment">// 网站描述（可选，默认：""）</span>
      <span class="token literal-property property">copyright</span><span class="token operator">:</span> <span class="token string">"Renovamen 2018-2021"</span><span class="token punctuation">,</span>  <span class="token comment">// 版权信息（可选，默认：""）</span>
      <span class="token literal-property property">count</span><span class="token operator">:</span> <span class="token number">20</span><span class="token punctuation">,</span>  <span class="token comment">// 需要在生成的 RSS 文件上显示多少篇文章（可选，默认：20）</span>
      <span class="token function-variable function">filter</span><span class="token operator">:</span> <span class="token punctuation">(</span><span class="token parameter">page</span><span class="token punctuation">)</span> <span class="token operator">=></span> <span class="token boolean">true</span>  <span class="token comment">// 文章筛选函数（可选，默认：(page) => true）</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="开源协议" tabindex="-1"><a class="header-anchor" href="#开源协议" aria-hidden="true">#</a> 开源协议</h2>
<p><a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/plugins/rss/LICENSE" target="_blank" rel="noopener noreferrer">MIT<ExternalLinkIcon/></a></p>
</div></template>


