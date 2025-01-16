# Gator

Gator is a command-line RSS feed aggregator that helps you follow and manage your favorite feeds. Share discoveries with friends and never miss an update!

## Requirements

- PostgreSQL (minimum version 14.15)
  - Verify installation: `psql --version`
  - [Download PostgreSQL](https://www.postgresql.org/download/)

- Go (minimum version 1.23.2)
  - Verify installation: `go version`
  - [Download Go](https://go.dev/dl/)


## Installation
`go install github.com/Falukey/gator@latest`

## Usage Examples

Authentication:
- `gator register` - Create a new account
- `gator login` - Sign in to your account
- `gator reset` - Reset your password

Feed Management:
- `gator addfeed <url>` - Add a new RSS feed
- `gator feeds` - List all your feeds

Social Features:
- `gator follow <username>` - Follow another user
- `gator following` - Show who you're following
- `gator unfollow <username>` - Unfollow a user

## Configuration

Create a config.json file in your home directory:

```json
{
    "database_url": "postgres://postgres:your_password@localhost:5432/gator"
}

## Getting Started

1. Install Gator: `go install github.com/Falukey/gator@latest`
2. Set up your database:
   - Connect to PostgreSQL: `psql -U postgres`
   - Create database: `CREATE DATABASE gator;`
3. Create config.json in your home directory with your database credentials
4. Register an account: `gator register`
5. Start following feeds:
   - Add your first feed: `gator addfeed <url>`
   - View your feeds: `gator feeds`