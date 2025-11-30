cat > docs/SETUP.md << 'EOF'
# Wardrobe OS - Development Setup

## Prerequisites
- Node.js 18+ 
- npm or yarn
- Docker (for database)
- Git

## Initial Setup

1. Clone the repository
2. Install dependencies: `npm install`
3. Start database: `docker-compose up -d`
4. Copy `.env.example` to `.env` and configure
5. Run migrations (when we create them)
6. Start development: `npm run dev`

## Database
- PostgreSQL 15 running in Docker
- Connection string: `postgresql://wardrobe:wardrobe_dev_password@localhost:5432/wardrobe_os`
- Access via: `docker exec -it wardrobe-db psql -U wardrobe -d wardrobe_os`

## Troubleshooting
- If port 5432 is in use, stop other PostgreSQL instances
- If Docker won't start, check Docker Desktop is running

Last updated: [Today's date]
EOF