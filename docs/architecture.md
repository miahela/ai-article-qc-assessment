# System Architecture

## Flow
Google Docs → n8n Parser → Quality Checks → Airtable Interface → WordPress Upload

## Key Components
1. **Article Workflow**: Extracts content, validates quality, writes to Airtable
2. **WordPress Webhook**: Mock upload handler triggered by Airtable buttons
3. **Airtable Interface**: Review dashboard with approval workflow

## Quality Validation
- Image count: 2-8 optimal
- Link count: 3-15 optimal  
- Google Drive hosting check
- Alt text validation
- Meta field extraction with fallbacks