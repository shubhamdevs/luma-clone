# Luma Event Management Platform Clone

## Project Overview
A modern event management platform inspired by Luma, allowing users to create, manage, and discover events with a clean, intuitive interface.

## Core Features

### 1. Navigation & Layout
- **Header Navigation**: Events, Calendars, Discover tabs
- **Dark Theme**: Primary dark background with purple/gray accents
- **Responsive Design**: Mobile-first approach with desktop optimization

### 2. Event Discovery Page
- **Event Listing**: Grid/list view of all public events
- **Search & Filter**: Find events by name, date, location, category
- **Event Cards**: Show event thumbnail, name, date, time, location preview

### 3. Create Event Page
Based on the UI design, the create event form includes:

#### Event Basic Information
- **Event Name**: Text input with placeholder styling
- **Calendar Integration**: Personal Calendar dropdown selector
- **Public/Private Toggle**: Visibility control in header
- **Event Cover**: Large colorful geometric pattern selection (left panel)

#### Date & Time Configuration
- **Start Date/Time**: "Wed, 9 Jul" format with time picker (09:00 AM)
- **End Date/Time**: "Wed, 9 Jul" format with time picker (10:00 AM)
- **Timezone Display**: GMT+05:30 Calcutta format
- **Duration Calculation**: Automatic duration display

#### Location Settings
- **Add Event Location**: Input field with placeholder "Offline location or virtual link"
- **Location Type**: Support for both physical addresses and virtual meeting links
- **Location Validation**: Verify URLs for virtual events

#### Event Content
- **Description**: Rich text editor with "Add Description" prompt
- **Media Upload**: Event images, videos, attachments
- **Event Tags**: Categorization and searchability

#### Event Options Panel
- **Tickets**: 
  - Free/Paid toggle
  - Price setting for paid events
  - Ticket types (General, VIP, Early Bird)
- **Require Approval**: Toggle switch (shown as enabled in design)
- **Capacity**: 
  - Unlimited/Limited options
  - Number input for limited capacity
  - Waitlist functionality

#### Theme Customization
- **Theme Selector**: Dropdown with "Minimal" and other theme options
- **Color Schemes**: Multiple pre-designed themes
- **Custom Branding**: Logo upload and color customization

#### Action Buttons
- **Create Event**: Primary action button (white background)
- **Save Draft**: Secondary action for incomplete events
- **Preview**: See how event appears to attendees

### 4. Event Management
- **Event Dashboard**: Host view with attendee management
- **Analytics**: Event performance metrics
- **Communication**: Message attendees, send updates
- **Check-in**: QR code or manual attendee verification

### 5. User Authentication & Profiles
- **Clerk Integration**: Secure authentication system
- **User Profiles**: Personal information, event history
- **Calendar Sync**: Integration with personal calendars
- **Notification Settings**: Email/SMS preferences

## Technical Architecture

### Tech Stack
- **Frontend**: React with plain CSS (no frameworks like Tailwind)
- **Database**: Supabase (PostgreSQL)
- **Authentication**: Clerk
- **Deployment**: Vercel/Netlify recommended
- **Version Control**: Git with GitHub

### Database Schema (Supabase)
```sql
-- Users table (managed by Clerk)
-- Events table
-- Attendees/Registrations table
-- Tickets table
-- Event themes table
```

### Folder Structure
```
src/
├── components/
│   ├── EventCard/
│   │   ├── EventCard.jsx
│   │   └── EventCard.module.css
│   ├── CreateEvent/
│   │   ├── CreateEvent.jsx
│   │   └── CreateEvent.module.css
│   ├── Navigation/
│   │   ├── Navigation.jsx
│   │   └── Navigation.module.css
│   └── Layout/
│       ├── Layout.jsx
│       └── Layout.module.css
├── pages/
│   ├── EventsPage/
│   ├── CreateEventPage/
│   └── EventDetailPage/
├── hooks/
├── utils/
├── styles/
│   ├── globals.css
│   └── variables.css
└── App.jsx
```

### Design System
- **Colors**: 
  - Primary: Dark purple/gray (#2D2B3A)
  - Secondary: Light gray text (#9CA3AF)
  - Accent: Green (#10B981), Blue (#3B82F6)
  - Background: Dark (#1F1D2B)
- **Typography**: Clean, modern font stack
- **Components**: Reusable UI components with consistent styling
- **Spacing**: 8px grid system
- **Border Radius**: Consistent rounded corners (8px, 12px)

### Key UI Components to Build
1. **DateTimePicker**: Custom date/time selection
2. **LocationInput**: Smart location input with validation
3. **ThemeSelector**: Visual theme picker
4. **ToggleSwitch**: Custom toggle for options
5. **EventCard**: Reusable event display component
6. **FormSection**: Consistent form layout wrapper

## Development Guidelines
- **Component Architecture**: Each component in separate folder with JSX and CSS module
- **State Management**: React hooks for local state, Context API for global state
- **Responsive Design**: Mobile-first CSS with media queries
- **Accessibility**: ARIA labels, keyboard navigation, screen reader support
- **Performance**: Lazy loading, image optimization, code splitting
- **Testing**: Jest + React Testing Library for component tests

## Security & Best Practices
- **Environment Variables**: Store sensitive data (API keys, DB credentials)
- **Input Validation**: Client and server-side validation
- **Authentication**: Secure route protection with Clerk
- **Data Sanitization**: Prevent XSS and SQL injection
- **Rate Limiting**: Prevent abuse of API endpoints

## Deployment
- **Build Process**: `npm run build`
- **Environment Setup**: Production environment variables
- **Database Migration**: Supabase migration files
- **CI/CD**: GitHub Actions for automated deployment
