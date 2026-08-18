# #100 About

<div class="about-og-preview" aria-hidden="true">
<img src="./100-about/dreaming-saints.png" alt="" width="96" height="96" />
</div>

<style>
.about-og-preview,
.about-og-preview a.post-image-link {
  display: none !important;
}
.about-hero {
  margin: 0 0 1.25rem;
}
.about-hero a.post-image-link {
  display: block !important;
  width: 100%;
  max-width: none !important;
  margin: 0 !important;
  padding: 0;
  line-height: 0;
  border: none !important;
  border-radius: 0 !important;
  background: none !important;
  box-shadow: none !important;
}
.about-hero img {
  display: block;
  width: 100% !important;
  height: auto !important;
  max-width: none !important;
  margin: 0 !important;
  border-radius: 5px !important;
  box-shadow: none !important;
  object-fit: cover;
}
.about-couple {
  position: relative;
  overflow: visible;
}
.about-couple > #stcost,
.about-couple > #sttaya {
  position: relative;
  overflow: visible;
}
.about-couple > #stcost::before,
.about-couple > #sttaya::before {
  content: "";
  position: absolute;
  top: 64px;
  left: 100%;
  width: 16px;
  height: 1px;
  background: var(--color-border);
  transition: background 0.15s ease;
  pointer-events: none;
  z-index: 1;
}
.about-couple > #stcost::after,
.about-couple > #sttaya::after {
  content: "";
  position: absolute;
  left: calc(100% + 15px);
  width: 1px;
  background: var(--color-border);
  transition: background 0.15s ease;
  pointer-events: none;
  z-index: 1;
}
.about-couple > #stcost::after {
  top: 64px;
  height: calc(100% - 64px + 1.25rem);
}
.about-couple > #sttaya::after {
  top: 0;
  height: 64px;
}
.about-engaged {
  position: relative;
  height: 0;
  margin: 0;
  line-height: 0;
  font-size: 0;
  z-index: 2;
  overflow: visible;
}
.about-engaged-gap {
  position: absolute;
  left: calc(100% + 16px);
  top: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 22px;
  height: 44px;
  transform: translate(calc(-50% - 2px), -50%);
  background: var(--color-bg-secondary);
}
.about-engaged svg {
  display: block;
  transform: rotate(90deg);
}
.about-engaged svg circle,
.about-engaged svg path {
  stroke: var(--color-border);
  transition: stroke 0.15s ease;
}
.about-couple:hover > #stcost::before,
.about-couple:hover > #stcost::after,
.about-couple:hover > #sttaya::before,
.about-couple:hover > #sttaya::after {
  background: var(--color-primary);
}
.about-couple:hover .about-engaged svg circle:first-of-type,
.about-couple:hover .about-engaged svg path {
  stroke: #ff8000;
}
.about-couple:hover .about-engaged svg circle:nth-of-type(2) {
  stroke: #0abab5;
}
.about-person { overflow: visible; }
.about-person > summary {
  display: flex;
  align-items: center;
  gap: 8px;
  font-weight: 400;
  overflow: visible;
  position: relative;
  z-index: 3;
  list-style: none;
  cursor: pointer;
}
.about-person > summary::-webkit-details-marker { display: none; }
.about-person > summary::marker { content: ""; }
.about-person > summary::before {
  content: "▸";
  flex-shrink: 0;
  width: 1em;
  color: var(--color-primary);
  font-size: 0.95em;
  line-height: 1;
}
.about-person[open] > summary::before { content: "▾"; }
.about-person[open] > summary {
  border-bottom: 1px solid #30363d;
  border-radius: 6px 6px 0 0;
  margin-bottom: 0.75rem;
}
.about-person > :not(summary) {
  box-sizing: border-box;
  max-width: calc(100% - 1.5rem);
}

.about-head {
  display: flex;
  align-items: stretch;
  flex-wrap: wrap;
  gap: 12px;
  min-width: 0;
  flex: 1 1 auto;
  padding: 4px 0;
}
.about-avatar-link,
.about-avatar-wrap {
  display: block;
  flex-shrink: 0;
  cursor: pointer;
}
.about-avatar-link {
  line-height: 0;
  text-decoration: none;
  color: inherit;
}
.about-avatar-wrap {
  position: relative;
  width: 96px;
  height: 96px;
  margin: 8px;
}
/* Live engine wraps each img in a.post-image-link; pin those links or they stack into other cards. */
.about-avatar-wrap > a {
  position: absolute;
  inset: 0;
  display: block !important;
  max-width: none !important;
  margin: 0 !important;
  padding: 0;
  line-height: 0;
  border: none !important;
  border-radius: 0 !important;
  background: none !important;
  box-shadow: none !important;
}
.about-avatar-wrap > a:last-child {
  z-index: 1;
  pointer-events: none;
}
.about-avatar-wrap img {
  display: block;
  position: absolute;
  margin: 0 !important;
  border-radius: 0 !important;
  box-shadow: none !important;
  background: none !important;
  max-width: none !important;
}
.about-avatar-wrap img[src*="avatars."] {
  inset: 2px;
  width: calc(100% - 4px) !important;
  height: calc(100% - 4px) !important;
  object-fit: cover;
}
.about-avatar-wrap img[src*="community_assets"] {
  inset: 0;
  width: 100% !important;
  height: 100% !important;
  object-fit: fill;
  transform: scale(1.22);
  z-index: 1;
  pointer-events: none;
}
.about-id { min-width: 0; flex: 0 0 auto; }
.about-name {
  display: block;
  margin: 0;
  font-size: 1.5em;
  font-weight: 700;
  line-height: 1.2;
  color: var(--color-primary);
}
.about-name a { color: inherit; text-decoration: none; }
.about-name a:hover { text-decoration: underline; }
.about-roles {
  margin: 0.3rem 0 0;
  padding-left: 1.2em;
  font-size: 0.85em;
  font-weight: 400;
  line-height: 1.35;
  color: #8b949e;
  list-style: disc;
}
.about-roles li { margin: 0; }
.about-head-split {
  align-self: stretch;
  width: 1px;
  margin: 4px 0;
  background: #30363d;
  flex-shrink: 0;
}

.about-tops {
  position: relative;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 6px;
  min-width: 0;
  flex: 1 1 auto;
  align-content: stretch;
  align-items: stretch;
  margin: calc(-0.5rem - 4px) -0.75rem calc(-0.5rem - 4px) -12px;
}
.about-tops::before,
.about-tops::after {
  content: "";
  position: absolute;
  pointer-events: none;
  background: #30363d;
  opacity: 0.85;
  z-index: 3;
}
.about-tops::before {
  top: 6%;
  bottom: 6%;
  left: 50%;
  width: 1px;
  transform: translateX(-50%);
}
.about-tops::after {
  left: 6%;
  right: 6%;
  top: 50%;
  height: 1px;
  transform: translateY(-50%);
}
.about-tops > .fav-chip {
  position: relative;
  display: block;
  width: 100%;
  height: 100%;
  min-width: 0;
  min-height: 0;
  padding: 0;
  overflow: visible;
  border: none;
  box-shadow: none;
}
.about-tops > .fav-chip:hover,
.about-tops > .fav-chip.tip-open {
  z-index: 80;
  border: none;
  box-shadow: none;
  text-decoration: none;
}
.about-tops > .fav-chip img {
  position: absolute;
  inset: 0;
  width: 100% !important;
  height: 100% !important;
  object-fit: cover;
  object-position: 50% 0%;
  margin: 0 !important;
  border-radius: 0 !important;
  box-shadow: none !important;
  background: #161b22;
}
.about-tops > .fav-chip:nth-child(4) img {
  object-fit: contain;
  object-position: 50% 50%;
  padding: 6px;
  box-sizing: border-box;
}
@keyframes about-tops-scroll {
  from { object-position: 50% 0%; }
  to { object-position: 50% 100%; }
}
.about-tops > .fav-chip:hover img,
.about-tops > .fav-chip:focus-visible img {
  animation: about-tops-scroll 14s linear infinite alternate;
}
.about-tops > .fav-chip:nth-child(4):hover img,
.about-tops > .fav-chip:nth-child(4):focus-visible img {
  animation: none;
}

@media (max-width: 720px) {
  .about-head-split {
    display: none;
  }
  .about-tops {
    flex: 1 1 100%;
    width: 100%;
    min-height: 120px;
    margin: 8px 0 0;
  }
  .about-tops::before,
  .about-tops::after {
    display: none;
  }
}

.about-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
  margin: 0 0 1rem;
  min-width: 0;
}
.about-row.about-meta {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
}
.about-row.about-meta > .about-section {
  flex: 1 1 auto;
  min-width: 0;
}
.about-row .about-section { margin: 0; }
.about-section {
  margin: 0 0 1rem;
  min-width: 0;
  overflow: visible;
}
.about-note .about-tip-trigger {
  z-index: 1;
}
.about-note .about-tip-trigger:hover,
.about-note .about-tip-trigger.tip-open,
.about-studio .about-tip-trigger:hover,
.about-studio .about-tip-trigger.tip-open {
  z-index: 40;
}
.about-section-label {
  display: flex;
  align-items: flex-end;
  gap: 8px;
  font-size: 0.75em;
  font-weight: 600;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: var(--color-primary);
  margin: 0 0 8px;
}
.about-section-label::after {
  content: "";
  flex: 1 1 auto;
  border-bottom: 1px solid #30363d;
  margin-bottom: 0.15em;
}
.about-note {
  margin: 0;
  font-size: 0.85em;
  color: #8b949e;
}
.about-section > .about-note + .about-note,
.about-section > .about-note + .fav-row {
  margin-top: 8px;
}
.about-note a.about-anchor {
  color: var(--color-primary);
  font-style: normal;
  text-decoration: none;
}
.about-note a.about-anchor:hover {
  color: var(--color-primary-hover);
  text-decoration: underline;
}

.fav-chip {
  color: inherit;
  text-decoration: none;
  border: 1px solid #30363d;
  border-radius: 4px;
  line-height: 1.2;
  font-size: 0.8em;
}
.fav-chip.about-tip-trigger {
  color: inherit;
  font-style: normal;
  text-decoration: none;
  cursor: pointer;
  z-index: 1;
}
.fav-chip.about-tip-trigger:hover,
.fav-chip.about-tip-trigger.tip-open {
  color: var(--color-primary-hover);
  border-color: var(--color-primary);
  z-index: 80;
}
.about-section:has(.about-tip-trigger:hover),
.about-section:has(.about-tip-trigger.tip-open),
.about-tops:has(.about-tip-trigger:hover),
.about-tops:has(.about-tip-trigger.tip-open) {
  position: relative;
  z-index: 60;
}
.fav-colors > .fav-chip.about-tip-trigger {
  color: inherit;
}

.fav-row {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
  grid-template-rows: masonry;
  grid-auto-flow: dense;
  gap: 6px;
  margin: 0;
  align-items: start;
  min-width: 0;
  max-width: 100%;
  overflow: visible;
  isolation: auto;
}
@supports not (grid-template-rows: masonry) {
  .fav-row {
    display: block;
    column-width: 108px;
    column-gap: 6px;
  }
  .fav-row > .fav-chip {
    width: 100%;
    margin: 0 0 6px;
    break-inside: avoid;
  }
}
.fav-row > .fav-chip {
  position: relative;
  display: block;
  padding: 0;
  overflow: visible;
  min-width: 0;
  max-width: 100%;
  height: fit-content;
}
.fav-row > .fav-chip > .about-tip,
.about-tops > .fav-chip > .about-tip,
.fav-colors > .fav-chip > .about-tip {
  position: absolute;
  left: 0;
  top: calc(100% + 6px);
}
.fav-row > .fav-chip:has(img[src*="/capsule_"]),
.fav-row > .fav-chip:has(img[src*="/header.jpg"]),
.fav-row > .fav-chip:has(img[src*="img.youtube.com"]) {
  grid-column: span 2;
}
.fav-row > .fav-chip img {
  display: block;
  width: 100% !important;
  height: auto !important;
  max-width: 100%;
  margin: 0 !important;
  border-radius: 0 !important;
  box-shadow: none !important;
  object-fit: cover;
  background: #161b22;
}
.fav-row > .fav-chip:has(img[src*="img.youtube.com"]) img {
  height: auto !important;
  object-fit: contain;
  object-position: center;
}
.fav-compact {
  grid-template-columns: repeat(auto-fill, minmax(50px, 1fr));
}
@supports not (grid-template-rows: masonry) {
  .fav-compact { column-width: 54px; }
}
.fav-compact > .fav-chip:has(img[src*="/capsule_"]),
.fav-compact > .fav-chip:has(img[src*="/header.jpg"]),
.fav-compact > .fav-chip:has(img[src*="img.youtube.com"]) {
  grid-column: span 1;
}
.about-meta .fav-compact {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}
.about-meta .fav-compact > .fav-chip {
  width: 50px;
  min-width: 50px;
  aspect-ratio: 1;
  margin: 0;
}
.about-meta .fav-compact > .fav-chip img {
  width: 100% !important;
  height: 100% !important;
  object-fit: contain;
  padding: 8px;
  box-sizing: border-box;
}

.fav-row > .fav-chip > span:not(.about-tip),
.about-tops > .fav-chip > span:not(.about-tip) {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 2;
  padding: 4px 5px 5px;
  font-size: 0.72em;
  text-align: center;
  white-space: normal;
  overflow-wrap: break-word;
  word-break: break-word;
  line-height: 1.15;
  overflow: hidden;
  text-shadow: 0 0 4px #000, 0 0 8px #000, 0 1px 2px #000;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.12s ease;
}
.fav-compact > .fav-chip > span:not(.about-tip) {
  font-size: 0.62em;
  padding: 3px;
}
.fav-row > .fav-chip:hover > span:not(.about-tip),
.fav-row > .fav-chip:focus-visible > span:not(.about-tip),
.about-tops > .fav-chip:hover > span:not(.about-tip),
.about-tops > .fav-chip:focus-visible > span:not(.about-tip) {
  opacity: 1;
}
.fav-row > .fav-chip:hover { text-decoration: none; }
.fav-row > .fav-chip:hover > span:not(.about-tip),
.about-tops > .fav-chip:hover > span:not(.about-tip) { text-decoration: underline; }

.fav-row > .fav-chip:first-child {
  border-color: rgba(212, 175, 55, 0.55);
  box-shadow: 0 0 18px 8px rgba(212, 175, 55, 0.22);
}
.fav-row > .fav-chip:first-child:hover,
.fav-row > .fav-chip:first-child.tip-open {
  border-color: rgba(240, 208, 96, 0.7);
  box-shadow: 0 0 22px 10px rgba(240, 208, 96, 0.28);
}
.about-meta .fav-row > .fav-chip:first-child {
  border-color: #30363d;
  box-shadow: none;
}
.about-meta .fav-row > .fav-chip:first-child:hover,
.about-meta .fav-row > .fav-chip:first-child.tip-open {
  border-color: var(--color-primary);
  box-shadow: none;
}

