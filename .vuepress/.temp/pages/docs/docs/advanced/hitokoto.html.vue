<template><div><p>::: info
This feature is disabled by default.
:::</p>
<p>A <a href="https://hitokoto.cn/" target="_blank" rel="noopener noreferrer">Hitokoto<ExternalLinkIcon/></a> bubble will appear on the home page when <code v-pre>hitokoto</code> is set to <code v-pre>true</code> and your mouse cursor is hovered over the avatar:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">hitokoto</span><span class="token operator">:</span> <span class="token boolean">true</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p><img src="/img/docs/hitokoto-bubble.jpg" alt="hitokoto"></p>
<p>You can also customize the requested API:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">hitokoto</span><span class="token operator">:</span> <span class="token string">"https://v1.hitokoto.cn?c=i"</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></div></template>


