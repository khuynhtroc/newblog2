<template><div><h2 id="博客文章" tabindex="-1"><a class="header-anchor" href="#博客文章" aria-hidden="true">#</a> 博客文章</h2>
<h3 id="front-matter" tabindex="-1"><a class="header-anchor" href="#front-matter" aria-hidden="true">#</a> Front Matter</h3>
<p>博客文章会在<RouterLink to="/">首页</RouterLink>显示。所有博客文章都需要在 front matter 里加上 <code v-pre>layout: Post</code>。</p>
<p>博客文章的 front matter 的格式为：</p>
<div class="language-yaml line-numbers-mode" data-ext="yml"><pre v-pre class="language-yaml"><code><span class="token punctuation">---</span>
<span class="token key atrule">layout</span><span class="token punctuation">:</span> Post  <span class="token comment"># 必须</span>
<span class="token key atrule">title</span><span class="token punctuation">:</span> 时间简史  <span class="token comment"># 博客标题（必须）</span>
<span class="token key atrule">subtitle</span><span class="token punctuation">:</span> 从大爆炸到黑洞  <span class="token comment"># 博客副标题（可选）</span>
<span class="token key atrule">date</span><span class="token punctuation">:</span> <span class="token datetime number">2020-03-31</span>  <span class="token comment"># 博客发表日期（可选）</span>
<span class="token key atrule">author</span><span class="token punctuation">:</span> 斯蒂芬·霍金  <span class="token comment"># 博客作者（可选，不填的话会使用 `themeConfig.personalInfo.name`）</span>
<span class="token key atrule">useHeaderImage</span><span class="token punctuation">:</span> <span class="token boolean important">true</span>  <span class="token comment"># 是否在博客中显示封面图（可选，默认：false）</span>
<span class="token key atrule">headerImage</span><span class="token punctuation">:</span> /img/test.jpg  <span class="token comment"># 博客封面图（必须，即使上一项选了 false，因为图片也需要在首页显示）</span>
<span class="token key atrule">headerMask</span><span class="token punctuation">:</span> rgba(40<span class="token punctuation">,</span> <span class="token number">57</span><span class="token punctuation">,</span> <span class="token number">101</span><span class="token punctuation">,</span> .4)  <span class="token comment"># 封面图遮罩（可选）</span>
<span class="token key atrule">headerImageCredit</span><span class="token punctuation">:</span> Jeremy Fenske  <span class="token comment"># 图片来源，比如图片作者的名字（可选，只在 "useHeaderImage: true" 时有效）</span>
<span class="token key atrule">headerImageCreditLink</span><span class="token punctuation">:</span> https<span class="token punctuation">:</span>//www.artstation.com/artwork/nLY0K  <span class="token comment"># 图片来源的链接（可选，只在 "useHeaderImage: true" 时有效）</span>
<span class="token key atrule">catalog</span><span class="token punctuation">:</span> <span class="token boolean important">true</span>  <span class="token comment"># 启用/禁用当前页的右侧目录，会覆写 `themeConfig.catalog`（可选，默认：true）</span>
<span class="token key atrule">giscus</span><span class="token punctuation">:</span> <span class="token boolean important">false</span>  <span class="token comment"># 启用/禁用当前页的 Giscus 评论（可选，默认：true）</span>
<span class="token key atrule">hide</span><span class="token punctuation">:</span> <span class="token boolean important">true</span>  <span class="token comment"># 是否在首页和标签页博客列表中隐藏这篇博客（可选，默认：false）</span>
<span class="token key atrule">tags</span><span class="token punctuation">:</span>  <span class="token comment"># 博客标签（可选）</span>
  <span class="token punctuation">-</span> 宇宙
  <span class="token punctuation">-</span> 物理
