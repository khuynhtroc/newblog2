<template><div><p>Welcome to VuePress theme Gungnir.</p>
<!-- more -->
<h2 id="paragraphs" tabindex="-1"><a class="header-anchor" href="#paragraphs" aria-hidden="true">#</a> Paragraphs</h2>
<h3 id="english" tabindex="-1"><a class="header-anchor" href="#english" aria-hidden="true">#</a> English</h3>
<p>A well-known scientist (some say it was ==Bertrand Russell==) once gave a public lecture on astronomy. He described how the earth orbits around the sun and how the sun, in turn, orbits around the center of a vast collection of stars called our galaxy. At the end of the lecture, a little old lady at the back of the room got up and said: “What you have told us is rubbish. The world is really a flat plate supported on the back of a giant tortoise.” The scientist gave a superior smile before replying, “What is the tortoise standing on.” “You’re very clever, young man, very clever,” said the old lady. “But it’s turtles all the way down!”</p>
<p>Most people would find the picture of our universe as an infinite <strong>tower of tortoises</strong> rather ridiculous, but why do we think we know better? What do we know about the universe, and how do we know it? Where did the universe come from, and where is it going? Did the universe have a beginning, and if so, what happened before then? What is the nature of time? Will it ever come to an end? Can we go back in time? Recent breakthroughs in physics, made possible in part by fantastic new technologies, suggest answers to some of these longstanding questions. Someday these answers may seem as obvious to us as the earth orbiting the sun – or perhaps as ridiculous as a tower of tortoises. Only time (whatever that may be) will tell. [^1]</p>
<h3 id="中文" tabindex="-1"><a class="header-anchor" href="#中文" aria-hidden="true">#</a> 中文</h3>
<p>一位著名的科学家（据说是 ==贝特朗·罗素==）曾经作过一次关于天文学方面的讲演。他描述了地球如何绕着太阳运动，以及太阳又是如何绕着我们称之为星系的巨大的恒星群的中心转动。演讲结束之时，一位坐在房间后排的矮个老妇人站起来说道：“你说得这些都是废话。这个世界实际上是驮在一只大乌龟的背上的一块平板。”这位科学家很有教养地微笑着答道：“那么这只乌龟是站在什么上面的呢？”“你很聪明，年轻人，的确很聪明，”老妇人说，“不过，这是一只驮着一只一直驮下去的乌龟塔啊！”</p>
<p>大部分人会觉得，把我们的宇宙喻为一个无限的<strong>乌龟塔</strong>相当荒谬，可是为什么我们自以为知道得更多一些呢？我们对宇宙了解了多少？而我们又是怎样才知道的呢？宇宙从何而来又将向何处去？宇宙有开端吗？如果有的话，在这开端之前发生了什么？时间的本质是什么？它会有一个终结吗？在物理学上的一些最新突破，使一部分奇妙的新技术得以实现，从而对于回答这些长期以来悬而未决的某些问题有所启发。也许有一天这些答案会像我们认为地球绕着太阳运动那样显而易见——当然也可能像乌龟塔那般荒唐可笑。不管怎样，惟有让时间来判断了。<a href="%E6%91%98%E8%87%AA%E3%80%8A%E6%97%B6%E9%97%B4%E7%AE%80%E5%8F%B2%E3%80%8B%EF%BC%8C%E4%BD%9C%E8%80%85%E4%B8%BA%E6%96%AF%E8%92%82%E8%8A%AC%C2%B7%E9%9C%8D%E9%87%91%E3%80%82">^2</a></p>
<h2 id="h2-heading" tabindex="-1"><a class="header-anchor" href="#h2-heading" aria-hidden="true">#</a> H2 Heading</h2>
<h3 id="h3-heading" tabindex="-1"><a class="header-anchor" href="#h3-heading" aria-hidden="true">#</a> H3 Heading</h3>
<h4 id="h4-heading" tabindex="-1"><a class="header-anchor" href="#h4-heading" aria-hidden="true">#</a> H4 Heading</h4>
<h5 id="h5-heading" tabindex="-1"><a class="header-anchor" href="#h5-heading" aria-hidden="true">#</a> H5 Heading</h5>
<h6 id="h6-heading" tabindex="-1"><a class="header-anchor" href="#h6-heading" aria-hidden="true">#</a> H6 Heading</h6>
<h2 id="code" tabindex="-1"><a class="header-anchor" href="#code" aria-hidden="true">#</a> Code</h2>
<h3 id="code-blocks" tabindex="-1"><a class="header-anchor" href="#code-blocks" aria-hidden="true">#</a> Code Blocks</h3>
<p>Click the green button on the upper-left corner to make the code block full screen.</p>
<div class="language-python line-numbers-mode" data-ext="py"><pre v-pre class="language-python"><code><span class="token keyword">import</span> food

