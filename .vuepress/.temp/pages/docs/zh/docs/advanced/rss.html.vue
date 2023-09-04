<template><div><p>::: info
默认不启用该功能。
:::</p>
<p>通过插件 <RouterLink to="/zh/docs/plugins/rss/">plugin-rss</RouterLink> 来提供 RSS 支持，生成的文件路径为 <code v-pre>./rss.xml</code>。插件配置：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">rss</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">siteURL</span><span class="token operator">:</span> <span class="token string">"https://zxh.io"</span><span class="token punctuation">,</span>  <span class="token comment">// 网站链接 （必须）</span>
      <span class="token literal-property property">title</span><span class="token operator">:</span> <span class="token string">"西伯利亚大恶龙的博客"</span><span class="token punctuation">,</span>  <span class="token comment">// 网站标题（可选，默认：`themeConfig.title`）</span>
      <span class="token literal-property property">description</span><span class="token operator">:</span> <span class="token string">"一个由 VuePress 和 Gungnir 强力驱动的博客"</span><span class="token punctuation">,</span>  <span class="token comment">// 网站描述（可选，默认：""）</span>
      <span class="token literal-property property">copyright</span><span class="token operator">:</span> <span class="token string">"Renovamen 2018-2021"</span><span class="token punctuation">,</span>  <span class="token comment">// 版权信息（可选，默认：""）</span>
      <span class="token literal-property property">count</span><span class="token operator">:</span> <span class="token number">20</span><span class="token punctuation">,</span>  <span class="token comment">// 需要在生成的 RSS 文件上显示多少篇文章（可选，默认：20）</span>
      <span class="token function-variable function">filter</span><span class="token operator">:</span> <span class="token punctuation">(</span><span class="token parameter">page</span><span class="token punctuation">)</span> <span class="token operator">=></span> <span class="token boolean">true</span>  <span class="token comment">// 文章筛选函数（可选，默认：(page) => true）</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p><a href="/rss.xml">这里</a>是本站的 RSS 文件。</p>
</div></template>


