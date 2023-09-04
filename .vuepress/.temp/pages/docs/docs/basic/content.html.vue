<template><div><h2 id="blog" tabindex="-1"><a class="header-anchor" href="#blog" aria-hidden="true">#</a> Blog</h2>
<h3 id="front-matter" tabindex="-1"><a class="header-anchor" href="#front-matter" aria-hidden="true">#</a> Front Matter</h3>
<p>Blog posts will be shown on <RouterLink to="/">home page</RouterLink>. A post file should be identified by <code v-pre>layout: Post</code> in its front matter. An example front matter for a post looks like:</p>
<div class="language-yaml line-numbers-mode" data-ext="yml"><pre v-pre class="language-yaml"><code><span class="token punctuation">---</span>
<span class="token key atrule">layout</span><span class="token punctuation">:</span> Post  <span class="token comment"># required</span>
<span class="token key atrule">title</span><span class="token punctuation">:</span> A Brief History of Time  <span class="token comment"># post title (required)</span>
<span class="token key atrule">subtitle</span><span class="token punctuation">:</span> From the Big Bang to Black Holes  <span class="token comment"># post subtitle (optional)</span>
<span class="token key atrule">date</span><span class="token punctuation">:</span> <span class="token datetime number">2020-03-31</span>  <span class="token comment"># publish date (optional)</span>
<span class="token key atrule">author</span><span class="token punctuation">:</span> Stephen Hawking  <span class="token comment"># post author (optional, will use `themeConfig.personalInfo.name` as default if it is not specified)</span>
<span class="token key atrule">useHeaderImage</span><span class="token punctuation">:</span> <span class="token boolean important">true</span>  <span class="token comment"># show header image in post or not (optional, default: false)</span>
<span class="token key atrule">headerImage</span><span class="token punctuation">:</span> /img/test.jpg  <span class="token comment"># path to the header image (required, even if `useHeaderImage` is false, becasue header image would also be shown on home page)</span>
<span class="token key atrule">headerMask</span><span class="token punctuation">:</span> rgba(40<span class="token punctuation">,</span> <span class="token number">57</span><span class="token punctuation">,</span> <span class="token number">101</span><span class="token punctuation">,</span> .4)  <span class="token comment"># mask of the header image (optional)</span>
<span class="token key atrule">headerImageCredit</span><span class="token punctuation">:</span> Jeremy Fenske  <span class="token comment"># source of the header image, like name of the author or website (optional, only works when "useHeaderImage: true")</span>
<span class="token key atrule">headerImageCreditLink</span><span class="token punctuation">:</span> https<span class="token punctuation">:</span>//www.artstation.com/artwork/nLY0K  <span class="token comment"># link to the source of the header image (optional, only works when "useHeaderImage: true")</span>
<span class="token key atrule">catalog</span><span class="token punctuation">:</span> <span class="token boolean important">false</span>  <span class="token comment"># enable/disable catalog of the current page, can rewrite `themeConfig.catalog` (optional, default: true)</span>
<span class="token key atrule">giscus</span><span class="token punctuation">:</span> <span class="token boolean important">false</span>  <span class="token comment"># enable/disable Giscus of the current page (optional, default: true)</span>
<span class="token key atrule">hide</span><span class="token punctuation">:</span> <span class="token boolean important">true</span>  <span class="token comment"># hide this blog in the blog list of home page and tags page or not (optional, default: false)</span>
<span class="token key atrule">tags</span><span class="token punctuation">:</span>  <span class="token comment"># post tags (optional)</span>
  <span class="token punctuation">-</span> space
  <span class="token punctuation">-</span> physics
