<template><div><p>::: info
默认启用该功能。
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>对于没有启用的功能，与它们相关的代码并不会被打包。</p>
</div>
<p>主题默认在文章头部显示估计出的阅读时长，该功能基于插件 <RouterLink to="/zh/docs/plugins/reading-time/">plugin-reading-time</RouterLink>。</p>
<h2 id="配置" tabindex="-1"><a class="header-anchor" href="#配置" aria-hidden="true">#</a> 配置</h2>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">readingTime</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">excludes</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token string">'/url1'</span><span class="token punctuation">,</span> <span class="token string">'/url2/.*'</span><span class="token punctuation">]</span><span class="token punctuation">,</span>  <span class="token comment">// 不需要进行统计的页面路径（可选，默认：[]）</span>
      <span class="token literal-property property">includes</span> <span class="token operator">:</span> <span class="token punctuation">[</span><span class="token string">"/url1"</span><span class="token punctuation">,</span> <span class="token string">"/url2/.*"</span><span class="token punctuation">]</span><span class="token punctuation">,</span>  <span class="token comment">// 需要进行统计的页面路径，如果指定了这一项，那么 `excludes` 项无效（可选，默认：[]）</span>
      <span class="token literal-property property">wordsPerMinuteCN</span><span class="token operator">:</span> <span class="token number">500</span><span class="token punctuation">,</span>  <span class="token comment">// 一分钟可以阅读多少个中文字符（可选，默认：300）</span>
      <span class="token literal-property property">wordsPerMinuteEN</span><span class="token operator">:</span> <span class="token number">200</span><span class="token punctuation">,</span>  <span class="token comment">// 一分钟可以阅读多少个英文字符（可选，默认：160）</span>
      <span class="token literal-property property">excludeCodeBlock</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>  <span class="token comment">// 是否排除所有代码块内的字符（可选，默认：false）</span>
      <span class="token literal-property property">excludeTexBlock</span><span class="token operator">:</span> <span class="token boolean">true</span>    <span class="token comment">// 是否排除所有公式块内的字符（可选，默认：false）</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="重写" tabindex="-1"><a class="header-anchor" href="#重写" aria-hidden="true">#</a> 重写</h2>
<p>可以在文章的 <code v-pre>frontmatter</code> 中强行重写阅读时长：</p>
<div class="language-yaml line-numbers-mode" data-ext="yml"><pre v-pre class="language-yaml"><code><span class="token key atrule">title</span><span class="token punctuation">:</span> Hello Word
<span class="token key atrule">readingTime</span><span class="token punctuation">:</span> <span class="token punctuation">{</span> <span class="token key atrule">minutes</span><span class="token punctuation">:</span> <span class="token number">3</span> <span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="禁用" tabindex="-1"><a class="header-anchor" href="#禁用" aria-hidden="true">#</a> 禁用</h2>
<p>禁用该功能：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">readingTime</span><span class="token operator">:</span> <span class="token boolean">false</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></div></template>


