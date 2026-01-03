# InversedTeams

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Minecraft](https://img.shields.io/badge/minecraft-1.21.4-green.svg)
![Java](https://img.shields.io/badge/java-21-orange.svg)

A complete and advanced team management plugin for Minecraft. Perfect for PvP, Faction, and Survival servers with modern features, custom GUIs, alliance system, team bank, detailed statistics, dynamic leaderboards, and much more.

Developed by **InversedDevelopment** 🚀

---

## 📋 Main Features

### 🎨 Modern Design
- **Ergonomic GUIs**: Customized graphical interfaces with modern design (pink/purple)
- **Customizable Menus**: All menus, messages, and almost all elements are fully configurable
- **Multi-Language System**: Support for multiple languages (EN/IT) with automatic file management

### 👥 Complete Team System
- **Team Creation**: Create your team with a custom name
- **Member Management**: Invite, remove, and manage team members
- **Role System**: Owner, Admin, and Member with differentiated permissions
- **Ownership Transfer**: Transfer team ownership to other members
- **Team Info**: View detailed team information

### 💰 Team Bank
- **Shared Bank**: Deposit/withdrawal system shared among team members
- **Customizable Permissions**: Control who can deposit and withdraw
- **Vault Integration**: Economy system based on Vault

### 📦 Team Enderchest
- **Shared Storage**: Ender chest shared among all team members
- **Configurable**: Customizable size and permissions
- **Easy Access**: Quick opening via GUI or command

### 🤝 Alliance System
- **Alliance Requests**: Send and accept alliance requests between teams
- **Ally Chat**: Dedicated chat to communicate with allied teams
- **Protection**: Configurable friendly fire system for allies
- **Management**: Remove alliances when necessary

### 📊 Advanced Statistics
Complete team statistics tracking:
- **Kills & Deaths**: Player kills and deaths
- **K/D Ratio**: Automatically calculated kills/deaths ratio
- **Mob Kills**: Mob kills
- **Blocks**: Blocks placed and broken
- **Level**: Total team level
- **Money**: Total team money
- **Playtime**: Total playtime

### 🏆 Leaderboard
- **Global Rankings**: View the best teams
- **Multiple Categories**: Leaderboards for kills, level, and money
- **Intuitive GUI**: Graphical interface to view rankings
- **PlaceholderAPI Integration**: Placeholders for custom leaderboards

### 🏠 Team Home
- **Set Home**: Set the team home
- **Teleport**: Quick teleport to team home
- **Configurable Cooldown**: Customizable cooldown system

### 💬 Team Chat
- **Dedicated Chat**: Private chat for the team
- **Customizable Format**: Customize message format
- **Toggle**: Enable/disable team chat

### 🛡️ Team Protection
- **Friendly Fire**: Disable PvP between members of the same team
- **Ally Protection**: Also protect members of allied teams
- **Configurable**: Enable/disable protections from config

### 🔧 Admin Commands
- **Advanced Management**: Commands for server administrators
- **Reload**: Reload configurations and messages
- **Force Actions**: Delete teams, forcibly remove members

---

## 📦 Installation

1. **Download** the plugin `.jar` file
2. **Place** the file in your server's `plugins` folder
3. **Install dependencies**: Vault and PlaceholderAPI (optional)
4. **Restart** the server
5. **Configure** the `config.yml` and `messages_XX.yml` files in the `plugins/InversedTeams/` folder

---

## 🎮 Commands

### Player Commands

#### `/team` - Main team menu
- `/team create <name>` - Create a new team
- `/team disband` - Delete your team (owner only)
- `/team invite <player>` - Invite a player to the team
- `/team join <team>` - Accept a team invitation
- `/team leave` - Leave the team
- `/team kick <player>` - Remove a member from the team
- `/team promote <player>` - Promote a member to admin
- `/team demote <player>` - Demote an admin to member
- `/team transfer <player>` - Transfer team ownership
- `/team home` - Teleport to team home
- `/team sethome` - Set the team home
- `/team chat [message]` - Toggle team chat or send a message
- `/team info [team]` - View information about a team
- `/team list` - List all teams

#### `/ally` - Alliance management
- `/ally add <team>` - Send an alliance request
- `/ally remove <team>` - Remove an alliance
- `/ally accept <team>` - Accept an alliance request
- `/ally deny <team>` - Deny an alliance request
- `/ally list` - List your team's alliances
- `/ally chat [message]` - Toggle ally chat or send a message

### Admin Commands

#### `/teamadmin` - Administrative commands
- `/teamadmin reload` - Reload config and messages
- `/teamadmin delete <team>` - Forcibly delete a team
- `/teamadmin info <team>` - View detailed information about a team
- `/teamadmin kick <player>` - Remove a player from their team
- `/teamadmin addmember <team> <player>` - Add a player to a team
- `/teamadmin setowner <team> <player>` - Set a new owner for a team

---

## 🔑 Permissions

### Player Permissions
- `inversedteams.team` - Access to basic team commands (default: true)
- `inversedteams.team.create` - Permission to create a team
- `inversedteams.team.disband` - Permission to delete your own team
- `inversedteams.team.invite` - Permission to invite players
- `inversedteams.team.kick` - Permission to remove members
- `inversedteams.team.promote` - Permission to promote members
- `inversedteams.team.demote` - Permission to demote members
- `inversedteams.team.transfer` - Permission to transfer ownership
- `inversedteams.team.sethome` - Permission to set home
- `inversedteams.team.home` - Permission to use home
- `inversedteams.team.chat` - Permission to use team chat
- `inversedteams.team.bank` - Permission to access the bank
- `inversedteams.team.enderchest` - Permission to access the enderchest
- `inversedteams.ally` - Access to alliance commands (default: true)
- `inversedteams.ally.add` - Permission to send alliance requests
- `inversedteams.ally.remove` - Permission to remove alliances
- `inversedteams.ally.chat` - Permission to use ally chat

### Admin Permissions
- `inversedteams.admin` - Access to all admin commands (default: op)
- `inversedteams.admin.reload` - Permission to reload the plugin
- `inversedteams.admin.delete` - Permission to delete teams
- `inversedteams.admin.kick` - Permission to remove players from teams
- `inversedteams.admin.addmember` - Permission to add members to teams
- `inversedteams.admin.setowner` - Permission to change team owners

---

## 🔧 Configuration

### config.yml

```yaml
# Plugin language (en_US or it_IT)
language: "en_US"

# Team Configuration
team:
  # Minimum and maximum team name length
  name-min-length: 3
  name-max-length: 16
  # Maximum number of members per team
  max-members: 10
  # Cooldown for /team home command (in seconds)
  home-cooldown: 5
  # Enable friendly fire (damage between same team members)
  friendly-fire: false
  # Enable ally protection
  ally-protection: true

# Statistics Configuration
stats:
  # Enable statistics tracking
  enabled: true
  # Automatic statistics saving (in minutes)
  auto-save-interval: 5

# Team Chat Format
chat:
  team-format: "&d[TEAM] &f{player}: {message}"
  ally-format: "&b[ALLY] &f{player}: {message}"
```

### Multi-Language System

The plugin supports multiple languages with automatic file management:

**How it works:**
1. On plugin startup, the language file specified in `config.yml` is automatically created
2. Only the active language file is created (e.g., `messages_en_US.yml` or `messages_it_IT.yml`)
3. Other language files are automatically removed to avoid confusion

**To change language:**
1. Modify the `language` parameter in `config.yml`:
   - `en_US` for English (default)
   - `it_IT` for Italian

2. Reload the plugin with `/teamadmin reload`

3. The old language file will be removed and the new language file will be automatically created

**Note:** The language file is automatically generated on first plugin installation, it is not included in the JAR file.

---

## 🎯 PlaceholderAPI

### Available Placeholders

#### Team Information
- `%inversedteams_team_name%` - Player's team name
- `%inversedteams_team_role%` - Player's role in team
- `%inversedteams_team_members%` - Number of members in team
- `%inversedteams_has_team%` - Whether player has a team (true/false)

#### Team Statistics
- `%inversedteams_team_kills%` - Total team kills
- `%inversedteams_team_deaths%` - Total team deaths
- `%inversedteams_team_kd%` - Team K/D ratio
- `%inversedteams_team_mobkills%` - Team mob kills
- `%inversedteams_team_level%` - Total team level
- `%inversedteams_team_money%` - Total team money
- `%inversedteams_team_playtime%` - Total team playtime
- `%inversedteams_team_blocksplaced%` - Blocks placed by team
- `%inversedteams_team_blocksbroken%` - Blocks broken by team

#### Leaderboard
- `%inversedteams_top_kills_<position>%` - Team name at position X for kills
- `%inversedteams_top_kills_<position>_value%` - Kills value at position X
- `%inversedteams_top_level_<position>%` - Team name at position X for level
- `%inversedteams_top_level_<position>_value%` - Level value at position X
- `%inversedteams_top_money_<position>%` - Team name at position X for money
- `%inversedteams_top_money_<position>_value%` - Money value at position X

Example: `%inversedteams_top_kills_1%` shows the team name with most kills

---

## 🔌 Dipendenze

### Richieste
- **Spigot/Paper**: 1.21.4 o superiore (compatibile dalla 1.16+)
- **Java**: 21

### Optional
- **Vault**: For economy system and Team Bank
- **PlaceholderAPI**: For custom placeholders

---

## 🐛 Bugs and Support

If you find bugs or have suggestions, contact us on Discord or open an issue on GitHub.

---

## 📝 License

This plugin was developed by **InversedDevelopment**.

---

## 💖 Credits

Developed with ❤️ by **InversedDevelopment**

---

**InversedTeams** - The best plugin to manage teams on your Minecraft server! 🚀
