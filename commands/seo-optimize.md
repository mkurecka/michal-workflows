---
name: seo-optimize
description: Optimize project SEO - titles, meta descriptions, structured data, sitemap.
arguments:
  - name: scope
    description: Optimization scope (full, meta, structured, sitemap)
    required: false
---

# /seo-optimize - SEO Optimization

Analyze and improve your project's SEO.

## Instructions

### Phase 1: Analyze Current SEO
1. Find HTML files or framework config
2. Check current state:
   - Page titles
   - Meta descriptions
   - Open Graph tags
   - Twitter cards
   - Structured data (JSON-LD)
   - Sitemap.xml
   - robots.txt

### Phase 2: Meta Tags (scope=meta or full)
1. **Titles**:
   - Ensure unique per page
   - 50-60 characters
   - Include primary keyword
   - Brand at end

2. **Meta Descriptions**:
   - 150-160 characters
   - Include call to action
   - Unique per page

3. **Open Graph**:
   - og:title, og:description, og:image
   - og:url, og:type

4. **Twitter Cards**:
   - twitter:card, twitter:title
   - twitter:description, twitter:image

### Phase 3: Structured Data (scope=structured or full)
Add JSON-LD for:
- Organization/Person
- WebSite with SearchAction
- BreadcrumbList
- Article (for blog posts)
- Product (for e-commerce)
- FAQ (if applicable)

### Phase 4: Technical SEO (scope=sitemap or full)
1. **sitemap.xml**:
   - Generate or update
   - Include all public pages
   - Set priorities and changefreq

2. **robots.txt**:
   - Allow search engines
   - Reference sitemap
   - Block admin/private paths

3. **Canonical URLs**:
   - Add canonical tags
   - Prevent duplicate content

### Phase 5: Report
- Changes made
- SEO score improvement
- Remaining recommendations

## Example Usage

```
/seo-optimize                    # Full SEO audit and fix
/seo-optimize meta               # Just meta tags
/seo-optimize structured         # Add structured data
/seo-optimize sitemap            # Generate sitemap
```

## Framework-Specific

**Next.js**: Update `app/layout.tsx` metadata
**Nuxt**: Update `nuxt.config.ts` head
**HTML**: Update `<head>` directly
**WordPress**: Update theme functions or plugin

## SEO Checklist

- [ ] Unique titles per page
- [ ] Meta descriptions 150-160 chars
- [ ] Open Graph tags
- [ ] Twitter cards
- [ ] Structured data (JSON-LD)
- [ ] sitemap.xml
- [ ] robots.txt
- [ ] Canonical URLs
- [ ] Mobile-friendly
- [ ] Fast loading
