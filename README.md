# Article Quality Control Assessment

**Description:** An automated article quality control system that parses Google Docs, runs quality checks for images and links, and manages the content through an Airtable interface with WordPress upload functionality.

## Repository Structure

```
ai-article-qc-assessment/
├── README.md
├── n8n/
│   ├── 01_article_workflow.json          # Main parsing & QC workflow
│   └── 02_wordpress_webhook.json         # Upload webhook handler
├── airtable/
│   ├── schema.md                         # Airtable field definitions
├── output/
│   ├── article.html                      # Sample processed article HTML
├── docs/
│   ├── architecture.md                   # System architecture overview
│   └── future-features.md                # Enhancement suggestions
```

## What the System Does

**Extracts from Google Docs:**
- Meta Title and Meta Description (from labeled lines)
- Article Title (H1 heading)
- All images with alt text and Google Drive verification
- All links (excluding image anchors)
- Clean article HTML content

**Quality Checks:**
- Image count (2-8 optimal range)
- Link count (3-15 optimal range)
- Google Drive hosting verification for all images
- Alt text presence validation
- Overall quality score (PASS/WARNING/FAIL)

**Airtable Interface:**
- Displays all extracted content and quality metrics
- Shows pass/fail status with detailed issue descriptions
- Provides "Upload to WordPress" button for approved articles

## Next Steps

This assessment covers the core requirements. I can record a Loom walkthrough video explaining the code architecture and decisions if you'd like to proceed with the full evaluation.

**Live Demo**: [Airtable Interface](https://airtable.com/invite/l?inviteId=invqmJYwGAXVoiUkS&inviteToken=94668d196083544ab38ae1d3eec1149b66c5c9f5b57ab07f44bd0f68a6113dd5)