.fav-colors {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 6px;
  margin: 0.4rem 0 0;
}
.fav-colors > .fav-chip {
  position: relative;
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 3px 8px 3px 4px;
  max-width: 100%;
  overflow: visible;
}
.fav-swatch {
  display: inline-block;
  width: 16px;
  height: 16px;
  border-radius: 3px;
  flex-shrink: 0;
  border: 1px solid #30363d;
}
.fav-swatch.orange { background: #ff8000; }
.fav-swatch.black { background: #111; }
.fav-swatch.tiffany { background: #0abab5; }
.fav-swatch.purple { background: #800080; }
.fav-swatch.ultramarine { background: #120A8F; }
.about-studio {
  position: relative;
  overflow: visible;
  margin: 0 0 1.25rem;
  font-size: 0.95em;
  line-height: 1.5;
}
.about-studio a.about-tip-title {
  position: relative;
}
.about-tip-trigger {
  position: relative;
  color: var(--color-primary);
  font-style: italic;
  text-decoration: underline dashed;
  text-decoration-color: var(--color-primary);
  text-underline-offset: 0.2em;
  text-decoration-thickness: 1px;
  cursor: help;
}
.about-tip-trigger:hover {
  color: var(--color-primary-hover);
  text-decoration-color: var(--color-primary-hover);
}
.about-tip {
  display: none;
  position: absolute;
  left: 0;
  top: calc(100% + 6px);
  z-index: 10000;
  width: min(272px, calc(100vw - 16px));
  margin: 0;
  pointer-events: auto;
  background: var(--color-bg-secondary, #161b22);
  border: 1px solid #30363d;
  border-radius: 6px;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.45);
  overflow: hidden;
  color: #c9d1d9;
  font-weight: 400;
  font-style: normal;
  letter-spacing: normal;
  line-height: 1.35;
  text-align: left;
  text-decoration: none;
  text-transform: none;
  white-space: normal;
}
.about-tip.is-open,
.about-tip-trigger:hover > .about-tip,
.about-tip-trigger.tip-open > .about-tip {
  display: block;
  color: #c9d1d9;
  text-decoration: none;
}
.about-tip-art {
  display: block;
  width: 100%;
  aspect-ratio: 460 / 215;
  background: #0d1117 center / cover no-repeat;
}
.fav-compact .about-tip-art,
.about-tops > .fav-chip:nth-child(4) .about-tip-art {
  background-size: 64px;
  background-repeat: no-repeat;
  aspect-ratio: 2 / 1;
}
.about-tip-body {
  display: block;
  padding: 8px 10px 10px;
}
a.about-tip-title {
  display: inline;
  font-size: 0.95em;
  font-weight: 600;
  color: var(--color-primary);
  cursor: pointer;
  text-decoration: none;
}
a.about-tip-title:hover {
  color: var(--color-primary-hover);
  text-decoration: underline;
}
.about-tip-date {
  display: inline;
  margin: 0 0 0 6px;
  font-size: 0.75em;
  font-weight: 400;
  color: #6e7681;
}
.about-tip-desc {
  display: block;
  margin-top: 6px;
  font-size: 0.8em;
  color: #8b949e;
}
.about-tip-note {
  display: block;
  margin-top: 8px;
  font-size: 0.75em;
  font-style: italic;
  color: #8b949e;
}
.about-tip-said {
  display: flex;
  align-items: flex-end;
  gap: 8px;
  margin: 0 0 6px;
  font-style: normal;
  font-weight: 600;
  color: #6e7681;
}
.about-tip-said::after {
  content: "";
  flex: 1 1 auto;
  border-bottom: 1px solid #30363d;
  margin-bottom: 0.2em;
}
.about-studio small,
.about-note small {
  font-size: 0.8em;
  color: #6e7681;
  font-weight: 400;
}
.about-team-header {
  display: flex;
  align-items: flex-end;
  gap: 8px;
  font-size: 0.85em;
  font-weight: 600;
  color: var(--color-primary);
  margin: 0 0 8px;
}
.about-team-header::after {
  content: "";
  flex: 1 1 auto;
  border-bottom: 1px solid #30363d;
  margin-bottom: 0.15em;
}
</style>

<div class="about-hero">
<img src="./100-about/studio-name.png" alt="Dreaming Saints" width="724" height="155" />
</div>

<p class="about-studio">Inspired by <span class="about-tip-trigger">BONEWORKS<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/823500/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/823500/">BONEWORKS</a><span class="about-tip-date">10 Dec 2019</span><span class="about-tip-desc">BONEWORKS is an Experimental Physics VR Adventure. Use found physics weapons, tools, and objects to fight across dangerous playscapes and mysterious architecture.</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Best VR adventure I experienced. Physical climbing is fun, feels like cheating. Many paths to approach problems. I love entering a room, pushing doors open using gun barrels and then blasting the null bodies. Still the best VR game for me.</span></span></span></span> and VR tech, we gathered a team to make <span class="about-tip-trigger">RISING BONEvR<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/1775350/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/1775350/RISING_BONEvR/">RISING BONEvR</a><span class="about-tip-date">demo 7 Nov 2021</span><span class="about-tip-desc">(First level demo available!) Physics based puzzle about climbing out of deep hell without any legs</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Quite a challenge to implement VR physics similar to BONEWORKS. Learned more math, vectors, matrices. Level design is terrible, physics clunky, but gameplay was fun when it works. My first proper C# game, and fiancee StTaya helped by making her first 3D models in Blender. Some day we'll continue - we learned many new lessons since then.</span></span></span></span> <small>(demo 7 Nov 2021)</small>. Now focused on our dream-game <span class="about-tip-trigger">COLLAPSE MACHINE<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/2980830/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/2980830/COLLAPSE_MACHINE">COLLAPSE MACHINE</a><span class="about-tip-date">since Sep 2023</span><span class="about-tip-desc">In COLLAPSE MACHINE - scavenge, raid, and survive a super-magnetic wasteland in co-op PvE. Hoard tesla-punk tech, mine voxel terrain, run a mobile vehicle base through shifting seasons, intercept rivals, and siege their factories</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Initial idea was to freely walk in co-op inside the vehicle cargo hangar, while a friend drives the car over desert dunes. Solved it by hiding static colliders, while visuals render near the car. The camera sees real movement, while physics of internal objects stays stable.</span></span></span></span> <small>(since Sep 2023)</small>. Quick side-projects: <span class="about-tip-trigger">Whomers Ate My Lawn!<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/3600250/69ff0311912878d48a0a7cb7523639b51370982b/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/3600250/Whomers_Ate_My_Lawn/">Whomers Ate My Lawn!</a><span class="about-tip-date">released 6 Apr 2025</span><span class="about-tip-desc">Dive into a simple yet charming world where curious Whomers creatures dig, eat, and survive in a compact 64x64 grid. This minimalistic simulation offers a peaceful experience of watching and interacting with small digital beings as they go about their lives</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Inspired by RimWorld, I wanted my own small semi-afk villager-manager. Made small creatures digging the lawn. You as God restore or dig more grass. Grow plants for more carrots. All to grow the population of Whomers. Made in 1 month with MonoGame in C#.</span></span></span></span> <small>(released 6 Apr 2025)</small> and <span class="about-tip-trigger">Ball-Aqua<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/4967660/b2762559bd37c68c7df2cc04f47b19fb3be7d7ef/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/4967660/">Ball-Aqua</a><span class="about-tip-date">demo 20 Aug 2026</span><span class="about-tip-desc">Demo Launch on August 20! Roll a physics ball through tropical obstacle courses. Beat the timer, collect bubbles and stars, and chase 100% clears. Play Freeroam solo or co-op, compete in Race, build levels, and share on Steam Workshop.</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>I've seen many ball-rolling games recently. But all of them had terrible movement and platforms - just thin beams. I wanted to speed and jump forward, not short hops on thin platforms. That day I stumbled on the Frutiger Aero water album Alezya - Dream Island (youtube.com/watch?v=3R6beuJQkxM). Such hydrated music inspired me to make a water-themed ball-rolling multiplayer with a level editor and freedom. Spent about a month on a playable version to show as a demo. A few more months to polish and make more levels for the full release.</span></span></span></span> <small>(demo 20 Aug 2026)</small>.</p>

<div class="about-team-header">Meet the team and what we like</div>
<div class="about-couple">
<details class="about-person" id="stcost">
<summary><span class="about-head"><span class="about-avatar-link"><span class="about-avatar-wrap"><img src="https://avatars.fastly.steamstatic.com/bce10ec46b619fd7a8660cc783d36462d44aa89e_full.jpg" alt="StCost" width="96" height="96" /><img src="https://shared.fastly.steamstatic.com/community_assets/images/items/1239690/f0af6694686ebf42992824a3ee5f6313fc00cd7c.png" alt=" " width="96" height="96" /></span></span><span class="about-id"><h2 class="about-name"><a class="about-anchor" href="#stcost">StCost</a></h2><ul class="about-roles"><li>Team Lead</li><li>Software Engineer</li><li>Game Designer</li></ul></span><span class="about-head-split"></span><span class="about-tops"><span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/823500/capsule_184x69.jpg" alt="BONEWORKS" width="28" height="28" /><span>BONEWORKS</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/823500/header.jpg?t=1581381377')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/823500/">BONEWORKS</a><span class="about-tip-date">10 Dec, 2019</span><span class="about-tip-desc">BONEWORKS is an Experimental Physics VR Adventure. Use found physics weapons, tools, and objects to fight across dangerous playscapes and mysterious architecture.</span></span></span></span><span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/nbogUmJkeBI/mqdefault.jpg" alt="2 Mello - I Wanna Kno" width="28" height="28" /><span>2 Mello - I Wanna Kno</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/nbogUmJkeBI/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.youtube.com/watch?v=nbogUmJkeBI">2 Mello - I Wanna Kno</a><span class="about-tip-desc">2 Mello - I Wanna Kno from Sounds of Tokyo-To Future (2021).</span></span></span></span><span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/The_Venture_Bros_logo.svg/250px-The_Venture_Bros_logo.svg.png" alt="The Venture Bros." width="28" height="28" /><span>The Venture Bros.</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/The_Venture_Bros_logo.svg/250px-The_Venture_Bros_logo.svg.png?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Venture_Bros.">The Venture Bros.</a><span class="about-tip-desc">The Venture Bros. is an American adult animated action-adventure television series created by Jackson Publick and Doc Hammer for Cartoon Network's late night programming block Adult Swim. Following a pilot episode on February 16, 2003, the series premiered on August 7, 2004. The Venture Bros.</span></span></span></span><span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/unity/FFFFFF" alt="Unity" width="28" height="28" /><span>Unity</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/unity/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://unity.com/">Unity</a><span class="about-tip-desc">Real-time 3D engine used to make the studio games.</span></span></span></span></span></span></summary>
<div class="about-row">
<div class="about-section">
<div class="about-section-label">About</div>
<p class="about-note">2011: got own PC, was <span class="about-tip-trigger">TF2<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/440/header.jpg?t=1757348372')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/440/">TF2</a><span class="about-tip-date">10 Oct, 2007</span><span class="about-tip-desc">Nine distinct classes provide a broad range of tactical abilities and personalities. Constantly updated with new game modes, maps, equipment and, most importantly, hats!</span></span></span></span> and <span class="about-tip-trigger">Minecraft<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.minecraft.net/content/dam/minecraftnet/franchise/logos/minecraft-creeper-face.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.minecraft.net/">Minecraft</a><span class="about-tip-desc">Minecraft is a sandbox where you build, explore, and survive in blocky worlds.</span></span></span></span> server admin. 2016: first games - C++ terminal at university (<span class="about-tip-trigger">see 34<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/2980830/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://dreamingsaints.github.io/blog/34-collapse-machine-stages/">see 34</a><span class="about-tip-desc">Post 34: stages of making COLLAPSE MACHINE, from first C++ terminal games onward.</span></span></span></span>). Developed <span class="about-tip-trigger">FiveM<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/5/5a/FiveM-Logo.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://fivem.net/">FiveM</a><span class="about-tip-desc">FiveM is a GTA V multiplayer modification framework for custom servers.</span></span></span></span> themed Max-Max survival role-play server 32/32. Spent too much time in <span class="about-tip-trigger">TF2<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/440/header.jpg?t=1757348372')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/440/">TF2</a><span class="about-tip-date">10 Oct, 2007</span><span class="about-tip-desc">Nine distinct classes provide a broad range of tactical abilities and personalities. Constantly updated with new game modes, maps, equipment and, most importantly, hats!</span></span></span></span>. Hobbies: skateboarding, FPV piloting.</p>
</div>
<div class="about-section">
<div class="about-section-label">Likes</div>
<p class="about-note"><a class="about-anchor" href="#sttaya">StTaya</a>, <span class="about-tip-trigger">Pepsi<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/thumb/6/68/Pepsi_2023.svg/320px-Pepsi_2023.svg.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.pepsi.com/">Pepsi</a><span class="about-tip-desc">Pepsi is a cola soft drink.</span></span></span></span>, <span class="about-tip-trigger">Nutella<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/thumb/d/d3/Nutella_logo.svg/320px-Nutella_logo.svg.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.nutella.com/">Nutella</a><span class="about-tip-desc">Nutella is a sweet hazelnut cocoa spread.</span></span></span></span>, buns, <span class="about-tip-trigger">Earl Grey tea<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Frisch_aufgebr%C3%BChter_EarlGrey_Tee.jpg/3840px-Frisch_aufgebr%C3%BChter_EarlGrey_Tee.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Earl_Grey_tea">Earl Grey tea</a><span class="about-tip-desc">Earl Grey tea is a tea blend which has been flavoured with oil of bergamot. The rind's fragrant oil is added to black tea to give Earl Grey its unique taste. However, many, if not most, Earl Greys use other natural or artificial flavours or synthetic oils instead as this is cheaper and results in a longer shelf-life.</span></span></span></span>, chips, beefsteak, strawberries.</p>
<div class="fav-colors">
<span class="fav-chip about-tip-trigger"><span class="fav-swatch orange"></span><span>Perfect Orange (#ff8000)</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/2980830/0b01155737650eba424b929432cb0b73401a7fdc/header.jpg?t=1777318206')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/2980830/COLLAPSE_MACHINE">COLLAPSE MACHINE</a><span class="about-tip-desc">In COLLAPSE MACHINE - scavenge, raid, and survive a super-magnetic wasteland in co-op PvE. Hoard tesla-punk tech, mine voxel terrain, run a mobile vehicle base through shifting seasons, intercept rivals, and siege their factories</span></span></span></span>
</div>
</div>
</div>
<div class="about-row about-meta">
<div class="about-section">
<div class="about-section-label">Media</div>
<p class="fav-row fav-compact">
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/discord/5865F2" alt="Discord" width="28" height="28" /><span>Discord</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/discord/5865F2')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://discord.com/invite/xQwWSFDC8Y">Discord</a><span class="about-tip-desc">Dreaming Saints Discord - studio chat and playtests.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="Steam" width="28" height="28" /><span>Steam</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/steam/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://steamcommunity.com/id/StCost">Steam</a><span class="about-tip-desc">StCost on Steam.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/gmail/EA4335" alt="Email" width="28" height="28" /><span>Email</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/gmail/EA4335')"></span><span class="about-tip-body"><a class="about-tip-title" href="mailto:dreamingsaints@gmail.com">Email</a><span class="about-tip-desc">Studio email: dreamingsaints@gmail.com</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="Dreaming Saints" width="28" height="28" /><span>Dreaming Saints</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/2980830/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/search/?developer=Dreaming%20Saints">Dreaming Saints</a><span class="about-tip-desc">Dreaming Saints games on Steam.</span></span></span></span>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Tools</div>
<p class="fav-row fav-compact">
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/unity/FFFFFF" alt="Unity" width="28" height="28" /><span>Unity</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/unity/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://unity.com/">Unity</a><span class="about-tip-desc">Real-time 3D engine used to make the studio games.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/blender/E87D0D" alt="Blender" width="28" height="28" /><span>Blender</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/blender/E87D0D')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.blender.org/">Blender</a><span class="about-tip-desc">Free 3D modeling, animation, and rendering suite.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/cursor/FFFFFF" alt="Cursor" width="28" height="28" /><span>Cursor</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/cursor/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://cursor.com/">Cursor</a><span class="about-tip-desc">AI code editor used to write and ship the games and this site.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/googlechrome/4285F4" alt="Google Chrome" width="28" height="28" /><span>Google Chrome</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/googlechrome/4285F4')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.google.com/chrome/">Google Chrome</a><span class="about-tip-desc">Google Chrome web browser.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/discord/5865F2" alt="Discord" width="28" height="28" /><span>Discord</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/discord/5865F2')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://discord.com/">Discord</a><span class="about-tip-desc">Voice, video, and text chat for communities and teams.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/teamspeak/2580C3" alt="TeamSpeak" width="28" height="28" /><span>TeamSpeak</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/teamspeak/2580C3')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.teamspeak.com/">TeamSpeak</a><span class="about-tip-desc">Low-latency voice chat client.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://www.getpaint.net/favicon.ico" alt="Paint.NET" width="28" height="28" /><span>Paint.NET</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.getpaint.net/favicon.ico')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.getpaint.net/">Paint.NET</a><span class="about-tip-desc">Windows image editor for 2D art and textures.</span></span></span></span>
</p>
</div>
</div>
<div class="about-section">
<div class="about-section-label">Games</div>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/823500/capsule_184x69.jpg" alt="BONEWORKS" width="28" height="28" /><span>BONEWORKS</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/823500/header.jpg?t=1581381377')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/823500/">BONEWORKS</a><span class="about-tip-date">10 Dec, 2019</span><span class="about-tip-desc">BONEWORKS is an Experimental Physics VR Adventure. Use found physics weapons, tools, and objects to fight across dangerous playscapes and mysterious architecture.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/22380/capsule_184x69.jpg" alt="Fallout New Vegas" width="28" height="28" /><span>Fallout: New Vegas</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/22380/header.jpg?t=1765992876')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/22380/">Fallout: New Vegas</a><span class="about-tip-date">21 Oct, 2010</span><span class="about-tip-desc">Welcome to Vegas. New Vegas. Enjoy your stay!</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/22350/capsule_184x69.jpg" alt="Brink" width="28" height="28" /><span>Brink</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/22350/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/22350/">Brink</a><span class="about-tip-date">10 May, 2011</span><span class="about-tip-desc">A first-person shooter with parkour movement. Fight for security or resistance on the floating city of The Ark.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/2000770/capsule_184x69.jpg" alt="Ballance" width="28" height="28" /><span>Ballance</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/2000770/header.jpg?t=1704463128')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/2000770/">Ballance</a><span class="about-tip-date">5 Jan, 2024</span><span class="about-tip-desc">In this 2004 classic originally released by Atari games, you will navigate 12 sky-high courses. Each course is fraught with different obstacles that will block your path, slide your marble off course, or blow them right into the bottomless void below.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/3124230/header.jpg" alt="Jackal" width="28" height="28" /><span>Jackal</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/3124230/953b10dcee407cbb6671efd94d889a63b3746eb7/header.jpg?t=1770321213')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/3124230/">Jackal</a><span class="about-tip-date">5 Feb, 2026</span><span class="about-tip-desc">Execute ultra-violent raids in 1970s casino hotels. Take down the Las Vegas mob as a drug super-powered hitman in physics-fueled top-down close combat</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/223470/capsule_184x69.jpg" alt="POSTAL 2" width="28" height="28" /><span>POSTAL 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/223470/header.jpg?t=1782946265')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/223470/">POSTAL 2</a><span class="about-tip-date">2 Nov, 2012</span><span class="about-tip-desc">Live a week in the life of "The POSTAL Dude"; a hapless everyman just trying to check off some chores. Buying milk, returning an overdue library book, getting Gary Coleman's autograph, what could possibly go wrong?</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/620/capsule_184x69.jpg" alt="Portal 2" width="28" height="28" /><span>Portal 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/620/header.jpg?t=1745363004')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/620/">Portal 2</a><span class="about-tip-date">18 Apr, 2011</span><span class="about-tip-desc">The "Perpetual Testing Initiative" has been expanded to allow you to design co-op puzzles for you and your friends!</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1353230/capsule_184x69.jpg" alt="Bomb Rush Cyberfunk" width="28" height="28" /><span>Bomb Rush Cyberfunk</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/1353230/header.jpg?t=1785851738')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/1353230/">Bomb Rush Cyberfunk</a><span class="about-tip-date">18 Aug, 2023</span><span class="about-tip-desc">Bomb Rush Cyberfunk is 1 second per second of advanced funkstyle. Battle rival crews and dispatch militarized police to conquer the five boroughs of New Amsterdam. Become All City.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/632360/capsule_184x69.jpg" alt="Risk of Rain 2" width="28" height="28" /><span>Risk of Rain 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/632360/header.jpg?t=1783621122')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/632360/">Risk of Rain 2</a><span class="about-tip-date">11 Aug, 2020</span><span class="about-tip-desc">Escape a chaotic alien planet by fighting through hordes of frenzied monsters – with your friends, or on your own. Combine loot in surprising ways and master each character until you become the havoc you feared upon your first crash landing.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/294100/capsule_184x69.jpg" alt="RimWorld" width="28" height="28" /><span>RimWorld</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/294100/76e0613b8197327299d5dbabb0a7fd7828a689a2/header.jpg?t=1782756789')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/294100/">RimWorld</a><span class="about-tip-date">17 Oct, 2018</span><span class="about-tip-desc">A sci-fi colony sim driven by an intelligent AI storyteller. Generates stories by simulating psychology, ecology, gunplay, melee combat, climate, biomes, diplomacy, interpersonal relationships, art, medicine, trade, and more.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/427520/capsule_184x69.jpg" alt="Factorio" width="28" height="28" /><span>Factorio</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/427520/header.jpg?t=1763986204')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/427520/">Factorio</a><span class="about-tip-date">14 Aug, 2020</span><span class="about-tip-desc">Factorio is a game about building and creating automated factories to produce items of increasing complexity, within an infinite 2D world. Use your imagination to design your factory, combine simple elements into ingenious structures, and finally protect it from the creatures who don't really like you.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/892970/capsule_184x69.jpg" alt="Valheim" width="28" height="28" /><span>Valheim</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/892970/de0bdcf6c008c508a79d8e75eb91fc67f4bebd5d/header.jpg?t=1786012504')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/892970/">Valheim</a><span class="about-tip-date">2 Feb, 2021</span><span class="about-tip-desc">A brutal exploration and survival game for 1-10 players, set in a procedurally-generated purgatory inspired by viking culture. Battle, build, and conquer your way to a saga worthy of Odin’s patronage!</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/70/capsule_184x69.jpg" alt="Half-Life" width="28" height="28" /><span>Half-Life</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/70/header.jpg?t=1745368462')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/70/">Half-Life</a><span class="about-tip-date">19 Nov, 1998</span><span class="about-tip-desc">Named Game of the Year by over 50 publications, Valve's debut title blends action and adventure with award-winning technology to create a frighteningly realistic world where players must think to survive. Also includes an exciting multiplayer mode that allows you to play against friends and enemies around the world.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/220/capsule_184x69.jpg" alt="Half-Life 2" width="28" height="28" /><span>Half-Life 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/220/header.jpg?t=1745368545')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/220/">Half-Life 2</a><span class="about-tip-date">16 Nov, 2004</span><span class="about-tip-desc">Reawakened from stasis in the occupied metropolis of City 17, Gordon Freeman is joined by Alyx Vance as he leads a desperate human resistance. Experience the landmark first-person shooter packed with immersive world-building, boundary-pushing physics, and exhilarating combat.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/546560/capsule_184x69.jpg" alt="Half-Life Alyx" width="28" height="28" /><span>Half-Life: Alyx</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/546560/header.jpg?t=1762986588')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/546560/">Half-Life: Alyx</a><span class="about-tip-date">23 Mar, 2020</span><span class="about-tip-desc">Half-Life: Alyx is Valve’s VR return to the Half-Life series. It’s the story of an impossible fight against a vicious alien race known as the Combine, set between the events of Half-Life and Half-Life 2. Playing as Alyx Vance, you are humanity’s only chance for survival.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/440/capsule_184x69.jpg" alt="Team Fortress 2" width="28" height="28" /><span>Team Fortress 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/440/header.jpg?t=1757348372')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/440/">Team Fortress 2</a><span class="about-tip-date">10 Oct, 2007</span><span class="about-tip-desc">Nine distinct classes provide a broad range of tactical abilities and personalities. Constantly updated with new game modes, maps, equipment and, most importantly, hats!</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/71250/capsule_184x69.jpg" alt="Sonic Adventure DX" width="28" height="28" /><span>Sonic Adventure DX</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/71250/header.jpg?t=1762751624')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/71250/">Sonic Adventure DX</a><span class="about-tip-date">4 Mar, 2011</span><span class="about-tip-desc">An ancient evil lurking within the Master Emerald has been unleashed from its slumber by the devious Dr. Eggman and is on the verge of becoming the ultimate monster using the 7 Chaos Emeralds. Only Sonic and his friends are heroic enough to put a stop to Dr. Eggman and his evil minions.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/1/1b/Vintage_Story_Logo.png" alt="Vintage Story" width="28" height="28" /><span>Vintage Story</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/1/1b/Vintage_Story_Logo.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.vintagestory.at/">Vintage Story</a><span class="about-tip-desc">Vintage Story is a voxel survival sandbox with deep crafting, smithing, and seasons.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/704270/capsule_184x69.jpg" alt="Generation Zero" width="28" height="28" /><span>Generation Zero</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/704270/header.jpg?t=1733993638')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/704270/">Generation Zero</a><span class="about-tip-date">26 Mar, 2019</span><span class="about-tip-desc">Generation Zero is a stealth-action shooter where you wage guerilla warfare against lethal mechanical enemies. Explore a vast open world map inspired by the Swedish Cold War era, take part in the resistance alone or with up to three friends in seamless co-op.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://www.minecraft.net/content/dam/minecraftnet/franchise/logos/minecraft-creeper-face.jpg" alt="Minecraft" width="28" height="28" /><span>Minecraft</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.minecraft.net/content/dam/minecraftnet/franchise/logos/minecraft-creeper-face.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.minecraft.net/">Minecraft</a><span class="about-tip-desc">Minecraft is a sandbox where you build, explore, and survive in blocky worlds.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/220240/capsule_184x69.jpg" alt="Far Cry 3" width="28" height="28" /><span>Far Cry 3</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/220240/3848aafeb6e5cff40cbf6210c34413f3034150da/header.jpg?t=1785282057')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/220240/">Far Cry 3</a><span class="about-tip-date">28 Nov, 2012</span><span class="about-tip-desc">Stranded on the Rook Islands as Jason Brody, fight your way through a lawless tropical open world using a powerful arsenal to save your friends and escape the madness of this acclaimed visceral FPS.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/1/15/Sonic_Riders_Coverart.png" alt="Sonic Riders" width="28" height="28" /><span>Sonic Riders</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/1/15/Sonic_Riders_Coverart.png?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Sonic_Riders">Sonic Riders</a><span class="about-tip-desc">Sonic Riders is a 2006 racing video game developed by Sonic Team and Now Production and published by Sega for the GameCube, PlayStation 2, and Xbox.</span></span></span></span>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Music</div>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/nbogUmJkeBI/mqdefault.jpg" alt="2 Mello - I Wanna Kno" width="28" height="28" /><span>2 Mello - I Wanna Kno</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/nbogUmJkeBI/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.youtube.com/watch?v=nbogUmJkeBI">2 Mello - I Wanna Kno</a><span class="about-tip-desc">2 Mello - I Wanna Kno from Sounds of Tokyo-To Future (2021).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/Dw1ZC6sZjIY/mqdefault.jpg" alt="Frank Sinatra - Blue Moon" width="28" height="28" /><span>Frank Sinatra - Blue Moon</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/Dw1ZC6sZjIY/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.youtube.com/watch?v=Dw1ZC6sZjIY">Frank Sinatra - Blue Moon</a><span class="about-tip-desc">CAKE - Frank Sinatra from Fashion Nugget (1996).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/Pd-qu_ErkbE/mqdefault.jpg" alt="Pink Floyd - Crazy Diamond" width="28" height="28" /><span>Pink Floyd - Crazy Diamond</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/Pd-qu_ErkbE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.youtube.com/watch?v=Pd-qu_ErkbE">Pink Floyd - Crazy Diamond</a><span class="about-tip-desc">Pink Floyd - Shine On You Crazy Diamond (Pts. 1-9, New Stereo Mix) from Wish You Were Here 50 (2025).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/c0SrxSMHDmE/mqdefault.jpg" alt="Bullet For My Valentine - Hand Of Blood" width="28" height="28" /><span>Bullet For My Valentine - Hand Of Blood</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/c0SrxSMHDmE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.youtube.com/watch?v=c0SrxSMHDmE">Bullet For My Valentine - Hand Of Blood</a><span class="about-tip-desc">bulletvalentineVEVO - Bullet For My Valentine - Hand Of Blood (Official Video).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music118/v4/98/f2/79/98f279ea-f1a2-e258-d96a-8ceff77f8e58/859728161827_cover.jpg/100x100bb.jpg" alt="Evans Blue - iGod" width="28" height="28" /><span>Evans Blue - iGod</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Music118/v4/98/f2/79/98f279ea-f1a2-e258-d96a-8ceff77f8e58/859728161827_cover.jpg/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/search?q=Evans+Blue+iGod">Evans Blue - iGod</a><span class="about-tip-desc">Evans Blue - iGod from Letters from the Dead (2016).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/_Y_a0PWlBr8/mqdefault.jpg" alt="Breaking Benjamin - Psycho" width="28" height="28" /><span>Breaking Benjamin - Psycho</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/_Y_a0PWlBr8/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.youtube.com/watch?v=_Y_a0PWlBr8">Breaking Benjamin - Psycho</a><span class="about-tip-desc">BreakingBenjaminVEVO - Breaking Benjamin - Psycho (Audio Only).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/MM62wjLrgmA/mqdefault.jpg" alt="TOOL - Schism" width="28" height="28" /><span>TOOL - Schism</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/MM62wjLrgmA/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.youtube.com/watch?v=MM62wjLrgmA">TOOL - Schism</a><span class="about-tip-desc">TOOLVEVO - TOOL - Schism (Official Video).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/3NNaUQnFL2c/mqdefault.jpg" alt="A Perfect Circle - Rose" width="28" height="28" /><span>A Perfect Circle - Rose</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/3NNaUQnFL2c/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.youtube.com/watch?v=3NNaUQnFL2c">A Perfect Circle - Rose</a><span class="about-tip-desc">A Perfect Circle - Rose from Mer De Noms (2000).</span></span></span></span>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Movies/series/cartoons</div>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/The_Venture_Bros_logo.svg/250px-The_Venture_Bros_logo.svg.png" alt="The Venture Bros." width="28" height="28" /><span>The Venture Bros.</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/The_Venture_Bros_logo.svg/250px-The_Venture_Bros_logo.svg.png?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Venture_Bros.">The Venture Bros.</a><span class="about-tip-desc">The Venture Bros. is an American adult animated action-adventure television series created by Jackson Publick and Doc Hammer for Cartoon Network's late night programming block Adult Swim. Following a pilot episode on February 16, 2003, the series premiered on August 7, 2004. The Venture Bros.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/7/75/JoJo_Part_3_Stardust_Crusaders.jpg" alt="Stardust Crusaders" width="28" height="28" /><span>Stardust Crusaders</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/7/75/JoJo_Part_3_Stardust_Crusaders.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/JoJo%27s_Bizarre_Adventure:_Stardust_Crusaders">Stardust Crusaders</a><span class="about-tip-desc">JoJo's Bizarre Adventure: Stardust Crusaders is the second season of the JoJo's Bizarre Adventure anime by David Production, based on the JoJo's Bizarre Adventure manga series by Hirohiko Araki.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/f/f6/Equilibriumposter.jpg" alt="Equilibrium" width="28" height="28" /><span>Equilibrium</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/f/f6/Equilibriumposter.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Equilibrium_(film)">Equilibrium</a><span class="about-tip-desc">Equilibrium is a 2002 American science fiction dystopian action film written and directed by Kurt Wimmer, and starring Christian Bale, Emily Watson, and Taye Diggs.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/f/f7/Mad_max_two_the_road_warrior.jpg" alt="Mad Max 2" width="28" height="28" /><span>Mad Max 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/f/f7/Mad_max_two_the_road_warrior.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Mad_Max_2">Mad Max 2</a><span class="about-tip-desc">Mad Max 2 is a 1981 Australian post-apocalyptic dystopian action film directed by George Miller, who co-wrote it with Terry Hayes and Brian Hannant. It is the sequel to Mad Max (1979) and the second installment in the Mad Max franchise.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/a4/1c/85/a41c85f8-947d-ede3-ebaa-9b5ee2251eb3/mzl.eqyyqnmm.lsr/600x600bb.jpg" alt="Westworld" width="28" height="28" /><span>Westworld</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/a4/1c/85/a41c85f8-947d-ede3-ebaa-9b5ee2251eb3/mzl.eqyyqnmm.lsr/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Westworld_(TV_series)">Westworld</a><span class="about-tip-desc">Westworld is an American dystopian science fiction Western drama television series created by Jonathan Nolan and Lisa Joy that aired from 2016 to 2022 on HBO. It is based upon the 1973 film of the same name written and directed by Michael Crichton and loosely upon its 1976 sequel, Futureworld.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/b/b9/The_Day_of_the_Jackal_%282025%29_title_card.jpg" alt="The Day of the Jackal" width="28" height="28" /><span>The Day of the Jackal</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/b/b9/The_Day_of_the_Jackal_%282025%29_title_card.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Day_of_the_Jackal_(TV_series)">The Day of the Jackal</a><span class="about-tip-desc">The Day of the Jackal is a British spy thriller television series, based on the Frederick Forsyth novel and 1973 film of the same name. It stars Eddie Redmayne and Lashana Lynch.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/c/c7/Memento_poster.jpg" alt="Memento" width="28" height="28" /><span>Memento</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/c/c7/Memento_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Memento_(film)">Memento</a><span class="about-tip-desc">Memento is a 2000 American neo-noir psychological thriller film written for the screen and directed by Christopher Nolan, based on the 2001 short story "Memento Mori" by his brother, Jonathan Nolan. The film stars Guy Pearce, Carrie-Anne Moss, and Joe Pantoliano.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/4/4c/WALL-E_poster.jpg" alt="WALL-E" width="28" height="28" /><span>WALL-E</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/4/4c/WALL-E_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/WALL-E">WALL-E</a><span class="about-tip-desc">WALL-E is a 2008 American animated romantic science fiction film directed by Andrew Stanton, who co-wrote the screenplay with Jim Reardon, based on a story by Stanton and Pete Docter.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/b/b9/Shrek_2_poster.jpg" alt="Shrek 2" width="28" height="28" /><span>Shrek 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/b/b9/Shrek_2_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Shrek_2">Shrek 2</a><span class="about-tip-desc">Shrek 2 is a 2004 American animated fantasy comedy film loosely based on the 1990 children's picture book Shrek! by William Steig. Directed by Andrew Adamson, Kelly Asbury, and Conrad Vernon from a screenplay by Adamson, Joe Stillman, and the writing team of J. David Stem and David N.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/3/36/Madagascar_Theatrical_Poster.jpg" alt="Madagascar" width="28" height="28" /><span>Madagascar</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/3/36/Madagascar_Theatrical_Poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Madagascar_(2005_film)">Madagascar</a><span class="about-tip-desc">Madagascar is a 2005 American animated comedy film directed by Eric Darnell and Tom McGrath and written by Mark Burton, Billy Frolick, Darnell and McGrath Produced by DreamWorks Animation and PDI/DreamWorks. The first installment in Madagascar film series and Madagascar trilogy.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/0/02/Hellsing_1.png" alt="Hellsing" width="28" height="28" /><span>Hellsing</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/0/02/Hellsing_1.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Hellsing">Hellsing</a><span class="about-tip-desc">Hellsing is a Japanese manga series written and illustrated by Kouta Hirano. It was serialized in Shonen Gahosha's seinen manga magazine Young King OURs from April 1997 to September 2008, with its chapters collected in ten tankobon volumes.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/a/a1/Cyberpunk_Edgerunners_poster.jpg" alt="Cyberpunk: Edgerunners" width="28" height="28" /><span>Cyberpunk: Edgerunners</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/a/a1/Cyberpunk_Edgerunners_poster.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Cyberpunk:_Edgerunners">Cyberpunk: Edgerunners</a><span class="about-tip-desc">Cyberpunk: Edgerunners is an original net animation (ONA) miniseries created by Rafal Jaki. It was produced by the Polish video game company CD Projekt Red and the Japanese animation studio Trigger, and premiered on Netflix on September 13, 2022.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video49/v4/a7/c7/4c/a7c74cd4-ab55-e95a-a8d3-752a2bba1036/mzl.ibrfkcdo.lsr/600x600bb.jpg" alt="The Sopranos" width="28" height="28" /><span>The Sopranos</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video49/v4/a7/c7/4c/a7c74cd4-ab55-e95a-a8d3-752a2bba1036/mzl.ibrfkcdo.lsr/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Sopranos">The Sopranos</a><span class="about-tip-desc">The Sopranos is an American crime drama television series created by David Chase for HBO. The series follows Tony Soprano, a New Jersey Mafia boss who has panic attacks.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/af/2d/85/af2d8510-0c8b-4869-4b39-23df93d0edc9/mzl.tdpjxlkl.lsr/600x600bb.jpg" alt="Breaking Bad" width="28" height="28" /><span>Breaking Bad</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/af/2d/85/af2d8510-0c8b-4869-4b39-23df93d0edc9/mzl.tdpjxlkl.lsr/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Breaking_Bad">Breaking Bad</a><span class="about-tip-desc">Breaking Bad is an American neo-Western crime drama television series created by Vince Gilligan for AMC.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ee/Fallout_television_series_logo.svg/500px-Fallout_television_series_logo.svg.png" alt="Fallout" width="28" height="28" /><span>Fallout</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/thumb/e/ee/Fallout_television_series_logo.svg/500px-Fallout_television_series_logo.svg.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Fallout_(American_TV_series)">Fallout</a><span class="about-tip-desc">Fallout is an American post-apocalyptic drama television series created by Graham Wagner and Geneva Robertson-Dworet for Amazon Prime Video.</span></span></span></span>
</p>
</div>
</details>

