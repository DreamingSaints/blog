<div class="games-grid">
  <div class="game-cell">
    <div class="game-cell-top">
      <span class="about-tip-trigger">COLLAPSE MACHINE<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/2980830/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/2980830/COLLAPSE_MACHINE">COLLAPSE MACHINE</a><span class="about-tip-date">since Sep 2023</span><span class="about-tip-desc">In COLLAPSE MACHINE - scavenge, raid, and survive a super-magnetic wasteland in co-op PvE. Hoard tesla-punk tech, mine voxel terrain, run a mobile vehicle base through shifting seasons, intercept rivals, and siege their factories</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Initial idea was to freely walk in co-op inside the vehicle cargo hangar, while a friend drives the car over desert dunes. Solved it by hiding static colliders, while visuals render near the car. The camera sees real movement, while physics of internal objects stays stable.</span></span></span></span> 💥🚕
      <small class="game-status">(coming)</small>
    </div>
    <p class="game-desc">a tesla-punk co-op open-world imm-sim fps sandbox</p>
  </div>
  <div class="game-cell">
    <div class="game-cell-top">
      <span class="about-tip-trigger">Ball-Aqua<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/4967660/b2762559bd37c68c7df2cc04f47b19fb3be7d7ef/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/4967660/">Ball-Aqua</a><span class="about-tip-date">demo 20 Aug 2026</span><span class="about-tip-desc">Demo Launch on August 20! Roll a physics ball through tropical obstacle courses. Beat the timer, collect bubbles and stars, and chase 100% clears. Play Freeroam solo or co-op, compete in Race, build levels, and share on Steam Workshop.</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>I've seen many ball-rolling games recently. But all of them had terrible movement and platforms - just thin beams. I wanted to speed and jump forward, not short hops on thin platforms. That day I stumbled on the Frutiger Aero water album Alezya - Dream Island (youtube.com/watch?v=3R6beuJQkxM). Such hydrated music inspired me to make a water-themed ball-rolling multiplayer with a level editor and freedom. Spent about a month on a playable version to show as a demo. A few more months to polish and make more levels for the full release.</span></span></span></span> 🔮🌊
      <small class="game-status">(demo 20 Aug 2026)</small>
    </div>
    <p class="game-desc">a tropical ball-rolling multiplayer 3D platformer</p>
  </div>
  <div class="game-cell">
    <div class="game-cell-top">
      <span class="about-tip-trigger">Whomers Ate My Lawn!<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/3600250/69ff0311912878d48a0a7cb7523639b51370982b/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/3600250/Whomers_Ate_My_Lawn/">Whomers Ate My Lawn!</a><span class="about-tip-date">released 6 Apr 2025</span><span class="about-tip-desc">Dive into a simple yet charming world where curious Whomers creatures dig, eat, and survive in a compact 64x64 grid. This minimalistic simulation offers a peaceful experience of watching and interacting with small digital beings as they go about their lives</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Inspired by RimWorld, I wanted my own small semi-afk villager-manager. Made small creatures digging the lawn. You as God restore or dig more grass. Grow plants for more carrots. All to grow the population of Whomers. Made in 1 month with MonoGame in C#.</span></span></span></span> 👾🥕
      <small class="game-status">(released 6 Apr 2025)</small>
    </div>
    <p class="game-desc">a farm of tiny pets digging lawn to find carrots</p>
  </div>
  <div class="game-cell">
    <div class="game-cell-top">
      <span class="about-tip-trigger">RISING BONEvR<span class="about-tip"><span class="about-tip-art" style="background-image:url('https://cdn.cloudflare.steamstatic.com/steam/apps/1775350/header.jpg')"></span><span class="about-tip-body"><a class="about-tip-title" href="https://store.steampowered.com/app/1775350/RISING_BONEvR/">RISING BONEvR</a><span class="about-tip-date">demo 7 Nov 2021</span><span class="about-tip-desc">(First level demo available!) Physics based puzzle about climbing out of deep hell without any legs</span><span class="about-tip-note"><span class="about-tip-said">StCost says</span>Quite a challenge to implement VR physics similar to BONEWORKS. Learned more math, vectors, matrices. Level design is terrible, physics clunky, but gameplay was fun when it works. My first proper C# game, and fiancee StTaya helped by making her first 3D models in Blender. Some day we'll continue - we learned many new lessons since then.</span></span></span></span> 🧗‍♀️💀
      <small class="game-status">(demo 7 Nov 2021)</small>
    </div>
    <p class="game-desc">a physics VR climb out of hell without legs</p>
  </div>
</div>

