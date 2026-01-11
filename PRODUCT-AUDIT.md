# Product Audit System

A routine audit system for Skittish Farms to track product coverage, verify affiliate links, and identify content gaps.

---

## Quick Start

```bash
# Run full audit
node scripts/audit.js

# Check affiliate links only
node scripts/audit.js --links-only

# Generate summary report
node scripts/audit.js --report
```

**Dashboard**: Open `admin/product-audit.html` in your browser for a visual interface.

---

## System Components

| File | Purpose |
|------|---------|
| `product-audit.json` | Central database of all products, ASINs, prices, and coverage status |
| `admin/product-audit.html` | Visual dashboard with checklists and gap analysis |
| `scripts/audit.js` | Automated audit script for links, schema, and reports |
| `reports/` | Generated audit reports (created automatically) |

---

## Current Product Coverage

### Ring (11/13 covered)

| Product | Price | Dedicated Page | Status |
|---------|-------|----------------|--------|
| Ring Stick Up Cam Battery | $99.99 | ring-stick-up-cam-review.html | ✓ |
| Ring Stick Up Cam Plug-In | $99.99 | ring-stick-up-cam-review.html | ✓ |
| Ring Stick Up Cam Solar | $149 | ring-solar-camera-setup.html | ✓ |
| Ring Floodlight Cam Wired Plus | $199 | ring-floodlight-camera-guide.html | ✓ |
| Ring Floodlight Cam Wired Pro | $249 | ring-floodlight-camera-guide.html | ✓ |
| Ring Spotlight Cam Plus Battery | $179 | ring-spotlight-cam-comparison.html | ✓ |
| Ring Spotlight Cam Plus Solar | $229 | ring-spotlight-cam-comparison.html | ✓ |
| Ring Spotlight Cam Pro Battery | $229 | ring-spotlight-cam-comparison.html | ✓ |
| Ring Spotlight Cam Pro Solar | $279 | ring-spotlight-cam-comparison.html | ✓ |
| Ring Peephole Cam | $129 | ring-peephole-camera-review.html | ✓ |
| Ring Solar Panel | $49 | ring-solar-camera-setup.html | ✓ |
| Ring Indoor Cam (2nd Gen) | $59 | — | ✗ Gap |
| Ring Battery Doorbell Plus | $149 | — | ✗ Gap |

### Blink (0/4 covered)

| Product | Price | Dedicated Page | Status |
|---------|-------|----------------|--------|
| Blink Outdoor 4 (4th Gen) | $99.99 | — | ✗ **HIGH PRIORITY** |
| Blink Mini 2 | $39 | — | ✗ Gap |
| Blink Video Doorbell | $49 | — | ✗ Gap |
| Blink Solar Panel | $29 | — | Accessory |

### Nest (3/5 covered)

| Product | Price | Dedicated Page | Status |
|---------|-------|----------------|--------|
| Google Nest Cam (Battery) | $179 | nest-outdoor-camera-guide.html | ✓ |
| Google Nest Cam with Floodlight | $279 | nest-floodlight-camera-review.html | ✓ |
| Google Nest Cam (Wired) | $99 | nest-outdoor-camera-guide.html | ✓ |
| Google Nest Doorbell (Battery) | $179 | — | ✗ Gap |
| Google Nest Doorbell (Wired) | $179 | — | ✗ Gap |

---

## Content Gaps (Priority Order)

### HIGH Priority

| Product | ASIN | Price | Search Volume | Action |
|---------|------|-------|---------------|--------|
| **Blink Outdoor 4** | B0B1N5HW22 | $99.99 | ~8,100/mo | Create `blink-outdoor-4-review.html` |

**Why urgent**: Major competitor product with 2-year battery life (key differentiator). Currently only mentioned in ring-vs-blink-comparison.html. Missing significant search traffic.

### MEDIUM Priority

| Product | ASIN | Price | Search Volume | Suggested File |
|---------|------|-------|---------------|----------------|
| Ring Indoor Cam | B0B6GLQ23P | $59 | ~3,600/mo | `ring-indoor-cam-review.html` |
| Ring Doorbell Plus | B09WZBPX7K | $149 | ~12,000/mo | `ring-doorbell-review.html` |
| Blink Mini 2 | B0BWV2HXHJ | $39 | ~4,400/mo | `blink-mini-review.html` |
| Blink Video Doorbell | B08SG2MS3V | $49 | ~2,900/mo | `blink-doorbell-review.html` |
| Nest Doorbell | B09FCLPLWX | $179 | ~5,400/mo | `nest-doorbell-review.html` |

### LOW Priority

