# Smart India Hackathon Workshop
# Date:24-11-2026
## Reference Number:26019043
## Name: Ragavan S

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution
### KisanSetu is a mobile-first (Android + web) marketplace with three user groups:

### Farmers/FPOs list produce with quantity, quality grade, harvest date and expected price. They use voice input and regional languages, and the app also works over SMS/IVR for low-literacy users.
### Consumers (households, RWAs, hostels) place orders for fresh produce, either on subscription (weekly baskets) or one-off.
### Bulk buyers (retailers, restaurants, canteens, mandis, processors) post demand and run reverse auctions or bulk RFQs.

### Core modules:

### Listing and quality grading: photo-based AI grading and a simple farmer-side checklist.
### Price discovery: a transparent price range based on live mandi (Agmarknet) prices, so farmers know the fair value and buyers see the cost breakdown.
### Logistics layer: village-level collection points, pooled pickups, a cold-chain partner network and last-mile delivery.
### Payments: UPI and escrow, with payment released on delivery confirmation and settled to the farmer within 24-48 hours.
### AI engine: demand forecasting, price forecasting, route optimization and spoilage-risk alerts.
### Government dashboard: real-time view of prices, supply-demand gaps and the share of the consumer price that reaches the farmer.

### 2. How it addresses the problem

### Problem	How KisanSetu responds
### Multiple intermediaries take margin	Direct farmer-to-buyer matching, with only a small, transparent platform and logistics fee
### Farmers lack price information	Live mandi benchmarks and price forecasts
### Consumers pay inflated prices	Shorter chain means lower retail price, and fees are shown openly
### Post-harvest loss and waste	Demand forecasting tells farmers what, when and how much to sell, and logistics cuts transit time
### No logistics access for small farmers	Aggregation by FPOs and pooled pickups
### Delayed payments	Escrow with fast settlement

### 3. Innovation and uniqueness

### Forecast-driven selling: farmers get "what to grow/sell and when" advice, not just a listing page.
### Pooled, AI-optimized logistics: orders from many small farmers are batched into shared routes to cut cost per kg.
### Price transparency ledger: each order shows the split (farmer share, logistics, platform fee), which also gives policymakers measurable data on intermediary margins.
### Inclusive access: voice, vernacular and IVR/SMS for farmers with basic phones.
### Interoperability: built on open networks (ONDC, AgriStack, eNAM) so it complements existing systems rather than replacing them.

## Technical Approach
### 1. Technologies

### Layer	Stack
### Mobile/Web	Flutter or React Native; React for web and the admin dashboard
### Backend	Python (FastAPI) or Node.js; PostgreSQL + PostGIS; Redis
### AI/ML	Python, scikit-learn, XGBoost/LightGBM and Prophet or LSTM for demand and price forecasting; Google OR-Tools for vehicle routing; CNN (MobileNet/EfficientNet) for produce quality grading
### Language/voice	Bhashini APIs for speech and translation in Indian languages
### Payments	UPI/payment gateway with escrow
### Maps/routing	OpenStreetMap/OSRM or Google Maps API
### Cloud/DevOps	AWS/Azure/MeghRaj, Docker, Kubernetes, CI/CD
### Notifications	SMS, WhatsApp Business API, IVR
### Data sources	Agmarknet, eNAM, IMD weather data, Open Government Data
### Optional IoT	Temperature and humidity sensors for cold-chain tracking

### 2. Methodology and process

### Flow:

### Farmer/FPO lists produce → AI grading + price suggestion
        ↓
### Demand matching (consumers, bulk buyers)
        ↓
### Order confirmed → payment held in escrow
        ↓
### Pooled pickup at village collection point (route optimized)
        ↓
### Transport via hub/cold chain → last-mile delivery
        ↓
### Buyer confirms delivery → payment released to farmer
        ↓
### Data feeds back into forecasting and the government dashboard

### Implementation phases:

### Discovery: survey farmers, FPOs and buyers in 1-2 pilot districts.
### MVP: listings, orders, payments, basic logistics booking and the price dashboard.
### AI integration: demand and price forecasting, route optimization and quality grading.
### Pilot: one district with 3-5 FPOs and 500-1,000 consumers and bulk buyers.
### Scale: add districts, integrate ONDC/eNAM and onboard more logistics partners.

### For the prototype or presentation, include: an app wireframe (farmer listing, buyer cart, tracking), the architecture diagram, a sample forecast chart and a route-optimization demo.

## Feasibility and Viability
### 1. Feasibility

### Technical: all components (marketplace, forecasting, routing, payments) use mature, available tools.
### Policy fit: it aligns with government priorities such as FPO promotion, eNAM, ONDC and Digital Agriculture Mission.
### Economic: the platform earns a small commission (about 2-4%) plus logistics margin. Per-kg savings from removing intermediary layers can fund both the commission and better farmer prices.
### Operational: FPOs already aggregate produce, which makes onboarding practical.

### 2. Potential challenges and risks

### Low digital literacy and smartphone access among farmers.
### Perishability and cold-chain costs.
### Trust issues: buyers fear quality mismatch and farmers fear delayed payment.
### Scattered farms make first-mile collection costly.
### Mandi traders may resist, and farmers may sell off-platform once relationships form.
### Cold-start problem: buyers need supply and farmers need demand.
### Data quality for forecasting in early stages.

### 3. Strategies to overcome them

### Use FPOs, Krishi Mitras and CSCs as local "assisted" onboarding agents, with voice and vernacular interfaces.
### Partner with existing cold-chain and logistics providers instead of building assets, and use collection points to keep first-mile cost down.
### Build trust through escrow, quality grading with photo evidence, ratings and a dispute-resolution process.
### Start hyperlocal in one cluster (a district and its nearby city) to solve cold start, and anchor demand with institutional buyers such as hostels, canteens and retailers.
### Make the platform useful beyond transactions (price advice, forecasts, faster payment) so farmers stay on it.
### Begin with public data and historical mandi data, then improve models as order data accumulates.

## Impact and Benefits
### 1. Impact on the target audience

### Farmers/FPOs: a larger share of the consumer price, faster payment and better planning through forecasts.
### Consumers: fresher produce at lower prices, with price transparency.
### Bulk buyers: reliable supply, bulk pricing and traceability.
### Government: real-time data on supply, demand and prices for policy and inflation monitoring.

### 2. Benefits

### Economic: better farmer income, lower consumer prices, less price volatility and a lower cost per kg for logistics. Rural jobs are created for pickup agents, aggregators and drivers.
### Social: support for small and marginal farmers, empowerment of FPOs and women-led groups, and wider access to fresh food.
### Environmental: less food waste, fewer empty-return trips through route optimization, and lower fuel use and emissions.
### Systemic: a shorter, more transparent supply chain and a dataset for evidence-based agricultural policy.

### Suggested KPIs for the pilot: farmer price realization (%), consumer price reduction (%), post-harvest loss reduction, average delivery time, and payment settlement time.

## Research and References
### eNAM (National Agriculture Market): enam.gov.in
### Agmarknet (mandi price data): agmarknet.gov.in
### ONDC (Open Network for Digital Commerce): ondc.org
### AgriStack / Digital Agriculture Mission: agristack.gov.in
### Bhashini (Indian-language AI): bhashini.gov.in
### Government scheme for promotion of 10,000 FPOs: Ministry of Agriculture & Farmers Welfare
### Google OR-Tools (vehicle routing): developers.google.com/optimization
### Facebook Prophet / time-series forecasting documentation
### Studies on the farmer's share of consumer rupee and mandi margins (for example NABARD, NITI Aayog and ICRIER reports on agricultural marketing)
