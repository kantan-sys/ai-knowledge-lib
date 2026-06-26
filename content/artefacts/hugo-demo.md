---
title: "Hugo-Powered Slide Deck Demo"
type: docs
layout: "slide-deck"
bookHidden: false
slides:
  - content: |
      <div class="s1-row">
        <div>
          <div class="slide-label">Hugo + Design System</div>
          <h1>Slide Decks <span class="gradient-text">Powered by Hugo</span></h1>
        </div>
        <div class="slide-meta">AI Knowledge Library<br>Built with Hugo Extended</div>
      </div>
      <p class="subtitle" style="margin-bottom:6px;">
        This slide deck is rendered by Hugo using a custom <strong style="color:var(--color-accent-llm);">slide-deck</strong> layout.
        All CSS uses design tokens from <code>assets/css/design-tokens.css</code> — consistent colors,
        typography, and spacing across the entire AI Knowledge Library.
      </p>
      <div class="s1-toc">
        <div class="s1-toc-item"><div class="s1-toc-num">1</div><h4>Design System</h4><p>CSS custom properties for consistency</p></div>
        <div class="s1-toc-item"><div class="s1-toc-num">2</div><h4>Hugo Templates</h4><p>Slides defined in frontmatter</p></div>
        <div class="s1-toc-item"><div class="s1-toc-num">3</div><h4>Reusable Components</h4><p>Stats, cards, tables, code blocks</p></div>
        <div class="s1-toc-item"><div class="s1-toc-num">4</div><h4>Keyboard Nav</h4><p>Arrow keys, Home, End, Space</p></div>
        <div class="s1-toc-item"><div class="s1-toc-num">5</div><h4>Responsive</h4><p>Viewport-fit with clamp() scaling</p></div>
        <div class="s1-toc-item"><div class="s1-toc-num">6</div><h4>Hugo Book Theme</h4><p>Browseable documentation site</p></div>
      </div>
  - content: |
      <div class="dd-header">
        <div><div class="slide-label">Design System</div><h2>Design Tokens in Action</h2></div>
        <div class="slide-meta">All components use CSS custom properties</div>
      </div>
      <div class="dd-content">
        <div class="dd-left">
          <h4 style="color:var(--color-text-secondary);margin-bottom:6px;">Color Palette (from tokens)</h4>
          <div class="stat-grid">
            <div class="stat-card"><div class="stat-value accent">#060912</div><div class="stat-label">Primary background</div></div>
            <div class="stat-card"><div class="stat-value accent">#8b5cf6</div><div class="stat-label">Apps accent</div></div>
            <div class="stat-card"><div class="stat-value amber">#818cf8</div><div class="stat-label">LLM accent</div></div>
            <div class="stat-card"><div class="stat-value amber">#34d399</div><div class="stat-label">Success color</div></div>
          </div>
          <h4 style="color:var(--color-text-secondary);margin-bottom:6px;margin-top:10px;">Typography Scale (responsive clamping)</h4>
          <div class="code-block">
text-xs:   clamp(9px,  0.75vw, 10px)  — labels
text-sm:   clamp(10px, 0.85vw, 11px)  — metadata
text-base: clamp(11px, 1.05vw, 13px)  — body
text-md:   clamp(12px, 1.2vw,  14px)  — subtitles
text-lg:   clamp(14px, 1.5vw,  17px)  — h3
text-xl:   clamp(18px, 2.2vw,  26px)  — h2
text-2xl:  clamp(22px, 2.8vw,  36px)  — h1
          </div>
        </div>
        <div class="dd-right">
          <h4 style="color:var(--color-text-secondary);margin-bottom:6px;">Component Showcase</h4>
          <div class="do-dont">
            <div class="do-card">
              <h4>Do Card</h4>
              <ul><li>Uses success color tokens</li><li>Green theme for positive examples</li><li>Checkmark bullets</li></ul>
            </div>
            <div class="dont-card">
              <h4>Don't Card</h4>
              <ul><li>Uses error color tokens</li><li>Red theme for anti-patterns</li><li>X-mark bullets</li></ul>
            </div>
          </div>
          <div class="diagram-box">
            <h4>Diagram Box Component</h4>
            <p class="body-text">Semi-transparent backgrounds and borders from design tokens. Great for flow diagrams, architecture overviews, and process explanations.</p>
          </div>
          <div class="implication-box">
            <h4>Key Insight Box</h4>
            <p>Uses accent background and text tokens. Perfect for key insights and takeaways at the bottom of slides.</p>
          </div>
        </div>
      </div>
  - content: |
      <div class="dd-header">
        <div><div class="slide-label">Hugo Architecture</div><h2>How This Works</h2></div>
        <div class="slide-meta">Markdown frontmatter → Hugo → HTML slide deck</div>
      </div>
      <div class="dd-content">
        <div class="dd-left">
          <h4 style="color:var(--color-text-secondary);margin-bottom:6px;">The Build Pipeline</h4>
          <div class="flow-row">
            <div class="flow-step"><div class="step-name">Markdown</div><div class="step-desc">YAML frontmatter<br>+ HTML content</div></div>
            <span class="flow-arrow">→</span>
            <div class="flow-step"><div class="step-name">Hugo</div><div class="step-desc">Extended v0.163<br>processes templates</div></div>
            <span class="flow-arrow">→</span>
            <div class="flow-step"><div class="step-name">Layout</div><div class="step-desc">slide-deck.html<br>renders each slide</div></div>
            <span class="flow-arrow">→</span>
            <div class="flow-step"><div class="step-name">Output</div><div class="step-desc">Standalone HTML<br>keyboard navigable</div></div>
          </div>
          <h4 style="color:var(--color-text-secondary);margin-bottom:6px;margin-top:10px;">What Makes This Work</h4>
          <p class="body-text">Hugo's template engine loops through the <strong style="color:var(--color-accent-llm);">slides</strong> array in the frontmatter, wrapping each slide's content in the slide-deck layout. The same Markdown file renders as a normal documentation page in the Hugo Book theme — dual purpose from a single source file.</p>
        </div>
        <div class="dd-right">
          <h4 style="color:var(--color-text-secondary);margin-bottom:6px;">Key Benefits of Hugo + Design System</h4>
          <ul class="key-points">
            <li><strong>Separation of concerns.</strong> Content lives in Markdown frontmatter; presentation is handled by the Hugo layout template</li>
            <li><strong>Design tokens.</strong> Colors, fonts, spacing use CSS custom properties — change one variable, update everywhere</li>
            <li><strong>Consistency.</strong> Every slide deck shares the same layout, navigation, and design language</li>
            <li><strong>Dual purpose.</strong> Same content renders as slide deck OR browsable documentation via Hugo Book theme</li>
            <li><strong>No build tools.</strong> Hugo compiles to static HTML. Deploy anywhere, open in any browser</li>
            <li><strong>GitHub Pages ready.</strong> Add a GitHub Actions workflow for automatic deployment</li>
          </ul>
          <div class="implication-box">
            <h4>Key Insight</h4>
            <p>Hugo transforms the AI Knowledge Library from standalone HTML files into a structured, navigable documentation website — while preserving the self-contained slide deck experience. Content authors write Markdown; Hugo handles the rest.</p>
          </div>
        </div>
      </div>
---