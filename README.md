# 1.PROJECT INSTALLATION
## 1.1. Requirements
- NodeJS 20+ 
- PostgreSQL 15.8.1.022
- PostgREST 12.2.3

## 1.2. Installation
- `git clone https://github.com/vuongmanhnghia/nagix-plan.git`
- `cd nagix-plan`
- `npm install`
- Set up environment:
+ **.env**:
```
DATABASE_URL=
# Direct connection to the database. Used for migrations.
DIRECT_URL=
NEXT_PUBLIC_SITE_URL=
```
+ **.env.local**:
```
AUTH_SECRET=
AUTH_GOOGLE_ID=
AUTH_GOOGLE_SECRET=
```
- Run migrations: `npx prisma migrate dev`
- Run project: `npm run dev`

# 2.PROJECT STRUCTURE 
```
└── 📁PlanBuddy
    └── 📁app
        └── 📁fonts
        └── globals.css
        └── layout.tsx // root layout
        └── 📁api // api routing
        └── auth.ts
        └── 📁dashboard // page routing
        └── 📁meeting
            └── 📁[meetingId] // dynamic page routing
                └── page.tsx
        └── page.tsx
    └── 📁components
        └── 📁common
        └── 📁features // special components for each page
            └── 📁AddGoogleCalendar
            └── 📁Auth
            └── 📁AvailabilityFill
            └── 📁Dashboard
            └── 📁MeetingCUForm
        └── 📁Layout // special components for layojt
            └── 📁Footer
            └── 📁Navbar
        └── 📁ui // shadcn's components
        └── 📁utils
            └── constant.ts
            └── 📁helper
    └── 📁hooks
    └── 📁lib
        └── meeting.ts // api service functions
        └── prisma.ts // db connect
        └── utils.ts 
    └── 📁prisma
        └── 📁migrations
        └── 📁schema 
            └── schema.prisma
            └── auth.prisma
            └── meeting.prisma
            ...
    └── 📁public // public assets
        └── 📁icons
        └── 📁logos
    └── 📁types // typescript interfaces
    ...
```