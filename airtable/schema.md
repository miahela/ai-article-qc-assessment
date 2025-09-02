# Airtable Schema

## Base: Article Quality Control
**Base ID**: appPJFQscfuHzbEc4

## Table: Articles

| Field Name | Type | Description |
|------------|------|-------------|
| Article Title | Single line text | H1 heading extracted from document |
| Meta Title | Single line text | SEO meta title from document |
| Meta Description | Long text | SEO meta description from document |
| Quality Score | Single select | PASS/WARNING/FAIL based on quality checks |
| Image Count | Number | Total number of images found |
| Link Count | Number | Total number of links found |
| Issues | Long text | Semicolon-separated list of quality issues |
| Ready for WordPress | Checkbox | Auto-calculated: true if Quality Score = PASS |
| Processing Date | Date | When the article was processed |
| WordPress Upload Status | Single select | Pending/Uploaded/Failed |
| Meta Title Length | Formula/Number | Character count of meta title |
| Meta Description Length | Formula/Number | Character count of meta description |
| Total Elements | Formula/Number | Sum of images + links |
| Has Issues | Formula/Checkbox | True if Issues field is not empty |
| Days Since Processing | Formula/Number | Days between Processing Date and today |
| SEO Improvement Suggestions | Long text | Manual field for SEO recommendations |
| Content Quality Feedback | Long text | Manual field for editorial feedback |
| Upload to WordPress | Button | Triggers webhook URL to mock WordPress upload |

## Quality Score Logic
- **PASS**: No quality issues detected
- **WARNING**: 1-2 minor issues (still uploadable)
- **FAIL**: 3+ issues or critical problems

## Quality Check Thresholds
- **Images**: 2-8 images optimal
- **Links**: 3-15 links optimal
- **Image hosting**: Must be Google Drive URLs
- **Alt text**: Required for all images

## Sample Data Structure
Based on your current records, each processed article includes tech topics (React, APIs, Node.js) and e-commerce content (product reviews).