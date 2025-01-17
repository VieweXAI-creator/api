# Viewe X AI API

<p align="center">
  <img src="https://avatars.githubusercontent.com/u/195435388?v=4" alt="Fithom Labs Logo" width="200" />
</p>

## About
**Viewe X AI: Revolutionizing Gaming with AI-Powered Agents on the Solana Blockchain**

Step into the future of gaming with Viewe X AI, a groundbreaking token project on the Solana network. Designed to seamlessly integrate cutting-edge artificial intelligence with immersive gaming experiences, Viewe X AI empowers players to interact with intelligent agents in dynamic and innovative ways.

Our vision is to create a gaming ecosystem where AI agents evolve, learn, and compete, offering unmatched depth and realism. Leveraging the speed and efficiency of Solana's blockchain, Viewe X AI ensures secure, scalable, and lightning-fast transactions, setting the stage for a truly decentralized gaming revolution.

Join us as we redefine what’s possible in the intersection of AI and gaming—where every interaction is smarter, every move is strategic, and every moment is unforgettable. Welcome to the world of Viewe X AI, where AI-powered gaming meets blockchain innovation.

## API Base URL
`https://api.viewexai.io`

## Folder Structure
```
api/
├── src/
│   ├── config/
│   │   └── solana.ts       # Configuration for Solana connection
│   ├── controllers/
│   │   ├── agent.ts        # Controller for AI agent interactions
│   │   ├── game.ts         # Controller for game-related logic
│   │   └── token.ts        # Controller for token-related operations
│   ├── routes/
│   │   ├── agentRoutes.ts  # Routes for AI agent interactions
│   │   ├── gameRoutes.ts   # Routes for game-related endpoints
│   │   └── tokenRoutes.ts  # Routes for token-related operations
│   ├── services/
│   │   ├── agentService.ts # Business logic for AI agents
│   │   ├── gameService.ts  # Business logic for games
│   │   └── tokenService.ts # Business logic for token operations
│   ├── utils/
│   │   └── helpers.ts      # Utility functions
│   ├── middlewares/
│   │   └── auth.ts         # Authentication middleware
│   ├── app.ts              # Express app setup
│   └── index.ts            # Entry point
├── tests/
│   ├── integration/        # Integration tests
│   │   └── integration.test.ts
│   ├── unit/               # Unit tests
│   │   └── unit.test.ts
│   └── mockData/           # Mock data for testing
│       └── mockData.json
├── .env                    # Environment variables
├── .gitignore              # Git ignore file
├── package.json            # NPM dependencies and scripts
├── README.md               # Documentation
└── tsconfig.json           # TypeScript configuration
```

## Features
- **AI Agent Interactions**: APIs for interacting with AI agents, including creating, updating, and deleting agents.
- **Game Mechanics**: Endpoints to handle game-related logic, such as starting games, retrieving scores, and managing in-game assets.
- **Token Operations**: Secure management of Viewe X AI tokens on the Solana blockchain, including transfers, balances, and staking.
- **Authentication**: Secure user authentication using JWT and role-based access control.
- **Fast and Scalable**: Built with Solana for low-latency and high throughput.

## API Endpoints
### Agents
- `POST /api/agents`: Create a new AI agent.
- `GET /api/agents/:id`: Retrieve details of an AI agent.
- `PUT /api/agents/:id`: Update an AI agent.
- `DELETE /api/agents/:id`: Delete an AI agent.

### Games
- `POST /api/games/start`: Start a new game.
- `GET /api/games/:id`: Retrieve game details.
- `POST /api/games/score`: Submit a score for a game.

### Tokens
- `GET /api/tokens/balance`: Retrieve token balance.
- `POST /api/tokens/transfer`: Transfer tokens to another wallet.
- `POST /api/tokens/stake`: Stake tokens for rewards.

## Prerequisites
- [Node.js](https://nodejs.org/) (version 16 or higher)
- [TypeScript](https://www.typescriptlang.org/)
- [Solana CLI](https://docs.solana.com/cli/install-solana-cli)
- [PostgreSQL](https://www.postgresql.org/) (for user and game data storage)

## Setup and Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/viewexai/api.git
   cd viewexai-api
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Setup environment variables:**
   Create a `.env` file in the root directory and add the following:
   ```env
   SOLANA_NETWORK=mainnet-beta
   PRIVATE_KEY=your-private-key
   API_PORT=3000
   DATABASE_URL=postgresql://user:password@localhost:5432/viewexai
   JWT_SECRET=your-jwt-secret
   ```

4. **Setup database:**
   Initialize the PostgreSQL database:
   ```bash
   npm run db:setup
   ```

5. **Start the server:**
   ```bash
   npm run dev
   ```

6. **API Documentation:**
   Visit `http://localhost:3000/api-docs` (if using Swagger or similar).

## Scripts
- `npm run dev`: Start the development server.
- `npm run build`: Build the project.
- `npm run test`: Run tests.
- `npm run db:setup`: Initialize and migrate the database.

## Testing
- **Unit Tests:**
  ```bash
  npm run test:unit
  ```
- **Integration Tests:**
  ```bash
  npm run test:integration
  ```

## Contributing
Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md) for details.

## License
[MIT License](LICENSE)
