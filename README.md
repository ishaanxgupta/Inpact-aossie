# Inpact - AI-Powered Creator Collaboration & Sponsorship Matchmaking

Inpact is an open-source AI-powered platform designed to connect content creators, brands, and agencies through data-driven insights. By leveraging Generative AI (GenAI), audience analytics, and engagement metrics, Inpact ensures highly relevant sponsorship opportunities for creators while maximizing ROI for brands investing in influencer marketing.

## Features

### AI-Driven Sponsorship Matchmaking
- Automatically connects creators with brands based on audience demographics, engagement rates, and content style.

### AI-Powered Creator Collaboration Hub
- Facilitates partnerships between creators with complementary audiences and content niches.

### AI-Based Pricing & Deal Optimization
- Provides fair sponsorship pricing recommendations based on engagement, market trends, and historical data.

### AI-Powered Negotiation & Contract Assistant
- Assists in structuring deals, generating contracts, and optimizing terms using AI insights.

### Performance Analytics & ROI Tracking
- Enables brands and creators to track sponsorship performance, audience engagement, and campaign success.

## Tech Stack
- **Frontend**: ReactJS
- **Backend**: FastAPI
- **Database**: Supabase
- **AI Integration**: GenAI for audience analysis and sponsorship recommendations

---

## Workflow

### 1. User Registration & Profile Setup
- Creators, brands, and agencies sign up and set up their profiles.
- AI gathers audience insights and engagement data.

### 2. AI-Powered Sponsorship Matchmaking
- The platform suggests brands and sponsorship deals based on audience metrics.
- Creators can apply for sponsorships or receive brand invitations.

### 3. Collaboration Hub
- Creators can find and connect with others for joint campaigns.
- AI recommends potential collaborations based on niche and audience overlap.

### 4. AI-Based Pricing & Contract Optimization
- AI provides fair pricing recommendations for sponsorships.
- Auto-generates contract templates with optimized terms.

### 5. Campaign Execution & Tracking
- Creators execute sponsorship campaigns.
- Brands track campaign performance through engagement and ROI metrics.

### 6. Performance Analysis & Continuous Optimization
- AI analyzes campaign success and suggests improvements for future deals.
- Brands and creators receive insights for optimizing future sponsorships.

---

## Getting Started

### Prerequisites
Ensure you have the following installed:
- Node.js & npm
- Python & FastAPI
- Supabase account

### Installation
#### 1. Clone the repository
```sh
 git clone https://github.com/your-repo/inpact.git
 cd inpact
```

#### 2. Install Frontend Dependencies
```sh
cd client
npm install
```

#### 3. Install Backend Dependencies
```sh
cd server
pip install -r requirements.txt
```

#### 4. Set Up Environment Variables
Create a `.env` file in both the frontend and backend directories with necessary API keys and Supabase credentials.

#### 5. Start Development Servers
- **Frontend**:
```sh
npm start
```
- **Backend**:
```sh
uvicorn main:app --reload
```

---

## Contributing
We welcome contributions from the community! To contribute:
1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Added feature"`).
4. Push to your branch (`git push origin feature-name`).
5. Open a Pull Request.

---


**Overall Workflow**

```mermaid
graph TD;
  A[User Signup/Login] -->|via Supabase Auth| B[User Dashboard];
  
  B -->|Fetch Audience & Engagement Data| C[AI-Powered Sponsorship Matchmaking];
  C -->|Suggest Ideal Brand Deals| D[Creator Applies for Sponsorship];
  D -->|Submit Application| E[Brand Reviews & Shortlists];
  E -->|AI-Based Pricing & Negotiation| F[Contract Generation via AI];
  F -->|Sign Deal| G[Sponsorship Execution];
  
  G -->|Track Performance| H[AI-Powered ROI Analytics];
  H -->|Optimized Insights| I[Brands & Creators Adjust Strategies];
  
  I -->|Feedback Loop| C;
```


**FRONTEND workflow in detail**

```mermaid
graph TD;
  A[User Visits Inpact] -->|Supabase Auth| B[Login/Signup];
  B -->|Fetch User Profile| C[Dashboard Loaded];

  C -->|Request AI-Powered Matches| D[Fetch Sponsorship Deals via API];
  D -->|Display Relevant Matches| E[User Applies for Sponsorship];

  E -->|Send Application via API| F[Wait for Brand Response];
  F -->|Fetch Application Status| G[Show Application Updates];

  G -->|If Approved| H[Contract Generation Page];
  H -->|AI Drafts Contract| I[User Reviews & Signs Contract];

  I -->|Start Campaign Execution| J[Track Sponsorship Performance];
  J -->|Show Performance Analytics| K[AI Optimizes Future Matches];
```

**BACKEND workflow in detail**

```mermaid
graph TD;
  A[User Authentication] -->|Supabase Auth API| B[Verify User];
  B -->|Store User Data in DB| C[Return JWT Token];

  C -->|Fetch User Profile| D[Return Profile Data];

  D -->|Receive Sponsorship Match Request| E[Query AI Engine];
  E -->|Analyze Audience & Engagement| F[Generate Sponsorship Matches];
  F -->|Return Matches via API| G[Send to Frontend];

  G -->|User Applies for Sponsorship| H[Store Application in DB];
  H -->|Notify Brand| I[Brand Reviews Application];

  I -->|Brand Approves/Rejects| J[Update Application Status];
  J -->|If Approved| K[Generate AI-Powered Contract];

  K -->|AI Suggests Pricing & Terms| L[Store Finalized Contract in DB];

  L -->|Track Campaign Performance| M[Analyze Engagement & ROI];
  M -->|Return Insights| N[AI Refines Future Recommendations];

```


## Contact
For queries, issues, or feature requests, please raise an issue or reach out on discord server.

Happy Coding! 