<span class="token punctuation">---</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><div class="custom-container warning"><p class="custom-container-title">WARNING</p>
<p><code v-pre>title</code> will be used as the first-level heading in a post, so <strong>DO NOT write a first-level heading in your post content</strong>.</p>
</div>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>Posts that with <code v-pre>tags</code> item in front matter will be appear on <RouterLink to="/tags/">tags page</RouterLink>.</p>
</div>
<h3 id="url" tabindex="-1"><a class="header-anchor" href="#url" aria-hidden="true">#</a> URL</h3>
<p>If you would like the URL of a blog be shown in the form of <code v-pre>/post/year/month/day/post-title/</code>, just add this line to its front matter:</p>
<div class="language-yaml line-numbers-mode" data-ext="yml"><pre v-pre class="language-yaml"><code><span class="token punctuation">---</span>
<span class="token key atrule">layout</span><span class="token punctuation">:</span> Post
<span class="token key atrule">title</span><span class="token punctuation">:</span> A Brief History of Time
<span class="token key atrule">date</span><span class="token punctuation">:</span> <span class="token datetime number">2020-03-31</span>
<span class="token key atrule">permalinkPattern</span><span class="token punctuation">:</span> /post/<span class="token punctuation">:</span>year/<span class="token punctuation">:</span>month/<span class="token punctuation">:</span>day/<span class="token punctuation">:</span>slug/
<span class="token punctuation">---</span>
</code></pre><div class="highlight-lines"><br><br><br><br><div class="highlight-line">&nbsp;</div><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>See <a href="https://v2.vuepress.vuejs.org/reference/frontmatter.html#permalinkpattern" target="_blank" rel="noopener noreferrer">here<ExternalLinkIcon/></a> for more details.</p>
<div class="custom-container warning"><p class="custom-container-title">WARNING</p>
<p>When using this permalink pattern, you must <strong>specify the date</strong> in front matter or filename/dirname. See <a href="https://v2.vuepress.vuejs.org/reference/frontmatter.html#permalinkpattern" target="_blank" rel="noopener noreferrer">here<ExternalLinkIcon/></a> for more details.</p>
</div>
<h3 id="excerpt" tabindex="-1"><a class="header-anchor" href="#excerpt" aria-hidden="true">#</a> Excerpt</h3>
<p>In a blog markdown file, any content above the <code v-pre>&lt;!-- more --&gt;</code> comment will be extracted, rendered as excerpt and displayed on the home page.</p>
<h2 id="documentation" tabindex="-1"><a class="header-anchor" href="#documentation" aria-hidden="true">#</a> Documentation</h2>
<p>Gungnir can also be used for writing documentation, refer to <a href="https://v2.vuepress.vuejs.org/guide/" target="_blank" rel="noopener noreferrer">Documentation of VuePress<ExternalLinkIcon/></a> for basic usage.</p>
<p>An example front matter for a documentation page looks likes:</p>
<div class="language-yaml line-numbers-mode" data-ext="yml"><pre v-pre class="language-yaml"><code><span class="token punctuation">---</span>
<span class="token key atrule">title</span><span class="token punctuation">:</span> A Brief History of Time  <span class="token comment"># title (required)</span>
<span class="token key atrule">date</span><span class="token punctuation">:</span> <span class="token datetime number">2020-03-31</span>  <span class="token comment"># publish date (optional)</span>
<span class="token key atrule">author</span><span class="token punctuation">:</span> Stephen Hawking  <span class="token comment"># author (optional, will use `themeConfig.personalInfo.name` as default if it is not specified)</span>
<span class="token key atrule">giscus</span><span class="token punctuation">:</span> <span class="token boolean important">false</span>  <span class="token comment"># enable/disable Giscus of the current page (optional, default: true)</span>
<span class="token punctuation">---</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><div class="custom-container warning"><p class="custom-container-title">WARNING</p>
<p>Again, <code v-pre>title</code> will be used as the first-level heading in a documentation page, so <strong>DO NOT write a first-level heading in your documentation content</strong>.</p>
</div>
<h2 id="markdown-syntax" tabindex="-1"><a class="header-anchor" href="#markdown-syntax" aria-hidden="true">#</a> Markdown Syntax</h2>
<p>See:</p>
<ul>
<li><a href="https://www.markdownguide.org/basic-syntax/" target="_blank" rel="noopener noreferrer">Markdown Baisc Syntax<ExternalLinkIcon/></a></li>
<li><a href="https://v2.vuepress.vuejs.org/guide/markdown.html" target="_blank" rel="noopener noreferrer">VuePress's Markdown Extensions<ExternalLinkIcon/></a></li>
<li><RouterLink to="/docs/advanced/features/">Gungnir's Markdown Extensions</RouterLink></li>
</ul>
<h2 id="containers" tabindex="-1"><a class="header-anchor" href="#containers" aria-hidden="true">#</a> Containers</h2>
<h3 id="link-card-container" tabindex="-1"><a class="header-anchor" href="#link-card-container" aria-hidden="true">#</a> Link Card Container</h3>
<p>Gungnir adds a new container: link card.</p>
<h4 id="syntax" tabindex="-1"><a class="header-anchor" href="#syntax" aria-hidden="true">#</a> Syntax</h4>
<p>The syntax of it looks like:</p>
<div class="language-markdown line-numbers-mode" data-ext="md"><pre v-pre class="language-markdown"><code>::: link {Icon Name | Image URL} <span class="token url">[<span class="token content">title</span>](<span class="token url">url</span>)</span>
description
:::
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Some examples:</p>
<p>::: link <RouterLink to="/docs/basic/intro.html">Introduction</RouterLink>
vuepress-theme-gungnir Introduction
:::</p>
<p>::: link {fa-github-alt} <a href="https://github.com/Renovamen/vuepress-theme-gungnir" target="_blank" rel="noopener noreferrer">vuepress-theme-gungnir<ExternalLinkIcon/></a>
A blog theme for VuePress 2.
:::</p>
<p>::: link {/img/links/me.png} <a href="https://blog.zxh.io" target="_blank" rel="noopener noreferrer">My Blog<ExternalLinkIcon/></a>
My blog 🧐, powered by VuePress 2, themed by Gungnir.
:::</p>
<div class="language-markdown line-numbers-mode" data-ext="md"><pre v-pre class="language-markdown"><code>::: link <span class="token url">[<span class="token content">Introduction</span>](<span class="token url">/docs/basic/intro.html</span>)</span>
vuepress-theme-gungnir Introduction
:::