<span class="token keyword">class</span> <span class="token class-name">Dragon</span><span class="token punctuation">:</span>
  <span class="token keyword">def</span> <span class="token function">__init__</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> happiness<span class="token punctuation">)</span><span class="token punctuation">:</span>
    self<span class="token punctuation">.</span>happiness <span class="token operator">=</span> happiness
  <span class="token keyword">def</span> <span class="token function">code</span><span class="token punctuation">(</span>self<span class="token punctuation">)</span><span class="token punctuation">:</span>
    <span class="token triple-quoted-string string">""" just code """</span>
    self<span class="token punctuation">.</span>happiness <span class="token operator">-=</span> <span class="token number">60</span>
  <span class="token keyword">def</span> <span class="token function">eat</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> n<span class="token punctuation">)</span>
    <span class="token comment"># just eat</span>
    self<span class="token punctuation">.</span>happiness <span class="token operator">+=</span> n <span class="token operator">*</span> food<span class="token punctuation">.</span>size

me <span class="token operator">=</span> Dragon<span class="token punctuation">(</span><span class="token number">100</span><span class="token punctuation">)</span>

<span class="token keyword">while</span> <span class="token boolean">True</span><span class="token punctuation">:</span>
  me<span class="token punctuation">.</span>code<span class="token punctuation">(</span><span class="token punctuation">)</span>
  me<span class="token punctuation">.</span>eat<span class="token punctuation">(</span><span class="token number">10</span><span class="token punctuation">)</span>
