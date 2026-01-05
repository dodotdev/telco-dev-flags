<h1 align="center">flags.telco.dev</h1>
<h3 align="center">Free Flag Assets for Developers</h3>
<p align="center">
  <strong>327 world and US flags</strong> in SVG and PNG formats, ready to use in your projects.
</p>
<p align="center">
  <a href="world/us/"><img src="https://flags.telco.dev/world/us/us_48x32.png" alt="US"></a>
  <a href="world/gb/"><img src="https://flags.telco.dev/world/gb/gb_48x32.png" alt="UK"></a>
  <a href="world/jp/"><img src="https://flags.telco.dev/world/jp/jp_48x32.png" alt="Japan"></a>
  <a href="world/de/"><img src="https://flags.telco.dev/world/de/de_48x32.png" alt="Germany"></a>
  <a href="world/fr/"><img src="https://flags.telco.dev/world/fr/fr_48x32.png" alt="France"></a>
  <a href="world/br/"><img src="https://flags.telco.dev/world/br/br_48x32.png" alt="Brazil"></a>
  <a href="world/ca/"><img src="https://flags.telco.dev/world/ca/ca_48x32.png" alt="Canada"></a>
  <a href="world/au/"><img src="https://flags.telco.dev/world/au/au_48x32.png" alt="Australia"></a>
</p>
<p align="center">
  <a href="world/">World Flags</a> •
  <a href="us/">US State Flags</a> •
  <a href="#usage-examples">Usage Examples</a> •
  <a href="#url-pattern">API Reference</a>
</p>

---

## Quick Start

Embed a flag directly in your HTML:

```html
<img src="https://flags.telco.dev/world/jp/jp_240x160.png" alt="Japan">
```

Or fetch metadata via JSON:

```javascript
const response = await fetch('https://flags.telco.dev/world/jp/jp.json');
const flag = await response.json();
// { name: "Japan", abbreviation: "JP", files: { svg: "...", png_48x32: "...", ... } }
```

## What's Included

| Collection | Count | Description |
|------------|-------|-------------|
| [World Flags](world/) | 271 | All UN member states, territories, regional flags, and international organizations |
| [US State Flags](us/) | 56 | 50 states, DC, and 5 US territories |
| **Total** | **327** | Each with SVG + 5 PNG sizes + JSON metadata |

## File Formats

Each flag is available in 6 formats:

| Format | Dimensions | Use Case |
|--------|-----------|----------|
| SVG | Vector | Scalable graphics, web |
| PNG 48x32 | 48 × 32 px | Icons, favicons |
| PNG 120x80 | 120 × 80 px | Small thumbnails |
| PNG 240x160 | 240 × 160 px | Thumbnails |
| PNG 480x320 | 480 × 320 px | Medium display |
| PNG 960x640 | 960 × 640 px | Large display, print |

All PNG files feature transparent backgrounds with flags proportionally scaled and centered.

## Usage Examples

### Direct URL Access

```html
<!-- World flag (Germany) -->
<img src="https://flags.telco.dev/world/de/de_240x160.png" alt="Germany">

<!-- US state flag (California) -->
<img src="https://flags.telco.dev/us/ca/ca_240x160.png" alt="California">
```

### Fetch Metadata via JSON

```javascript
const response = await fetch('https://flags.telco.dev/world/jp/jp.json');
const flag = await response.json();

console.log(flag.name);           // "Japan"
console.log(flag.abbreviation);   // "JP"
console.log(flag.files.svg);      // Full SVG URL
```

### URL Pattern

```
https://flags.telco.dev/{type}/{code}/{code}.{format}

Where:
  {type}   = "world" or "us"
  {code}   = 2-letter code (lowercase)
  {format} = "svg", "json", or "{code}_{width}x{height}.png"
```

## Country Codes (ISO 3166-1 alpha-2)

World flags use standard ISO 3166-1 alpha-2 country codes. Below is a sample of common codes. For the complete list of all 271 flags, browse the [`world/`](world/) directory.

