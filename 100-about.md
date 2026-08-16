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
  overflow: hidden;
  border: none;
  box-shadow: none;
}
.about-tops > a.fav-chip:hover {
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
.about-note a {
  color: var(--color-primary);
  text-decoration: none;
}
.about-note a:hover {
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
a.fav-chip { color: var(--color-primary); }
a.fav-chip:hover {
  color: var(--color-primary-hover);
  border-color: var(--color-primary);
}

.fav-row {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
  grid-template-rows: masonry;
  grid-auto-flow: dense;
  gap: 6px;
  margin: 0;
  align-items: start;
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
  overflow: hidden;
  isolation: isolate;
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
  margin: 0 !important;
  border-radius: 0 !important;
  box-shadow: none !important;
  object-fit: cover;
  background: #161b22;
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

.fav-row > .fav-chip span,
.about-tops > .fav-chip span {
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
.fav-compact > .fav-chip span {
  font-size: 0.62em;
  padding: 3px;
}
.fav-row > .fav-chip:hover span,
.fav-row > .fav-chip:focus-visible span,
.about-tops > .fav-chip:hover span,
.about-tops > .fav-chip:focus-visible span {
  opacity: 1;
}
.fav-row > a.fav-chip:hover { text-decoration: none; }
.fav-row > a.fav-chip:hover span,
.about-tops > a.fav-chip:hover span { text-decoration: underline; }

.fav-row > .fav-chip:first-child {
  border-color: rgba(212, 175, 55, 0.55);
  box-shadow: 0 0 18px 8px rgba(212, 175, 55, 0.22);
}
.fav-row > a.fav-chip:first-child:hover {
  border-color: rgba(240, 208, 96, 0.7);
  box-shadow: 0 0 22px 10px rgba(240, 208, 96, 0.28);
}
.about-meta .fav-row > .fav-chip:first-child {
  border-color: #30363d;
  box-shadow: none;
}
.about-meta .fav-row > a.fav-chip:first-child:hover {
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
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 3px 8px 3px 4px;
  max-width: 100%;
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
.about-studio a {
  position: relative;
  color: var(--color-primary);
  text-decoration: none;
}
.about-studio a:hover {
  color: var(--color-primary-hover);
  text-decoration: underline;
}
.about-tip {
  display: none;
  position: absolute;
  left: 0;
  top: calc(100% + 6px);
  z-index: 50;
  width: 272px;
  pointer-events: none;
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
.about-studio a:hover > .about-tip {
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
.about-tip-body {
  display: block;
  padding: 8px 10px 10px;
}
.about-tip-title {
  display: inline;
  font-size: 0.95em;
  font-weight: 600;
  color: var(--color-primary);
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

<p class="about-studio">Inspired by <a href="https://store.steampowered.com/app/823500/">BONEWORKS<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/823500/header.jpg')"></span><span class="about-tip-body"><span class="about-tip-title">BONEWORKS</span><span class="about-tip-date">10 Dec 2019</span><span class="about-tip-desc">BONEWORKS is an Experimental Physics VR Adventure. Use found physics weapons, tools, and objects to fight across dangerous playscapes and mysterious architecture.</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Best VR adventure I experienced. Physical climbing is fun, feels like cheating. Many paths to approach problems. I love entering a room, pushing doors open using gun barrels and then blasting the null bodies. Still the best VR game for me.</span></span></span></a> and VR tech, we gathered a team to make <a href="https://store.steampowered.com/app/1775350/RISING_BONEvR/">RISING BONEvR<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/1775350/header.jpg')"></span><span class="about-tip-body"><span class="about-tip-title">RISING BONEvR</span><span class="about-tip-date">demo 7 Nov 2021</span><span class="about-tip-desc">(First level demo available!) Physics based puzzle about climbing out of deep hell without any legs</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Quite a challenge to implement VR physics similar to BONEWORKS. Learned more math, vectors, matrices. Level design is terrible, physics clunky, but gameplay was fun when it works. My first proper C# game, and fiancee StTaya helped by making her first 3D models in Blender. Some day we'll continue - we learned many new lessons since then.</span></span></span></a> <small>(demo 7 Nov 2021)</small>. Now focused on our dream-game <a href="https://store.steampowered.com/app/2980830/COLLAPSE_MACHINE">COLLAPSE MACHINE<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/2980830/header.jpg')"></span><span class="about-tip-body"><span class="about-tip-title">COLLAPSE MACHINE</span><span class="about-tip-date">since Sep 2023</span><span class="about-tip-desc">In COLLAPSE MACHINE - scavenge, raid, and survive a super-magnetic wasteland in co-op PvE. Hoard tesla-punk tech, mine voxel terrain, run a mobile vehicle base through shifting seasons, intercept rivals, and siege their factories</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Initial idea was to freely walk in co-op inside the vehicle cargo hangar, while a friend drives the car over desert dunes. Solved it by hiding static colliders, while visuals render near the car. The camera sees real movement, while physics of internal objects stays stable.</span></span></span></a> <small>(since Sep 2023)</small>. Quick side-projects: <a href="https://store.steampowered.com/app/3600250/Whomers_Ate_My_Lawn/">Whomers Ate My Lawn!<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/3600250/69ff0311912878d48a0a7cb7523639b51370982b/header.jpg')"></span><span class="about-tip-body"><span class="about-tip-title">Whomers Ate My Lawn!</span><span class="about-tip-date">released 6 Apr 2025</span><span class="about-tip-desc">Dive into a simple yet charming world where curious Whomers creatures dig, eat, and survive in a compact 64x64 grid. This minimalistic simulation offers a peaceful experience of watching and interacting with small digital beings as they go about their lives</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Inspired by RimWorld, I wanted my own small semi-afk villager-manager. Made small creatures digging the lawn. You as God restore or dig more grass. Grow plants for more carrots. All to grow the population of Whomers. Made in 1 month with MonoGame in C#.</span></span></span></a> <small>(released 6 Apr 2025)</small> and <a href="https://store.steampowered.com/app/4967660/">Ball-Aqua<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/4967660/b2762559bd37c68c7df2cc04f47b19fb3be7d7ef/header.jpg')"></span><span class="about-tip-body"><span class="about-tip-title">Ball-Aqua</span><span class="about-tip-date">demo 20 Aug 2026</span><span class="about-tip-desc">Demo Launch on August 20! Roll a physics ball through tropical obstacle courses. Beat the timer, collect bubbles and stars, and chase 100% clears. Play Freeroam solo or co-op, compete in Race, build levels, and share on Steam Workshop.</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>I've seen many ball-rolling games recently. But all of them had terrible movement and platforms - just thin beams. I wanted to speed and jump forward, not short hops on thin platforms. That day I stumbled on the Frutiger Aero water album Alezya - Dream Island (youtube.com/watch?v=3R6beuJQkxM). Such hydrated music inspired me to make a water-themed ball-rolling multiplayer with a level editor and freedom. Spent about a month on a playable version to show as a demo. A few more months to polish and make more levels for the full release.</span></span></span></a> <small>(demo 20 Aug 2026)</small>.</p>

<div class="about-team-header">Meet the team and what we like</div>
<div class="about-couple">
<details class="about-person" id="stcost">
<summary><span class="about-head"><span class="about-avatar-link"><span class="about-avatar-wrap"><img src="https://avatars.fastly.steamstatic.com/bce10ec46b619fd7a8660cc783d36462d44aa89e_full.jpg" alt="StCost" width="96" height="96" /><img src="https://shared.fastly.steamstatic.com/community_assets/images/items/1239690/f0af6694686ebf42992824a3ee5f6313fc00cd7c.png" alt=" " width="96" height="96" /></span></span><span class="about-id"><h2 class="about-name"><a class="about-anchor" href="#stcost">StCost</a></h2><ul class="about-roles"><li>Team Lead</li><li>Software Engineer</li><li>Game Designer</li></ul></span><span class="about-head-split"></span><span class="about-tops"><a class="fav-chip" href="https://store.steampowered.com/app/823500/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/823500/capsule_184x69.jpg" alt="BONEWORKS" width="28" height="28" /><span>BONEWORKS</span></a><a class="fav-chip" href="https://www.youtube.com/watch?v=nbogUmJkeBI"><img src="https://img.youtube.com/vi/nbogUmJkeBI/mqdefault.jpg" alt="2 Mello - I Wanna Kno" width="28" height="28" /><span>2 Mello - I Wanna Kno</span></a><a class="fav-chip" href="https://en.wikipedia.org/wiki/The_Venture_Bros."><img src="https://media.themoviedb.org/t/p/w185/ckQE1aLYQkRpp2HmHljiELAiOr1.jpg" alt="The Venture Bros." width="28" height="28" /><span>The Venture Bros.</span></a><a class="fav-chip" href="https://unity.com/"><img src="https://cdn.simpleicons.org/unity/FFFFFF" alt="Unity" width="28" height="28" /><span>Unity</span></a></span></span></summary>
<div class="about-row">
<div class="about-section">
<div class="about-section-label">About</div>
<p class="about-note">2011: got own PC, was <a href="https://store.steampowered.com/app/440/">TF2</a> and <a href="https://www.minecraft.net/">Minecraft</a> server admin. 2016: first games - C++ terminal at university (<a href="https://dreamingsaints.github.io/blog/34-collapse-machine-stages/">see 34</a>). Developed <a href="https://fivem.net/">FiveM</a> themed Max-Max survival role-play server 32/32. Spent too much time in <a href="https://store.steampowered.com/app/440/">TF2</a>. Hobbies: skateboarding, FPV piloting.</p>
</div>
<div class="about-section">
<div class="about-section-label">Likes</div>
<p class="about-note"><a class="about-anchor" href="#sttaya">StTaya</a>, <a href="https://www.pepsi.com/">Pepsi</a>, <a href="https://www.nutella.com/">Nutella</a>, buns, <a href="https://en.wikipedia.org/wiki/Earl_Grey_tea">Earl Grey tea</a>, chips, beefsteak, strawberries.</p>
<div class="fav-colors">
<a class="fav-chip" href="https://store.steampowered.com/app/2980830/COLLAPSE_MACHINE"><span class="fav-swatch orange"></span><span>Perfect Orange (#ff8000)</span></a>
</div>
</div>
</div>
<div class="about-row about-meta">
<div class="about-section">
<div class="about-section-label">Media</div>
<p class="fav-row fav-compact">
<a class="fav-chip" href="https://discord.com/invite/xQwWSFDC8Y"><img src="https://cdn.simpleicons.org/discord/5865F2" alt="Discord" width="28" height="28" /><span>Discord</span></a>
<a class="fav-chip" href="https://steamcommunity.com/id/StCost"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="Steam" width="28" height="28" /><span>Steam</span></a>
<a class="fav-chip" href="mailto:dreamingsaints@gmail.com"><img src="https://cdn.simpleicons.org/gmail/EA4335" alt="Email" width="28" height="28" /><span>Email</span></a>
<a class="fav-chip" href="https://store.steampowered.com/search/?developer=Dreaming%20Saints"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="Dreaming Saints" width="28" height="28" /><span>Dreaming Saints</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Tools</div>
<p class="fav-row fav-compact">
<a class="fav-chip" href="https://unity.com/"><img src="https://cdn.simpleicons.org/unity/FFFFFF" alt="Unity" width="28" height="28" /><span>Unity</span></a>
<a class="fav-chip" href="https://www.blender.org/"><img src="https://cdn.simpleicons.org/blender/E87D0D" alt="Blender" width="28" height="28" /><span>Blender</span></a>
<a class="fav-chip" href="https://cursor.com/"><img src="https://cdn.simpleicons.org/cursor/FFFFFF" alt="Cursor" width="28" height="28" /><span>Cursor</span></a>
<a class="fav-chip" href="https://www.google.com/chrome/"><img src="https://cdn.simpleicons.org/googlechrome/4285F4" alt="Google Chrome" width="28" height="28" /><span>Google Chrome</span></a>
<a class="fav-chip" href="https://discord.com/"><img src="https://cdn.simpleicons.org/discord/5865F2" alt="Discord" width="28" height="28" /><span>Discord</span></a>
<a class="fav-chip" href="https://www.teamspeak.com/"><img src="https://cdn.simpleicons.org/teamspeak/2580C3" alt="TeamSpeak" width="28" height="28" /><span>TeamSpeak</span></a>
<a class="fav-chip" href="https://www.getpaint.net/"><img src="https://www.getpaint.net/favicon.ico" alt="Paint.NET" width="28" height="28" /><span>Paint.NET</span></a>
</p>
</div>
</div>
<div class="about-section">
<div class="about-section-label">Games</div>
<p class="fav-row">
<a class="fav-chip" href="https://store.steampowered.com/app/823500/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/823500/capsule_184x69.jpg" alt="BONEWORKS" width="28" height="28" /><span>BONEWORKS</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/22380/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/22380/capsule_184x69.jpg" alt="Fallout New Vegas" width="28" height="28" /><span>Fallout: New Vegas</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/22350/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/22350/capsule_184x69.jpg" alt="Brink" width="28" height="28" /><span>Brink</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/2000770/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/2000770/capsule_184x69.jpg" alt="Ballance" width="28" height="28" /><span>Ballance</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/3124230/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/3124230/header.jpg" alt="Jackal" width="28" height="28" /><span>Jackal</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/223470/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/223470/capsule_184x69.jpg" alt="POSTAL 2" width="28" height="28" /><span>POSTAL 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/620/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/620/capsule_184x69.jpg" alt="Portal 2" width="28" height="28" /><span>Portal 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/1353230/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1353230/capsule_184x69.jpg" alt="Bomb Rush Cyberfunk" width="28" height="28" /><span>Bomb Rush Cyberfunk</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/632360/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/632360/capsule_184x69.jpg" alt="Risk of Rain 2" width="28" height="28" /><span>Risk of Rain 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/294100/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/294100/capsule_184x69.jpg" alt="RimWorld" width="28" height="28" /><span>RimWorld</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/427520/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/427520/capsule_184x69.jpg" alt="Factorio" width="28" height="28" /><span>Factorio</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/892970/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/892970/capsule_184x69.jpg" alt="Valheim" width="28" height="28" /><span>Valheim</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/70/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/70/capsule_184x69.jpg" alt="Half-Life" width="28" height="28" /><span>Half-Life</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/220/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/220/capsule_184x69.jpg" alt="Half-Life 2" width="28" height="28" /><span>Half-Life 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/546560/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/546560/capsule_184x69.jpg" alt="Half-Life Alyx" width="28" height="28" /><span>Half-Life: Alyx</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/440/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/440/capsule_184x69.jpg" alt="Team Fortress 2" width="28" height="28" /><span>Team Fortress 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/71250/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/71250/capsule_184x69.jpg" alt="Sonic Adventure DX" width="28" height="28" /><span>Sonic Adventure DX</span></a>
<a class="fav-chip" href="https://www.vintagestory.at/"><img src="https://upload.wikimedia.org/wikipedia/en/1/1b/Vintage_Story_Logo.png" alt="Vintage Story" width="28" height="28" /><span>Vintage Story</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/704270/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/704270/capsule_184x69.jpg" alt="Generation Zero" width="28" height="28" /><span>Generation Zero</span></a>
<a class="fav-chip" href="https://www.minecraft.net/"><img src="https://www.minecraft.net/content/dam/minecraftnet/franchise/logos/minecraft-creeper-face.jpg" alt="Minecraft" width="28" height="28" /><span>Minecraft</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/220240/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/220240/capsule_184x69.jpg" alt="Far Cry 3" width="28" height="28" /><span>Far Cry 3</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Sonic_Riders"><img src="https://upload.wikimedia.org/wikipedia/en/1/15/Sonic_Riders_Coverart.png" alt="Sonic Riders" width="28" height="28" /><span>Sonic Riders</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Music</div>
<p class="fav-row">
<a class="fav-chip" href="https://www.youtube.com/watch?v=nbogUmJkeBI"><img src="https://img.youtube.com/vi/nbogUmJkeBI/mqdefault.jpg" alt="2 Mello - I Wanna Kno" width="28" height="28" /><span>2 Mello - I Wanna Kno</span></a>
<a class="fav-chip" href="https://www.youtube.com/watch?v=Dw1ZC6sZjIY"><img src="https://img.youtube.com/vi/Dw1ZC6sZjIY/mqdefault.jpg" alt="Frank Sinatra - Blue Moon" width="28" height="28" /><span>Frank Sinatra - Blue Moon</span></a>
<a class="fav-chip" href="https://www.youtube.com/watch?v=Pd-qu_ErkbE"><img src="https://img.youtube.com/vi/Pd-qu_ErkbE/mqdefault.jpg" alt="Pink Floyd - Crazy Diamond" width="28" height="28" /><span>Pink Floyd - Crazy Diamond</span></a>
<a class="fav-chip" href="https://www.youtube.com/watch?v=c0SrxSMHDmE"><img src="https://img.youtube.com/vi/c0SrxSMHDmE/mqdefault.jpg" alt="Bullet For My Valentine - Hand Of Blood" width="28" height="28" /><span>Bullet For My Valentine - Hand Of Blood</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Evans+Blue+iGod"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music118/v4/98/f2/79/98f279ea-f1a2-e258-d96a-8ceff77f8e58/859728161827_cover.jpg/100x100bb.jpg" alt="Evans Blue - iGod" width="28" height="28" /><span>Evans Blue - iGod</span></a>
<a class="fav-chip" href="https://www.youtube.com/watch?v=_Y_a0PWlBr8"><img src="https://img.youtube.com/vi/_Y_a0PWlBr8/mqdefault.jpg" alt="Breaking Benjamin - Psycho" width="28" height="28" /><span>Breaking Benjamin - Psycho</span></a>
<a class="fav-chip" href="https://www.youtube.com/watch?v=MM62wjLrgmA"><img src="https://img.youtube.com/vi/MM62wjLrgmA/mqdefault.jpg" alt="TOOL - Schism" width="28" height="28" /><span>TOOL - Schism</span></a>
<a class="fav-chip" href="https://www.youtube.com/watch?v=3NNaUQnFL2c"><img src="https://img.youtube.com/vi/3NNaUQnFL2c/mqdefault.jpg" alt="A Perfect Circle - Rose" width="28" height="28" /><span>A Perfect Circle - Rose</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Movies/series/cartoons</div>
<p class="fav-row">
<a class="fav-chip" href="https://en.wikipedia.org/wiki/The_Venture_Bros."><img src="https://media.themoviedb.org/t/p/w185/ckQE1aLYQkRpp2HmHljiELAiOr1.jpg" alt="The Venture Bros." width="28" height="28" /><span>The Venture Bros.</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/JoJo%27s_Bizarre_Adventure:_Stardust_Crusaders"><img src="https://media.themoviedb.org/t/p/w185/kX9noqY0YpOPKwXpRXYg1hEIqmM.jpg" alt="Stardust Crusaders" width="28" height="28" /><span>Stardust Crusaders</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Equilibrium_(film)"><img src="https://media.themoviedb.org/t/p/w185/q6VzUsHs4Z3myBHkrPAA3avfGwn.jpg" alt="Equilibrium" width="28" height="28" /><span>Equilibrium</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Mad_Max_2"><img src="https://media.themoviedb.org/t/p/w185/l1KVEhkGDpWRzQ0VqIhZqDDuOim.jpg" alt="Mad Max 2" width="28" height="28" /><span>Mad Max 2</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Westworld_(TV_series)"><img src="https://media.themoviedb.org/t/p/w185/ALlSU9du9iRiKIIoY1sREGNqQ5.jpg" alt="Westworld" width="28" height="28" /><span>Westworld</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/The_Day_of_the_Jackal_(TV_series)"><img src="https://media.themoviedb.org/t/p/w185/tYLecM3WSEjlkKhkGiH5G68Dprm.jpg" alt="The Day of the Jackal" width="28" height="28" /><span>The Day of the Jackal</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Memento_(film)"><img src="https://media.themoviedb.org/t/p/w185/nzlv62aC0octS5AklAiWpXLX9Z0.jpg" alt="Memento" width="28" height="28" /><span>Memento</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/WALL-E"><img src="https://media.themoviedb.org/t/p/w185/hbhFnRzzg6ZDmm8YAmxBnQpQIPh.jpg" alt="WALL-E" width="28" height="28" /><span>WALL-E</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Shrek_2"><img src="https://media.themoviedb.org/t/p/w185/2yYP0PQjG8zVqturh1BAqu2Tixl.jpg" alt="Shrek 2" width="28" height="28" /><span>Shrek 2</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Madagascar_(2005_film)"><img src="https://media.themoviedb.org/t/p/w185/zMpJY5CJKUufG9OTw0In4eAFqPX.jpg" alt="Madagascar" width="28" height="28" /><span>Madagascar</span></a>
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
<summary><span class="about-head"><span class="about-avatar-link"><span class="about-avatar-wrap"><img src="https://avatars.fastly.steamstatic.com/5bb86930eb99f482e56abc25937b7d6be37e83c3_full.jpg" alt="StTaya" width="96" height="96" /><img src="https://shared.fastly.steamstatic.com/community_assets/images/items/944220/91b1c881cd9fc1b0f9f77f0d410b30eb3192cc41.png" alt=" " width="96" height="96" /></span></span><span class="about-id"><h2 class="about-name"><a class="about-anchor" href="#sttaya">StTaya</a></h2><ul class="about-roles"><li>3D Artist</li><li>Art Designer</li><li>Animator</li><li>Level Designer</li></ul></span><span class="about-head-split"></span><span class="about-tops"><a class="fav-chip" href="https://store.steampowered.com/app/1361210/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1361210/capsule_184x69.jpg" alt="Darktide" width="28" height="28" /><span>Darktide</span></a><a class="fav-chip" href="https://music.youtube.com/search?q=Jesper+Kyd"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/JesperKyd.jpg/120px-JesperKyd.jpg" alt="Jesper Kyd" width="28" height="28" /><span>Jesper Kyd</span></a><a class="fav-chip" href="https://en.wikipedia.org/wiki/Sucker_Punch_(2011_film)"><img src="https://media.themoviedb.org/t/p/w185/jtaUDnvIiHUd2ranDcjB5AbPx6o.jpg" alt="Sucker Punch" width="28" height="28" /><span>Sucker Punch</span></a><a class="fav-chip" href="https://www.blender.org/"><img src="https://cdn.simpleicons.org/blender/E87D0D" alt="Blender" width="28" height="28" /><span>Blender</span></a></span></span></summary>
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
<a class="fav-chip" href="https://steamcommunity.com/id/sttaya"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="Steam" width="28" height="28" /><span>Steam</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Tools</div>
<p class="fav-row fav-compact">
<a class="fav-chip" href="https://www.blender.org/"><img src="https://cdn.simpleicons.org/blender/E87D0D" alt="Blender" width="28" height="28" /><span>Blender</span></a>
<a class="fav-chip" href="https://www.getpaint.net/"><img src="https://www.getpaint.net/favicon.ico" alt="Paint.NET" width="28" height="28" /><span>Paint.NET</span></a>
</p>
</div>
</div>
<div class="about-section">
<div class="about-section-label">Games</div>
<p class="fav-row">
<a class="fav-chip" href="https://store.steampowered.com/app/1361210/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1361210/capsule_184x69.jpg" alt="Darktide" width="28" height="28" /><span>Darktide</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/548430/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/548430/capsule_184x69.jpg" alt="Deep Rock Galactic" width="28" height="28" /><span>Deep Rock Galactic</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/553850/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/553850/capsule_184x69.jpg" alt="HELLDIVERS 2" width="28" height="28" /><span>HELLDIVERS 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/1086940/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1086940/capsule_184x69.jpg" alt="Baldur's Gate 3" width="28" height="28" /><span>Baldur's Gate 3</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/632360/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/632360/capsule_184x69.jpg" alt="Risk of Rain 2" width="28" height="28" /><span>Risk of Rain 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/2835570/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/2835570/capsule_184x69.jpg" alt="Buckshot Roulette" width="28" height="28" /><span>Buckshot Roulette</span></a>
<a class="fav-chip" href="https://www.vintagestory.at/"><img src="https://upload.wikimedia.org/wikipedia/en/1/1b/Vintage_Story_Logo.png" alt="Vintage Story" width="28" height="28" /><span>Vintage Story</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/377160/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/377160/capsule_184x69.jpg" alt="Fallout 4" width="28" height="28" /><span>Fallout 4</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/704270/" title="first game"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/704270/capsule_184x69.jpg" alt="Generation Zero" width="28" height="28" /><span>Generation Zero</span></a>
<a class="fav-chip" href="https://www.minecraft.net/"><img src="https://www.minecraft.net/content/dam/minecraftnet/franchise/logos/minecraft-creeper-face.jpg" alt="Minecraft" width="28" height="28" /><span>Minecraft</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/220240/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/220240/capsule_184x69.jpg" alt="Far Cry 3" width="28" height="28" /><span>Far Cry 3</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Sonic_Riders"><img src="https://upload.wikimedia.org/wikipedia/en/1/15/Sonic_Riders_Coverart.png" alt="Sonic Riders" width="28" height="28" /><span>Sonic Riders</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Music</div>
<p class="fav-row">
<a class="fav-chip" href="https://music.youtube.com/search?q=Jesper+Kyd"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/JesperKyd.jpg/120px-JesperKyd.jpg" alt="Jesper Kyd" width="28" height="28" /><span>Jesper Kyd</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Chris+Christodoulou"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music221/v4/f6/b7/7e/f6b77e09-ebb7-bf28-d7a5-309a875bc47c/194152351575.png/100x100bb.jpg" alt="Chris Christodoulou" width="28" height="28" /><span>Chris Christodoulou</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Die+Antwoord"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/11/2019_RiP_Die_Antwoord_-_by_2eight_-_ZSC2923_%28cropped%29.jpg/120px-2019_RiP_Die_Antwoord_-_by_2eight_-_ZSC2923_%28cropped%29.jpg" alt="Die Antwoord" width="28" height="28" /><span>Die Antwoord</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Zheani"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music211/v4/65/e8/28/65e828f4-3c08-3097-21d9-abd451b4d05d/9332727129650_cover.jpg/100x100bb.jpg" alt="Zheani" width="28" height="28" /><span>Zheani</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Starjunk+95"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music221/v4/db/a0/0f/dba00f1c-913e-bff1-3dc7-a991c7525ff0/cover.jpg/100x100bb.jpg" alt="Starjunk 95" width="28" height="28" /><span>Starjunk 95</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Machine+Girl"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music221/v4/dd/82/5a/dd825afa-a2f8-a6eb-d9e9-41cce7ee0ade/195162206244_cover.jpg/100x100bb.jpg" alt="Machine Girl" width="28" height="28" /><span>Machine Girl</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Jaybooty"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music211/v4/ed/67/bf/ed67bf96-8b5f-a4eb-91af-cf8f0669dff9/artwork.jpg/100x100bb.jpg" alt="Jaybooty" width="28" height="28" /><span>Jaybooty</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Massive+Attack"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/41/Massive_Attack%2C_Saint-Petersburg%2C_2010-09-26_%28cropped%29.jpg/120px-Massive_Attack%2C_Saint-Petersburg%2C_2010-09-26_%28cropped%29.jpg" alt="Massive Attack" width="28" height="28" /><span>Massive Attack</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Doja+Cat"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Doja_Cat_x_Amazon1.1_%28cropped%29.jpg/120px-Doja_Cat_x_Amazon1.1_%28cropped%29.jpg" alt="Doja Cat" width="28" height="28" /><span>Doja Cat</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=BLACKPINK"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/20240809_Blackpink_Pink_Carpet_09.png/120px-20240809_Blackpink_Pink_Carpet_09.png" alt="BLACKPINK" width="28" height="28" /><span>BLACKPINK</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Perturbator"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music115/v4/e4/1e/00/e41e00e2-f286-ce49-ab70-9e50d0952675/5060366780843_cover.jpg/100x100bb.jpg" alt="Perturbator" width="28" height="28" /><span>Perturbator</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Mick+Gordon"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Mike_Gordon_at_GDC_Festival_conference.jpg/120px-Mike_Gordon_at_GDC_Festival_conference.jpg" alt="Mick Gordon" width="28" height="28" /><span>Mick Gordon</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Maximum+the+Hormone"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b2/Maximum_The_Hormone_%282014%29.jpg/120px-Maximum_The_Hormone_%282014%29.jpg" alt="Maximum the Hormone" width="28" height="28" /><span>Maximum the Hormone</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=The+Prodigy"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fe/The_Prodigy_IMG_2972_%285353883317%29_%28cropped%29.jpg/120px-The_Prodigy_IMG_2972_%285353883317%29_%28cropped%29.jpg" alt="The Prodigy" width="28" height="28" /><span>The Prodigy</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Movies/series/cartoons</div>
<p class="fav-row">
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Sucker_Punch_(2011_film)"><img src="https://media.themoviedb.org/t/p/w185/jtaUDnvIiHUd2ranDcjB5AbPx6o.jpg" alt="Sucker Punch" width="28" height="28" /><span>Sucker Punch</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/The_Hunger_Games_(film)"><img src="https://media.themoviedb.org/t/p/w185/yXCbOiVDCxO71zI7cuwBRXdftq8.jpg" alt="The Hunger Games" width="28" height="28" /><span>The Hunger Games</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Forrest_Gump"><img src="https://media.themoviedb.org/t/p/w185/Cw4hIUIAmSYfK9QfaUW5igp9La.jpg" alt="Forrest Gump" width="28" height="28" /><span>Forrest Gump</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Real_Steel"><img src="https://media.themoviedb.org/t/p/w185/4GIeI5K5YdDUkR3mNQBoScpSFEf.jpg" alt="Real Steel" width="28" height="28" /><span>Real Steel</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Peaceful_Warrior"><img src="https://media.themoviedb.org/t/p/w185/r4VQCZe3aSo7TmmsxcyLqaoMR1l.jpg" alt="Peaceful Warrior" width="28" height="28" /><span>Peaceful Warrior</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/JoJo%27s_Bizarre_Adventure:_Stardust_Crusaders"><img src="https://media.themoviedb.org/t/p/w185/kX9noqY0YpOPKwXpRXYg1hEIqmM.jpg" alt="Stardust Crusaders" width="28" height="28" /><span>Stardust Crusaders</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/The_Venture_Bros."><img src="https://media.themoviedb.org/t/p/w185/ckQE1aLYQkRpp2HmHljiELAiOr1.jpg" alt="The Venture Bros." width="28" height="28" /><span>The Venture Bros.</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Halo_(TV_series)"><img src="https://media.themoviedb.org/t/p/w185/4UmNhZCEu8Vt3byMvNxNEPyf8EY.jpg" alt="Halo" width="28" height="28" /><span>Halo</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Game_of_Thrones"><img src="https://media.themoviedb.org/t/p/w185/1XS1oqL89opfnbLl8WnZY1O1uJx.jpg" alt="Game of Thrones" width="28" height="28" /><span>Game of Thrones</span></a>
</p>
</div>
</details>
</div>

<details class="about-person" id="stgrikus">
<summary><span class="about-head"><span class="about-avatar-link"><span class="about-avatar-wrap"><img src="https://avatars.fastly.steamstatic.com/55ca41f5225fee88d359222787ebac8f11241fa1_full.jpg" alt="StGrikus" width="96" height="96" /><img src="https://shared.fastly.steamstatic.com/community_assets/images/items/1361210/6a2ff332dc612e923dd1330b12981aa34ebc4895.png" alt=" " width="96" height="96" /></span></span><span class="about-id"><h2 class="about-name"><a class="about-anchor" href="#stgrikus">StGrikus</a></h2><ul class="about-roles"><li>Sound Designer</li><li>Sound Engineer</li><li>Marketing</li></ul></span><span class="about-head-split"></span><span class="about-tops"><a class="fav-chip" href="https://store.steampowered.com/app/1361210/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1361210/capsule_184x69.jpg" alt="Darktide" width="28" height="28" /><span>Darktide</span></a><a class="fav-chip" href="https://music.youtube.com/watch?v=Z_Jp2mlzEjw"><img src="https://images.genius.com/c4a8791231ded0415f792b94cc59a059.1000x1000x1.png" alt="Twenty One Pilots" width="28" height="28" /><span>Twenty One Pilots</span></a><a class="fav-chip" href="https://en.wikipedia.org/wiki/Back_to_the_Future"><img src="https://upload.wikimedia.org/wikipedia/en/d/d2/Back_to_the_Future.jpg" alt="Back to the Future" width="28" height="28" /><span>Back to the Future</span></a><a class="fav-chip" href="https://www.fmod.com/"><img src="https://www.fmod.com/favicon.ico" alt="FMOD" width="28" height="28" /><span>FMOD</span></a></span></span></summary>
<div class="about-row">
<div class="about-section">
<div class="about-section-label">About</div>
<p class="about-note">Technical sound designer. 2012: started learning guitar, and music and sound have absorbed me ever since. Started studying <a href="https://www.fmod.com/">FMOD</a> and how sound works in games in 2025. Spent too much time in <a href="https://store.steampowered.com/app/730/">CS:GO</a>. Hobbies: guitar, skateboarding.</p>
</div>
<div class="about-section">
<div class="about-section-label">Likes</div>
<p class="about-note">Analyzing song structure and soundstage, <a href="https://en.wikipedia.org/wiki/Da_Hong_Pao">Da Hong Pao</a>, White Oolong.</p>
<div class="fav-colors">
<span class="fav-chip"><span class="fav-swatch purple"></span><span>Purple</span></span>
<span class="fav-chip"><span class="fav-swatch ultramarine"></span><span>#120A8F</span></span>
</div>
</div>
</div>
<div class="about-section">
<div class="about-section-label">Coffee</div>
<p class="about-note">2021: got into coffee by drinking V60, Chemex, and AeroPress in cafés. After getting a V60 for my birthday, started brewing at home and going deeper into beans. Autumn 2023: joined one of the city's best coffee shops and dove into processing, roasting, brewing, and how origins differ. Mid-2024: placed 2nd in a Brewers Cup, brewing Hario Switch and V60. Taught brewing workshops, lectured on coffee varieties and processing methods, and hosted open cuppings.</p>
<p class="about-note">Favorite brew methods: <a href="https://www.hario-usa.com/products/switch-immersion-dripper">Hario Switch</a>, <a href="https://en.wikipedia.org/wiki/Chemex_Coffeemaker">Chemex</a>, <a href="https://www.hario-usa.com/products/v60-coffee-dripper-02-ceramic">V60</a>.</p>
<p class="fav-row">
<a class="fav-chip" href="https://heatroasters.com/product/colombia-grape/" title="Armenia, co-fermentation"><img src="https://heatroasters.com/wp-content/uploads/2026/04/grape-775x1024.png" alt="Colombia Grape" width="28" height="28" /><span>Colombia Grape</span></a>
<a class="fav-chip" href="https://heatroasters.com/product/colombia-paraiso-92/" title="Huila, washed, yeast fermentation and thermal shock"><img src="https://heatroasters.com/wp-content/uploads/2026/02/paraiso92-775x1024.png" alt="Colombia Paraiso 92" width="28" height="28" /><span>Colombia Paraiso 92</span></a>
<a class="fav-chip" href="https://heatroasters.com/product/colombia-tres-letras/" title="Arauca, natural"><img src="https://heatroasters.com/wp-content/uploads/2026/02/tres-letras.png" alt="Colombia Tres Letras" width="28" height="28" /><span>Colombia Tres Letras</span></a>
<a class="fav-chip" href="https://heatroasters.com/product/kenya-gachatha/" title="Nyeri, washed"><img src="https://heatroasters.com/wp-content/uploads/2026/02/gachata-775x1024.png" alt="Kenya Gachatha" width="28" height="28" /><span>Kenya Gachatha</span></a>
<a class="fav-chip" href="https://heatroasters.com/product/ethiopia-gerba-dogo/" title="Guji, natural"><img src="https://heatroasters.com/wp-content/uploads/2026/02/gerba-dogo-1-775x1024.png" alt="Ethiopia Gerba Dogo" width="28" height="28" /><span>Ethiopia Gerba Dogo</span></a>
</p>
</div>
<div class="about-row about-meta">
<div class="about-section">
<div class="about-section-label">Media</div>
<p class="fav-row fav-compact">
<a class="fav-chip" href="https://steamcommunity.com/id/grikus"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="Steam" width="28" height="28" /><span>Steam</span></a>
<a class="fav-chip" href="https://www.instagram.com/stgrikus/"><img src="https://cdn.simpleicons.org/instagram/E4405F" alt="Instagram" width="28" height="28" /><span>Instagram</span></a>
<a class="fav-chip" href="https://t.me/stgrikussound"><img src="https://cdn.simpleicons.org/telegram/26A5E4" alt="Telegram" width="28" height="28" /><span>Telegram</span></a>
<a class="fav-chip" href="https://www.twitch.tv/stgrikus"><img src="https://cdn.simpleicons.org/twitch/9146FF" alt="Twitch" width="28" height="28" /><span>Twitch</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Tools</div>
<p class="fav-row fav-compact">
<a class="fav-chip" href="https://www.fmod.com/"><img src="https://www.fmod.com/favicon.ico" alt="FMOD" width="28" height="28" /><span>FMOD</span></a>
<a class="fav-chip" href="https://www.image-line.com/"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/6/69/FL_Studio_11_just_logo.png/120px-FL_Studio_11_just_logo.png" alt="FL Studio" width="28" height="28" /><span>FL Studio</span></a>
<a class="fav-chip" href="https://www.reaper.fm/"><img src="https://www.reaper.fm/v5img/logo.jpg" alt="REAPER" width="28" height="28" /><span>REAPER</span></a>
<a class="fav-chip" href="https://unity.com/"><img src="https://cdn.simpleicons.org/unity/FFFFFF" alt="Unity" width="28" height="28" /><span>Unity</span></a>
<a class="fav-chip" href="https://cursor.com/"><img src="https://cdn.simpleicons.org/cursor/FFFFFF" alt="Cursor" width="28" height="28" /><span>Cursor</span></a>
<a class="fav-chip" href="https://www.blackmagicdesign.com/products/davinciresolve"><img src="https://cdn.simpleicons.org/davinciresolve/FFFFFF" alt="DaVinci Resolve" width="28" height="28" /><span>DaVinci Resolve</span></a>
<a class="fav-chip" href="https://www.adobe.com/products/photoshop.html"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Adobe_Photoshop_CC_icon.svg/120px-Adobe_Photoshop_CC_icon.svg.png" alt="Photoshop" width="28" height="28" /><span>Photoshop</span></a>
<a class="fav-chip" href="https://obsproject.com/"><img src="https://cdn.simpleicons.org/obsstudio/FFFFFF" alt="OBS Studio" width="28" height="28" /><span>OBS Studio</span></a>
</p>
</div>
</div>
<div class="about-section">
<div class="about-section-label">Games</div>
<p class="fav-row">
<a class="fav-chip" href="https://store.steampowered.com/app/1361210/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1361210/capsule_184x69.jpg" alt="Darktide" width="28" height="28" /><span>Darktide</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/22380/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/22380/capsule_184x69.jpg" alt="Fallout New Vegas" width="28" height="28" /><span>Fallout: New Vegas</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/553850/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/553850/capsule_184x69.jpg" alt="HELLDIVERS 2" width="28" height="28" /><span>HELLDIVERS 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/427520/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/427520/capsule_184x69.jpg" alt="Factorio" width="28" height="28" /><span>Factorio</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/892970/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/892970/capsule_184x69.jpg" alt="Valheim" width="28" height="28" /><span>Valheim</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/632360/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/632360/capsule_184x69.jpg" alt="Risk of Rain 2" width="28" height="28" /><span>Risk of Rain 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/570/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/570/capsule_184x69.jpg" alt="Dota 2" width="28" height="28" /><span>Dota 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/1086940/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1086940/capsule_184x69.jpg" alt="Baldur's Gate 3" width="28" height="28" /><span>Baldur's Gate 3</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/227300/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/227300/capsule_184x69.jpg" alt="Euro Truck Simulator 2" width="28" height="28" /><span>Euro Truck Simulator 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/22350/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/22350/capsule_184x69.jpg" alt="Brink" width="28" height="28" /><span>Brink</span></a>
<a class="fav-chip" href="https://www.vintagestory.at/"><img src="https://upload.wikimedia.org/wikipedia/en/1/1b/Vintage_Story_Logo.png" alt="Vintage Story" width="28" height="28" /><span>Vintage Story</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/2186680/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/2186680/capsule_184x69.jpg" alt="Warhammer 40,000: Rogue Trader" width="28" height="28" /><span>Warhammer 40,000: Rogue Trader</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/231430/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/231430/capsule_184x69.jpg" alt="Company of Heroes 2" width="28" height="28" /><span>Company of Heroes 2</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/489830/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/489830/capsule_184x69.jpg" alt="Skyrim" width="28" height="28" /><span>Skyrim</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/990080/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/990080/capsule_184x69.jpg" alt="Hogwarts Legacy" width="28" height="28" /><span>Hogwarts Legacy</span></a>
<a class="fav-chip" href="https://store.steampowered.com/app/271590/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/271590/capsule_184x69.jpg" alt="GTA V" width="28" height="28" /><span>GTA V</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Music</div>
<p class="fav-row">
<a class="fav-chip" href="https://music.youtube.com/watch?v=Z_Jp2mlzEjw"><img src="https://images.genius.com/c4a8791231ded0415f792b94cc59a059.1000x1000x1.png" alt="Twenty One Pilots" width="28" height="28" /><span>Twenty One Pilots</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=dML7QMkbpnQ"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music221/v4/9d/2b/28/9d2b28ce-421f-85f5-d48c-7a79ba8f9edb/859728051630_cover.jpg/100x100bb.jpg" alt="The Midnight" width="28" height="28" /><span>The Midnight</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=Wk9mMbOpAaA"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSA2SnxsBS8JSYhe9V_Jn4NYpgWHcABvCRsEhk8UbK_OA&amp;s=10" alt="GUNSHIP" width="28" height="28" /><span>GUNSHIP</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=vJ1oyOazhEk"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music125/v4/c1/2d/fe/c12dfe8f-cdf6-e179-d69a-8ec35f760266/00602537248681.rgb.jpg/100x100bb.jpg" alt="Kavinsky" width="28" height="28" /><span>Kavinsky</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=d5vRK1fubEE"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music122/v4/ae/f3/3c/aef33c9b-9ab4-6a7e-4b22-d3984b2ff469/849320014362.png/100x100bb.jpg" alt="Nothing More" width="28" height="28" /><span>Nothing More</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=9B1Dbimbnl4"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRfc-hXgbQ0gc6NqtvzHIHfD6Y0tUpiN7pT3SHjHmje8lwkI04B0bFgvCI&amp;s=10" alt="Radiotehnika" width="28" height="28" /><span>Radiotehnika</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=DdLMr4aj0iE"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music211/v4/70/7d/0c/707d0ccf-dab2-f2e1-92f0-e7d1b6e5812d/artwork.jpg/100x100bb.jpg" alt="Kalax" width="28" height="28" /><span>Kalax</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=CtiuMnhP3Qk"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Tool_live_Birmingham_2022.jpg/120px-Tool_live_Birmingham_2022.jpg" alt="TOOL" width="28" height="28" /><span>TOOL</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=DowAWZgDO8c"><img src="https://i.guim.co.uk/img/media/c5ee7639198c9cdc058beed0486fff93a9654f7c/543_703_6053_3634/master/6053.jpg?width=1200&amp;height=1200&amp;quality=85&amp;auto=format&amp;fit=crop&amp;s=99c1c81cc004be107b86352060b9f7d7" alt="Red Hot Chili Peppers" width="28" height="28" /><span>Red Hot Chili Peppers</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=RRMbhEdmhYw"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/68/Daft_Punk_in_2013_2-_centered.jpg/120px-Daft_Punk_in_2013_2-_centered.jpg" alt="Daft Punk" width="28" height="28" /><span>Daft Punk</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=Obim8BYGnOE"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRAqUsD62ZNtSOkXJtL8WSUby28QTZJgCMC0CCBfE9SaelpBDvpdYkEQLk&amp;s=10" alt="Eminem" width="28" height="28" /><span>Eminem</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=5H99tg2_pwA"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4jQd4K5wsNbJPvrbXcekjZ25dW5iRbJdDOaeJNy52SCof7UTd7SJgYF97&amp;s=10" alt="Linkin Park" width="28" height="28" /><span>Linkin Park</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=av2xYzcSO-Q"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music221/v4/fc/dc/8a/fcdc8a3e-1c89-1fcc-5a56-4c35d09f4d51/859741339685_cover.jpg/100x100bb.jpg" alt="Cathode Electrode" width="28" height="28" /><span>Cathode Electrode</span></a>
<a class="fav-chip" href="https://music.youtube.com/watch?v=2kc4cyBZ7dw"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music124/v4/f1/2a/21/f12a2180-7926-00a2-d526-f9f695f7a7f6/00602517178502.rgb.jpg/100x100bb.jpg" alt="Drake Bell" width="28" height="28" /><span>Drake Bell</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Movies/series/cartoons</div>
<p class="fav-row">
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Back_to_the_Future"><img src="https://upload.wikimedia.org/wikipedia/en/d/d2/Back_to_the_Future.jpg" alt="Back to the Future" width="28" height="28" /><span>Back to the Future</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Attack_on_Titan_(TV_series)"><img src="https://media.themoviedb.org/t/p/w185/hTP1DtLGFamjfu8WqjnuQdP1n4i.jpg" alt="Attack on Titan" width="28" height="28" /><span>Attack on Titan</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Interstellar_(film)"><img src="https://upload.wikimedia.org/wikipedia/en/b/bc/Interstellar_film_poster.jpg" alt="Interstellar" width="28" height="28" /><span>Interstellar</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Inception"><img src="https://upload.wikimedia.org/wikipedia/en/2/2e/Inception_%282010%29_theatrical_poster.jpg" alt="Inception" width="28" height="28" /><span>Inception</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Joker_(2019_film)"><img src="https://upload.wikimedia.org/wikipedia/en/e/e1/Joker_%282019_film%29_poster.jpg" alt="Joker" width="28" height="28" /><span>Joker</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Soul_(2020_film)"><img src="https://upload.wikimedia.org/wikipedia/en/3/39/Soul_%282020_film%29_poster.jpg" alt="Soul" width="28" height="28" /><span>Soul</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Luck_(2022_film)"><img src="https://upload.wikimedia.org/wikipedia/en/6/6e/Luck_%282022%29_poster.png" alt="Luck" width="28" height="28" /><span>Luck</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/The_World%27s_Fastest_Indian"><img src="https://upload.wikimedia.org/wikipedia/en/6/68/Worlds_fastest_indian.jpg" alt="The World's Fastest Indian" width="28" height="28" /><span>The World's Fastest Indian</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Rick_and_Morty"><img src="https://cdn.27.ua/sc--media--prod/default/41/3d/5b/413d5bd0-3fcd-482c-ab82-b7ca46636893.jpg" alt="Rick and Morty" width="28" height="28" /><span>Rick and Morty</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Hacksaw_Ridge"><img src="https://upload.wikimedia.org/wikipedia/en/8/8a/Hacksaw_Ridge_poster.png" alt="Hacksaw Ridge" width="28" height="28" /><span>Hacksaw Ridge</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Iron_Man_(2008_film)"><img src="https://upload.wikimedia.org/wikipedia/en/0/02/Iron_Man_%282008_film%29_poster.jpg" alt="Iron Man" width="28" height="28" /><span>Iron Man</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Iron_Man_2"><img src="https://upload.wikimedia.org/wikipedia/en/e/ed/Iron_Man_2_poster.jpg" alt="Iron Man 2" width="28" height="28" /><span>Iron Man 2</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Batman_Begins"><img src="https://upload.wikimedia.org/wikipedia/en/a/af/Batman_Begins_Poster.jpg" alt="Batman Begins" width="28" height="28" /><span>Batman Begins</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Oppenheimer_(film)"><img src="https://upload.wikimedia.org/wikipedia/en/4/4a/Oppenheimer_%28film%29.jpg" alt="Oppenheimer" width="28" height="28" /><span>Oppenheimer</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/The_Mask_(1994_film)"><img src="https://upload.wikimedia.org/wikipedia/en/4/4b/The_Mask_%28film%29_poster.jpg" alt="The Mask" width="28" height="28" /><span>The Mask</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Drake_%26_Josh"><img src="https://m.media-amazon.com/images/M/MV5BNmM3MWFkZjctYzBhNC00YWU1LWIzYTktZjUxMzYyNGE5MjhlXkEyXkFqcGc@._V1_.jpg" alt="Drake &amp; Josh" width="28" height="28" /><span>Drake &amp; Josh</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/L%C3%A9on:_The_Professional"><img src="https://upload.wikimedia.org/wikipedia/en/0/03/Leon-poster.jpg" alt="Léon: The Professional" width="28" height="28" /><span>Léon: The Professional</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/8_Mile_(film)"><img src="https://upload.wikimedia.org/wikipedia/en/1/1e/8_Mile_official_poster.jpg" alt="8 Mile" width="28" height="28" /><span>8 Mile</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/28_Days_Later"><img src="https://upload.wikimedia.org/wikipedia/en/e/e4/28_days_later.jpg" alt="28 Days Later" width="28" height="28" /><span>28 Days Later</span></a>
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
})();
</script>