::: link {fa-github-alt} <span class="token url">[<span class="token content">vuepress-theme-gungnir</span>](<span class="token url">https://github.com/Renovamen/vuepress-theme-gungnir</span>)</span>
A blog theme for VuePress 2.
:::

::: link {/img/links/me.png} <span class="token url">[<span class="token content">My Blog</span>](<span class="token url">https://blog.zxh.io</span>)</span>
My blog 🧐, powered by VuePress 2, themed by Gungnir.
:::
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h4 id="options" tabindex="-1"><a class="header-anchor" href="#options" aria-hidden="true">#</a> Options</h4>
<p>You can choose to hide the site domain:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">container</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token literal-property property">link</span><span class="token operator">:</span> <span class="token punctuation">{</span>
          <span class="token literal-property property">siteDomain</span><span class="token operator">:</span> <span class="token boolean">false</span>  <span class="token comment">// optional, default: true</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><img src="/img/docs/link-card-without-site-domain.png" width="370px" style="margin-left: 0" alt="link-card-without-site-domain" />
<p>or disable this container:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">container</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token literal-property property">link</span><span class="token operator">:</span> <span class="token boolean">false</span>  <span class="token comment">// optional, default: true</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="other-containers" tabindex="-1"><a class="header-anchor" href="#other-containers" aria-hidden="true">#</a> Other Containers</h3>
<p>Here are some showcases of the <a href="https://v2.vuepress.vuejs.org/reference/plugin/container.html" target="_blank" rel="noopener noreferrer">custom containers<ExternalLinkIcon/></a> supported by Gungnir by default:</p>
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


