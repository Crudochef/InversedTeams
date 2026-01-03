# InversedTeams

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Minecraft](https://img.shields.io/badge/minecraft-1.21.4-green.svg)
![Java](https://img.shields.io/badge/java-21-orange.svg)

Un plugin completo e avanzato per la gestione di team in Minecraft. Perfetto per server PvP, Faction e Survival con funzionalità moderne, GUI personalizzate, sistema di alleanze, team bank, statistiche dettagliate, leaderboard dinamiche e molto altro.

Sviluppato da **InversedDevelopment** 🚀

---

## 📋 Caratteristiche Principali

### 🎨 Design Moderno
- **GUI Ergonomiche**: Interfacce grafiche personalizzate con design moderno (rosa/viola)
- **Menu Personalizzabili**: Tutti i menu, messaggi e quasi tutti gli elementi sono completamente configurabili
- **Sistema Multi-Lingua**: Supporto per più lingue (EN/IT) con gestione automatica dei file

### 👥 Sistema Team Completo
- **Creazione Team**: Crea il tuo team con nome personalizzato
- **Gestione Membri**: Invita, rimuovi e gestisci i membri del team
- **Sistema Ruoli**: Owner, Admin e Member con permessi differenziati
- **Trasferimento Ownership**: Trasferisci la proprietà del team ad altri membri
- **Team Info**: Visualizza informazioni dettagliate sui team

### 💰 Team Bank
- **Banca Condivisa**: Sistema di deposito/prelievo condiviso tra i membri del team
- **Permessi Personalizzabili**: Controlla chi può depositare e prelevare
- **Integrazione Vault**: Sistema economico basato su Vault

### 📦 Team Enderchest
- **Storage Condiviso**: Ender chest condiviso tra tutti i membri del team
- **Configurabile**: Dimensioni e permessi personalizzabili
- **Accesso Facile**: Apertura rapida tramite GUI o comando

### 🤝 Sistema Alleanze
- **Richieste di Alleanza**: Invia e accetta richieste di alleanza tra team
- **Chat Alleati**: Chat dedicata per comunicare con i team alleati
- **Protezione**: Sistema di friendly fire per alleati configurabile
- **Gestione**: Rimuovi alleanze quando necessario

### 📊 Statistiche Avanzate
Tracciamento completo delle statistiche del team:
- **Kills & Deaths**: Uccisioni di giocatori e morti
- **K/D Ratio**: Rapporto kills/deaths calcolato automaticamente
- **Mob Kills**: Uccisioni di mob
- **Blocks**: Blocchi piazzati e rotti
- **Level**: Livello totale del team
- **Money**: Denaro totale del team
- **Playtime**: Tempo di gioco totale

### 🏆 Leaderboard
- **Classifiche Globali**: Visualizza i migliori team
- **Categorie Multiple**: Leaderboard per kills, level e money
- **GUI Intuitiva**: Interfaccia grafica per visualizzare le classifiche
- **Integrazione PlaceholderAPI**: Placeholders per leaderboard personalizzate

### 🏠 Team Home
- **Setta Home**: Imposta la home del team
- **Teleport**: Teletrasporto rapido alla home del team
- **Cooldown Configurabile**: Sistema di cooldown personalizzabile

### 💬 Team Chat
- **Chat Dedicata**: Chat privata per il team
- **Formato Personalizzabile**: Personalizza il formato dei messaggi
- **Toggle**: Attiva/disattiva la chat del team

### 🛡️ Protezione Team
- **Friendly Fire**: Disattiva il PvP tra membri dello stesso team
- **Protezione Alleati**: Proteggi anche i membri dei team alleati
- **Configurabile**: Attiva/disattiva le protezioni dal config

### 🔧 Comandi Admin
- **Gestione Avanzata**: Comandi per amministratori del server
- **Reload**: Ricarica configurazioni e messaggi
- **Forza Azioni**: Elimina team, rimuovi membri forzatamente

---

## 📦 Installazione

1. **Scarica** il file `.jar` del plugin
2. **Inserisci** il file nella cartella `plugins` del tuo server
3. **Installa dipendenze**: Vault e PlaceholderAPI (opzionale)
4. **Riavvia** il server
5. **Configura** i file `config.yml` e `messages_XX.yml` nella cartella `plugins/InversedTeams/`

---

## 🎮 Comandi

### Comandi Giocatore

#### `/team` - Menu principale del team
- `/team create <nome>` - Crea un nuovo team
- `/team disband` - Elimina il tuo team (solo owner)
- `/team invite <giocatore>` - Invita un giocatore nel team
- `/team join <team>` - Accetta un invito a un team
- `/team leave` - Abbandona il team
- `/team kick <giocatore>` - Rimuovi un membro dal team
- `/team promote <giocatore>` - Promuovi un membro ad admin
- `/team demote <giocatore>` - Retrocedi un admin a member
- `/team transfer <giocatore>` - Trasferisci la ownership del team
- `/team home` - Teletrasportati alla home del team
- `/team sethome` - Imposta la home del team
- `/team chat [messaggio]` - Attiva/disattiva la chat del team o invia un messaggio
- `/team info [team]` - Visualizza informazioni su un team
- `/team list` - Lista di tutti i team

#### `/ally` - Gestione alleanze
- `/ally add <team>` - Invia una richiesta di alleanza
- `/ally remove <team>` - Rimuovi un'alleanza
- `/ally accept <team>` - Accetta una richiesta di alleanza
- `/ally deny <team>` - Rifiuta una richiesta di alleanza
- `/ally list` - Lista delle alleanze del tuo team
- `/ally chat [messaggio]` - Attiva/disattiva la chat alleati o invia un messaggio

### Comandi Admin

#### `/teamadmin` - Comandi amministrativi
- `/teamadmin reload` - Ricarica config e messaggi
- `/teamadmin delete <team>` - Elimina un team forzatamente
- `/teamadmin info <team>` - Visualizza informazioni dettagliate su un team
- `/teamadmin kick <giocatore>` - Rimuovi un giocatore dal suo team
- `/teamadmin addmember <team> <giocatore>` - Aggiungi un giocatore a un team
- `/teamadmin setowner <team> <giocatore>` - Imposta un nuovo owner per un team

---

## 🔑 Permessi

### Permessi Giocatore
- `inversedteams.team` - Accesso ai comandi base del team (default: true)
- `inversedteams.team.create` - Permesso per creare un team
- `inversedteams.team.disband` - Permesso per eliminare il proprio team
- `inversedteams.team.invite` - Permesso per invitare giocatori
- `inversedteams.team.kick` - Permesso per rimuovere membri
- `inversedteams.team.promote` - Permesso per promuovere membri
- `inversedteams.team.demote` - Permesso per retrocedere membri
- `inversedteams.team.transfer` - Permesso per trasferire ownership
- `inversedteams.team.sethome` - Permesso per impostare la home
- `inversedteams.team.home` - Permesso per usare la home
- `inversedteams.team.chat` - Permesso per usare la chat del team
- `inversedteams.team.bank` - Permesso per accedere alla bank
- `inversedteams.team.enderchest` - Permesso per accedere all'enderchest
- `inversedteams.ally` - Accesso ai comandi delle alleanze (default: true)
- `inversedteams.ally.add` - Permesso per inviare richieste di alleanza
- `inversedteams.ally.remove` - Permesso per rimuovere alleanze
- `inversedteams.ally.chat` - Permesso per usare la chat alleati

### Permessi Admin
- `inversedteams.admin` - Accesso a tutti i comandi admin (default: op)
- `inversedteams.admin.reload` - Permesso per ricaricare il plugin
- `inversedteams.admin.delete` - Permesso per eliminare team
- `inversedteams.admin.kick` - Permesso per rimuovere giocatori dai team
- `inversedteams.admin.addmember` - Permesso per aggiungere membri ai team
- `inversedteams.admin.setowner` - Permesso per cambiare owner dei team

---

## 🔧 Configurazione

### config.yml

```yaml
# Lingua del plugin (en_US o it_IT)
language: "en_US"

# Configurazione Team
team:
  # Lunghezza minima e massima del nome team
  name-min-length: 3
  name-max-length: 16
  # Numero massimo di membri per team
  max-members: 10
  # Cooldown per il comando /team home (in secondi)
  home-cooldown: 5
  # Abilita friendly fire (danno tra membri dello stesso team)
  friendly-fire: false
  # Abilita protezione alleati
  ally-protection: true

# Configurazione Statistiche
stats:
  # Abilita il tracciamento delle statistiche
  enabled: true
  # Salvataggio automatico delle statistiche (in minuti)
  auto-save-interval: 5

# Formato Chat Team
chat:
  team-format: "&d[TEAM] &f{player}: {message}"
  ally-format: "&b[ALLY] &f{player}: {message}"
```

### Sistema Multi-Lingua

Il plugin supporta più lingue con gestione automatica dei file:

**Funzionamento:**
1. All'avvio del plugin, viene creato automaticamente il file di lingua specificato nel `config.yml`
2. Viene creato solo il file della lingua attiva (es: `messages_en_US.yml` o `messages_it_IT.yml`)
3. I file delle altre lingue vengono automaticamente rimossi per evitare confusione

**Per cambiare lingua:**
1. Modifica il parametro `language` nel `config.yml`:
   - `en_US` per inglese (default)
   - `it_IT` per italiano

2. Ricarica il plugin con `/teamadmin reload`

3. Il vecchio file di lingua verrà rimosso e verrà creato automaticamente quello della nuova lingua selezionata

**Nota:** Il file di lingua viene generato automaticamente alla prima installazione del plugin, non è incluso nel file JAR.

---

## 🎯 PlaceholderAPI

### Placeholders Disponibili

#### Informazioni Team
- `%inversedteams_team_name%` - Nome del team del giocatore
- `%inversedteams_team_role%` - Ruolo del giocatore nel team
- `%inversedteams_team_members%` - Numero di membri nel team
- `%inversedteams_has_team%` - Se il giocatore ha un team (true/false)

#### Statistiche Team
- `%inversedteams_team_kills%` - Kills totali del team
- `%inversedteams_team_deaths%` - Deaths totali del team
- `%inversedteams_team_kd%` - Rapporto K/D del team
- `%inversedteams_team_mobkills%` - Mob kills del team
- `%inversedteams_team_level%` - Livello totale del team
- `%inversedteams_team_money%` - Denaro totale del team
- `%inversedteams_team_playtime%` - Playtime totale del team
- `%inversedteams_team_blocksplaced%` - Blocchi piazzati dal team
- `%inversedteams_team_blocksbroken%` - Blocchi rotti dal team

#### Leaderboard
- `%inversedteams_top_kills_<posizione>%` - Nome del team in posizione X per kills
- `%inversedteams_top_kills_<posizione>_value%` - Valore kills della posizione X
- `%inversedteams_top_level_<posizione>%` - Nome del team in posizione X per level
- `%inversedteams_top_level_<posizione>_value%` - Valore level della posizione X
- `%inversedteams_top_money_<posizione>%` - Nome del team in posizione X per money
- `%inversedteams_top_money_<posizione>_value%` - Valore money della posizione X

Esempio: `%inversedteams_top_kills_1%` mostra il nome del team con più kills

---

## 🔌 Dipendenze

### Richieste
- **Spigot/Paper**: 1.21.4 o superiore (compatibile dalla 1.16+)
- **Java**: 21

### Opzionali
- **Vault**: Per il sistema economico e Team Bank
- **PlaceholderAPI**: Per i placeholders personalizzati

---

## 🐛 Bug e Supporto

Se trovi bug o hai suggerimenti, contattaci su Discord o apri una issue su GitHub.

---

## 📝 Licenza

Questo plugin è stato sviluppato da **InversedDevelopment**.

---

## 💖 Crediti

Sviluppato con ❤️ da **InversedDevelopment**

---

**InversedTeams** - Il miglior plugin per gestire team sul tuo server Minecraft! 🚀