<span class="token punctuation">---</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><div class="custom-container warning"><p class="custom-container-title">WARNING</p>
<p><code v-pre>title</code> 会作为一级标题在博客中显示，所以<strong>不需要在博客正文中写一级标题</strong>。</p>
</div>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p><code v-pre>front-matter</code> 中有 <code v-pre>tags</code> 项的博客会在<RouterLink to="/tags/">标签页</RouterLink>显示。</p>
</div>
<h3 id="url" tabindex="-1"><a class="header-anchor" href="#url" aria-hidden="true">#</a> URL</h3>
<p>如果你希望博客文章的 URL 格式为 <code v-pre>/post/year/month/day/post-title/</code>，请在 front matter 里添加 <code v-pre>permalinkPattern</code> 项：</p>
<div class="language-yaml line-numbers-mode" data-ext="yml"><pre v-pre class="language-yaml"><code><span class="token punctuation">---</span>
<span class="token key atrule">layout</span><span class="token punctuation">:</span> Post
<span class="token key atrule">title</span><span class="token punctuation">:</span> A Brief History of Time
<span class="token key atrule">date</span><span class="token punctuation">:</span> <span class="token datetime number">2020-03-31</span>
<span class="token key atrule">permalinkPattern</span><span class="token punctuation">:</span> /post/<span class="token punctuation">:</span>year/<span class="token punctuation">:</span>month/<span class="token punctuation">:</span>day/<span class="token punctuation">:</span>slug/
<span class="token punctuation">---</span>
</code></pre><div class="highlight-lines"><br><br><br><br><div class="highlight-line">&nbsp;</div><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>更多细节请参考<a href="https://v2.vuepress.vuejs.org/zh/reference/frontmatter.html#permalinkpattern" target="_blank" rel="noopener noreferrer">这里<ExternalLinkIcon/></a>。</p>
<div class="custom-container warning"><p class="custom-container-title">WARNING</p>
<p>如果配置了这个 permalinkPattern，就必须通过博客文章的 front matter 或文件名/目录名<strong>指定 date（博客发表日期）</strong>。具体细节请参考<a href="https://v2.vuepress.vuejs.org/zh/reference/frontmatter.html#permalinkpattern" target="_blank" rel="noopener noreferrer">这里<ExternalLinkIcon/></a>。</p>
</div>
<h3 id="摘要" tabindex="-1"><a class="header-anchor" href="#摘要" aria-hidden="true">#</a> 摘要</h3>
<p>文章中 <code v-pre>&lt;!-- more --&gt;</code> 以上部分会被当作摘要，摘要会在首页文章流中显示。</p>
<h2 id="文档文章" tabindex="-1"><a class="header-anchor" href="#文档文章" aria-hidden="true">#</a> 文档文章</h2>
<p>同时本主题也保留了 VuePress 的文档功能，基本的使用方法及侧边栏配置方法请参考 <a href="https://v2.vuepress.vuejs.org/zh/guide/" target="_blank" rel="noopener noreferrer">VuePress 文档<ExternalLinkIcon/></a>。</p>
<p>文档文章的 <code v-pre>front-matter</code> 格式为：</p>
<div class="language-yaml line-numbers-mode" data-ext="yml"><pre v-pre class="language-yaml"><code><span class="token punctuation">---</span>
<span class="token key atrule">title</span><span class="token punctuation">:</span> 时间简史  <span class="token comment"># 文档标题（必须）</span>
<span class="token key atrule">date</span><span class="token punctuation">:</span> <span class="token datetime number">2020-03-31</span>  <span class="token comment"># 文档日期，会显示在文章头部（可选）</span>
<span class="token key atrule">author</span><span class="token punctuation">:</span> 斯蒂芬·霍金  <span class="token comment"># 文档作者（可选，不填的话会使用 `themeConfig.personalInfo.name`）</span>
<span class="token key atrule">giscus</span><span class="token punctuation">:</span> <span class="token boolean important">false</span>  <span class="token comment"># 启用/禁用当前页的 Giscus 评论（可选，默认：true）</span>
<span class="token punctuation">---</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><div class="custom-container warning"><p class="custom-container-title">WARNING</p>
<p>同样，<code v-pre>title</code> 会作为一级标题在文档中显示，所以也<strong>不需要在文档正文中写一级标题</strong>。</p>
</div>
<h2 id="markdown-语法" tabindex="-1"><a class="header-anchor" href="#markdown-语法" aria-hidden="true">#</a> Markdown 语法</h2>
<p>请参考：</p>
<ul>
<li><a href="https://www.markdownguide.org/basic-syntax/" target="_blank" rel="noopener noreferrer">Markdown 原生语法<ExternalLinkIcon/></a></li>
<li><a href="https://v1.vuepress.vuejs.org/zh/guide/markdown.html" target="_blank" rel="noopener noreferrer">VuePress 的 Markdown 拓展语法<ExternalLinkIcon/></a></li>
<li><RouterLink to="/zh/docs/advanced/markdown/">本主题的 Markdown 拓展语法</RouterLink></li>
</ul>
<h2 id="容器" tabindex="-1"><a class="header-anchor" href="#容器" aria-hidden="true">#</a> 容器</h2>
<h3 id="链接卡片容器" tabindex="-1"><a class="header-anchor" href="#链接卡片容器" aria-hidden="true">#</a> 链接卡片容器</h3>
<p>本主题新增了链接卡片容器。</p>
<h4 id="语法" tabindex="-1"><a class="header-anchor" href="#语法" aria-hidden="true">#</a> 语法</h4>
<div class="language-markdown line-numbers-mode" data-ext="md"><pre v-pre class="language-markdown"><code>::: link {Icon Name | Image URL} <span class="token url">[<span class="token content">title</span>](<span class="token url">url</span>)</span>
description
:::
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>示例:</p>
<p>::: link <RouterLink to="/zh/docs/basic/intro.html">介绍</RouterLink>
vuepress-theme-gungnir Introduction
:::</p>
<p>::: link {fa-github-alt} <a href="https://github.com/Renovamen/vuepress-theme-gungnir" target="_blank" rel="noopener noreferrer">vuepress-theme-gungnir<ExternalLinkIcon/></a>
A blog theme for VuePress 2.
:::</p>
<p>::: link {/img/links/me.png} <a href="https://blog.zxh.io" target="_blank" rel="noopener noreferrer">My Blog<ExternalLinkIcon/></a>
My blog 🧐, powered by VuePress 2, themed by Gungnir.
:::</p>
<div class="language-markdown line-numbers-mode" data-ext="md"><pre v-pre class="language-markdown"><code>::: link <span class="token url">[<span class="token content">介绍</span>](<span class="token url">/zh/docs/basic/intro.html</span>)</span>
vuepress-theme-gungnir Introduction
:::