| Code | Country | Code | Country | Code | Country |
|------|---------|------|---------|------|---------|
| ad | Andorra | jp | Japan | se | Sweden |
| ae | UAE | ke | Kenya | sg | Singapore |
| af | Afghanistan | kr | South Korea | th | Thailand |
| au | Australia | mx | Mexico | tr | Turkey |
| br | Brazil | ng | Nigeria | ua | Ukraine |
| ca | Canada | nl | Netherlands | gb | United Kingdom |
| cn | China | nz | New Zealand | us | United States |
| de | Germany | ph | Philippines | vn | Vietnam |
| es | Spain | pl | Poland | za | South Africa |
| fr | France | pt | Portugal | | |
| in | India | ru | Russia | | |
| it | Italy | sa | Saudi Arabia | | |

### Special Codes

| Code | Entity |
|------|--------|
| eu | European Union |
| un | United Nations |
| arab | Arab League |
| asean | ASEAN |
| gb-eng | England |
| gb-sct | Scotland |
| gb-wls | Wales |
| gb-nir | Northern Ireland |
| es-ct | Catalonia |
| es-ga | Galicia |
| es-pv | Basque Country |

## US State Codes

| State | Code | | State | Code |
|-------|------|-|-------|------|
| Alabama | al | | Montana | mt |
| Alaska | ak | | Nebraska | ne |
| Arizona | az | | Nevada | nv |
| Arkansas | ar | | New Hampshire | nh |
| California | ca | | New Jersey | nj |
| Colorado | co | | New Mexico | nm |
| Connecticut | ct | | New York | ny |
| Delaware | de | | North Carolina | nc |
| Florida | fl | | North Dakota | nd |
| Georgia | ga | | Ohio | oh |
| Hawaii | hi | | Oklahoma | ok |
| Idaho | id | | Oregon | or |
| Illinois | il | | Pennsylvania | pa |
| Indiana | in | | Rhode Island | ri |
| Iowa | ia | | South Carolina | sc |
| Kansas | ks | | South Dakota | sd |
| Kentucky | ky | | Tennessee | tn |
| Louisiana | la | | Texas | tx |
| Maine | me | | Utah | ut |
| Maryland | md | | Vermont | vt |
| Massachusetts | ma | | Virginia | va |
| Michigan | mi | | Washington | wa |
| Minnesota | mn | | West Virginia | wv |
| Mississippi | ms | | Wisconsin | wi |
| Missouri | mo | | Wyoming | wy |

### US Territories & District

| Territory | Code |
|-----------|------|
| American Samoa | as |
| District of Columbia | dc |
| Guam | gu |
| Northern Mariana Islands | mp |
| Puerto Rico | pr |
| U.S. Virgin Islands | vi |

## JSON Schema

Every flag folder contains a `{code}.json` file:

```typescript
interface FlagMetadata {
  name: string;           // Full name (e.g., "United States", "Texas")
  abbreviation: string;   // Uppercase code (e.g., "US", "TX")
  files: {
    svg: string;          // URL to SVG
    png_48x32: string;    // URL to 48x32 PNG
    png_120x80: string;   // URL to 120x80 PNG
    png_240x160: string;  // URL to 240x160 PNG
    png_480x320: string;  // URL to 480x320 PNG
    png_960x640: string;  // URL to 960x640 PNG
  };
}
```

## Repository Structure

```
├── world/                    # 271 country/territory flags
│   ├── us/
│   │   ├── us.svg
│   │   ├── us.json          # Metadata + URLs
│   │   ├── us_48x32.png
│   │   ├── us_120x80.png
│   │   ├── us_240x160.png
│   │   ├── us_480x320.png
│   │   └── us_960x640.png
│   ├── gb/
│   ├── jp/
│   └── ...
│
└── us/                       # 56 US state/territory flags
    ├── tx/
    │   ├── tx.svg
    │   ├── tx.json
    │   └── ...
    └── ...
```

## Disclaimer

While we strive to keep all flag data as accurate and up-to-date as possible, we cannot guarantee its accuracy or completeness. Flags and their designs may change over time. Use of these assets is at your own risk.

---

<h3 align="center">Built by <a href="https://do.dev">DoDev</a></h3>
<p align="center">We build developer tools and free resources for the community.</p>
<p align="center">
  <a href="https://github.com/dodotdev">GitHub</a> •
  <a href="https://do.dev">Website</a> •
  <a href="mailto:help@do.dev">Contact</a>
</p>
<p align="center"><em>This is a free, open resource for developers and designers.</em></p>
