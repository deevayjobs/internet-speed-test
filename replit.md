# SpeedCheck Internet Speed Test Application

## Overview

SpeedCheck is a modern, web-based internet speed testing application that provides accurate measurements of download speed, upload speed, ping latency, and jitter. Built with React and Node.js, the application features a clean, responsive interface with real-time progress tracking and comprehensive test results visualization.

The application simulates network performance testing by measuring various metrics against multiple test servers, providing users with detailed insights into their internet connection quality. It includes features like server selection, progress visualization with animated gauges, and comprehensive result reporting.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: React hooks with custom speed test hook for managing test state and progress
- **UI Components**: Radix UI primitives with shadcn/ui component system for consistent, accessible interface
- **Styling**: Tailwind CSS with custom design system using CSS variables for theming
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework for API endpoints
- **API Design**: RESTful endpoints for server discovery, ping testing, and speed measurements
- **Development Server**: Integrated Vite development server with middleware for seamless full-stack development
- **Static Serving**: Express serves built React application in production

### Data Layer
- **Database ORM**: Drizzle ORM configured for PostgreSQL with type-safe queries
- **Schema Location**: Shared schema definitions in `/shared/schema.ts` for type consistency
- **Migrations**: Drizzle Kit for database migration management
- **Storage Interface**: Abstracted storage layer with in-memory implementation for speed test data

### Component Architecture
- **Speed Test Engine**: Custom service class managing test phases (ping, download, upload) with progress callbacks
- **Real-time Updates**: Progress tracking through callback system updating React state
- **Test Visualization**: Animated gauge component showing current speeds with SVG-based progress rings
- **Results Display**: Comprehensive results section with metric cards and sharing functionality

### External Dependencies
- **Database**: PostgreSQL via Neon serverless database connection
- **UI Framework**: Radix UI primitives for accessible, unstyled components
- **Icons**: Lucide React for consistent iconography
- **HTTP Client**: TanStack Query for API state management and caching
- **Form Handling**: React Hook Form with Zod validation schemas
- **Date Utilities**: date-fns for timestamp formatting and manipulation

The application follows a modular architecture with clear separation between client and server code, shared type definitions, and reusable UI components. The speed test functionality is implemented as a service class that can be easily extended or modified without affecting the UI layer.