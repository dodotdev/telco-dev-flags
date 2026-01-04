# Flag Assets Library

A comprehensive collection of world country flags and US state flags, available as SVG vectors and PNG images at multiple resolutions. Each flag includes a JSON metadata file with direct GitHub URLs for easy integration.

## Quick Start

Every flag folder contains a JSON file with metadata and direct download URLs:

```json
{
  "name": "Japan",
  "abbreviation": "JP",
  "files": {
    "svg": "https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/world/jp/jp.svg",
    "png_48x32": "https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/world/jp/jp_48x32.png",
    "png_120x80": "https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/world/jp/jp_120x80.png",
    "png_240x160": "https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/world/jp/jp_240x160.png",
    "png_480x320": "https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/world/jp/jp_480x320.png",
    "png_960x640": "https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/world/jp/jp_960x640.png"
  }
}
```

## Repository Structure

```
flags/
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
    │   ├── tx.json          # Metadata + URLs
    │   ├── tx_48x32.png
    │   ├── tx_120x80.png
    │   ├── tx_240x160.png
    │   ├── tx_480x320.png
    │   └── tx_960x640.png
    ├── ca/
    ├── ny/
    └── ...
```

## What's Included

### World Flags (`/flags/world/`)

**271 flags** including:
- All UN member states
- Territories and dependencies
- Regional flags (England, Scotland, Wales, Catalonia, etc.)
- International organizations (EU, UN, ASEAN, Arab League, etc.)

### US State Flags (`/flags/us/`)

**56 flags** including:
- 50 US states
- District of Columbia
- 5 US territories (American Samoa, Guam, Northern Mariana Islands, Puerto Rico, U.S. Virgin Islands)

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

All PNG files feature:
- Transparent backgrounds
- Consistent dimensions across all flags
- Flags proportionally scaled and centered

## Usage Examples

### Direct URL Access

```html
<!-- World flag (Germany) -->
<img src="https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/world/de/de_240x160.png" alt="Germany">

<!-- US state flag (California) -->
<img src="https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/us/ca/ca_240x160.png" alt="California">
```

### Fetch Metadata via JSON

```javascript
// Fetch flag metadata
const response = await fetch('https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/world/jp/jp.json');
const flag = await response.json();

console.log(flag.name);           // "Japan"
console.log(flag.abbreviation);   // "JP"
console.log(flag.files.svg);      // Full SVG URL
```

### URL Pattern

```
https://raw.githubusercontent.com/dodotdev/telco-dev-flags/master/flags/{type}/{code}/{code}.{format}

Where:
  {type}   = "world" or "us"
  {code}   = 2-letter code (lowercase)
  {format} = "svg", "json", or "{code}_{width}x{height}.png"
```

## Country Codes (ISO 3166-1 alpha-2)

World flags use standard ISO 3166-1 alpha-2 country codes:

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
| fr | France | pt | Portugal | ... | [271 total] |
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
    svg: string;          // Raw GitHub URL to SVG
    png_48x32: string;    // Raw GitHub URL to 48x32 PNG
    png_120x80: string;   // Raw GitHub URL to 120x80 PNG
    png_240x160: string;  // Raw GitHub URL to 240x160 PNG
    png_480x320: string;  // Raw GitHub URL to 480x320 PNG
    png_960x640: string;  // Raw GitHub URL to 960x640 PNG
  };
}
```

## Statistics

| Category | Count |
|----------|-------|
| World Flags | 271 |
| US State Flags | 56 |
| **Total Flags** | **327** |
| Files per Flag | 7 (1 SVG + 5 PNG + 1 JSON) |
| **Total Files** | **2,289** |

## License

This repository is a public resource for artists and developers.

## Contributing

For errors, corrections, or suggestions:
- Open a GitHub issue
- Email: help@do.dev
