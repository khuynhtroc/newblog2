<template><div><h1 id="renovamen-vuepress-plugin-reading-time-next" tabindex="-1"><a class="header-anchor" href="#renovamen-vuepress-plugin-reading-time-next" aria-hidden="true">#</a> @renovamen/vuepress-plugin-reading-time@next</h1>
<p><a href="https://www.npmjs.com/package/@renovamen/vuepress-plugin-reading-time/v/next" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/npm/v/@renovamen/vuepress-plugin-reading-time/next.svg?style=flat-square&amp;logo=npm" alt="npm"><ExternalLinkIcon/></a> <a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/reading-time.html" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Docs-@renovamen/vuepress--plugin--reading--time-26A2FF?style=flat-square" alt="docs"><ExternalLinkIcon/></a> <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-green?style=flat-square" alt="license"></a></p>
<p>Plugin <code v-pre>@renovamen/vuepress-plugin-reading-time@next</code> for counting words and estimating reading time in <a href="https://v2.vuepress.vuejs.org/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a>. Compare to other similar VuePress plugins, this plugin supports:</p>
<ul>
<li>Setting reading speed for English and Chinese separately</li>
<li>Excluding all content inside code blocks or tex blocks</li>
</ul>
<p><a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/reading-time.html" target="_blank" rel="noopener noreferrer">Demo<ExternalLinkIcon/></a> (see the number beside the clock icon)</p>
<p> </p>
<h2 id="install" tabindex="-1"><a class="header-anchor" href="#install" aria-hidden="true">#</a> Install</h2>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token comment"># pnpm</span>
<span class="token function">pnpm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-reading-time@next
<span class="token comment"># yarn</span>
<span class="token function">yarn</span> <span class="token function">add</span> @renovamen/vuepress-plugin-reading-time@next
<span class="token comment"># npm</span>
<span class="token function">npm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-reading-time@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Then add it to your <code v-pre>.vuepress/config.js</code>:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> readingTimePlugin <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"@renovamen/vuepress-plugin-reading-time"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">readingTimePlugin</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p> </p>
<h2 id="usage" tabindex="-1"><a class="header-anchor" href="#usage" aria-hidden="true">#</a> Usage</h2>
<p>The <code v-pre>readingTime</code> data can be accessed by:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">import</span> <span class="token punctuation">{</span> pageData <span class="token punctuation">}</span> <span class="token keyword">from</span> <span class="token string">"@vuepress/client"</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>pageData<span class="token punctuation">.</span>value<span class="token punctuation">.</span>readingTime<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div></div></div><p>An example <code v-pre>readingTime</code> data:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token punctuation">{</span>
  <span class="token literal-property property">minutes</span><span class="token operator">:</span> <span class="token number">12</span><span class="token punctuation">,</span>
  <span class="token literal-property property">words</span><span class="token operator">:</span> <span class="token number">3500</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>You can override by specifying <code v-pre>readingTime</code> data in frontmatter</p>
<div class="language-yaml line-numbers-mode" data-ext="yml"><pre v-pre class="language-yaml"><code><span class="token key atrule">title</span><span class="token punctuation">:</span> Hello Word
<span class="token key atrule">readingTime</span><span class="token punctuation">:</span> <span class="token punctuation">{</span> <span class="token key atrule">minutes</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token key atrule">words</span><span class="token punctuation">:</span> <span class="token number">1500</span> <span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div></div></div><p> </p>
<h2 id="options" tabindex="-1"><a class="header-anchor" href="#options" aria-hidden="true">#</a> Options</h2>
<h3 id="excludes" tabindex="-1"><a class="header-anchor" href="#excludes" aria-hidden="true">#</a> excludes</h3>
<p>Exclude pages by their path via a regular expression. Will be ignored if <a href="#includes"><code v-pre>includes</code></a> is specified.</p>
<ul>
<li>Type: <code v-pre>Array&lt;string&gt;</code></li>
<li>Default: <code v-pre>[]</code></li>
</ul>
<p>Example:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
  <span class="token function">readingTimePlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">excludes</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token string">"/docs/.*"</span><span class="token punctuation">,</span> <span class="token string">"/posts/hello-word.html"</span><span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">]</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="includes" tabindex="-1"><a class="header-anchor" href="#includes" aria-hidden="true">#</a> includes</h3>
<p>An allowlist of all pages that should be computed word count and reading time for. Includes pages by their path via a regular expression.</p>
<p>If <code v-pre>includes</code> is specified, <a href="#excludes"><code v-pre>excludes</code></a> will be ignored.</p>
<ul>
<li>Type: <code v-pre>Array&lt;string&gt;</code></li>
<li>Default: <code v-pre>[]</code></li>
</ul>
<p>Example:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
  <span class="token function">readingTimePlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">includes</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token string">"/docs/.*"</span><span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">]</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="wordsperminutecn" tabindex="-1"><a class="header-anchor" href="#wordsperminutecn" aria-hidden="true">#</a> wordsPerMinuteCN</h3>
<p>The number of Chinese words per minute a user can read.</p>
<ul>
<li>Type: <code v-pre>int</code></li>
<li>Default: <code v-pre>300</code></li>
</ul>
<p>Example:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
  <span class="token function">readingTimePlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">wordsPerMinuteCN</span><span class="token operator">:</span> <span class="token number">500</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">]</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="wordsperminuteen" tabindex="-1"><a class="header-anchor" href="#wordsperminuteen" aria-hidden="true">#</a> wordsPerMinuteEN</h3>
<p>The number of English words per minute a user can read.</p>
<ul>
<li>Type: <code v-pre>int</code></li>
<li>Default: <code v-pre>160</code></li>
</ul>
<p>Example:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
  <span class="token function">readingTimePlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">wordsPerMinuteEN</span><span class="token operator">:</span> <span class="token number">200</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">]</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="excludecodeblock" tabindex="-1"><a class="header-anchor" href="#excludecodeblock" aria-hidden="true">#</a> excludeCodeBlock</h3>
<p>Exclude all content inside code blocks or not.</p>
<ul>
<li>Type: <code v-pre>boolean</code></li>
<li>Default: <code v-pre>false</code></li>
</ul>
<p>Example:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
  <span class="token function">readingTimePlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">excludeCodeBlock</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">]</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="excludetexblock" tabindex="-1"><a class="header-anchor" href="#excludetexblock" aria-hidden="true">#</a> excludeTexBlock</h3>
<p>Exclude all content inside tex blocks or not.</p>
<ul>
<li>Type: <code v-pre>boolean</code></li>
<li>Default: <code v-pre>false</code></li>
</ul>
<p>Example:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
  <span class="token function">readingTimePlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">excludeTexBlock</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">]</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p> </p>
<h2 id="license" tabindex="-1"><a class="header-anchor" href="#license" aria-hidden="true">#</a> License</h2>
<p><a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/plugins/reading-time/LICENSE" target="_blank" rel="noopener noreferrer">MIT<ExternalLinkIcon/></a></p>
</div></template>


