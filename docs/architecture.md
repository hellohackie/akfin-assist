# Architecture

## Overview

AkFinAssist is a full-stack stock signal application build with monorepo structure.

## Components

- **Backend (FastAPI)**: REST API  WebSocket server
- **Frontend (React + Vite)**: Single-page dashboard application
- **PostgreSQL + TimescaleDB**: Time-series data storage
- **Redis**: Caching and pub/sub for real-time updates

## Data Flow

1. **Data Ingestion**: Background scheduler fetches stock prices from data providers
2. **Signal Computation**: Technical indicators are computed on price data
3. **Signal Storage**: Computed signals are stored in the database
4. **API Serving**: Frontend queries signals and price data via REST API
5. **Real-time Updates**: WebSocket pushes new signals to connected clients