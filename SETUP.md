# Quick Start Guide - Vessel Tracking System

## Setup Instructions

### 1. Install Dependencies
```bash
cd c:\Users\MANSOOR\Desktop\web
npm install
```

### 2. Start Development Server
```bash
npm start
```
The app will open at `http://localhost:3000`

### 3. Build for Production
```bash
npm run build
```

## Project Features Implemented

✅ **VesselSearch Component**
- Search bar with autoclear
- Real-time search suggestions
- Disabled state while loading

✅ **VesselFilters Component**
- Expandable filter panel
- Dropdowns for: Vessel Type, Flag State, Status
- Speed range slider (min/max)
- Active filter badge counter
- Reset filters functionality

✅ **VesselList Component**
- List of vessels with expandable details
- Status badges with color coding
- Detailed vessel information grid
- Subscribe and "View on Map" buttons
- Loading states and empty states

✅ **VesselMap Component**
- Interactive SVG map visualization
- Vessel position markers
- Map legend with status indicators
- Selected vessel highlighting
- Grid overlay for navigation

✅ **SubscribeButton Component**
- Modal options for alert types
- 6 different alert type options:
  - Position Change
  - Port Arrival
  - Port Departure
  - Speed Change
  - Course Change
  - Alerts
- Subscribe/Unsubscribe functionality

✅ **API Service Layer**
- Centralized API client
- Vessel endpoints (search, filter, details)
- Subscription endpoints
- Alert endpoints
- Error handling

✅ **Main App & Page**
- VesselsPage with full integration
- Search & filter coordination
- State management
- Mock data (can be replaced with real API)

## File Structure

```
web/
├── src/
│   ├── components/
│   │   ├── VesselSearch.jsx + .css
│   │   ├── VesselFilters.jsx + .css
│   │   ├── VesselList.jsx + .css
│   │   ├── VesselMap.jsx + .css
│   │   └── SubscribeButton.jsx + .css
│   ├── pages/
│   │   └── VesselsPage.jsx + .css
│   ├── services/
│   │   └── api.js
│   ├── App.js + .css
│   └── index.js
├── public/
│   └── index.html
├── package.json
├── tsconfig.json
├── .gitignore
└── README.md
```

## Key Features

### Search & Filter
- Real-time search by vessel name, IMO, or MMSI
- Advanced filters for type, flag, status, and speed
- Live filter counter

### Vessel Display
- Expandable vessel cards with full details
- Color-coded status badges
- Position and navigation information
- Last update timestamp

### Subscriptions
- One-click alert subscription
- Multiple alert type selection
- Easy management of subscriptions

### Responsive Design
- Works on desktop, tablet, and mobile
- Responsive grid layout
- Mobile-optimized sidebar

## Mock Data

The app comes with 5 sample vessels:
1. MAERSK SEALAND - Container Ship (Underway)
2. CMA CGM ANTOINE - Container Ship (Underway)
3. NORDIC ORION - Bulk Carrier (At Anchor)
4. MSC OSCAR - Cargo Ship (Underway)
5. EVERGREEN MARINE - Container Ship (Docked)

Replace with real API calls in `VesselsPage.jsx` fetchVessels function.

## Environment Variables

Create a `.env` file:
```
REACT_APP_API_URL=http://localhost:5000/api
```

## Next Steps

1. Connect to your backend API
2. Replace mock data with real vessel data
3. Implement WebSocket for real-time updates
4. Add authentication if needed
5. Integrate with Leaflet/Mapbox for advanced mapping
6. Deploy to production

## Support

For detailed documentation, see README.md
