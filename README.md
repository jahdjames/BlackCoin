# BlackCoin - Contact & Financial Management System

BlackCoin is a modern web application for managing contacts, financial transactions, and contracts. It provides a comprehensive solution for businesses and individuals to track their professional relationships and financial activities.

## Features

### Contact Management
- Store and manage contact information including name, email, phone, company, and address
- Track contact status (active/inactive)
- Add notes and additional details for each contact
- Automatic timestamp tracking for creation and updates

### Financial Ledger
- Record income and expense transactions
- Link transactions to specific contacts
- Track transaction status (pending, completed, cancelled)
- Include reference numbers and detailed descriptions
- Automatic date tracking and amount calculations
- Support for decimal precision in financial amounts

### Contract Management
- Create and manage contracts with associated contacts
- Track contract lifecycle (draft, active, completed, terminated)
- Record contract terms, amounts, and important dates
- Store detailed descriptions and notes
- Monitor contract status and timelines

## Tech Stack

### Frontend
- **Framework**: Next.js 14 (React)
- **Styling**: Tailwind CSS
- **UI Components**: Custom components with Tailwind CSS
- **State Management**: React Hooks and Context API
- **Form Handling**: React Hook Form
- **Date Handling**: date-fns

### Backend
- **Database**: PostgreSQL (via Supabase)
- **API**: Supabase REST and Realtime APIs
- **Authentication**: Supabase Auth
- **Database Features**:
  - UUID primary keys
  - Automatic timestamp management
  - Referential integrity
  - Check constraints for data validation
  - Optimized indexes for performance
  - Trigger-based updated_at timestamp management

### Development Tools
- **Language**: TypeScript
- **Package Manager**: npm
- **Version Control**: Git
- **Environment Variables**: .env.local for local development
- **Code Quality**: ESLint
- **Styling**: PostCSS

## Database Schema

### Contacts Table
- UUID primary key
- Timestamps (created_at, updated_at)
- Contact details (name, email, phone, company, address)
- Status tracking (is_active)
- Notes field

### Ledger Entries Table
- UUID primary key
- Timestamps (created_at, updated_at)
- Contact reference (foreign key)
- Financial details (amount, type, description)
- Transaction metadata (date, status, reference_number)
- Notes field

### Contracts Table
- UUID primary key
- Timestamps (created_at, updated_at)
- Contact reference (foreign key)
- Contract details (title, description, terms)
- Financial information (amount)
- Status tracking
- Date management (start_date, end_date)
- Notes field

## Getting Started

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up environment variables:
   - Copy `.env.example` to `.env.local`
   - Add your Supabase credentials

4. Run the development server:
   ```bash
   npm run dev
   ```

5. Access the application at `http://localhost:3000`

## Development

- The application uses Next.js 14 with the App Router
- Tailwind CSS is configured for styling
- Database migrations are managed through Supabase
- TypeScript ensures type safety throughout the application

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.