<style>
.games-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px 20px;
  margin: 0 0 0.75rem;
  overflow: visible;
}
@media (max-width: 720px) {
  .games-grid {
    grid-template-columns: 1fr;
    gap: 10px;
  }
  .game-cell:nth-child(even) .about-tip {
    left: 0;
    right: auto;
  }
}
.game-cell {
  position: relative;
  z-index: 1;
  overflow: visible;
}
.game-cell:hover {
  z-index: 40;
}
.game-cell-top {
  display: flex;
  flex-wrap: wrap;
  align-items: baseline;
  gap: 6px;
}
.game-cell-top .about-tip-trigger {
  position: relative;
  color: #a06739;
  font-style: italic;
  text-decoration: underline dashed;
  text-decoration-color: rgba(160, 103, 57, 0.7);
  text-underline-offset: 0.2em;
  text-decoration-thickness: 1px;
  cursor: help;
}
.game-cell-top .about-tip-trigger:hover {
  color: #c48952;
  text-decoration-color: #c48952;
}
.game-status {
  color: #6e7681;
  font-size: 0.75em;
  font-weight: 400;
}
.game-desc {
  margin: 0.2rem 0 0;
  font-size: 0.85em;
  color: #8b949e;
}
.games-grid .about-tip {
  display: none;
  position: absolute;
  left: 0;
  top: 100%;
  z-index: 50;
  width: min(272px, calc(100vw - 16px));
  padding-top: 6px;
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
.game-cell:nth-child(even) .about-tip {
  left: auto;
  right: 0;
}
.game-cell-top .about-tip-trigger:hover > .about-tip,
.game-cell-top .about-tip-trigger.tip-open > .about-tip {
  display: block;
  color: #c9d1d9;
  text-decoration: none;
}
.games-grid .about-tip-art {
  display: block;
  width: 100%;
  aspect-ratio: 460 / 215;
  background: #0d1117 center / cover no-repeat;
}
.games-grid .about-tip-body {
  display: block;
  padding: 8px 10px 10px;
}
.games-grid a.about-tip-title {
  display: inline;
  font-size: 0.95em;
  font-weight: 600;
  color: var(--color-primary);
  cursor: pointer;
  text-decoration: none;
}
.games-grid a.about-tip-title:hover {
  color: var(--color-primary-hover);
  text-decoration: underline;
}
.games-grid .about-tip-date {
  display: inline;
  margin: 0 0 0 6px;
  font-size: 0.75em;
  font-weight: 400;
  color: #6e7681;
}
.games-grid .about-tip-desc {
  display: block;
  margin-top: 6px;
  font-size: 0.8em;
  color: #8b949e;
}
.games-grid .about-tip-note {
  display: block;
  margin-top: 8px;
  font-size: 0.75em;
  font-style: italic;
  color: #8b949e;
}
.games-grid .about-tip-said {
  display: flex;
  align-items: flex-end;
  gap: 8px;
  margin: 0 0 6px;
  font-style: normal;
  font-weight: 600;
  color: #6e7681;
}
.games-grid .about-tip-said::after {
  content: "";
  flex: 1 1 auto;
  border-bottom: 1px solid #30363d;
  margin-bottom: 0.2em;
}
.pinned-find > summary {
  display: flex;
  align-items: center;
  gap: 8px;
  cursor: pointer;
  list-style: none;
}
.pinned-find > summary::-webkit-details-marker { display: none; }
.pinned-find > summary::marker { content: ""; }
.pinned-find > summary::before {
  content: "▸";
  flex-shrink: 0;
  width: 1em;
  color: var(--color-primary);
  font-size: 0.95em;
  line-height: 1;
}
.pinned-find[open] > summary::before { content: "▾"; }
.pinned-find-label {
  margin-right: auto;
  color: var(--color-primary);
  font-weight: 600;
}
.pinned-find > summary:hover .pinned-find-label {
  color: var(--color-primary-hover);
  text-decoration: underline;
}
.pinned-about-us {
  display: inline-flex;
  align-items: center;
  gap: 5px;
  flex-shrink: 0;
  white-space: nowrap;
  font-weight: 600;
  padding-left: 12px;
  margin-left: 4px;
  border-left: 1px solid var(--color-border);
}
.pinned-about-us svg {
  display: block;
  width: 14px;
  height: 14px;
  flex-shrink: 0;
}
.pinned-links {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 8px 12px;
  width: 100%;
  margin-top: 8px;
  text-align: left;
}
.pinned-link-title {
  font-weight: 700;
  margin: 0 0 2px;
}
.pinned-link-title a {
  display: inline-flex;
  padding: 8px;
}
.pinned-link-grid {
  display: flex;
  flex-direction: column;
}
.pinned-links a {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px;
  line-height: 1;
}
.pinned-links img {
  display: block;
  width: 20px !important;
  height: 20px !important;
  margin: 0 !important;
  border-radius: 0 !important;
  box-shadow: none !important;
  flex-shrink: 0;
}
@media (max-width: 720px) {
  .pinned-links {
    grid-template-columns: 1fr;
    gap: 14px;
  }
  .pinned-link-title {
    margin: 0 0 4px;
    padding-bottom: 2px;
    border-bottom: 1px solid var(--color-border);
  }
  .pinned-link-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}
</style>

<details class="pinned-find">
<summary><span class="pinned-find-label">Find Us</span><a class="pinned-about-us" href="100-about/" onclick="event.stopPropagation()">About Us<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg></a></summary>
<div class="pinned-links">
  <div class="pinned-link-col">
    <div class="pinned-link-title"><a href="https://discord.com/invite/xQwWSFDC8Y">Dreaming Saints</a></div>
    <div class="pinned-link-grid">
      <a href="https://discord.com/invite/xQwWSFDC8Y"><img src="https://cdn.simpleicons.org/discord/5865F2" alt="" width="20" height="20" /> Discord</a>
      <a href="https://www.youtube.com/@DreamingSaints"><img src="https://cdn.simpleicons.org/youtube/FF0000" alt="" width="20" height="20" /> YouTube</a>
      <a href="https://x.com/DreamingSaints"><img src="https://cdn.simpleicons.org/x/FFFFFF" alt="" width="20" height="20" /> X</a>
      <a href="https://www.tiktok.com/@dreamingsaints"><img src="https://cdn.simpleicons.org/tiktok/FFFFFF" alt="" width="20" height="20" /> TikTok</a>
      <a href="https://t.me/dreamingsaints"><img src="https://cdn.simpleicons.org/telegram" alt="" width="20" height="20" /> Telegram</a>
      <a href="https://www.facebook.com/groups/2216398175431222"><img src="https://cdn.simpleicons.org/facebook" alt="" width="20" height="20" /> Facebook</a>
      <a href="mailto:dreamingsaints@gmail.com"><img src="https://cdn.simpleicons.org/gmail/EA4335" alt="" width="20" height="20" /> Email</a>
    </div>
  </div>
  <div class="pinned-link-col">
    <div class="pinned-link-title"><a href="https://store.steampowered.com/app/4967660/">Ball-Aqua</a></div>
    <div class="pinned-link-grid">
      <a href="https://store.steampowered.com/app/4967660/"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="" width="20" height="20" /> Steam</a>
      <a href="https://store.steampowered.com/app/5011940/"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="" width="20" height="20" /> Demo</a>
      <a href="https://discussions.unity.com/t/ball-aqua-multiplayer-tropical-ball-rolling-platforming/1734009"><img src="https://cdn.simpleicons.org/unity/FFFFFF" alt="" width="20" height="20" /> Unity</a>
      <a href="https://www.youtube.com/@DreamingSaints"><img src="https://cdn.simpleicons.org/youtube/FF0000" alt="" width="20" height="20" /> YouTube</a>
      <a href="https://x.com/DreamingSaints"><img src="https://cdn.simpleicons.org/x/FFFFFF" alt="" width="20" height="20" /> X</a>
      <a href="https://www.tiktok.com/@dreamingsaints"><img src="https://cdn.simpleicons.org/tiktok/FFFFFF" alt="" width="20" height="20" /> TikTok</a>
      <a href="https://www.instagram.com/ball.aqua/"><img src="https://cdn.simpleicons.org/instagram/E4405F" alt="" width="20" height="20" /> Instagram</a>
      <a href="https://bsky.app/profile/collapsemachine.bsky.social"><img src="https://cdn.simpleicons.org/bluesky" alt="" width="20" height="20" /> Bluesky</a>
    </div>
  </div>
  <div class="pinned-link-col">
    <div class="pinned-link-title"><a href="https://store.steampowered.com/app/2980830/COLLAPSE_MACHINE">COLLAPSE MACHINE</a></div>
    <div class="pinned-link-grid">
      <a href="https://store.steampowered.com/app/2980830/COLLAPSE_MACHINE"><img src="https://cdn.simpleicons.org/steam/FFFFFF" alt="" width="20" height="20" /> Steam</a>
      <a href="https://discussions.unity.com/t/collapse-machine-a-tesla-punk-co-op-open-world-imm-sim-sci-fi-sandbox/1586558/5"><img src="https://cdn.simpleicons.org/unity/FFFFFF" alt="" width="20" height="20" /> Unity</a>
      <a href="https://www.youtube.com/@COLLAPSEMACHINE"><img src="https://cdn.simpleicons.org/youtube/FF0000" alt="" width="20" height="20" /> YouTube</a>
      <a href="https://www.reddit.com/r/COLLAPSEMACHINE"><img src="https://cdn.simpleicons.org/reddit/FF4500" alt="" width="20" height="20" /> Reddit</a>
      <a href="https://www.instagram.com/collapsemachine"><img src="https://cdn.simpleicons.org/instagram/E4405F" alt="" width="20" height="20" /> Instagram</a>
      <a href="https://bsky.app/profile/collapsemachine.bsky.social"><img src="https://cdn.simpleicons.org/bluesky" alt="" width="20" height="20" /> Bluesky</a>
      <a href="https://stcost.github.io/SolidOS/?window=changelog-content"><img src="https://cdn.simpleicons.org/rss/FF6600" alt="" width="20" height="20" /> Implemented Features</a>
      <a href="https://dreamingsaints.github.io/blog/game-design"><img src="https://cdn.simpleicons.org/rss/FF6600" alt="" width="20" height="20" /> Design Guide Lines</a>
    </div>
  </div>
</div>
</details>
