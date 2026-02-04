# Invoice Control System - FastAPI Backend

A comprehensive invoice processing system built with FastAPI that handles invoice intake via email polling, PDF parsing, validation against price records, and mismatch resolution.

## Features

- **Email Polling Service**: Automatically polls Microsoft Graph API for invoice emails with PDF attachments
- **PDF Parsing**: Extracts structured data from PDF invoices using pdfplumber (non-OCR)
- **Scanned PDF Detection**: Flags scanned PDFs for future OCR processing
- **Invoice Validation**: Validates invoice lines against buying_price_records and supplier_sku_mappings
- **Mismatch Resolution**: Handles price acceptance, disputes, and audit logging
- **Manual Upload**: Web interface for manual invoice upload
- **Audit Logging**: Comprehensive logging of all price changes and disputes


## Architecture

```
invoice/
├── backend/
│   ├── api/v1/endpoints/     # API endpoints
│   ├── services/              # Business logic services
│   ├── schemas/pydantic/      # Pydantic schemas
│   ├── core/                 # Configuration and logging
│   ├── main.py               # FastAPI app entry point
│   ├── Dockerfile            # Docker configuration
│   └── requirements.txt      # Python dependencies
├── docker-compose.yml        # Docker Compose configuration
└── README.md
```