| Product | ASIN | Price | Notes |
|---------|------|-------|-------|
| Ring Chime | B0B9HQKDMH | $37 | Accessory - covered in setup guide |
| Ring Chime Pro | B0B9HQJPHL | $49 | Accessory - covered in setup guide |
| Blink Solar Panel | B08SHR5SFH | $29 | Accessory - can include in Blink pages |

---

## Audit Schedule

### Weekly Tasks
- [ ] Check all affiliate links are functional
- [ ] Verify product prices match Amazon
- [ ] Review dateModified in schema markup
- [ ] Check for new product releases
- [ ] Review Google Search Console for errors
- [ ] Check Amazon Associates for policy warnings

### Monthly Tasks
- [ ] Full content accuracy review
- [ ] Update comparison tables if prices changed
- [ ] Check competitor content for gaps
- [ ] Review search rankings for target keywords
- [ ] Update "Updated" dates in articles
- [ ] Create at least one new page from gap list

### Quarterly Tasks
- [ ] Full site audit for broken links
- [ ] Review and update all product specifications
- [ ] Add new products to database
- [ ] Create new content for high-priority gaps
- [ ] Review and update schema markup

---

## Affiliate Link Format

All affiliate links must follow this format:

```
https://www.amazon.com/dp/{ASIN}?tag=organicallysu-20
```

**Example**:
```html
<a href="https://www.amazon.com/dp/B0B1N5HW22?tag=organicallysu-20"
   class="buy-button"
   target="_blank"
   rel="nofollow noopener">
   Check Price on Amazon
</a>
```

---

## Product Database (ASINs)

### Ring
| Product | ASIN |
|---------|------|
| Ring Stick Up Cam Battery | B0B9HP68LL |
| Ring Stick Up Cam Plug-In | B0B9HN5RWX |
| Ring Stick Up Cam Solar | B0B9HQJPHL |
| Ring Floodlight Cam Wired Plus | B08F6GPQQ7 |
| Ring Floodlight Cam Wired Pro | B08FCWRXQR |
| Ring Spotlight Cam Plus Battery | B09DRX62ZV |
| Ring Spotlight Cam Plus Solar | B09DRPMHL7 |
| Ring Spotlight Cam Pro Battery | B09DRX62ZV |
| Ring Spotlight Cam Pro Solar | B0B83HZVCF |
| Ring Peephole Cam | B0B9HMD22K |
| Ring Indoor Cam (2nd Gen) | B0B6GLQ23P |
| Ring Solar Panel | B07YNQ4V2V |
| Ring Battery Doorbell Plus | B09WZBPX7K |

### Blink
| Product | ASIN |
|---------|------|
| Blink Outdoor 4 | B0B1N5HW22 |
| Blink Mini 2 | B0BWV2HXHJ |
| Blink Video Doorbell | B08SG2MS3V |
| Blink Solar Panel | B08SHR5SFH |

### Nest
| Product | ASIN |
|---------|------|
| Google Nest Cam (Battery) | B09FCLPLWX |
| Google Nest Cam with Floodlight | B09FCLVB2Q |
| Google Nest Cam (Wired) | B094FMDHQS |
| Google Nest Doorbell (Battery) | B09FCLPLWX |
| Google Nest Doorbell (Wired) | B09FCLM5P3 |

### Accessories
| Product | ASIN |
|---------|------|
| Ring Chime | B0B9HQKDMH |
| Ring Chime Pro | B0B9HQJPHL |

---

## Running the Audit Script

### Full Audit
```bash
node scripts/audit.js
```

Checks:
- All affiliate links for proper tag
- Internal links for 404s
- Schema markup validation
- Content gap identification

Output: Saves report to `reports/audit-{date}.json`

### Links Only
```bash
node scripts/audit.js --links-only
```

Quick check of all affiliate links for proper formatting.

### Report Only
```bash
node scripts/audit.js --report
```

Generates summary of products, coverage, and gaps without running checks.

---

## Adding New Products

1. Edit `product-audit.json`
2. Add product to appropriate category in `products` object:

```json
{
  "id": "product-slug",
  "name": "Product Name",
  "asin": "B0XXXXXXXX",
  "listedPrice": 99.99,
  "lastPriceCheck": null,
  "currentPrice": null,
  "priceStatus": "needs_check",
  "dedicatedPage": null,
  "mentionedIn": [],
  "affiliateLinkStatus": "needs_check",
  "lastContentUpdate": null,
  "contentGaps": ["No dedicated review page"],
  "auditNotes": "Notes about this product"
}
```

3. Run audit to verify: `node scripts/audit.js --report`

---

## Dashboard Usage

Open `admin/product-audit.html` in a browser to:

- View stats overview (products, coverage, gaps)
- See prioritized content gaps with search volume
- Browse product inventory by category
- Track page audit status
- Use weekly/monthly checklists (saved to localStorage)
- Export audit reports as JSON

---

*Last updated: January 2026*
