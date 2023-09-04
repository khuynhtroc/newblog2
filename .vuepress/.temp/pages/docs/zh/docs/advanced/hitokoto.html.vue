<template><div><p>::: info
默认不启用该功能。
:::</p>
<p>将 <code v-pre>hitokoto</code> 项设置为 <code v-pre>true</code> 可以开启首页的<a href="https://hitokoto.cn/" target="_blank" rel="noopener noreferrer">一言<ExternalLinkIcon/></a>气泡，将鼠标悬浮在头像上气泡就会显示出来：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">hitokoto</span><span class="token operator">:</span> <span class="token boolean">true</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p><img src="/img/docs/hitokoto-bubble.jpg" alt="hitokoto"></p>
<p>如果你想更改一言的请求参数，或想使用其他的接口，可以：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">hitokoto</span><span class="token operator">:</span> <span class="token string">"https://v1.hitokoto.cn?c=i"</span>  <span class="token comment">// 只返回诗词</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></div></template>