</code></pre><div class="highlight-lines"><br><br><br><br><br><br><br><div class="highlight-line">&nbsp;</div><br><br><br><br><br><br><br><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="code-groups" tabindex="-1"><a class="header-anchor" href="#code-groups" aria-hidden="true">#</a> Code Groups</h3>
<CodeGroup>
<CodeGroupItem title="YARN" active>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">yarn</span> <span class="token function">add</span> <span class="token parameter variable">-D</span> vuepress-theme-gungnir@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
<CodeGroupItem title="NPM">
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token function">npm</span> <span class="token function">install</span> <span class="token parameter variable">-D</span> vuepress-theme-gungnir@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
</CodeGroup>
<h3 id="inline-code" tabindex="-1"><a class="header-anchor" href="#inline-code" aria-hidden="true">#</a> Inline Code</h3>
<p><code v-pre>const a = 1</code></p>
<h2 id="table" tabindex="-1"><a class="header-anchor" href="#table" aria-hidden="true">#</a> Table</h2>
<table>
<thead>
<tr>
<th>Name</th>
<th>Info</th>
</tr>
</thead>
<tbody>
<tr>
<td>vuepress-theme-gungnir</td>
<td>Gungnir is a blog theme for Vuepress 2.</td>
</tr>
</tbody>
</table>
<h2 id="badges" tabindex="-1"><a class="header-anchor" href="#badges" aria-hidden="true">#</a> Badges <Badge text="tip" /> <Badge text="warning" type="warning" /> <Badge text="danger" type="danger" /> <Badge text="tip middle" vertical="middle" /></h2>
<h2 id="charts" tabindex="-1"><a class="header-anchor" href="#charts" aria-hidden="true">#</a> Charts</h2>
<h3 id="chart-js" tabindex="-1"><a class="header-anchor" href="#chart-js" aria-hidden="true">#</a> Chart.js</h3>
<div class="language-chart line-numbers-mode" data-ext="chart"><pre v-pre class="language-chart"><code>{
  &quot;type&quot;: &quot;bar&quot;,
  &quot;data&quot;: {
    &quot;labels&quot;: [&quot;Red&quot;, &quot;Blue&quot;, &quot;Yellow&quot;, &quot;Green&quot;, &quot;Purple&quot;, &quot;Orange&quot;],
    &quot;datasets&quot;: [{
      &quot;label&quot;: &quot;# of Votes&quot;,
      &quot;data&quot;: [12, 19, 3, 5, 2, 3],
      &quot;backgroundColor&quot;: [
        &quot;rgba(255, 99, 132, 0.2)&quot;,
        &quot;rgba(54, 162, 235, 0.2)&quot;,
        &quot;rgba(255, 206, 86, 0.2)&quot;,
        &quot;rgba(75, 192, 192, 0.2)&quot;,
        &quot;rgba(153, 102, 255, 0.2)&quot;,
        &quot;rgba(255, 159, 64, 0.2)&quot;
      ],
      &quot;borderColor&quot;: [
        &quot;rgba(255, 99, 132, 1)&quot;,
        &quot;rgba(54, 162, 235, 1)&quot;,
        &quot;rgba(255, 206, 86, 1)&quot;,
        &quot;rgba(75, 192, 192, 1)&quot;,
        &quot;rgba(153, 102, 255, 1)&quot;,
        &quot;rgba(255, 159, 64, 1)&quot;
      ],
      &quot;borderWidth&quot;: 1
    }]
  },
  &quot;options&quot;: {
    &quot;scales&quot;: {
      &quot;y&quot;: {
        &quot;ticks&quot;: {
          &quot;beginAtZero&quot;: true,
          &quot;callback&quot;: &quot;function(value){ return value + 'k'; }&quot;
        }
      }
    }
  }
}
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="mermaid" tabindex="-1"><a class="header-anchor" href="#mermaid" aria-hidden="true">#</a> Mermaid</h3>
<div class="language-mermaidjs line-numbers-mode" data-ext="mermaidjs"><pre v-pre class="language-mermaidjs"><code>sequenceDiagram
  Alice-&gt;John: Hello John, how are you?
  loop Every minute
    John--&gt;Alice: Great!
  end
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="images" tabindex="-1"><a class="header-anchor" href="#images" aria-hidden="true">#</a> Images</h2>
<p><img src="/img/home-bg/3.jpg" alt="Image Example"></p>
<h2 id="maths" tabindex="-1"><a class="header-anchor" href="#maths" aria-hidden="true">#</a> Maths</h2>
<p>Inline math: $E = mc^2$</p>
<p>Display math:</p>
<p>$$
i\hbar\frac{\partial \psi}{\partial t} = \frac{-\hbar^2}{2m} ( \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} + \frac{\partial^2}{\partial z^2} ) \psi + V \psi.
$$</p>
<p>With tags:</p>
<p>$$
\begin{gather}
A = \text{softmax}(\frac{QK^T}{\sqrt{d_k}}) \
F_{\text{out}} = A V
\end{gather}
$$</p>
<h2 id="emojis" tabindex="-1"><a class="header-anchor" href="#emojis" aria-hidden="true">#</a> Emojis</h2>
<p>😄 😏 🐎 🐺</p>
<h2 id="containers" tabindex="-1"><a class="header-anchor" href="#containers" aria-hidden="true">#</a> Containers</h2>
<p>::: link {fa-github-alt} <a href="https://github.com/Renovamen/vuepress-theme-gungnir" target="_blank" rel="noopener noreferrer">vuepress-theme-gungnir<ExternalLinkIcon/></a>
A blog theme for VuePress 2.
:::</p>
<p>::: link {/img/links/me.png} <a href="https://blog.zxh.io" target="_blank" rel="noopener noreferrer">My Blog<ExternalLinkIcon/></a>
My blog 🧐, powered by VuePress 2, themed by Gungnir.
:::</p>
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
<details class="custom-container details"><summary>Show me the code group.</summary>
<CodeGroup>
<CodeGroupItem title="JS" active>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code>console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Hello World!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
<CodeGroupItem title="PY">
<div class="language-python line-numbers-mode" data-ext="py"><pre v-pre class="language-python"><code><span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Hello World!"</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></CodeGroupItem>
</CodeGroup>
</details>
<h2 id="references" tabindex="-1"><a class="header-anchor" href="#references" aria-hidden="true">#</a> References</h2>
<p>[^1]: Excerpted from: <em>A Brief History of Time</em>, written by Stephen Hawking.</p>
</div></template>


