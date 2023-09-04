<template><div><p>
  <a href="https://www.npmjs.com/package/@renovamen/vuepress-plugin-mermaid/v/next" target="_blank">
    <img src="https://img.shields.io/npm/v/@renovamen/vuepress-plugin-mermaid/next.svg?style=flat-square&logo=npm" style="display: inline; margin: 0 4px 0 0" alt="npm">
  </a>
  <a href="https://github.com/Renovamen/vuepress-theme-gungnir/tree/main/packages/plugins/mermaid" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-@renovamen/vuepress--plugin--mermaid-26A2FF?style=flat-square&logo=github" style="display: inline; margin: 0 4px 0 0" alt="github">
  </a>
  <a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/plugins/mermaid/LICENSE" target="_blank">
    <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" style="display: inline; margin: 0 4px 0 0" alt="license">
  </a>
</p>
<p><code v-pre>@renovamen/vuepress-plugin-mermaid@next</code> 插件，用于在 <a href="https://v2.vuepress.vuejs.org/zh/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a> 的 Markdown 中使用 <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">Mermaid<ExternalLinkIcon/></a>，从而在文章中加入流程图、状态图、时序图、甘特图等。</p>
<h2 id="安装" tabindex="-1"><a class="header-anchor" href="#安装" aria-hidden="true">#</a> 安装</h2>
<CodeGroup>
<CodeGroupItem title="PNPM" active>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">pnpm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-mermaid@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
<CodeGroupItem title="YARN" active>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">yarn</span> <span class="token function">add</span> @renovamen/vuepress-plugin-mermaid@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
<CodeGroupItem title="NPM">
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">npm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-mermaid@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
</CodeGroup>
<p>然后在 <code v-pre>.vuepress/config.js</code> 中引入这个插件：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> mermaidPlugin <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"@renovamen/vuepress-plugin-mermaid"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">mermaidPlugin</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="配置项" tabindex="-1"><a class="header-anchor" href="#配置项" aria-hidden="true">#</a> 配置项</h2>
<h3 id="token" tabindex="-1"><a class="header-anchor" href="#token" aria-hidden="true">#</a> token</h3>
<ul>
<li>
<p>类型：<code v-pre>string</code></p>
</li>
<li>
<p>默认值：<code v-pre>&quot;mermaidjs&quot;</code></p>
</li>
<li>
<p>详情：自定义代码块的 token</p>
</li>
</ul>
<h3 id="theme" tabindex="-1"><a class="header-anchor" href="#theme" aria-hidden="true">#</a> theme</h3>
<ul>
<li>
<p>类型：<code v-pre>string</code></p>
</li>
<li>
<p>默认值：<code v-pre>&quot;default&quot;</code></p>
</li>
<li>
<p>详情：主题（<a href="https://github.com/mermaid-js/mermaid/tree/develop/src/themes" target="_blank" rel="noopener noreferrer">这里<ExternalLinkIcon/></a>是所有 Mermaid 支持的主题）</p>
</li>
</ul>
<h3 id="darktheme" tabindex="-1"><a class="header-anchor" href="#darktheme" aria-hidden="true">#</a> darkTheme</h3>
<ul>
<li>
<p>类型：<code v-pre>string</code></p>
</li>
<li>
<p>默认值：<code v-pre>&quot;dark&quot;</code></p>
</li>
<li>
<p>详情：夜间模式主题，只在 <a href="#darkselector">darkSelector</a> 和 <a href="#darkclass">darkClass</a> 都被设置了的情况下有效</p>
</li>
</ul>
<h3 id="darkselector" tabindex="-1"><a class="header-anchor" href="#darkselector" aria-hidden="true">#</a> darkSelector</h3>
<ul>
<li>
<p>类型：<code v-pre>string</code></p>
</li>
<li>
<p>默认值：<code v-pre>undefined</code></p>
</li>
<li>
<p>详情</p>
<ul>
<li>一个 CSS 选择器，插件会根据它选择一个 HTML 元素，然后通过 <a href="#darkclass">darkClass</a> 来判断当前是否为夜间模式</li>
<li>对于默认主题和 Gungnir 主题，这一项需要被设为 <code v-pre>html</code></li>
</ul>
</li>
</ul>
<h3 id="darkclass" tabindex="-1"><a class="header-anchor" href="#darkclass" aria-hidden="true">#</a> darkClass</h3>
<ul>
<li>
<p>类型：<code v-pre>string</code></p>
</li>
<li>
<p>默认值：<code v-pre>undefined</code></p>
</li>
<li>
<p>详情</p>
<ul>
<li>一个类名，插件会根据它来判断当前是否为夜间模式</li>
<li>对于默认主题和 Gungnir 主题，这一项需要被设为 <code v-pre>dark</code></li>
</ul>
</li>
</ul>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>在启用夜间模式时，默认主题和 Gungnir 主题会在 <code v-pre>html</code> 元素上添加一个类名 <code v-pre>dark</code>。</p>
<p>点击右下角的模式切换按钮，体验 Mermaid 的主题切换。</p>
</div>
<h2 id="使用" tabindex="-1"><a class="header-anchor" href="#使用" aria-hidden="true">#</a> 使用</h2>
<p>代码块的 token info 需要为 <code v-pre>mermaidjs</code>（如果你使用了自定义代码块 token，则需要为 <code v-pre>options.token</code>），例子：</p>
<div class="language-mermaidjs line-numbers-mode" data-ext="mermaidjs"><pre v-pre class="language-mermaidjs"><code>sequenceDiagram
  Alice-&gt;John: Hello John, how are you?
  loop Every minute
    John--&gt;Alice: Great!
  end
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><details class="custom-container details"><summary>代码</summary>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>```mermaidjs
sequenceDiagram
  Alice->John: Hello John, how are you?
  loop Every minute
    John-->Alice: Great!
  end
```
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></details>
<p>更详细的用法可以参考 <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">Mermaid 文档<ExternalLinkIcon/></a>。</p>
<h2 id="开源协议" tabindex="-1"><a class="header-anchor" href="#开源协议" aria-hidden="true">#</a> 开源协议</h2>
<p><a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/plugins/mermaid/LICENSE" target="_blank" rel="noopener noreferrer">MIT<ExternalLinkIcon/></a></p>
</div></template>


