<template><div><p>::: info
This feature is disabled by default.
:::</p>
<p><RouterLink to="/docs/plugins/rss.html">plugin-rss</RouterLink> is used to generate the RSS file <code v-pre>./rss.xml</code> automatically. It can be cofigurated by:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">rss</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">siteURL</span><span class="token operator">:</span> <span class="token string">"https://zxh.io"</span><span class="token punctuation">,</span>  <span class="token comment">// site URL (required)</span>
      <span class="token literal-property property">title</span><span class="token operator">:</span> <span class="token string">"Renovamen's blog"</span><span class="token punctuation">,</span>  <span class="token comment">// site title (optional, default: `themeConfig.title`)</span>
      <span class="token literal-property property">description</span><span class="token operator">:</span> <span class="token string">"A blog powered by VuePress and Gungnir"</span><span class="token punctuation">,</span>  <span class="token comment">// site description (optional, default: "")</span>
      <span class="token literal-property property">copyright</span><span class="token operator">:</span> <span class="token string">"Renovamen 2018-2022"</span><span class="token punctuation">,</span>  <span class="token comment">// site copyright (optional, default: "")</span>
      <span class="token literal-property property">count</span><span class="token operator">:</span> <span class="token number">20</span><span class="token punctuation">,</span>  <span class="token comment">// number of posts to be generated (optional, default: 20)</span>
      <span class="token function-variable function">filter</span><span class="token operator">:</span> <span class="token punctuation">(</span><span class="token parameter">page</span><span class="token punctuation">)</span> <span class="token operator">=></span> <span class="token boolean">true</span>  <span class="token comment">// filter function to choose which posts to be generated (optional, default: (page) => true)</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Check <a href="/rss.xml">RSS file of this site</a> for an example.</p>
</div></template>


