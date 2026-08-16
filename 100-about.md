# #100 About

<style>
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
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
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
</style>

<details class="about-person" id="stcost">
<summary><span class="about-head"><span class="about-avatar-link"><span class="about-avatar-wrap"><img src="https://avatars.fastly.steamstatic.com/bce10ec46b619fd7a8660cc783d36462d44aa89e_full.jpg" alt="StCost" width="96" height="96" /><img src="https://shared.fastly.steamstatic.com/community_assets/images/items/1239690/f0af6694686ebf42992824a3ee5f6313fc00cd7c.png" alt=" " width="96" height="96" /></span></span><span class="about-id"><h2 class="about-name"><a class="about-anchor" href="#stcost">StCost</a></h2><ul class="about-roles"><li>Team Lead</li><li>Software Engineer</li><li>Game Designer</li></ul></span><span class="about-head-split"></span><span class="about-tops"><a class="fav-chip" href="https://store.steampowered.com/app/22380/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/22380/capsule_184x69.jpg" alt="Fallout New Vegas" width="28" height="28" /><span>Fallout: New Vegas</span></a><a class="fav-chip" href="https://music.youtube.com/search?q=2+Mello"><img src="https://img.youtube.com/vi/nbogUmJkeBI/mqdefault.jpg" alt="2 Mello" width="28" height="28" /><span>2 Mello</span></a><a class="fav-chip" href="https://en.wikipedia.org/wiki/The_Venture_Bros."><img src="https://media.themoviedb.org/t/p/w185/ckQE1aLYQkRpp2HmHljiELAiOr1.jpg" alt="The Venture Bros." width="28" height="28" /><span>The Venture Bros.</span></a><a class="fav-chip" href="https://unity.com/"><img src="https://cdn.simpleicons.org/unity/FFFFFF" alt="Unity" width="28" height="28" /><span>Unity</span></a></span></span></summary>
<div class="about-row">
<div class="about-section">
<div class="about-section-label">About</div>
<p class="about-note">2016: first games — C++ terminal at university, see <a href="https://dreamingsaints.github.io/blog/34-collapse-machine-stages/">#34</a>. First Steam game <a href="https://store.steampowered.com/app/1775350/RISING_BONEvR/">RISING BONEvR</a> 2021. Spent too much time in <a href="https://store.steampowered.com/app/440/">TF2</a>. Hobbies: skateboarding, FPV piloting.</p>
</div>
<div class="about-section">
<div class="about-section-label">Likes</div>
<p class="about-note"><a class="about-anchor" href="#sttaya">StTaya</a>, <a href="https://www.pepsi.com/">Pepsi</a>, <a href="https://www.nutella.com/">Nutella</a>, buns, <a href="https://en.wikipedia.org/wiki/Earl_Grey_tea">Earl Grey tea</a>, chips, beefsteak, strawberries.</p>
<div class="fav-colors">
<a class="fav-chip" href="https://store.steampowered.com/app/2980830/COLLAPSE_MACHINE"><span class="fav-swatch orange"></span><span>#ff8000</span></a>
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
<a class="fav-chip" href="https://store.steampowered.com/app/823500/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/823500/capsule_184x69.jpg" alt="BONEWORKS" width="28" height="28" /><span>BONEWORKS</span></a>
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
<a class="fav-chip" href="https://music.youtube.com/search?q=2+Mello"><img src="https://img.youtube.com/vi/nbogUmJkeBI/mqdefault.jpg" alt="2 Mello" width="28" height="28" /><span>2 Mello</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Frank+Sinatra"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e3/Frank_Sinatra_%281957_studio_portrait_close-up%29.jpg/120px-Frank_Sinatra_%281957_studio_portrait_close-up%29.jpg" alt="Frank Sinatra" width="28" height="28" /><span>Frank Sinatra</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Pink+Floyd"><img src="https://upload.wikimedia.org/wikipedia/en/d/d6/Pink_Floyd_-_all_members.jpg" alt="Pink Floyd" width="28" height="28" /><span>Pink Floyd</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Bullet+for+My+Valentine"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Bullet_for_My_Valentine_Full_Force_2022_17.jpg/120px-Bullet_for_My_Valentine_Full_Force_2022_17.jpg" alt="Bullet for My Valentine" width="28" height="28" /><span>Bullet for My Valentine</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Evans+Blue"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/05/EvansBlueLive.JPG/120px-EvansBlueLive.JPG" alt="Evans Blue" width="28" height="28" /><span>Evans Blue</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=SAINT+PEPSI"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music211/v4/47/b0/53/47b053ee-d011-2d7f-36d9-237adb441f09/820233284479.jpg/100x100bb.jpg" alt="SAINT PEPSI" width="28" height="28" /><span>SAINT PEPSI</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Breaking+Benjamin"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Breaking_Benjamin_2-14-15.jpg/120px-Breaking_Benjamin_2-14-15.jpg" alt="Breaking Benjamin" width="28" height="28" /><span>Breaking Benjamin</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=TOOL"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Tool_live_Birmingham_2022.jpg/120px-Tool_live_Birmingham_2022.jpg" alt="TOOL" width="28" height="28" /><span>TOOL</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=A+Perfect+Circle"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/A_Perfect_Circle_Lollapalooza_Chile_2013.jpg/120px-A_Perfect_Circle_Lollapalooza_Chile_2013.jpg" alt="A Perfect Circle" width="28" height="28" /><span>A Perfect Circle</span></a>
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
<span class="fav-chip"><span class="fav-swatch black"></span><span>Black</span></span>
<span class="fav-chip"><span class="fav-swatch tiffany"></span><span>Tiffany</span></span>
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
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Peaceful_Warrior"><img src="https://media.themoviedb.org/t/p/w185/9OqDWRgUDtrkLZ57RwyMz8NzV81.jpg" alt="Peaceful Warrior" width="28" height="28" /><span>Peaceful Warrior</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/JoJo%27s_Bizarre_Adventure:_Stardust_Crusaders"><img src="https://media.themoviedb.org/t/p/w185/kX9noqY0YpOPKwXpRXYg1hEIqmM.jpg" alt="Stardust Crusaders" width="28" height="28" /><span>Stardust Crusaders</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/The_Venture_Bros."><img src="https://media.themoviedb.org/t/p/w185/ckQE1aLYQkRpp2HmHljiELAiOr1.jpg" alt="The Venture Bros." width="28" height="28" /><span>The Venture Bros.</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Halo_(TV_series)"><img src="https://media.themoviedb.org/t/p/w185/4UmNhZCEu8Vt3byMvNxNEPyf8EY.jpg" alt="Halo" width="28" height="28" /><span>Halo</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Game_of_Thrones"><img src="https://media.themoviedb.org/t/p/w185/1XS1oqL89opfnbLl8WnZY1O1uJx.jpg" alt="Game of Thrones" width="28" height="28" /><span>Game of Thrones</span></a>
</p>
</div>
</details>

