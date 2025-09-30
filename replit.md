# Overview

This is a mobile-first React web application called "Smart Nutritionist" (also known as "Pocket Dietitian") designed to help users manage their dietary needs and nutrition goals. The application features a comprehensive profile management system, personalized nutrition tracking, and AI-powered dietary assistance. Built with modern web technologies, it provides an intuitive interface for users to track their food intake, manage dietary restrictions, and receive personalized nutrition recommendations.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **Routing**: Wouter for client-side routing with mobile-optimized page structure
- **UI Components**: Radix UI primitives with shadcn/ui component library for consistent design
- **Styling**: Tailwind CSS with CSS variables for theming support
- **State Management**: React Context API for global app state combined with TanStack Query for server state
- **Forms**: React Hook Form with Zod validation for type-safe form handling
- **Responsive Design**: Mobile-first approach with max-width container limiting to mobile dimensions

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful API with structured route handlers
- **Error Handling**: Centralized error middleware with proper HTTP status codes
- **Request Logging**: Custom middleware for API request/response logging
- **Development Server**: Integrated Vite dev server with HMR support

## Data Storage Solutions
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Schema**: Shared schema definitions between client and server using Drizzle-Zod
- **Tables**: 
  - Profiles (user dietary profiles with restrictions and goals)
  - Settings (app configuration and preferences)
  - History (user interaction and activity tracking)
- **Storage Implementation**: Dual storage approach with in-memory storage for development and PostgreSQL for production

## Key Features Architecture
- **Multi-Profile Support**: Users can create and switch between different dietary profiles
- **Internationalization**: Multi-language support (English, Armenian, Russian, Ukrainian, Chinese)
- **Voice Input**: Web Speech API integration for hands-free data entry
- **Theme System**: Dynamic theming with 10+ pre-defined color schemes
- **Currency Support**: Multi-currency support for pricing features

## External Dependencies

- **Database Provider**: Neon Database (@neondatabase/serverless) for managed PostgreSQL hosting
- **UI Framework**: Radix UI component primitives for accessible UI components
- **Validation**: Zod for runtime type validation and schema definitions
- **Date Handling**: date-fns for date manipulation and formatting
- **Development Tools**: Replit-specific plugins for development environment integration
- **Build Tools**: ESBuild for server bundling and Vite for client-side bundling
- **Session Management**: connect-pg-simple for PostgreSQL-backed session storage

The application follows a clean separation of concerns with shared type definitions, modular component architecture, and a scalable backend structure that can easily accommodate additional features like AI integration, payment processing, and advanced nutrition analysis.