---
layout: default
title: Chalk World
description: A shared canvas for you and the AI. An application platform for human–LLM collaboration.
---

<section class="hero">
  <div class="wrap">
    <span class="hero__eyebrow">Being built in public</span>
    <h1 class="hero__title">A shared canvas for you <em>and the AI</em>.</h1>
    <p class="hero__beat">A fresh take on visual collaboration with AI.</p>
    <p class="hero__lede">
      Chalk World is an application platform for human–LLM collaboration.
      The AI steps into a domain-expert role, picks up chalk, and reaches
      for the canvas when the conversation needs grounding. Modules are
      the proof points. The platform is what's underneath.
    </p>
    <div class="hero__cta">
      <a class="btn btn--primary" href="{{ '/blog/' | relative_url }}">Follow the build →</a>
      <a class="btn btn--ghost" href="#home-philosophy">What's the idea?</a>
    </div>
  </div>
</section>

<section class="block" id="home-philosophy">
  <div class="wrap">
    <p class="section-label">The idea</p>
    <h2 class="section-title">Chatbots give you text. Image models give you pictures. Chalk World gives you a place to think together.</h2>
    <div class="cols">
      <div class="col">
        <h3>AI as a collaborator at the canvas</h3>
        <p>
          Most AI tools make the model an oracle on the other side of a
          prompt. You type, it answers, you squint. Chalk World gives the
          AI a seat at the conversation — a reasoning partner that
          reaches for the canvas when words aren't enough.
        </p>
        <p>
          The unit of work isn't a message. It's the thing you're both
          looking at.
        </p>
        <p class="col__beat">Not a smarter pencil. Not an enterprise whiteboard. Chalk in the AI's hand, canvas between you.</p>
      </div>
      <div class="col">
        <h3>Why "chalk"?</h3>
        <p>
          Chalk is one of the oldest drawing mediums there is.
          Primitive — cave paintings, slate, a kid's sidewalk drawing.
          It represents the fundamentals of visual communication. And
          the AI has now been handed a piece of chalk for the first
          time.
        </p>
        <p>
          Chalk is ephemeral by nature, not just erasable. That's a
          feature, not a flaw. Chalk is for thinking in the moment; the
          persistence of what the thinking produced lives elsewhere —
          in the save format, the state, the record underneath the
          canvas.
        </p>
      </div>
    </div>
  </div>
</section>

<section class="pull-quote" aria-label="Quotation">
  <div class="wrap">
    <hr class="pull-quote__rule" aria-hidden="true">
    <blockquote>&ldquo;The canvas computes. The LLM interprets. The user guides.&rdquo;</blockquote>
    <hr class="pull-quote__rule" aria-hidden="true">
  </div>
</section>

<section class="block">
  <div class="wrap">
    <p class="section-label">What you can build on it</p>
    <h2 class="section-title">A platform, not a product.</h2>
    <p class="section-lede">
      CW is modular because the breakthrough is general: a human and an
      AI thinking together on a shared canvas works the same way
      whether the canvas is a yard, a game board, or a musical score.
      Modules are what specialize it for the work at hand. All of them
      share the same substrate underneath — the shared canvas, the
      model-as-collaborator stance, the save format, the plumbing. The
      modules prove the platform. The platform is the real project.
    </p>
    <div class="modules">
      <article class="module-card">
        <span class="module-card__tag">Semi-pro</span>
        <h3 class="module-card__name">Landscape</h3>
        <p class="module-card__desc">
          Plan your yard with the AI seeing the yard with you. Beds,
          paths, plant sightlines, sun exposure — all on the same page.
          Started here because text-and-a-plant-list isn't a landscape.
        </p>
      </article>
      <article class="module-card">
        <span class="module-card__tag">Semi-pro</span>
        <h3 class="module-card__name">TTRPG</h3>
        <p class="module-card__desc">
          A shared game surface for human and AI to GM, play, and build
          maps together. One canvas for the party, the model, and
          whatever the party is pointing at this round.
        </p>
      </article>
      <article class="module-card">
        <span class="module-card__tag">Semi-pro</span>
        <h3 class="module-card__name">Sheet Music</h3>
        <p class="module-card__desc">
          Compose, notate, and iterate on a single score. The model
          reads and writes the same notation you do. Not another "ask it
          to write a song" box.
        </p>
      </article>
      <article class="module-card">
        <span class="module-card__tag module-card__tag--show">Showcase</span>
        <h3 class="module-card__name">Describe-a-Game</h3>
        <p class="module-card__desc">
          Describe a board game in plain words. Chalk World builds you a
          playable version on the canvas. The module isn't the point —
          it's a demo of what the substrate underneath can do.
        </p>
      </article>
      <article class="module-card">
        <span class="module-card__tag module-card__tag--show">Showcase</span>
        <h3 class="module-card__name">More, as the build finds them</h3>
        <p class="module-card__desc">
          The platform is deliberately not a short list. If something
          reads well as "you and the AI on the same page" — a lesson
          plan, a renovation, a route, a schedule — it can live here.
        </p>
      </article>
      <article class="module-card" style="background: var(--bg-sunk); border-style: dashed;">
        <span class="module-card__tag" style="background: transparent; color: var(--ink-faint); padding-left: 0;">Status</span>
        <h3 class="module-card__name" style="color: var(--ink-muted);">In the workshop</h3>
        <p class="module-card__desc">
          None of the modules are shippable yet. This site exists so the
          build has a public home while that's still true. Read the blog
          to see what's actually working today.
        </p>
      </article>
    </div>
  </div>
</section>

<section class="block">
  <div class="wrap">
    <p class="section-label">Follow along</p>
    <h2 class="section-title">A running log of the build.</h2>
    <p class="section-lede">
      The blog is a chronicle, not a marketing channel. Engineering
      decisions, architectural trade-offs, the dead ends, the occasional
      essay about why any of this. If you want to see a platform get
      built in public, this is where.
    </p>
    <ul class="teaser-list">
      {% for post in site.posts limit: 5 %}
      <li>
        <a href="{{ post.url | relative_url }}">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
          <span class="teaser-list__title">{{ post.title }}</span>
        </a>
      </li>
      {% endfor %}
    </ul>
    <p class="block__see-all">
      <a href="{{ '/blog/' | relative_url }}">See all posts →</a>
    </p>
  </div>
</section>