<details class="about-person" id="stgrikus">
<summary><span class="about-head"><span class="about-avatar-link"><span class="about-avatar-wrap"><img src="https://avatars.fastly.steamstatic.com/55ca41f5225fee88d359222787ebac8f11241fa1_full.jpg" alt="StGrikus" width="96" height="96" /><img src="https://shared.fastly.steamstatic.com/community_assets/images/items/1361210/6a2ff332dc612e923dd1330b12981aa34ebc4895.png" alt=" " width="96" height="96" /></span></span><span class="about-id"><h2 class="about-name"><a class="about-anchor" href="#stgrikus">StGrikus</a></h2><ul class="about-roles"><li>Sound Designer</li><li>Sound Engineer</li><li>Marketing</li></ul></span><span class="about-head-split"></span><span class="about-tops"><a class="fav-chip" href="https://store.steampowered.com/app/1361210/"><img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1361210/capsule_184x69.jpg" alt="Darktide" width="28" height="28" /><span>Darktide</span></a><a class="fav-chip" href="https://music.youtube.com/search?q=Twenty+One+Pilots"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f4/Twenty_One_Pilots_%2822314815091%29.jpg/120px-Twenty_One_Pilots_%2822314815091%29.jpg" alt="Twenty One Pilots" width="28" height="28" /><span>Twenty One Pilots</span></a><a class="fav-chip" href="https://en.wikipedia.org/wiki/Back_to_the_Future"><img src="https://media.themoviedb.org/t/p/w185/WPRsNihhKPQmmQgckg1XLTRMYa.jpg" alt="Back to the Future" width="28" height="28" /><span>Back to the Future</span></a><a class="fav-chip" href="https://www.fmod.com/"><img src="https://www.fmod.com/favicon.ico" alt="FMOD" width="28" height="28" /><span>FMOD</span></a></span></span></summary>
<div class="about-row">
<div class="about-section">
<div class="about-section-label">About</div>
<p class="about-note">Coffee enthusiast and technical sound designer. 2012: started learning guitar, and music and sound have absorbed me ever since. Since 2023, worked as a barista at one of the city's best coffee shops, took part in coffee roasting more than once, and placed second in a Brewers Cup. Started studying <a href="https://www.fmod.com/">FMOD</a> and how sound works in games in 2025. Spent too much time in <a href="https://store.steampowered.com/app/730/">CS:GO</a>. Hobbies: guitar, coffee, skateboarding.</p>
</div>
<div class="about-section">
<div class="about-section-label">Likes</div>
<p class="about-note">Analyzing song structure and soundstage, <a href="https://heatroasters.com/product/colombia-grape/">HeatRoasters Colombia Grape</a> (Armenia, co-fermentation), <a href="https://heatroasters.com/product/colombia-paraiso-92/">HeatRoasters Colombia Paraiso 92</a> (Huila, washed, yeast fermentation and thermal shock), <a href="https://en.wikipedia.org/wiki/Da_Hong_Pao">Da Hong Pao</a>, White Oolong.</p>
<div class="fav-colors">
<span class="fav-chip"><span class="fav-swatch purple"></span><span>Purple</span></span>
<span class="fav-chip"><span class="fav-swatch ultramarine"></span><span>#120A8F</span></span>
</div>
</div>
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
<a class="fav-chip" href="https://music.youtube.com/search?q=Twenty+One+Pilots"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f4/Twenty_One_Pilots_%2822314815091%29.jpg/120px-Twenty_One_Pilots_%2822314815091%29.jpg" alt="Twenty One Pilots" width="28" height="28" /><span>Twenty One Pilots</span></a>
<a class="fav-chip" href="https://music.youtube.com/@themidnightofficial"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music221/v4/9d/2b/28/9d2b28ce-421f-85f5-d48c-7a79ba8f9edb/859728051630_cover.jpg/100x100bb.jpg" alt="The Midnight" width="28" height="28" /><span>The Midnight</span></a>
<a class="fav-chip" href="https://music.youtube.com/@GUNSHIPMUSIC"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music113/v4/7e/0e/6a/7e0e6a27-f9c5-178c-f045-c7211beb4217/192641495236_Cover.jpg/100x100bb.jpg" alt="GUNSHIP" width="28" height="28" /><span>GUNSHIP</span></a>
<a class="fav-chip" href="https://music.youtube.com/@KAVINSKY"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music125/v4/c1/2d/fe/c12dfe8f-cdf6-e179-d69a-8ec35f760266/00602537248681.rgb.jpg/100x100bb.jpg" alt="Kavinsky" width="28" height="28" /><span>Kavinsky</span></a>
<a class="fav-chip" href="https://music.youtube.com/channel/UCr7ZuYFBf8Xna3QWDMaqXbQ"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music122/v4/ae/f3/3c/aef33c9b-9ab4-6a7e-4b22-d3984b2ff469/849320014362.png/100x100bb.jpg" alt="Nothing More" width="28" height="28" /><span>Nothing More</span></a>
<a class="fav-chip" href="https://music.youtube.com/channel/UCHuHOg9oIYKKkdfkxQj7urw"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music211/v4/41/0b/06/410b069f-c25f-f9bc-7cca-1299ff520ff5/0.jpg/100x100bb.jpg" alt="Radiotehnika" width="28" height="28" /><span>Radiotehnika</span></a>
<a class="fav-chip" href="https://music.youtube.com/channel/UCEwg4JDZJEkST4oiiFv_nrg"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music211/v4/70/7d/0c/707d0ccf-dab2-f2e1-92f0-e7d1b6e5812d/artwork.jpg/100x100bb.jpg" alt="Kalax" width="28" height="28" /><span>Kalax</span></a>
<a class="fav-chip" href="https://music.youtube.com/@TOOLmusic"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Tool_live_Birmingham_2022.jpg/120px-Tool_live_Birmingham_2022.jpg" alt="TOOL" width="28" height="28" /><span>TOOL</span></a>
<a class="fav-chip" href="https://music.youtube.com/channel/UCrSorX845CEWXzU4Z7BojjA"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9b/Red_Hot_Chili_Peppers_2012-07-02_001.jpg/120px-Red_Hot_Chili_Peppers_2012-07-02_001.jpg" alt="Red Hot Chili Peppers" width="28" height="28" /><span>Red Hot Chili Peppers</span></a>
<a class="fav-chip" href="https://music.youtube.com/channel/UCRr1xG_2WIDs18a6cIiCxeA"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/68/Daft_Punk_in_2013_2-_centered.jpg/120px-Daft_Punk_in_2013_2-_centered.jpg" alt="Daft Punk" width="28" height="28" /><span>Daft Punk</span></a>
<a class="fav-chip" href="https://music.youtube.com/@eminem"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Eminem_Lollapalooza_2014_Chicago_%28cropped%29.jpg/120px-Eminem_Lollapalooza_2014_Chicago_%28cropped%29.jpg" alt="Eminem" width="28" height="28" /><span>Eminem</span></a>
<a class="fav-chip" href="https://music.youtube.com/@LinkinPark"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/73/Linkin_Park_at_Soundwave_2013.jpg/120px-Linkin_Park_at_Soundwave_2013.jpg" alt="Linkin Park" width="28" height="28" /><span>Linkin Park</span></a>
<a class="fav-chip" href="https://music.youtube.com/search?q=Cathode+Electrode"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music221/v4/fc/dc/8a/fcdc8a3e-1c89-1fcc-5a56-4c35d09f4d51/859741339685_cover.jpg/100x100bb.jpg" alt="Cathode Electrode" width="28" height="28" /><span>Cathode Electrode</span></a>
<a class="fav-chip" href="https://music.youtube.com/@DrakeBellOfficial"><img src="https://is1-ssl.mzstatic.com/image/thumb/Music124/v4/f1/2a/21/f12a2180-7926-00a2-d526-f9f695f7a7f6/00602517178502.rgb.jpg/100x100bb.jpg" alt="Drake Bell" width="28" height="28" /><span>Drake Bell</span></a>
</p>
</div>
<div class="about-section">
<div class="about-section-label">Movies/series/cartoons</div>
<p class="fav-row">
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Back_to_the_Future"><img src="https://media.themoviedb.org/t/p/w185/WPRsNihhKPQmmQgckg1XLTRMYa.jpg" alt="Back to the Future" width="28" height="28" /><span>Back to the Future</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Attack_on_Titan_(TV_series)"><img src="https://media.themoviedb.org/t/p/w185/hTP1DtLGFamjfu8WqjnuQdP1n4i.jpg" alt="Attack on Titan" width="28" height="28" /><span>Attack on Titan</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Interstellar_(film)"><img src="https://media.themoviedb.org/t/p/w185/9d1sCoMSGJZtghS2X9us1h9u8lW.jpg" alt="Interstellar" width="28" height="28" /><span>Interstellar</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Inception"><img src="https://media.themoviedb.org/t/p/w185/r84x4x93LbZ2gozISTBYVeq0gLZ.jpg" alt="Inception" width="28" height="28" /><span>Inception</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Joker_(2019_film)"><img src="https://media.themoviedb.org/t/p/w185/5h77YBF7g9s0ju5yblWskkN3wa7.jpg" alt="Joker" width="28" height="28" /><span>Joker</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Soul_(2020_film)"><img src="https://media.themoviedb.org/t/p/w185/nPHeauU0udKIpFH208cxhnvmHFB.jpg" alt="Soul" width="28" height="28" /><span>Soul</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Luck_(2022_film)"><img src="https://media.themoviedb.org/t/p/w185/w7qTIyUz2LED8Jpd24sPx0GGQpC.jpg" alt="Luck" width="28" height="28" /><span>Luck</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/The_World%27s_Fastest_Indian"><img src="https://media.themoviedb.org/t/p/w185/1ucKR3oNvWa8ft0mq2g8qA8bITy.jpg" alt="The World's Fastest Indian" width="28" height="28" /><span>The World's Fastest Indian</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Rick_and_Morty"><img src="https://media.themoviedb.org/t/p/w185/tnXwqcZ98EVKuMzRtcvPRJukwI3.jpg" alt="Rick and Morty" width="28" height="28" /><span>Rick and Morty</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Hacksaw_Ridge"><img src="https://media.themoviedb.org/t/p/w185/8mYSAEymWKubpgRUyzN2BeiIoUo.jpg" alt="Hacksaw Ridge" width="28" height="28" /><span>Hacksaw Ridge</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Iron_Man_(2008_film)"><img src="https://media.themoviedb.org/t/p/w185/e196fIvszLpgaUItX3Yl3seyUTl.jpg" alt="Iron Man" width="28" height="28" /><span>Iron Man</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Iron_Man_2"><img src="https://media.themoviedb.org/t/p/w185/g9ANwGAcemCCOBUYKgAL3EsZJBE.jpg" alt="Iron Man 2" width="28" height="28" /><span>Iron Man 2</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Batman_Begins"><img src="https://media.themoviedb.org/t/p/w185/gDpMT5nrgsuSAgX3NfRg2ZOsr0d.jpg" alt="Batman Begins" width="28" height="28" /><span>Batman Begins</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Oppenheimer_(film)"><img src="https://media.themoviedb.org/t/p/w185/iAv3HAlrrIgjcf2yCFvedJzekXT.jpg" alt="Oppenheimer" width="28" height="28" /><span>Oppenheimer</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/The_Mask_(1994_film)"><img src="https://media.themoviedb.org/t/p/w185/v0mptZw5Zxf0KfF96JsZEBxBtzZ.jpg" alt="The Mask" width="28" height="28" /><span>The Mask</span></a>
<a class="fav-chip" href="https://en.wikipedia.org/wiki/Drake_%26_Josh"><img src="https://media.themoviedb.org/t/p/w185/aXDUxPkMswvgmwWuNjkTe4UgzfL.jpg" alt="Drake &amp; Josh" width="28" height="28" /><span>Drake &amp; Josh</span></a>
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
