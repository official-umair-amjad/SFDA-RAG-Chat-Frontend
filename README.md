# ChatBot App

A simple, responsive chat application built with Next.js, TypeScript, and Tailwind CSS. This app integrates with a webhook API to send messages and receive responses.

## Features

- 🎨 Modern, responsive UI with beautiful design
- 💬 Real-time chat interface
- 🔄 API integration with custom headers and body format
- 📱 Mobile-friendly responsive design
- ⚡ Fast and lightweight
- 🚀 Ready for Vercel deployment

## Tech Stack

- **Next.js 14** - React framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **UUID** - Session ID generation

## Getting Started

### Prerequisites

- Node.js 18+ and npm
- Git

### Local Development

1. Clone the repository:
```bash
git clone <your-repo-url>
cd chatbot-app
```

2. Install dependencies:
```bash
npm install
```

3. Run the development server:
```bash
npm run dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Deployment on Vercel

### Method 1: Deploy from GitHub (Recommended)

1. Push your code to a GitHub repository
2. Go to [Vercel](https://vercel.com)
3. Sign in with your GitHub account
4. Click "New Project"
5. Import your repository
6. Vercel will automatically detect it's a Next.js app
7. Click "Deploy"

### Method 2: Deploy with Vercel CLI

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Deploy:
```bash
vercel
```

3. Follow the prompts to deploy

## API Configuration

The app is configured to send POST requests to:
- **URL**: `https://754ddfd59c70.ngrok-free.app/webhook/bf4dd093-bb02-472c-9454-7ab9af97bd1d`
- **Headers**: 
  - `Content-Type: application/json`
  - `auth: thisisauth`
- **Body**:
  ```json
  {
    "chatInput": "user message",
    "sessionId": "unique-session-id"
  }
  ```

## Project Structure

```
chatbot-app/
├── app/
│   ├── globals.css      # Global styles with Tailwind
│   ├── layout.tsx       # Root layout component
│   └── page.tsx         # Main chat page
├── package.json         # Dependencies and scripts
├── next.config.js       # Next.js configuration
├── tailwind.config.js   # Tailwind CSS configuration
├── tsconfig.json        # TypeScript configuration
└── vercel.json          # Vercel deployment configuration
```

## Features Breakdown

- **Responsive Design**: Works perfectly on desktop, tablet, and mobile
- **Session Management**: Each chat session has a unique ID
- **Error Handling**: Graceful error handling for API failures
- **Loading States**: Visual feedback during message sending
- **Message History**: Persistent chat history during the session
- **Typing Indicators**: Shows when the bot is processing
- **Auto-scroll**: Automatically scrolls to latest messages

## Customization

You can easily customize:
- Colors in `tailwind.config.js`
- API endpoint in `app/page.tsx`
- Styling in `app/globals.css`
- Header information in `app/page.tsx`

## License

This project is open source and available under the [MIT License](LICENSE).