<div class="about-engaged" title="Engaged" aria-label="Engaged">
<span class="about-engaged-gap">
<svg xmlns="http://www.w3.org/2000/svg" width="36" height="20" viewBox="0 0 36 20" aria-hidden="true">
<circle cx="12.5" cy="10" r="7" fill="none" stroke="#ff8000" stroke-width="2.1"/>
<circle cx="23.5" cy="10" r="7" fill="none" stroke="#0abab5" stroke-width="2.1"/>
<path d="M18.2 5.2a7 7 0 0 1 2.6 4.8" fill="none" stroke="#ff8000" stroke-width="2.1"/>
</svg>
</span>
</div>

<details class="about-person" id="sttaya">
<summary><span class="about-head"><span class="about-avatar-link"><span class="about-avatar-wrap"><img src="https://avatars.fastly.steamstatic.com/5bb86930eb99f482e56abc25937b7d6be37e83c3_full.jpg" alt="StTaya" width="96" height="96" /><img src="https://shared.fastly.steamstatic.com/community_assets/images/items/944220/91b1c881cd9fc1b0f9f77f0d410b30eb3192cc41.png" alt=" " width="96" height="96" /></span></span><span class="about-id"><h2 class="about-name"><a class="about-anchor" href="#sttaya">StTaya</a></h2><ul class="about-roles"><li>3D Artist</li><li>Art Designer</li><li>Animator</li><li>Level Designer</li></ul></span><span class="about-head-split"></span><span class="about-tops"><span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1361210/capsule_184x69.jpg" alt="Darktide" width="28" height="28" /><span>Darktide</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/1361210/f07ebcb73a34112ac61c54608b1f1ded7e45eb8a/header.jpg?t=1782226781')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/1361210/">Darktide</a><span class="about-tip-date">30 Nov, 2022</span><span class="about-tip-desc">Take back the city of Tertium from hordes of bloodthirsty foes in this intense and brutal action shooter. Warhammer 40,000: Darktide is the new co-op focused experience from the award-winning team behind the Vermintide series. As Tertium falls, Rejects Will Rise.</span></span></span></span><span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/ZHtDG6O93nE/mqdefault.jpg" alt="Jesper Kyd" width="28" height="28" /><span>Jesper Kyd</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/ZHtDG6O93nE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=ZHtDG6O93nE">Jesper Kyd</a><span class="about-tip-desc">Jesper Kyd - The Ritual from Warhammer 40,000: Darktide Vol. 4 (Original Soundtrack) (2025).</span></span></span></span><span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/9/9f/Sucker_Punch_film_poster.jpg" alt="Sucker Punch" width="28" height="28" /><span>Sucker Punch</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/9/9f/Sucker_Punch_film_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Sucker_Punch_(2011_film)">Sucker Punch</a><span class="about-tip-desc">Sucker Punch is a 2011 fantasy action film directed by Zack Snyder and co-written by Snyder and Steve Shibuya. It is Snyder's first film based on an original concept. The film stars Emily Browning as "Babydoll", a young woman who is committed to a mental institution.</span></span></span></span><span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/blender/E87D0D" alt="Blender" width="28" height="28" /><span>Blender</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/blender/E87D0D')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.blender.org/">Blender</a><span class="about-tip-desc">Free 3D modeling, animation, and rendering suite.</span></span></span></span></span></span></summary>
<div class="about-row">
<div class="about-section">
<div class="about-section-label">About</div>
<p class="about-note">Hobbies: skateboarding, breakdance, boxing, kickboxing, camping.</p>
</div>
<div class="about-section">
<div class="about-section-label">Likes</div>
<p class="about-note"><a class="about-anchor" href="#stcost">StCost</a>, whiskey, burgers, beefsteak, strawberries, lettuce.</p>
<div class="fav-colors">
<span class="fav-chip"><span class="fav-swatch tiffany"></span><span>Tiffany</span></span>
<span class="fav-chip"><span class="fav-swatch black"></span><span>Black</span></span>
</div>
</div>
</div>
<div class="about-row about-meta">
<div class="about-section">
<div class="about-section-label">Media</div>
<p class="fav-row fav-compact">
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="Steam" width="28" height="28" /><span>Steam</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/steam/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://steamcommunity.com/id/sttaya">Steam</a><span class="about-tip-desc">StTaya on Steam.</span></span></span></span>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Tools</div>
<p class="fav-row fav-compact">
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/blender/E87D0D" alt="Blender" width="28" height="28" /><span>Blender</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/blender/E87D0D')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.blender.org/">Blender</a><span class="about-tip-desc">Free 3D modeling, animation, and rendering suite.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://www.getpaint.net/favicon.ico" alt="Paint.NET" width="28" height="28" /><span>Paint.NET</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.getpaint.net/favicon.ico')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.getpaint.net/">Paint.NET</a><span class="about-tip-desc">Windows image editor for 2D art and textures.</span></span></span></span>
</p>
</div>
</div>
<div class="about-section">
<div class="about-section-label">Games</div>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1361210/capsule_184x69.jpg" alt="Darktide" width="28" height="28" /><span>Darktide</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/1361210/f07ebcb73a34112ac61c54608b1f1ded7e45eb8a/header.jpg?t=1782226781')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/1361210/">Darktide</a><span class="about-tip-date">30 Nov, 2022</span><span class="about-tip-desc">Take back the city of Tertium from hordes of bloodthirsty foes in this intense and brutal action shooter. Warhammer 40,000: Darktide is the new co-op focused experience from the award-winning team behind the Vermintide series. As Tertium falls, Rejects Will Rise.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/548430/capsule_184x69.jpg" alt="Deep Rock Galactic" width="28" height="28" /><span>Deep Rock Galactic</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/548430/7218336ad0b0fdbe13bfe7503627f30ac901b02c/header_alt_assets_15.jpg?t=1786014445')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/548430/">Deep Rock Galactic</a><span class="about-tip-date">13 May, 2020</span><span class="about-tip-desc">Deep Rock Galactic is a 1-4 player co-op FPS featuring dwarven space miners, procedurally-generated destructible environments, and endless hordes of alien monsters. Explore cave systems, mine for minerals, and work together to survive!</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/553850/capsule_184x69.jpg" alt="HELLDIVERS 2" width="28" height="28" /><span>HELLDIVERS 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/553850/850e2f9e5bb15c5706bb9a1edc832f4f782e8be5/header.jpg?t=1786525389')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/553850/">HELLDIVERS 2</a><span class="about-tip-date">8 Feb, 2024</span><span class="about-tip-desc">The Galaxy’s Last Line of Offence. Enlist in the Helldivers and join the fight for freedom across a hostile galaxy in a fast, frantic, and ferocious third-person shooter.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1086940/capsule_184x69.jpg" alt="Baldur's Gate 3" width="28" height="28" /><span>Baldur's Gate 3</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/1086940/48a2fcbda8565bb45025e98fd8ebde8a7203f6a0/header.jpg?t=1777363040')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/1086940/">Baldur's Gate 3</a><span class="about-tip-date">3 Aug, 2023</span><span class="about-tip-desc">Baldur’s Gate 3 is a story-rich, party-based RPG set in the universe of Dungeons &amp; Dragons, where your choices shape a tale of fellowship and betrayal, survival and sacrifice, and the lure of absolute power.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/632360/capsule_184x69.jpg" alt="Risk of Rain 2" width="28" height="28" /><span>Risk of Rain 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/632360/header.jpg?t=1783621122')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/632360/">Risk of Rain 2</a><span class="about-tip-date">11 Aug, 2020</span><span class="about-tip-desc">Escape a chaotic alien planet by fighting through hordes of frenzied monsters – with your friends, or on your own. Combine loot in surprising ways and master each character until you become the havoc you feared upon your first crash landing.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/2835570/capsule_184x69.jpg" alt="Buckshot Roulette" width="28" height="28" /><span>Buckshot Roulette</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/2835570/header.jpg?t=1783085442')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/2835570/">Buckshot Roulette</a><span class="about-tip-date">4 Apr, 2024</span><span class="about-tip-desc">Play Russian roulette with a 12-gauge shotgun. Four enter. One leaves. Roll the dice with your life. Good luck!</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/1/1b/Vintage_Story_Logo.png" alt="Vintage Story" width="28" height="28" /><span>Vintage Story</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/1/1b/Vintage_Story_Logo.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.vintagestory.at/">Vintage Story</a><span class="about-tip-desc">Vintage Story is a voxel survival sandbox with deep crafting, smithing, and seasons.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/377160/capsule_184x69.jpg" alt="Fallout 4" width="28" height="28" /><span>Fallout 4</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/377160/header.jpg?t=1786648137')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/377160/">Fallout 4</a><span class="about-tip-date">9 Nov, 2015</span><span class="about-tip-desc">From Bethesda Game Studios, the award-winning creators of Starfield and The Elder Scrolls V: Skyrim, comes Fallout 4. A landmark in open-world RPG design and winner of over 200 ‘Best Of’ honors, including the DICE and BAFTA Game of the Year.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/704270/capsule_184x69.jpg" alt="Generation Zero" width="28" height="28" /><span>Generation Zero</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/704270/header.jpg?t=1733993638')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/704270/">Generation Zero</a><span class="about-tip-date">26 Mar, 2019</span><span class="about-tip-desc">first game. Generation Zero is a stealth-action shooter where you wage guerilla warfare against lethal mechanical enemies. Explore a vast open world map inspired by the Swedish Cold War era, take part in the resistance alone or with up to three friends in seamless co-op.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://www.minecraft.net/content/dam/minecraftnet/franchise/logos/minecraft-creeper-face.jpg" alt="Minecraft" width="28" height="28" /><span>Minecraft</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.minecraft.net/content/dam/minecraftnet/franchise/logos/minecraft-creeper-face.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.minecraft.net/">Minecraft</a><span class="about-tip-desc">Minecraft is a sandbox where you build, explore, and survive in blocky worlds.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/220240/capsule_184x69.jpg" alt="Far Cry 3" width="28" height="28" /><span>Far Cry 3</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/220240/3848aafeb6e5cff40cbf6210c34413f3034150da/header.jpg?t=1785282057')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/220240/">Far Cry 3</a><span class="about-tip-date">28 Nov, 2012</span><span class="about-tip-desc">Stranded on the Rook Islands as Jason Brody, fight your way through a lawless tropical open world using a powerful arsenal to save your friends and escape the madness of this acclaimed visceral FPS.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/1/15/Sonic_Riders_Coverart.png" alt="Sonic Riders" width="28" height="28" /><span>Sonic Riders</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/1/15/Sonic_Riders_Coverart.png?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Sonic_Riders">Sonic Riders</a><span class="about-tip-desc">Sonic Riders is a 2006 racing video game developed by Sonic Team and Now Production and published by Sega for the GameCube, PlayStation 2, and Xbox.</span></span></span></span>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Music</div>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/ZHtDG6O93nE/mqdefault.jpg" alt="Jesper Kyd - The Ritual" width="28" height="28" /><span>Jesper Kyd - The Ritual</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/ZHtDG6O93nE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=ZHtDG6O93nE">Jesper Kyd - The Ritual</a><span class="about-tip-desc">Jesper Kyd - The Ritual from Warhammer 40,000: Darktide Vol. 4 (Original Soundtrack) (2025).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/qNznC_ASiK4/mqdefault.jpg" alt="Zheani - SPOILS OF WAR" width="28" height="28" /><span>Zheani - SPOILS OF WAR</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/qNznC_ASiK4/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=qNznC_ASiK4">Zheani - SPOILS OF WAR</a><span class="about-tip-desc">Zheani - SPOILS OF WAR (feat. BUTTRESS).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/jgXDwyPxB8g/mqdefault.jpg" alt="Reso - Spectres" width="28" height="28" /><span>Reso - Spectres</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/jgXDwyPxB8g/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=jgXDwyPxB8g">Reso - Spectres</a><span class="about-tip-desc">Reso - Spectres from Spectre - EP (2019).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/r6Eei81SuqE/mqdefault.jpg" alt="BLACKPINK - JUMP" width="28" height="28" /><span>BLACKPINK - JUMP</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/r6Eei81SuqE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=r6Eei81SuqE">BLACKPINK - JUMP</a><span class="about-tip-desc">BLACKPINK - JUMP from JUMP - Single (2025).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/P2aBhU6pLCg/mqdefault.jpg" alt="Massive Attack - I Against I" width="28" height="28" /><span>Massive Attack - I Against I</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/P2aBhU6pLCg/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=P2aBhU6pLCg">Massive Attack - I Against I</a><span class="about-tip-desc">Massive Attack &amp; Mos Def - I Against I from Collected (Deluxe Edition) (2002).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/cmyv2MA_Pf4/mqdefault.jpg" alt="Jodeci - Freek'n You" width="28" height="28" /><span>Jodeci - Freek'n You</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/cmyv2MA_Pf4/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=cmyv2MA_Pf4">Jodeci - Freek'n You</a><span class="about-tip-desc">Jodeci - Freek'n You from The Show, the After-Party, the Hotel (1995).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/NWh-ow-CT1Y/mqdefault.jpg" alt="Joey Valence &amp; Brae - Double Jump" width="28" height="28" /><span>Joey Valence &amp; Brae - Double Jump</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/NWh-ow-CT1Y/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=NWh-ow-CT1Y">Joey Valence &amp; Brae - Double Jump</a><span class="about-tip-desc">Joey Valence &amp; Brae - PUNK TACTICS from PUNK TACTICS - Single (2022).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/pTNlEf0bvRE/mqdefault.jpg" alt="Starjunk 95 - Ocean Memory Unit" width="28" height="28" /><span>Starjunk 95 - Ocean Memory Unit</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/pTNlEf0bvRE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=pTNlEf0bvRE">Starjunk 95 - Ocean Memory Unit</a><span class="about-tip-desc">Starjunk 95 - Ocean Memory Unit from Ocean Memory Unit - Single (2025).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/HLrqNhgdiC0/mqdefault.jpg" alt="Massive Attack - Angel" width="28" height="28" /><span>Massive Attack - Angel</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/HLrqNhgdiC0/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=HLrqNhgdiC0">Massive Attack - Angel</a><span class="about-tip-desc">Massive Attack - Angel from Mezzanine (1998).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/VAl4tW651QY/mqdefault.jpg" alt="Massive Attack - Montage" width="28" height="28" /><span>Massive Attack - Montage</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/VAl4tW651QY/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=VAl4tW651QY">Massive Attack - Montage</a><span class="about-tip-desc">Massive Attack - Montage from Danny the Dog (Original Motion Picture Soundtrack) (2004).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/Qezj9j_XLkE/mqdefault.jpg" alt="Starjunk 95 - Snowdream" width="28" height="28" /><span>Starjunk 95 - Snowdream</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/Qezj9j_XLkE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=Qezj9j_XLkE">Starjunk 95 - Snowdream</a><span class="about-tip-desc">Starjunk 95 - Snowdream from Snowdream - Single (2025).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/ZnfuDiwSSGQ/mqdefault.jpg" alt="Maximum the Hormone - Bu-ikikaesu!!" width="28" height="28" /><span>Maximum the Hormone - Bu-ikikaesu!!</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/ZnfuDiwSSGQ/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=ZnfuDiwSSGQ">Maximum the Hormone - Bu-ikikaesu!!</a><span class="about-tip-desc">MAXIMUM THE HORMONE - Bu-Ikikaesu!! from Bu-Ikikaesu (2007).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/ieG7lDh9DfQ/mqdefault.jpg" alt="Die Antwoord - FUTURE BABY" width="28" height="28" /><span>Die Antwoord - FUTURE BABY</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/ieG7lDh9DfQ/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=ieG7lDh9DfQ">Die Antwoord - FUTURE BABY</a><span class="about-tip-desc">Die Antwoord - FUTURE BABY.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/eU1g8LcFOmg/mqdefault.jpg" alt="Die Antwoord - DAZED &amp; CONFUSED" width="28" height="28" /><span>Die Antwoord - DAZED &amp; CONFUSED</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/eU1g8LcFOmg/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=eU1g8LcFOmg">Die Antwoord - DAZED &amp; CONFUSED</a><span class="about-tip-desc">Die Antwoord - DAZED &amp; CONFUSED.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/FbknH5wlkC8/mqdefault.jpg" alt="Venjent - Create Machines" width="28" height="28" /><span>Venjent - Create Machines</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/FbknH5wlkC8/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=FbknH5wlkC8">Venjent - Create Machines</a><span class="about-tip-desc">Venjent - Create Machines from Create Machines - Single (2023).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/tnekQAuqmmI/mqdefault.jpg" alt="Chris Christodoulou - The Face of the Deep" width="28" height="28" /><span>Chris Christodoulou - The Face of the Deep</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/tnekQAuqmmI/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=tnekQAuqmmI">Chris Christodoulou - The Face of the Deep</a><span class="about-tip-desc">Chris Christodoulou - The Face of the Deep (feat. Dimitris Tsakas) from Risk of Rain 2: Survivors of the Void (2022).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/X5I64Oobpfc/mqdefault.jpg" alt="Machine Girl - Sin to Win!" width="28" height="28" /><span>Machine Girl - Sin to Win!</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/X5I64Oobpfc/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=X5I64Oobpfc">Machine Girl - Sin to Win!</a><span class="about-tip-desc">Machine Girl - Sin to Win! from Neon White Soundtrack, Pt. 1 (the Wicked Heart) (2022).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/5wIeHP6dscU/mqdefault.jpg" alt="Doja Cat - MOOO!" width="28" height="28" /><span>Doja Cat - MOOO!</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/5wIeHP6dscU/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=5wIeHP6dscU">Doja Cat - MOOO!</a><span class="about-tip-desc">Doja Cat - Mooo! from Mooo! - Single (2018).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/QCZHO7IHouU/mqdefault.jpg" alt="Die Antwoord - Beat Boy" width="28" height="28" /><span>Die Antwoord - Beat Boy</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/QCZHO7IHouU/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=QCZHO7IHouU">Die Antwoord - Beat Boy</a><span class="about-tip-desc">Die Antwoord - Beat Boy.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/cKTpfRakdO4/mqdefault.jpg" alt="Psychedelic Limbo" width="28" height="28" /><span>Psychedelic Limbo</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/cKTpfRakdO4/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=cKTpfRakdO4">Psychedelic Limbo</a><span class="about-tip-desc">KazKon - Psychedelic Limbo - AMV.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/0nrnlS5ApfA/mqdefault.jpg" alt="Die Antwoord - STIEK UIT" width="28" height="28" /><span>Die Antwoord - STIEK UIT</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/0nrnlS5ApfA/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=0nrnlS5ApfA">Die Antwoord - STIEK UIT</a><span class="about-tip-desc">Die Antwoord - STIEK UIT.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/PkakXTo26Sg/mqdefault.jpg" alt="Björk - Army Of Me" width="28" height="28" /><span>Björk - Army Of Me</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/PkakXTo26Sg/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=PkakXTo26Sg">Björk - Army Of Me</a><span class="about-tip-desc">Björk - Army of Me from Post (1995).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/9GpFKrK7-c0/mqdefault.jpg" alt="Clown Core - Flat Earth" width="28" height="28" /><span>Clown Core - Flat Earth</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/9GpFKrK7-c0/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=9GpFKrK7-c0">Clown Core - Flat Earth</a><span class="about-tip-desc">Clown Core - Flat Earth from Van (2020).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/lRrOLTHu-ew/mqdefault.jpg" alt="JoJo - Awaken" width="28" height="28" /><span>JoJo - Awaken</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/lRrOLTHu-ew/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=lRrOLTHu-ew">JoJo - Awaken</a><span class="about-tip-desc">Samuel Kim - Pillar Men Theme (Awaken) [Cover] from JoJo's Bizarre Adventure: Epic Collection, Vol. 2 (Cover) - EP (2021).</span></span></span></span>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Movies/series/cartoons</div>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/9/9f/Sucker_Punch_film_poster.jpg" alt="Sucker Punch" width="28" height="28" /><span>Sucker Punch</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/9/9f/Sucker_Punch_film_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Sucker_Punch_(2011_film)">Sucker Punch</a><span class="about-tip-desc">Sucker Punch is a 2011 fantasy action film directed by Zack Snyder and co-written by Snyder and Steve Shibuya. It is Snyder's first film based on an original concept. The film stars Emily Browning as "Babydoll", a young woman who is committed to a mental institution.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/4/42/HungerGamesPoster.jpg" alt="The Hunger Games" width="28" height="28" /><span>The Hunger Games</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/4/42/HungerGamesPoster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Hunger_Games_(film)">The Hunger Games</a><span class="about-tip-desc">The Hunger Games is a 2012 American dystopian film directed by Gary Ross, who co-wrote the screenplay with Suzanne Collins and Billy Ray, based on the 2008 novel of the same name by Collins. It is the first installment in The Hunger Games film series.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/6/67/Forrest_Gump_poster.jpg" alt="Forrest Gump" width="28" height="28" /><span>Forrest Gump</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/6/67/Forrest_Gump_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Forrest_Gump">Forrest Gump</a><span class="about-tip-desc">Forrest Gump is a 1994 American comedy-drama film directed by Robert Zemeckis. An adaptation of the 1986 novel of the same name by Winston Groom, the film's screenplay was written by Eric Roth. It stars Tom Hanks in the title role, alongside Robin Wright, Gary Sinise, Mykelti Williamson, and Sally Field in lead roles.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/2/22/Real_Steel_Poster.jpg" alt="Real Steel" width="28" height="28" /><span>Real Steel</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/2/22/Real_Steel_Poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Real_Steel">Real Steel</a><span class="about-tip-desc">Real Steel is a 2011 American science fiction sports film starring Hugh Jackman. Produced and directed by Shawn Levy, the film is based on the short story "Steel", written by Richard Matheson, which was originally published in the May 1956 edition of The Magazine of Fantasy &amp; Science Fiction, and later adapted into a 1...</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/9/9c/Peaceful_warrior.jpg" alt="Peaceful Warrior" width="28" height="28" /><span>Peaceful Warrior</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/9/9c/Peaceful_warrior.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Peaceful_Warrior">Peaceful Warrior</a><span class="about-tip-desc">Peaceful Warrior is a 2006 sports drama film directed by Victor Salva and written by Kevin Bernhardt based on the 1980 novel Way of the Peaceful Warrior by Dan Millman. Set at U.C.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/7/75/JoJo_Part_3_Stardust_Crusaders.jpg" alt="Stardust Crusaders" width="28" height="28" /><span>Stardust Crusaders</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/7/75/JoJo_Part_3_Stardust_Crusaders.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/JoJo%27s_Bizarre_Adventure:_Stardust_Crusaders">Stardust Crusaders</a><span class="about-tip-desc">JoJo's Bizarre Adventure: Stardust Crusaders is the second season of the JoJo's Bizarre Adventure anime by David Production, based on the JoJo's Bizarre Adventure manga series by Hirohiko Araki.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/The_Venture_Bros_logo.svg/250px-The_Venture_Bros_logo.svg.png" alt="The Venture Bros." width="28" height="28" /><span>The Venture Bros.</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/thumb/7/7c/The_Venture_Bros_logo.svg/250px-The_Venture_Bros_logo.svg.png?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Venture_Bros.">The Venture Bros.</a><span class="about-tip-desc">The Venture Bros. is an American adult animated action-adventure television series created by Jackson Publick and Doc Hammer for Cartoon Network's late night programming block Adult Swim. Following a pilot episode on February 16, 2003, the series premiered on August 7, 2004. The Venture Bros.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video112/v4/37/39/e0/3739e08a-306b-0851-64d6-caa68005df0b/pr_source.lsr/600x600bb.jpg" alt="Halo" width="28" height="28" /><span>Halo</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video112/v4/37/39/e0/3739e08a-306b-0851-64d6-caa68005df0b/pr_source.lsr/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Halo_(TV_series)">Halo</a><span class="about-tip-desc">Halo is an American military science fiction television series developed by Kyle Killen and Steven Kane for the streaming service Paramount+.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/d/d8/Game_of_Thrones_title_card.jpg" alt="Game of Thrones" width="28" height="28" /><span>Game of Thrones</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/d/d8/Game_of_Thrones_title_card.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Game_of_Thrones">Game of Thrones</a><span class="about-tip-desc">Game of Thrones is an American fantasy drama television series created by David Benioff and D. B. Weiss for HBO. It is the first adaptation of the A Song of Ice and Fire franchise, a series of high fantasy novels by George R. R. Martin, the first of which is A Game of Thrones.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/c/cc/Kizumonogatari_Part_1_Tekketsu_poster.jpeg" alt="Kizumonogatari" width="28" height="28" /><span>Kizumonogatari</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/c/cc/Kizumonogatari_Part_1_Tekketsu_poster.jpeg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Kizumonogatari">Kizumonogatari</a><span class="about-tip-desc">Kizumonogatari is a Japanese anime film trilogy directed by Akiyuki Shinbo and Tatsuya Oishi and produced by Shaft. Together, the films are an adaptation of the 2008 light novel of the same name, which is the second entry in the Monogatari series written by Nisio Isin and a prequel to Bakemonogatari.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/0/02/Hellsing_1.png" alt="Hellsing" width="28" height="28" /><span>Hellsing</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/0/02/Hellsing_1.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Hellsing">Hellsing</a><span class="about-tip-desc">Hellsing is a Japanese manga series written and illustrated by Kouta Hirano. It was serialized in Shonen Gahosha's seinen manga magazine Young King OURs from April 1997 to September 2008, with its chapters collected in ten tankobon volumes.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video115/v4/1f/4c/05/1f4c05ee-429d-2e07-1937-16907bbef90b/pr_source.jpg/600x600bb.jpg" alt="Evangelion" width="28" height="28" /><span>Evangelion</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video115/v4/1f/4c/05/1f4c05ee-429d-2e07-1937-16907bbef90b/pr_source.jpg/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Neon_Genesis_Evangelion">Evangelion</a><span class="about-tip-desc">Neon Genesis Evangelion, also known as simply Evangelion or Eva, is a Japanese anime television series produced by Gainax and Tatsunoko Production, and directed by Hideaki Anno. It was broadcast on TV Tokyo and its affiliates from October 1995 to March 1996.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/d/db/Spirited_Away_Japanese_poster.png" alt="Spirited Away" width="28" height="28" /><span>Spirited Away</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/d/db/Spirited_Away_Japanese_poster.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Spirited_Away">Spirited Away</a><span class="about-tip-desc">Spirited Away is a 2001 Japanese animated fantasy film written and directed by Hayao Miyazaki. It was produced by Toshio Suzuki, animated by Studio Ghibli, and distributed by Toho.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/c0/6e/d9/c06ed98c-251d-1a6c-184c-98a719521e4a/mzl.ezxqyxcc.jpg/600x600bb.jpg" alt="Attack on Titan" width="28" height="28" /><span>Attack on Titan</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/c0/6e/d9/c06ed98c-251d-1a6c-184c-98a719521e4a/mzl.ezxqyxcc.jpg/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Attack_on_Titan_(TV_series)">Attack on Titan</a><span class="about-tip-desc">Attack on Titan is a Japanese dark fantasy anime television series based on the 2009–2021 manga series Attack on Titan by Hajime Isayama. The series premiered on April 7, 2013, and concluded on November 5, 2023. Animated by Wit Studio and MAPPA, the series aired on Mainichi Broadcasting System and NHK General TV.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/a/a1/Cyberpunk_Edgerunners_poster.jpg" alt="Cyberpunk: Edgerunners" width="28" height="28" /><span>Cyberpunk: Edgerunners</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/a/a1/Cyberpunk_Edgerunners_poster.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Cyberpunk:_Edgerunners">Cyberpunk: Edgerunners</a><span class="about-tip-desc">Cyberpunk: Edgerunners is an original net animation (ONA) miniseries created by Rafal Jaki. It was produced by the Polish video game company CD Projekt Red and the Japanese animation studio Trigger, and premiered on Netflix on September 13, 2022.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/b/bc/Interstellar_film_poster.jpg" alt="Interstellar" width="28" height="28" /><span>Interstellar</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/b/bc/Interstellar_film_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Interstellar_(film)">Interstellar</a><span class="about-tip-desc">Interstellar is a 2014 epic scientific fiction film directed by Christopher Nolan, who co-wrote the screenplay with his brother, Jonathan Nolan. It has an ensemble cast led by Matthew McConaughey, Anne Hathaway, Jessica Chastain, Bill Irwin, Ellen Burstyn, and Michael Caine.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/0/0e/Priest_Poster.jpg" alt="Priest" width="28" height="28" /><span>Priest</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/0/0e/Priest_Poster.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Priest_(2011_film)">Priest</a><span class="about-tip-desc">Priest is a 2011 American action horror film directed by Scott Stewart, written by Cory Goodman, and starring Paul Bettany as the title character. It is loosely based on the Korean comic of the same name by Hyung Min-woo.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/6/6e/Mad_Max_Fury_Road.jpg" alt="Mad Max: Fury Road" width="28" height="28" /><span>Mad Max: Fury Road</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/6/6e/Mad_Max_Fury_Road.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Mad_Max:_Fury_Road">Mad Max: Fury Road</a><span class="about-tip-desc">Mad Max: Fury Road is a 2015 Australian post-apocalyptic action film co-written, co-produced and directed by George Miller, who collaborated with Brendan McCarthy and Nico Lathouris on the screenplay.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video113/v4/c6/f7/90/c6f79006-9492-44bb-626c-fa149e147b2d/pr_source.lsr/600x600bb.jpg" alt="Friends" width="28" height="28" /><span>Friends</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video113/v4/c6/f7/90/c6f79006-9492-44bb-626c-fa149e147b2d/pr_source.lsr/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Friends">Friends</a><span class="about-tip-desc">Friends is an American television sitcom created by David Crane and Marta Kauffman, which aired on NBC from September 22, 1994, to May 6, 2004, lasting ten seasons.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video49/v4/a7/c7/4c/a7c74cd4-ab55-e95a-a8d3-752a2bba1036/mzl.ibrfkcdo.lsr/600x600bb.jpg" alt="The Sopranos" width="28" height="28" /><span>The Sopranos</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video49/v4/a7/c7/4c/a7c74cd4-ab55-e95a-a8d3-752a2bba1036/mzl.ibrfkcdo.lsr/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Sopranos">The Sopranos</a><span class="about-tip-desc">The Sopranos is an American crime drama television series created by David Chase for HBO. The series follows Tony Soprano, a New Jersey Mafia boss who has panic attacks.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/af/2d/85/af2d8510-0c8b-4869-4b39-23df93d0edc9/mzl.tdpjxlkl.lsr/600x600bb.jpg" alt="Breaking Bad" width="28" height="28" /><span>Breaking Bad</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/af/2d/85/af2d8510-0c8b-4869-4b39-23df93d0edc9/mzl.tdpjxlkl.lsr/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Breaking_Bad">Breaking Bad</a><span class="about-tip-desc">Breaking Bad is an American neo-Western crime drama television series created by Vince Gilligan for AMC.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/8/8a/Better_Call_Saul_logo.svg/500px-Better_Call_Saul_logo.svg.png" alt="Better Call Saul" width="28" height="28" /><span>Better Call Saul</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/thumb/8/8a/Better_Call_Saul_logo.svg/500px-Better_Call_Saul_logo.svg.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Better_Call_Saul">Better Call Saul</a><span class="about-tip-desc">Better Call Saul is an American neo-noir legal crime drama television series created by Vince Gilligan and Peter Gould for AMC.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/0/05/The_Witcher_Logo.png" alt="The Witcher" width="28" height="28" /><span>The Witcher</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/0/05/The_Witcher_Logo.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Witcher_(TV_series)">The Witcher</a><span class="about-tip-desc">The Witcher is a fantasy drama television series created by Lauren Schmidt Hissrich for Netflix. It is based on the book series by Polish author Andrzej Sapkowski.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/commons/f/f2/Arcane_Title_Text.png" alt="Arcane" width="28" height="28" /><span>Arcane</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/f/f2/Arcane_Title_Text.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Arcane_(TV_series)">Arcane</a><span class="about-tip-desc">Arcane is an animated steampunk action-adventure television series created by Christian Linke and Alex Yee. It was produced by the French animation studio Fortiche, under the supervision of Riot Games, and distributed by Netflix.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/68/The_Boys_TV_series_logo.svg/330px-The_Boys_TV_series_logo.svg.png" alt="The Boys" width="28" height="28" /><span>The Boys</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/thumb/6/68/The_Boys_TV_series_logo.svg/330px-The_Boys_TV_series_logo.svg.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Boys_(TV_series)">The Boys</a><span class="about-tip-desc">The Boys is an American satirical superhero streaming television series developed by Eric Kripke for Amazon Prime Video.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ee/Fallout_television_series_logo.svg/500px-Fallout_television_series_logo.svg.png" alt="Fallout" width="28" height="28" /><span>Fallout</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/thumb/e/ee/Fallout_television_series_logo.svg/500px-Fallout_television_series_logo.svg.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Fallout_(American_TV_series)">Fallout</a><span class="about-tip-desc">Fallout is an American post-apocalyptic drama television series created by Graham Wagner and Geneva Robertson-Dworet for Amazon Prime Video.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/a4/1c/85/a41c85f8-947d-ede3-ebaa-9b5ee2251eb3/mzl.eqyyqnmm.lsr/600x600bb.jpg" alt="Westworld" width="28" height="28" /><span>Westworld</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/a4/1c/85/a41c85f8-947d-ede3-ebaa-9b5ee2251eb3/mzl.eqyyqnmm.lsr/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Westworld_(TV_series)">Westworld</a><span class="about-tip-desc">Westworld is an American dystopian science fiction Western drama television series created by Jonathan Nolan and Lisa Joy that aired from 2016 to 2022 on HBO. It is based upon the 1973 film of the same name written and directed by Michael Crichton and loosely upon its 1976 sequel, Futureworld.</span></span></span></span>
</p>
</div>
</details>
</div>

