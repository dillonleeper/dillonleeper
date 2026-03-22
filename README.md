# Dillon Leeper

**Analytics Engineer** — building data pipelines, warehouse systems, and analytics tools for ecommerce operations.

I work at the intersection of data engineering and business analytics. I design and ship end-to-end data systems — API ingestion, raw file archival, dimensional warehouse modeling, and dashboard delivery — and I have 6+ years of ecommerce context that makes the data decisions meaningful.

Self-taught through production systems. Currently based in New York.

---

## Featured Project

### SellerIQ — Ecommerce Analytics Platform

SellerIQ is a full-stack ecommerce analytics platform for Amazon and Walmart marketplace sellers. It ingests raw marketplace data, models it into a clean dimensional warehouse, and serves it through a custom dashboard built in Next.js.

**Backend (pipeline):** [github.com/dillonleeper/SellerIQ](https://github.com/dillonleeper/SellerIQ)
**Frontend (dashboard):** [github.com/dillonleeper/selleriq-app](https://github.com/dillonleeper/selleriq-app)

**What it does:**
- Ingests Amazon Sales & Traffic, Catalog, Listings, and FBA Inventory reports via SP-API
- - Archives raw files to S3 before any transformation (immutable raw layer)
  - - Parses and loads data into a layered Postgres warehouse — staging → intermediate → fact/dim
    - - Resolves product identity across SKU, ASIN, and parent ASIN into a canonical `dim_product`
      - - Runs idempotent batch loads with full job logging, checksums, and error tracking
        - - Backfilled 62 weeks of historical sales data across US and CA marketplaces
          - - Dashboard with Sales Overview, Product Performance, Weekly Cadence heatmap, and more
           
            - **Backend tech:** Python · PostgreSQL · Amazon S3 · Amazon SP-API · psycopg2 · boto3
           
            - **Frontend tech:** Next.js · TypeScript · React · Recharts · Supabase · Tailwind CSS
           
            - ---

            ## Other Projects

            ### Amazon SP-API Sales Pipeline & Dashboard

            [github.com/dillonleeper/amazon-sp-api-sales-pipeline](https://github.com/dillonleeper/amazon-sp-api-sales-pipeline)

            The predecessor to SellerIQ — a Python pipeline pulling Amazon sales and traffic data from SP-API, loading into Google Sheets, and visualizing in Looker Studio. Built as an operational reporting tool before transitioning to the full warehouse architecture.

            **Tech:** Python · Amazon SP-API · Google Sheets API · Looker Studio

            ---

            ## Tech Stack

            ```
            Languages     Python, SQL, TypeScript
            Pipeline      Batch ETL, API ingestion, idempotent loading, job logging
            Warehouse     Dimensional modeling, staging/intermediate/fact/dim layers
            APIs          Amazon SP-API, Walmart Marketplace API
            Infra         Amazon S3, PostgreSQL, Supabase, psycopg2, boto3
            Frontend      Next.js, React, Recharts, Tailwind CSS
            Analytics     KPI design, contribution margin, marketplace performance
            ```

            ---

            ## Currently Working On

            - Phase 3 complete — FBA inventory snapshots live in production
            - - Building Inventory and Marketplace Compare dashboard pages
              - - Adding order item detail and finance/fee ingestion (Phases 4 & 5)
                - - Building toward an AI query layer over curated warehouse data
                 
                  - ---

                  *Open to Analytics Engineer and Data Engineer roles in New York or remote.*