::: link {fa-github-alt} <span class="token url">[<span class="token content">vuepress-theme-gungnir</span>](<span class="token url">https://github.com/Renovamen/vuepress-theme-gungnir</span>)</span>
A blog theme for VuePress 2.
:::

::: link {/img/links/me.png} <span class="token url">[<span class="token content">My Blog</span>](<span class="token url">https://blog.zxh.io</span>)</span>
My blog 🧐, powered by VuePress 2, themed by Gungnir.
:::
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h4 id="配置" tabindex="-1"><a class="header-anchor" href="#配置" aria-hidden="true">#</a> 配置</h4>
<p>如果你不需要再链接卡片中显示域名:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">container</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token literal-property property">link</span><span class="token operator">:</span> <span class="token punctuation">{</span>
          <span class="token literal-property property">siteDomain</span><span class="token operator">:</span> <span class="token boolean">false</span>  <span class="token comment">// 可选，默认："true"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><img src="/img/docs/link-card-without-site-domain.png" width="370px" style="margin-left: 0" alt="link-card-without-site-domain" />
<p>或者想要关闭该功能:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">container</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token literal-property property">link</span><span class="token operator">:</span> <span class="token boolean">false</span>  <span class="token comment">// 可选，默认："true"</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="其他容器" tabindex="-1"><a class="header-anchor" href="#其他容器" aria-hidden="true">#</a> 其他容器</h3>
<p>这里展示一下本主题默认支持的<a href="https://v2.vuepress.vuejs.org/zh/reference/plugin/container.html" target="_blank" rel="noopener noreferrer">容器<ExternalLinkIcon/></a>用法：</p>
<p>::: info
This is an info message.
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>This is a tip message.</p>
</div>
<div class="custom-container warning"><p class="custom-container-title">WARNING</p>
<p>This is a warning message.</p>
</div>
<div class="custom-container danger"><p class="custom-container-title">DANGER</p>
<p>This is a dangerous warning message.</p>
</div>
<details class="custom-container details"><summary>Show me the code.</summary>
<div class="language-cpp line-numbers-mode" data-ext="cpp"><pre v-pre class="language-cpp"><code>cout <span class="token operator">&lt;&lt;</span> <span class="token string">"Hello World!"</span> <span class="token operator">&lt;&lt;</span> <span class="token string">"\n"</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></details>
</div></template>


