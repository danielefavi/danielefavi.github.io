# Font provenance — vendored self-hosted faces (T04, DES-5)

The woff2 binaries in this folder are vendored ONCE into the repo and served
from this path by the static site — the build NEVER fetches fonts at build or
run time (PRIV-1; enforced by the `no-cdn` check). Do not re-run the vendoring
helper casually: `scripts/vendor-fonts.mjs` rewrites these files.

- **Fetched:** 2026-10-24T14:10:07.152Z
- **css2 request:** `https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:ital,wght@0,400;0,500;0,600;1,400&family=Saira+Condensed:wght@500;600;700&display=swap` with a modern Chrome UA
  (`Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36`) so Google served per-subset woff2 files.
- **Subsets kept:** latin + latin-ext only (the site's languages), 7 faces ×
  2 subsets = 14 woff2 files.
- **Faces:** IBM Plex Mono 400/500/600 + 400 italic · Saira Condensed
  500/600/700 (exactly the design contract's faces, DES-5).
- **Licenses:** both families are SIL Open Font License 1.1; the OFL texts
  (`ibm-plex-mono-OFL.txt`, `saira-condensed-OFL.txt`) accompany the binaries
  here and ship in the site output, as the OFL requires.

## unicode-range values (from the same css2 response — mirrored in tokens.css)

- latin: `U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD`
- latin-ext: `U+0100-02BA, U+02BD-02C5, U+02C7-02CC, U+02CE-02D7, U+02DD-02FF, U+0304, U+0308, U+0329, U+1D00-1DBF, U+1E00-1E9F, U+1EF2-1EFF, U+2020, U+20A0-20AB, U+20AD-20C4, U+2113, U+2C60-2C7F, U+A720-A7FF`

## Files (sha256 prefixes; full hashes in the manifest below)

| file | face | subset | sha256 |
| --- | --- | --- | --- |
| `ibm-plex-mono-latin-ext-400-italic.woff2` | IBM Plex Mono 400 italic | latin-ext | `c590f625acd1a180…` |
| `ibm-plex-mono-latin-400-italic.woff2` | IBM Plex Mono 400 italic | latin | `2665f5fbbb334780…` |
| `ibm-plex-mono-latin-ext-400.woff2` | IBM Plex Mono 400 | latin-ext | `f1050dc5317b4343…` |
| `ibm-plex-mono-latin-400.woff2` | IBM Plex Mono 400 | latin | `c36f509c0a8f9f85…` |
| `ibm-plex-mono-latin-ext-500.woff2` | IBM Plex Mono 500 | latin-ext | `77f03e26f981c582…` |
| `ibm-plex-mono-latin-500.woff2` | IBM Plex Mono 500 | latin | `a76f53ca6612e7b3…` |
| `ibm-plex-mono-latin-ext-600.woff2` | IBM Plex Mono 600 | latin-ext | `1b6b18fd0fd240bc…` |
| `ibm-plex-mono-latin-600.woff2` | IBM Plex Mono 600 | latin | `ad4580d8cb4b5f62…` |
| `saira-condensed-latin-ext-500.woff2` | Saira Condensed 500 | latin-ext | `5cb739a9d4288581…` |
| `saira-condensed-latin-500.woff2` | Saira Condensed 500 | latin | `f3e29f770fe0027d…` |
| `saira-condensed-latin-ext-600.woff2` | Saira Condensed 600 | latin-ext | `3cad01c27b0196fa…` |
| `saira-condensed-latin-600.woff2` | Saira Condensed 600 | latin | `6cc20b70e1ec8209…` |
| `saira-condensed-latin-ext-700.woff2` | Saira Condensed 700 | latin-ext | `36a60acd312cd642…` |
| `saira-condensed-latin-700.woff2` | Saira Condensed 700 | latin | `4773efcf48db56fc…` |

## Machine-readable manifest

The `files`/`licenses` lists below are the audit record; the unit suite
(`tests/unit/fonts.spec.js`) re-checks every dist hash against
`sha256` here and every tokens.css `url()` against `file` here.

```json
{
  "fetchedAt": "2026-10-24T14:10:07.152Z",
  "css2Url": "https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:ital,wght@0,400;0,500;0,600;1,400&family=Saira+Condensed:wght@500;600;700&display=swap",
  "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36",
  "subsets": [
    "latin",
    "latin-ext"
  ],
  "files": [
    {
      "file": "ibm-plex-mono-latin-ext-400-italic.woff2",
      "family": "IBM Plex Mono",
      "style": "italic",
      "weight": 400,
      "subset": "latin-ext",
      "unicodeRange": "U+0100-02BA, U+02BD-02C5, U+02C7-02CC, U+02CE-02D7, U+02DD-02FF, U+0304, U+0308, U+0329, U+1D00-1DBF, U+1E00-1E9F, U+1EF2-1EFF, U+2020, U+20A0-20AB, U+20AD-20C4, U+2113, U+2C60-2C7F, U+A720-A7FF",
      "source": "https://fonts.gstatic.com/s/ibmplexmono/v20/-F6pfjptAgt5VM-kVkqdyU8n1ioa23dgregdFOFh.woff2",
      "sha256": "c590f625acd1a18021f23486445b03b8435879b406db1003d3fdd7804e9319fb",
      "bytes": 9788
    },
    {
      "file": "ibm-plex-mono-latin-400-italic.woff2",
      "family": "IBM Plex Mono",
      "style": "italic",
      "weight": 400,
      "subset": "latin",
      "unicodeRange": "U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD",
      "source": "https://fonts.gstatic.com/s/ibmplexmono/v20/-F6pfjptAgt5VM-kVkqdyU8n1ioa1XdgregdFA.woff2",
      "sha256": "2665f5fbbb334780fa135c7f1dc6e2459061a2d6d44c32b7c1fdbc34cde65ede",
      "bytes": 11568
    },
    {
      "file": "ibm-plex-mono-latin-ext-400.woff2",
      "family": "IBM Plex Mono",
      "style": "normal",
      "weight": 400,
      "subset": "latin-ext",
      "unicodeRange": "U+0100-02BA, U+02BD-02C5, U+02C7-02CC, U+02CE-02D7, U+02DD-02FF, U+0304, U+0308, U+0329, U+1D00-1DBF, U+1E00-1E9F, U+1EF2-1EFF, U+2020, U+20A0-20AB, U+20AD-20C4, U+2113, U+2C60-2C7F, U+A720-A7FF",
      "source": "https://fonts.gstatic.com/s/ibmplexmono/v20/-F63fjptAgt5VM-kVkqdyU8n1iEq131nj-otFQ.woff2",
      "sha256": "f1050dc5317b43434c0aeda599d4624c774ffc162e87a8cf204b949b6a85816d",
      "bytes": 8860
    },
    {
      "file": "ibm-plex-mono-latin-400.woff2",
      "family": "IBM Plex Mono",
      "style": "normal",
      "weight": 400,
      "subset": "latin",
      "unicodeRange": "U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD",
      "source": "https://fonts.gstatic.com/s/ibmplexmono/v20/-F63fjptAgt5VM-kVkqdyU8n1i8q131nj-o.woff2",
      "sha256": "c36f509c0a8f9f85f29cb44bc8701d8a9e0b14c499e77a884f789ead7093a7ac",
      "bytes": 10052
    },
    {
      "file": "ibm-plex-mono-latin-ext-500.woff2",
      "family": "IBM Plex Mono",
      "style": "normal",
      "weight": 500,
      "subset": "latin-ext",
      "unicodeRange": "U+0100-02BA, U+02BD-02C5, U+02C7-02CC, U+02CE-02D7, U+02DD-02FF, U+0304, U+0308, U+0329, U+1D00-1DBF, U+1E00-1E9F, U+1EF2-1EFF, U+2020, U+20A0-20AB, U+20AD-20C4, U+2113, U+2C60-2C7F, U+A720-A7FF",
      "source": "https://fonts.gstatic.com/s/ibmplexmono/v20/-F6qfjptAgt5VM-kVkqdyU8n3twJwl5FgsAXHNlYzg.woff2",
      "sha256": "77f03e26f981c582bdba3a7abed4baa2d3149211c01366bb3ab3ba7622ec4ae5",
      "bytes": 8848
    },
    {
      "file": "ibm-plex-mono-latin-500.woff2",
      "family": "IBM Plex Mono",
      "style": "normal",
      "weight": 500,
      "subset": "latin",
      "unicodeRange": "U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD",
      "source": "https://fonts.gstatic.com/s/ibmplexmono/v20/-F6qfjptAgt5VM-kVkqdyU8n3twJwlBFgsAXHNk.woff2",
      "sha256": "a76f53ca6612e7b3828eec2311098675b7f9849ae4169a8bcef6302aec02a6c0",
      "bytes": 10060
    },
    {
      "file": "ibm-plex-mono-latin-ext-600.woff2",
      "family": "IBM Plex Mono",
      "style": "normal",
      "weight": 600,
      "subset": "latin-ext",
      "unicodeRange": "U+0100-02BA, U+02BD-02C5, U+02C7-02CC, U+02CE-02D7, U+02DD-02FF, U+0304, U+0308, U+0329, U+1D00-1DBF, U+1E00-1E9F, U+1EF2-1EFF, U+2020, U+20A0-20AB, U+20AD-20C4, U+2113, U+2C60-2C7F, U+A720-A7FF",
      "source": "https://fonts.gstatic.com/s/ibmplexmono/v20/-F6qfjptAgt5VM-kVkqdyU8n3vAOwl5FgsAXHNlYzg.woff2",
      "sha256": "1b6b18fd0fd240bc6d5850f4df621484722d4b5d3650ebdd1e3a8bbd81c75854",
      "bytes": 8960
    },
    {
      "file": "ibm-plex-mono-latin-600.woff2",
      "family": "IBM Plex Mono",
      "style": "normal",
      "weight": 600,
      "subset": "latin",
      "unicodeRange": "U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD",
      "source": "https://fonts.gstatic.com/s/ibmplexmono/v20/-F6qfjptAgt5VM-kVkqdyU8n3vAOwlBFgsAXHNk.woff2",
      "sha256": "ad4580d8cb4b5f627c2d18457656732f7f7b070f7837fbc380e08054157e6f6c",
      "bytes": 10120
    },
    {
      "file": "saira-condensed-latin-ext-500.woff2",
      "family": "Saira Condensed",
      "style": "normal",
      "weight": 500,
      "subset": "latin-ext",
      "unicodeRange": "U+0100-02BA, U+02BD-02C5, U+02C7-02CC, U+02CE-02D7, U+02DD-02FF, U+0304, U+0308, U+0329, U+1D00-1DBF, U+1E00-1E9F, U+1EF2-1EFF, U+2020, U+20A0-20AB, U+20AD-20C4, U+2113, U+2C60-2C7F, U+A720-A7FF",
      "source": "https://fonts.gstatic.com/s/sairacondensed/v12/EJRLQgErUN8XuHNEtX81i9TmEkrnUchQ-a2fhC61HpnY.woff2",
      "sha256": "5cb739a9d4288581c5591459bba0b4e765992ee6988c38fed8a81f5b243d17ab",
      "bytes": 10180
    },
    {
      "file": "saira-condensed-latin-500.woff2",
      "family": "Saira Condensed",
      "style": "normal",
      "weight": 500,
      "subset": "latin",
      "unicodeRange": "U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD",
      "source": "https://fonts.gstatic.com/s/sairacondensed/v12/EJRLQgErUN8XuHNEtX81i9TmEkrnUchQ962fhC61Hg.woff2",
      "sha256": "f3e29f770fe0027d2a9596af34c08c8dc29cc5faf4db4c1f34d92e7b1fba9d62",
      "bytes": 12336
    },
    {
      "file": "saira-condensed-latin-ext-600.woff2",
      "family": "Saira Condensed",
      "style": "normal",
      "weight": 600,
      "subset": "latin-ext",
      "unicodeRange": "U+0100-02BA, U+02BD-02C5, U+02C7-02CC, U+02CE-02D7, U+02DD-02FF, U+0304, U+0308, U+0329, U+1D00-1DBF, U+1E00-1E9F, U+1EF2-1EFF, U+2020, U+20A0-20AB, U+20AD-20C4, U+2113, U+2C60-2C7F, U+A720-A7FF",
      "source": "https://fonts.gstatic.com/s/sairacondensed/v12/EJRLQgErUN8XuHNEtX81i9TmEkrnfc9Q-a2fhC61HpnY.woff2",
      "sha256": "3cad01c27b0196fad2372ed577d9554b2d72a23c5854fe4e731c966689239686",
      "bytes": 10184
    },
    {
      "file": "saira-condensed-latin-600.woff2",
      "family": "Saira Condensed",
      "style": "normal",
      "weight": 600,
      "subset": "latin",
      "unicodeRange": "U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD",
      "source": "https://fonts.gstatic.com/s/sairacondensed/v12/EJRLQgErUN8XuHNEtX81i9TmEkrnfc9Q962fhC61Hg.woff2",
      "sha256": "6cc20b70e1ec820999536bf962732d49bf5c28eae259df5706584841dcc21df4",
      "bytes": 12244
    },
    {
      "file": "saira-condensed-latin-ext-700.woff2",
      "family": "Saira Condensed",
      "style": "normal",
      "weight": 700,
      "subset": "latin-ext",
      "unicodeRange": "U+0100-02BA, U+02BD-02C5, U+02C7-02CC, U+02CE-02D7, U+02DD-02FF, U+0304, U+0308, U+0329, U+1D00-1DBF, U+1E00-1E9F, U+1EF2-1EFF, U+2020, U+20A0-20AB, U+20AD-20C4, U+2113, U+2C60-2C7F, U+A720-A7FF",
      "source": "https://fonts.gstatic.com/s/sairacondensed/v12/EJRLQgErUN8XuHNEtX81i9TmEkrnGc5Q-a2fhC61HpnY.woff2",
      "sha256": "36a60acd312cd64223db68c4a92da2d140bbb6592bb8fe5b8fff4b14c46ae899",
      "bytes": 10184
    },
    {
      "file": "saira-condensed-latin-700.woff2",
      "family": "Saira Condensed",
      "style": "normal",
      "weight": 700,
      "subset": "latin",
      "unicodeRange": "U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+0304, U+0308, U+0329, U+2000-206F, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD",
      "source": "https://fonts.gstatic.com/s/sairacondensed/v12/EJRLQgErUN8XuHNEtX81i9TmEkrnGc5Q962fhC61Hg.woff2",
      "sha256": "4773efcf48db56fc229704467304bdee1766640a21a67f9898de46720e05e76a",
      "bytes": 12192
    }
  ],
  "licenses": [
    {
      "family": "IBM Plex Mono",
      "file": "ibm-plex-mono-OFL.txt",
      "source": "https://raw.githubusercontent.com/google/fonts/main/ofl/ibmplexmono/OFL.txt",
      "sha256": "7e6b2818edbd8f6a01ae80641cc8f16a51080d08fb4e532be3a0b6f74adb07da",
      "bytes": 4456
    },
    {
      "family": "Saira Condensed",
      "file": "saira-condensed-OFL.txt",
      "source": "https://raw.githubusercontent.com/google/fonts/main/ofl/sairacondensed/OFL.txt",
      "sha256": "0e2ccc5da1dd979f08ba82bca2fb61592506a1e58d3cbfc26d904f0db71bd812",
      "bytes": 4403
    }
  ]
}
```