<details class="about-person" id="stgrikus">
<summary><span class="about-head"><span class="about-avatar-link"><span class="about-avatar-wrap"><img src="https://avatars.fastly.steamstatic.com/55ca41f5225fee88d359222787ebac8f11241fa1_full.jpg" alt="StGrikus" width="96" height="96" /><img src="https://shared.fastly.steamstatic.com/community_assets/images/items/1361210/6a2ff332dc612e923dd1330b12981aa34ebc4895.png" alt=" " width="96" height="96" /></span></span><span class="about-id"><h2 class="about-name"><a class="about-anchor" href="#stgrikus">StGrikus</a></h2><ul class="about-roles"><li>Sound Designer</li><li>Sound Engineer</li><li>Marketing</li></ul></span><span class="about-head-split"></span><span class="about-tops"><span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1361210/capsule_184x69.jpg" alt="Darktide" width="28" height="28" /><span>Darktide</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/1361210/f07ebcb73a34112ac61c54608b1f1ded7e45eb8a/header.jpg?t=1782226781')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/1361210/">Darktide</a><span class="about-tip-date">30 Nov, 2022</span><span class="about-tip-desc">Take back the city of Tertium from hordes of bloodthirsty foes in this intense and brutal action shooter. Warhammer 40,000: Darktide is the new co-op focused experience from the award-winning team behind the Vermintide series. As Tertium falls, Rejects Will Rise.</span></span></span></span><span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/Z_Jp2mlzEjw/mqdefault.jpg" alt="Twenty One Pilots - Car Radio" width="28" height="28" /><span>Twenty One Pilots - Car Radio</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/Z_Jp2mlzEjw/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=Z_Jp2mlzEjw">Twenty One Pilots - Car Radio</a><span class="about-tip-desc">twenty one pilots - Car Radio from Vessel (2011).</span></span></span></span><span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/d/d2/Back_to_the_Future.jpg" alt="Back to the Future" width="28" height="28" /><span>Back to the Future</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/d/d2/Back_to_the_Future.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Back_to_the_Future">Back to the Future</a><span class="about-tip-desc">Back to the Future is a 1985 American science fiction film directed by Robert Zemeckis and written by Zemeckis and Bob Gale. It stars Michael J. Fox, Christopher Lloyd, Lea Thompson, Crispin Glover, and Thomas F. Wilson.</span></span></span></span><span class="fav-chip about-tip-trigger"><img src="https://www.fmod.com/favicon.ico" alt="FMOD" width="28" height="28" /><span>FMOD</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.fmod.com/favicon.ico')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.fmod.com/">FMOD</a><span class="about-tip-desc">Audio middleware for games - events, mixing, and spatial sound.</span></span></span></span></span></span></summary>
<div class="about-row">
<div class="about-section">
<div class="about-section-label">About</div>
<p class="about-note">Technical sound designer. 2012: started learning guitar, and music and sound have absorbed me ever since. Started studying <span class="about-tip-trigger">FMOD<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.fmod.com/favicon.ico')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.fmod.com/">FMOD</a><span class="about-tip-desc">Audio middleware for games - events, mixing, and spatial sound.</span></span></span></span> and how sound works in games in 2025. Spent too much time in <span class="about-tip-trigger">CS:GO<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/730/162664aa5da85f418105350c5d67ca565f6c3713/header.jpg?t=1784564069')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/730/">CS:GO</a><span class="about-tip-date">21 Aug, 2012</span><span class="about-tip-desc">For over two decades, Counter-Strike has offered an elite competitive experience, one shaped by millions of players from across the globe. And now the next chapter in the CS story is about to begin. This is Counter-Strike 2.</span></span></span></span>. Hobbies: guitar, skateboarding.</p>
</div>
<div class="about-section">
<div class="about-section-label">Likes</div>
<p class="about-note">Analyzing song structure and soundstage, <span class="about-tip-trigger">Da Hong Pao<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/2/29/Da_Hong_Pao_Oolong_tea_leaf.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Da_Hong_Pao">Da Hong Pao</a><span class="about-tip-desc">Da Hong Pao is a Wuyi rock tea grown in the Wuyi Mountains of Fujian Province, China. Da Hong Pao has a unique orchid fragrance and a long-lasting sweet aftertaste. Dry Da Hong Pao has a shape like tightly knotted ropes or slightly twisted strips, and is green and brown in color.</span></span></span></span>, White Oolong.</p>
<div class="fav-colors">
<span class="fav-chip"><span class="fav-swatch purple"></span><span>Purple</span></span>
<span class="fav-chip"><span class="fav-swatch ultramarine"></span><span>#120A8F</span></span>
</div>
</div>
</div>
<div class="about-section">
<div class="about-section-label">Coffee</div>
<p class="about-note">2021: got into coffee by drinking V60, Chemex, and AeroPress in cafés. After getting a V60 for my birthday, started brewing at home and going deeper into beans. Autumn 2023: joined one of the city's best coffee shops and dove into processing, roasting, brewing, and how origins differ. Mid-2024: placed 2nd in a Brewers Cup, brewing Hario Switch and V60. Taught brewing workshops, lectured on coffee varieties and processing methods, and hosted open cuppings.</p>
<p class="about-note">Favorite brew methods: <span class="about-tip-trigger">Hario Switch<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.hario-usa.com/cdn/shop/files/switch-immersion-dripper-01.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.hario-usa.com/products/switch-immersion-dripper">Hario Switch</a><span class="about-tip-desc">Hario Switch - immersion dripper that can also pour-over.</span></span></span></span>, <span class="about-tip-trigger">Chemex<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/a/a9/Peter_Schlumbohm._Coffee_Maker%2C_Designed_1941.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Chemex_Coffeemaker">Chemex</a><span class="about-tip-desc">The Chemex Coffeemaker is a manual pour-over style glass coffeemaker, invented by Peter Schlumbohm in 1941, manufactured by the Chemex Corporation in Chicopee, Massachusetts.</span></span></span></span>, <span class="about-tip-trigger">V60<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.hario-usa.com/cdn/shop/products/v60-ceramic-02.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.hario-usa.com/products/v60-coffee-dripper-02-ceramic">V60</a><span class="about-tip-desc">Hario V60 ceramic pour-over dripper.</span></span></span></span>.</p>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://heatroasters.com/wp-content/uploads/2026/04/grape-775x1024.png" alt="Colombia Grape" width="28" height="28" /><span>Colombia Grape</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://heatroasters.com/wp-content/uploads/2026/04/grape-775x1024.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://heatroasters.com/product/colombia-grape/">Colombia Grape</a><span class="about-tip-desc">Armenia, co-fermentation</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://heatroasters.com/wp-content/uploads/2026/02/paraiso92-775x1024.png" alt="Colombia Paraiso 92" width="28" height="28" /><span>Colombia Paraiso 92</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://heatroasters.com/wp-content/uploads/2026/02/paraiso92-775x1024.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://heatroasters.com/product/colombia-paraiso-92/">Colombia Paraiso 92</a><span class="about-tip-desc">Huila, washed, yeast fermentation and thermal shock</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://heatroasters.com/wp-content/uploads/2026/02/tres-letras.png" alt="Colombia Tres Letras" width="28" height="28" /><span>Colombia Tres Letras</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://heatroasters.com/wp-content/uploads/2026/02/tres-letras.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://heatroasters.com/product/colombia-tres-letras/">Colombia Tres Letras</a><span class="about-tip-desc">Arauca, natural</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://heatroasters.com/wp-content/uploads/2026/02/gachata-775x1024.png" alt="Kenya Gachatha" width="28" height="28" /><span>Kenya Gachatha</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://heatroasters.com/wp-content/uploads/2026/02/gachata-775x1024.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://heatroasters.com/product/kenya-gachatha/">Kenya Gachatha</a><span class="about-tip-desc">Nyeri, washed</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://heatroasters.com/wp-content/uploads/2026/02/gerba-dogo-1-775x1024.png" alt="Ethiopia Gerba Dogo" width="28" height="28" /><span>Ethiopia Gerba Dogo</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://heatroasters.com/wp-content/uploads/2026/02/gerba-dogo-1-775x1024.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://heatroasters.com/product/ethiopia-gerba-dogo/">Ethiopia Gerba Dogo</a><span class="about-tip-desc">Guji, natural</span></span></span></span>
</p>
</div>
<div class="about-row about-meta">
<div class="about-section">
<div class="about-section-label">Media</div>
<p class="fav-row fav-compact">
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="Steam" width="28" height="28" /><span>Steam</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/steam/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://steamcommunity.com/id/grikus">Steam</a><span class="about-tip-desc">StGrikus on Steam.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/instagram/E4405F" alt="Instagram" width="28" height="28" /><span>Instagram</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/instagram/E4405F')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.instagram.com/stgrikus/">Instagram</a><span class="about-tip-desc">StGrikus on Instagram.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/telegram/26A5E4" alt="Telegram" width="28" height="28" /><span>Telegram</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/telegram/26A5E4')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://t.me/stgrikussound">Telegram</a><span class="about-tip-desc">StGrikus sound Telegram.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/twitch/9146FF" alt="Twitch" width="28" height="28" /><span>Twitch</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/twitch/9146FF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.twitch.tv/stgrikus">Twitch</a><span class="about-tip-desc">StGrikus on Twitch.</span></span></span></span>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Tools</div>
<p class="fav-row fav-compact">
<span class="fav-chip about-tip-trigger"><img src="https://www.fmod.com/favicon.ico" alt="FMOD" width="28" height="28" /><span>FMOD</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.fmod.com/favicon.ico')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.fmod.com/">FMOD</a><span class="about-tip-desc">Audio middleware for games - events, mixing, and spatial sound.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/6/69/FL_Studio_11_just_logo.png/120px-FL_Studio_11_just_logo.png" alt="FL Studio" width="28" height="28" /><span>FL Studio</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/thumb/6/69/FL_Studio_11_just_logo.png/120px-FL_Studio_11_just_logo.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.image-line.com/">FL Studio</a><span class="about-tip-desc">FL Studio DAW for composing, arranging, and mixing.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://www.reaper.fm/v5img/logo.jpg" alt="REAPER" width="28" height="28" /><span>REAPER</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://www.reaper.fm/v5img/logo.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.reaper.fm/">REAPER</a><span class="about-tip-desc">REAPER digital audio workstation for recording and mixing.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/unity/FFFFFF" alt="Unity" width="28" height="28" /><span>Unity</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/unity/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://unity.com/">Unity</a><span class="about-tip-desc">Real-time 3D engine used to make the studio games.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/cursor/FFFFFF" alt="Cursor" width="28" height="28" /><span>Cursor</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/cursor/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://cursor.com/">Cursor</a><span class="about-tip-desc">AI code editor used to write and ship the games and this site.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/davinciresolve/FFFFFF" alt="DaVinci Resolve" width="28" height="28" /><span>DaVinci Resolve</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/davinciresolve/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.blackmagicdesign.com/products/davinciresolve">DaVinci Resolve</a><span class="about-tip-desc">DaVinci Resolve - editing, color, and audio post.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Adobe_Photoshop_CC_icon.svg/120px-Adobe_Photoshop_CC_icon.svg.png" alt="Photoshop" width="28" height="28" /><span>Photoshop</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Adobe_Photoshop_CC_icon.svg/120px-Adobe_Photoshop_CC_icon.svg.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.adobe.com/products/photoshop.html">Photoshop</a><span class="about-tip-desc">Adobe Photoshop for image editing and textures.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.simpleicons.org/obsstudio/FFFFFF" alt="OBS Studio" width="28" height="28" /><span>OBS Studio</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.simpleicons.org/obsstudio/FFFFFF')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://obsproject.com/">OBS Studio</a><span class="about-tip-desc">OBS Studio - free software for recording and livestreaming.</span></span></span></span>
</p>
</div>
</div>
<div class="about-section">
<div class="about-section-label">Games</div>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1361210/capsule_184x69.jpg" alt="Darktide" width="28" height="28" /><span>Darktide</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/1361210/f07ebcb73a34112ac61c54608b1f1ded7e45eb8a/header.jpg?t=1782226781')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/1361210/">Darktide</a><span class="about-tip-date">30 Nov, 2022</span><span class="about-tip-desc">Take back the city of Tertium from hordes of bloodthirsty foes in this intense and brutal action shooter. Warhammer 40,000: Darktide is the new co-op focused experience from the award-winning team behind the Vermintide series. As Tertium falls, Rejects Will Rise.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/22380/capsule_184x69.jpg" alt="Fallout New Vegas" width="28" height="28" /><span>Fallout: New Vegas</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/22380/header.jpg?t=1765992876')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/22380/">Fallout: New Vegas</a><span class="about-tip-date">21 Oct, 2010</span><span class="about-tip-desc">Welcome to Vegas. New Vegas. Enjoy your stay!</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/553850/capsule_184x69.jpg" alt="HELLDIVERS 2" width="28" height="28" /><span>HELLDIVERS 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/553850/850e2f9e5bb15c5706bb9a1edc832f4f782e8be5/header.jpg?t=1786525389')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/553850/">HELLDIVERS 2</a><span class="about-tip-date">8 Feb, 2024</span><span class="about-tip-desc">The Galaxy’s Last Line of Offence. Enlist in the Helldivers and join the fight for freedom across a hostile galaxy in a fast, frantic, and ferocious third-person shooter.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/427520/capsule_184x69.jpg" alt="Factorio" width="28" height="28" /><span>Factorio</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/427520/header.jpg?t=1763986204')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/427520/">Factorio</a><span class="about-tip-date">14 Aug, 2020</span><span class="about-tip-desc">Factorio is a game about building and creating automated factories to produce items of increasing complexity, within an infinite 2D world. Use your imagination to design your factory, combine simple elements into ingenious structures, and finally protect it from the creatures who don't really like you.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/892970/capsule_184x69.jpg" alt="Valheim" width="28" height="28" /><span>Valheim</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/892970/de0bdcf6c008c508a79d8e75eb91fc67f4bebd5d/header.jpg?t=1786012504')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/892970/">Valheim</a><span class="about-tip-date">2 Feb, 2021</span><span class="about-tip-desc">A brutal exploration and survival game for 1-10 players, set in a procedurally-generated purgatory inspired by viking culture. Battle, build, and conquer your way to a saga worthy of Odin’s patronage!</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/632360/capsule_184x69.jpg" alt="Risk of Rain 2" width="28" height="28" /><span>Risk of Rain 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/632360/header.jpg?t=1783621122')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/632360/">Risk of Rain 2</a><span class="about-tip-date">11 Aug, 2020</span><span class="about-tip-desc">Escape a chaotic alien planet by fighting through hordes of frenzied monsters – with your friends, or on your own. Combine loot in surprising ways and master each character until you become the havoc you feared upon your first crash landing.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/570/capsule_184x69.jpg" alt="Dota 2" width="28" height="28" /><span>Dota 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/570/header.jpg?t=1769535998')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/570/">Dota 2</a><span class="about-tip-date">9 Jul, 2013</span><span class="about-tip-desc">Every day, millions of players worldwide enter battle as one of over a hundred Dota heroes. And no matter if it's their 10th hour of play or 1,000th, there's always something new to discover. With regular updates that ensure a constant evolution of gameplay, features, and heroes, Dota 2 has taken on a life of its own.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1086940/capsule_184x69.jpg" alt="Baldur's Gate 3" width="28" height="28" /><span>Baldur's Gate 3</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/1086940/48a2fcbda8565bb45025e98fd8ebde8a7203f6a0/header.jpg?t=1777363040')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/1086940/">Baldur's Gate 3</a><span class="about-tip-date">3 Aug, 2023</span><span class="about-tip-desc">Baldur’s Gate 3 is a story-rich, party-based RPG set in the universe of Dungeons &amp; Dragons, where your choices shape a tale of fellowship and betrayal, survival and sacrifice, and the lure of absolute power.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/227300/capsule_184x69.jpg" alt="Euro Truck Simulator 2" width="28" height="28" /><span>Euro Truck Simulator 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/227300/9a81dc3126c56637297b654f9dcac057cfd79b77/header.jpg?t=1785394779')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/227300/">Euro Truck Simulator 2</a><span class="about-tip-date">12 Oct, 2012</span><span class="about-tip-desc">Travel across Europe as king of the road, a trucker who delivers important cargo across impressive distances! With dozens of cities to explore, your endurance, skill and speed will all be pushed to their limits.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/22350/capsule_184x69.jpg" alt="Brink" width="28" height="28" /><span>Brink</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/22350/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/22350/">Brink</a><span class="about-tip-date">10 May, 2011</span><span class="about-tip-desc">A first-person shooter with parkour movement. Fight for security or resistance on the floating city of The Ark.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/1/1b/Vintage_Story_Logo.png" alt="Vintage Story" width="28" height="28" /><span>Vintage Story</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/1/1b/Vintage_Story_Logo.png')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://www.vintagestory.at/">Vintage Story</a><span class="about-tip-desc">Vintage Story is a voxel survival sandbox with deep crafting, smithing, and seasons.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/2186680/capsule_184x69.jpg" alt="Warhammer 40,000: Rogue Trader" width="28" height="28" /><span>Warhammer 40,000: Rogue Trader</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/2186680/c7b0bd6f233f6c03fa68eee2fd1108a183329230/header.jpg?t=1781198086')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/2186680/">Warhammer 40,000: Rogue Trader</a><span class="about-tip-date">7 Dec, 2023</span><span class="about-tip-desc">Made in a close partnership with Games Workshop, Warhammer 40,000: Rogue Trader is a story-rich classical RPG from Owlcat Games, developers of the critically acclaimed game, Pathfinder: Wrath of the Righteous.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/231430/capsule_184x69.jpg" alt="Company of Heroes 2" width="28" height="28" /><span>Company of Heroes 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/231430/header.jpg?t=1750947634')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/231430/">Company of Heroes 2</a><span class="about-tip-date">25 Jun, 2013</span><span class="about-tip-desc">Experience the ultimate WWII RTS platform with COH2 and its standalone expansions. This package includes the base game, which you can then upgrade by purchasing The Western Front Armies, Ardennes Assault and/or The British Forces. More info in the "About This Game" section below.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/489830/capsule_184x69.jpg" alt="Skyrim" width="28" height="28" /><span>Skyrim</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/489830/header.jpg?t=1786648247')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/489830/">Skyrim</a><span class="about-tip-date">27 Oct, 2016</span><span class="about-tip-desc">Winner of more than 200 Game of the Year Awards, The Elder Scrolls V: Skyrim Special Edition brings the epic fantasy to life in stunning detail. The Special Edition includes the critically acclaimed game and add-ons with all-new features.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/990080/capsule_184x69.jpg" alt="Hogwarts Legacy" width="28" height="28" /><span>Hogwarts Legacy</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/990080/a3cdc6f40d97df8ac993679c2dd1edeb5222421e/header.jpg?t=1778797474')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/990080/">Hogwarts Legacy</a><span class="about-tip-date">10 Feb, 2023</span><span class="about-tip-desc">Hogwarts Legacy is an immersive, open-world action RPG. Now you can take control of the action and be at the center of your own adventure in the wizarding world.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/271590/capsule_184x69.jpg" alt="GTA V" width="28" height="28" /><span>GTA V</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/271590/header.jpg?t=1765387725')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/271590/">GTA V</a><span class="about-tip-date">13 Apr, 2015</span><span class="about-tip-desc">Grand Theft Auto V for PC offers players the option to explore the award-winning world of Los Santos and Blaine County in resolutions of up to 4k and beyond, as well as the chance to experience the game running at 60 frames per second.</span></span></span></span>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Music</div>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/Z_Jp2mlzEjw/mqdefault.jpg" alt="Twenty One Pilots - Car Radio" width="28" height="28" /><span>Twenty One Pilots - Car Radio</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/Z_Jp2mlzEjw/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=Z_Jp2mlzEjw">Twenty One Pilots - Car Radio</a><span class="about-tip-desc">twenty one pilots - Car Radio from Vessel (2011).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/dML7QMkbpnQ/mqdefault.jpg" alt="The Midnight - Summer's Ending Soon" width="28" height="28" /><span>The Midnight - Summer's Ending Soon</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/dML7QMkbpnQ/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=dML7QMkbpnQ">The Midnight - Summer's Ending Soon</a><span class="about-tip-desc">The Midnight - Summer's Ending Soon from Syndicate (2025).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/Wk9mMbOpAaA/mqdefault.jpg" alt="GUNSHIP - When You Grow up, Your Heart Dies" width="28" height="28" /><span>GUNSHIP - When You Grow up, Your Heart Dies</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/Wk9mMbOpAaA/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=Wk9mMbOpAaA">GUNSHIP - When You Grow up, Your Heart Dies</a><span class="about-tip-desc">GUNSHIP - When You Grow Up, Your Heart Dies from Dark All Day (2018).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/vJ1oyOazhEk/mqdefault.jpg" alt="Kavinsky - Odd Look" width="28" height="28" /><span>Kavinsky - Odd Look</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/vJ1oyOazhEk/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=vJ1oyOazhEk">Kavinsky - Odd Look</a><span class="about-tip-desc">Kavinsky - Odd Look.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/d5vRK1fubEE/mqdefault.jpg" alt="Nothing More - Still In Love" width="28" height="28" /><span>Nothing More - Still In Love</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/d5vRK1fubEE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=d5vRK1fubEE">Nothing More - Still In Love</a><span class="about-tip-desc">NOTHING MORE - Still in Love from The Stories We Tell Ourselves (2017).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/9B1Dbimbnl4/mqdefault.jpg" alt="Radiotehnika - радионочь" width="28" height="28" /><span>Radiotehnika - радионочь</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/9B1Dbimbnl4/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=9B1Dbimbnl4">Radiotehnika - радионочь</a><span class="about-tip-desc">radiotehnika - радионочь.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/DdLMr4aj0iE/mqdefault.jpg" alt="Kalax - Through It All" width="28" height="28" /><span>Kalax - Through It All</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/DdLMr4aj0iE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=DdLMr4aj0iE">Kalax - Through It All</a><span class="about-tip-desc">Kalax - Through It All from 11-11 - EP (2026).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/CtiuMnhP3Qk/mqdefault.jpg" alt="TOOL - Invincible" width="28" height="28" /><span>TOOL - Invincible</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/CtiuMnhP3Qk/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=CtiuMnhP3Qk">TOOL - Invincible</a><span class="about-tip-desc">TOOL - Invincible from Fear Inoculum (2019).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/DowAWZgDO8c/mqdefault.jpg" alt="Red Hot Chili Peppers - The Adventures of Rain Dance Maggie" width="28" height="28" /><span>Red Hot Chili Peppers - The Adventures of Rain Dance Maggie</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/DowAWZgDO8c/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=DowAWZgDO8c">Red Hot Chili Peppers - The Adventures of Rain Dance Maggie</a><span class="about-tip-desc">Red Hot Chili Peppers - The Adventures of Rain Dance Maggie from I'm With You (2011).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/RRMbhEdmhYw/mqdefault.jpg" alt="Daft Punk - Touch (feat. Paul Williams)" width="28" height="28" /><span>Daft Punk - Touch (feat. Paul Williams)</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/RRMbhEdmhYw/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=RRMbhEdmhYw">Daft Punk - Touch (feat. Paul Williams)</a><span class="about-tip-desc">Daft Punk &amp; Paul Williams - Touch from Random Access Memories (2013).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/Obim8BYGnOE/mqdefault.jpg" alt="Eminem - Till I Collapse" width="28" height="28" /><span>Eminem - Till I Collapse</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/Obim8BYGnOE/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=Obim8BYGnOE">Eminem - Till I Collapse</a><span class="about-tip-desc">Eminem - 'Till I Collapse (feat. Nate Dogg) from The Eminem Show (2002).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/5H99tg2_pwA/mqdefault.jpg" alt="Linkin Park - Leave Out All The Rest" width="28" height="28" /><span>Linkin Park - Leave Out All The Rest</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/5H99tg2_pwA/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=5H99tg2_pwA">Linkin Park - Leave Out All The Rest</a><span class="about-tip-desc">LINKIN PARK - Leave Out All The Rest from Minutes to Midnight (Deluxe Edition) (2007).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/av2xYzcSO-Q/mqdefault.jpg" alt="Cathode Electrode - Time Machine" width="28" height="28" /><span>Cathode Electrode - Time Machine</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/av2xYzcSO-Q/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=av2xYzcSO-Q">Cathode Electrode - Time Machine</a><span class="about-tip-desc">Cathode Electrode - Time Machine from 1985 (2022).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://img.youtube.com/vi/2kc4cyBZ7dw/mqdefault.jpg" alt="Drake Bell - Honest" width="28" height="28" /><span>Drake Bell - Honest</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://img.youtube.com/vi/2kc4cyBZ7dw/hqdefault.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://music.youtube.com/watch?v=2kc4cyBZ7dw">Drake Bell - Honest</a><span class="about-tip-desc">Drake Bell - Honest from Honest - EP (2017).</span></span></span></span>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Movies/series/cartoons</div>
<p class="fav-row">
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/d/d2/Back_to_the_Future.jpg" alt="Back to the Future" width="28" height="28" /><span>Back to the Future</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/d/d2/Back_to_the_Future.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Back_to_the_Future">Back to the Future</a><span class="about-tip-desc">Back to the Future is a 1985 American science fiction film directed by Robert Zemeckis and written by Zemeckis and Bob Gale. It stars Michael J. Fox, Christopher Lloyd, Lea Thompson, Crispin Glover, and Thomas F. Wilson.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/c0/6e/d9/c06ed98c-251d-1a6c-184c-98a719521e4a/mzl.ezxqyxcc.jpg/600x600bb.jpg" alt="Attack on Titan" width="28" height="28" /><span>Attack on Titan</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://is1-ssl.mzstatic.com/image/thumb/Video118/v4/c0/6e/d9/c06ed98c-251d-1a6c-184c-98a719521e4a/mzl.ezxqyxcc.jpg/600x600bb.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Attack_on_Titan_(TV_series)">Attack on Titan</a><span class="about-tip-desc">Attack on Titan is a Japanese dark fantasy anime television series based on the 2009–2021 manga series Attack on Titan by Hajime Isayama. The series premiered on April 7, 2013, and concluded on November 5, 2023. Animated by Wit Studio and MAPPA, the series aired on Mainichi Broadcasting System and NHK General TV.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/b/bc/Interstellar_film_poster.jpg" alt="Interstellar" width="28" height="28" /><span>Interstellar</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/b/bc/Interstellar_film_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Interstellar_(film)">Interstellar</a><span class="about-tip-desc">Interstellar is a 2014 epic scientific fiction film directed by Christopher Nolan, who co-wrote the screenplay with his brother, Jonathan Nolan. It has an ensemble cast led by Matthew McConaughey, Anne Hathaway, Jessica Chastain, Bill Irwin, Ellen Burstyn, and Michael Caine.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/2/2e/Inception_%282010%29_theatrical_poster.jpg" alt="Inception" width="28" height="28" /><span>Inception</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/2/2e/Inception_%282010%29_theatrical_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Inception">Inception</a><span class="about-tip-desc">Inception is a 2010 science fiction action film written and directed by Christopher Nolan, who also produced it with Emma Thomas, his wife. The film stars Leonardo DiCaprio as a professional thief who steals information by infiltrating the subconscious of his targets.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/e/e1/Joker_%282019_film%29_poster.jpg" alt="Joker" width="28" height="28" /><span>Joker</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/e/e1/Joker_%282019_film%29_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Joker_(2019_film)">Joker</a><span class="about-tip-desc">Joker is a 2019 American psychological thriller film directed by Todd Phillips from a screenplay he co-wrote with Scott Silver. Based on DC Comics characters, it stars Joaquin Phoenix and provides an alternative origin story for the Joker.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/3/39/Soul_%282020_film%29_poster.jpg" alt="Soul" width="28" height="28" /><span>Soul</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/3/39/Soul_%282020_film%29_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Soul_(2020_film)">Soul</a><span class="about-tip-desc">Soul is a 2020 American animated fantasy comedy-drama film produced by Pixar Animation Studios for Walt Disney Pictures.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/6/6e/Luck_%282022%29_poster.png" alt="Luck" width="28" height="28" /><span>Luck</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/6/6e/Luck_%282022%29_poster.png?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Luck_(2022_film)">Luck</a><span class="about-tip-desc">Luck is a 2022 American animated fantasy comedy film directed by Peggy Holmes from a screenplay written by Kiel Murray, and a story conceived by Murray and the writing team of Jonathan Aibel and Glenn Berger, based on an original concept created by Rebeca Carrasco, Juan De Dios, and Julián Romero.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/6/68/Worlds_fastest_indian.jpg" alt="The World's Fastest Indian" width="28" height="28" /><span>The World's Fastest Indian</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/6/68/Worlds_fastest_indian.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_World%27s_Fastest_Indian">The World's Fastest Indian</a><span class="about-tip-desc">The World's Fastest Indian is a 2005 New Zealand biographical sports drama film based on the story of New Zealand speed bike racer Burt Munro and his highly modified 1920 Indian Scout motorcycle.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/commons/b/b1/Rick_and_Morty.svg" alt="Rick and Morty" width="28" height="28" /><span>Rick and Morty</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/commons/b/b1/Rick_and_Morty.svg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Rick_and_Morty">Rick and Morty</a><span class="about-tip-desc">Rick and Morty is an American adult animated science fiction sitcom created by Justin Roiland and Dan Harmon for Cartoon Network's nighttime programming block Adult Swim.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/8/8a/Hacksaw_Ridge_poster.png" alt="Hacksaw Ridge" width="28" height="28" /><span>Hacksaw Ridge</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/8/8a/Hacksaw_Ridge_poster.png?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Hacksaw_Ridge">Hacksaw Ridge</a><span class="about-tip-desc">Hacksaw Ridge is a 2016 epic biographical war film directed by Mel Gibson, and starring Andrew Garfield as Desmond Doss, an American combat medic in World War II who, as a Seventh-day Adventist, refused to use a weapon of any kind; Doss became the first conscientious objector to be awarded the Medal of Honor, for his s...</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/0/02/Iron_Man_%282008_film%29_poster.jpg" alt="Iron Man" width="28" height="28" /><span>Iron Man</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/0/02/Iron_Man_%282008_film%29_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Iron_Man_(2008_film)">Iron Man</a><span class="about-tip-desc">Iron Man is a 2008 American superhero film based on the Marvel Comics character Iron Man. Produced by Marvel Studios and distributed by Paramount Pictures, it is the first film in the Marvel Cinematic Universe (MCU).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/e/ed/Iron_Man_2_poster.jpg" alt="Iron Man 2" width="28" height="28" /><span>Iron Man 2</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/e/ed/Iron_Man_2_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Iron_Man_2">Iron Man 2</a><span class="about-tip-desc">Iron Man 2 is a 2010 American superhero film based on the Marvel Comics character Iron Man. Produced by Marvel Studios and distributed by Paramount Pictures, it is the sequel to Iron Man (2008) and the third film in the Marvel Cinematic Universe (MCU).</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/a/af/Batman_Begins_Poster.jpg" alt="Batman Begins" width="28" height="28" /><span>Batman Begins</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/a/af/Batman_Begins_Poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Batman_Begins">Batman Begins</a><span class="about-tip-desc">Batman Begins is a 2005 superhero film based on the DC Comics character Batman. Directed by Christopher Nolan, who co-wrote the screenplay with David S.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/4/4a/Oppenheimer_%28film%29.jpg" alt="Oppenheimer" width="28" height="28" /><span>Oppenheimer</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/4/4a/Oppenheimer_%28film%29.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Oppenheimer_(film)">Oppenheimer</a><span class="about-tip-desc">Oppenheimer is a 2023 epic biographical thriller film written, co-produced, and directed by Christopher Nolan. It follows the life of J. Robert Oppenheimer, the American theoretical physicist who helped develop the first nuclear weapons during World War II.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/4/4b/The_Mask_%28film%29_poster.jpg" alt="The Mask" width="28" height="28" /><span>The Mask</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/4/4b/The_Mask_%28film%29_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/The_Mask_(1994_film)">The Mask</a><span class="about-tip-desc">The Mask is a 1994 American superhero slapstick comedy film loosely based on the 1991 comic book series by John Arcudi and Doug Mahnke. Directed by Chuck Russell and written by Mike Werb, the film stars Jim Carrey in the title role, along with Peter Riegert, Peter Greene, Amy Yasbeck, Richard Jeni, and Cameron Diaz.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://m.media-amazon.com/images/M/MV5BNmM3MWFkZjctYzBhNC00YWU1LWIzYTktZjUxMzYyNGE5MjhlXkEyXkFqcGc@._V1_.jpg" alt="Drake &amp; Josh" width="28" height="28" /><span>Drake &amp; Josh</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/thumb/f/f8/Drake_%26_Josh_Nickelodeon_Logo.svg/500px-Drake_%26_Josh_Nickelodeon_Logo.svg.png?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/Drake_%26_Josh">Drake &amp; Josh</a><span class="about-tip-desc">Drake &amp; Josh is an American buddy teen sitcom created by Dan Schneider for Nickelodeon. The series follows teenage stepbrothers Drake Parker and Josh Nichols as they live together despite their opposite personalities.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/0/03/Leon-poster.jpg" alt="Léon: The Professional" width="28" height="28" /><span>Léon: The Professional</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/0/03/Leon-poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/L%C3%A9on:_The_Professional">Léon: The Professional</a><span class="about-tip-desc">Léon is a 1994 French English-language action-thriller film written and directed by Luc Besson. It stars Jean Reno, Gary Oldman and Natalie Portman in her feature film debut.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/1/1e/8_Mile_official_poster.jpg" alt="8 Mile" width="28" height="28" /><span>8 Mile</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/1/1e/8_Mile_official_poster.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/8_Mile_(film)">8 Mile</a><span class="about-tip-desc">8 Mile is a 2002 American hip-hop biographical drama film produced and directed by Curtis Hanson from a script written by Scott Silver. It stars Eminem in his feature film debut, alongside Kim Basinger, Brittany Murphy, and Mekhi Phifer.</span></span></span></span>
<span class="fav-chip about-tip-trigger"><img src="https://upload.wikimedia.org/wikipedia/en/e/e4/28_days_later.jpg" alt="28 Days Later" width="28" height="28" /><span>28 Days Later</span><span class="about-tip"><span class="about-tip-art" style="background-image:url('https://upload.wikimedia.org/wikipedia/en/e/e4/28_days_later.jpg?utm_source=en.wikipedia.org&amp;utm_campaign=api&amp;utm_content=thumbnail_unscaled')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://en.wikipedia.org/wiki/28_Days_Later">28 Days Later</a><span class="about-tip-desc">28 Days Later is a 2002 British post-apocalyptic horror film directed by Danny Boyle and written by Alex Garland. It stars Cillian Murphy as a bicycle courier who awakens from a coma to discover that the accidental release of a highly contagious, aggression-inducing virus has caused the breakdown of society.</span></span></span></span>
</p>
</div>
</details>

<script>
(function () {
  if (window.__aboutPersonAnchors) return;
  window.__aboutPersonAnchors = true;
  function openFromHash() {
    var id = decodeURIComponent((location.hash || "").replace(/^#/, ""));
    if (!id) return;
    var el = document.getElementById(id);
    if (!el || el.tagName !== "DETAILS") return;
    el.open = true;
    el.scrollIntoView({ behavior: "smooth", block: "start" });
  }
  document.querySelectorAll("a.about-anchor").forEach(function (a) {
    a.addEventListener("click", function (e) {
      var href = a.getAttribute("href") || "";
      if (href.charAt(0) !== "#") return;
      e.preventDefault();
      e.stopPropagation();
      history.replaceState(null, "", href);
      openFromHash();
    });
  });
  window.addEventListener("hashchange", openFromHash);
  openFromHash();
  document.querySelectorAll(".about-person > summary .about-tip-trigger").forEach(function (el) {
    el.addEventListener("click", function (e) { e.stopPropagation(); });
  });
})();
</script>
