# MediaStack# 📺 Media Server Stack

This project deploys a complete **self-hosted media management ecosystem** using **Docker Compose**. It includes tools for organizing, automating, and managing Movies, TV Shows, Anime, Subtitles, and Media Requests, complete with web interfaces, monitoring dashboards, and chat integration.

## 🎬 Features

- **Plex Media Server** — Stream your movies, TV shows, music, and more to any device.
- **Radarr & Sonarr** — Automated movie and TV show management (including separate instances for 4K and Anime).
- **Prowlarr** — Centralized indexer manager for Radarr and Sonarr.
- **Bazarr** — Automated subtitle downloads (HD, 4K, and Anime-specific instances).
- **Requestrr** — Discord bot for requesting new media via chat.
- **Overseerr** — Web request management for Movies, TV Shows, and Anime.
- **Tautulli** — Plex monitoring and usage statistics.
- **Maintainerr** — Unified service health dashboard.

---

## 🛠️ Stack Overview

| Service         | Description                                                                          | Port   |
|-----------------|--------------------------------------------------------------------------------------|-------|
| **Plex**        | Organizes and streams your personal media library                                    | Host Networking |
| **Radarr**      | Automated HD movie management                                                        | 7878  |
| **Radarr 4K**   | Dedicated to 4K movie management                                                      | 7879  |
| **Radarr Anime**| Dedicated to Anime movie management                                                   | 7880  |
| **Sonarr**      | Automated HD TV show management                                                       | 8989  |
| **Sonarr 4K**   | Dedicated to 4K TV show management                                                    | 8990  |
| **Sonarr Anime**| Dedicated to Anime TV show management                                                 | 8991  |
| **Prowlarr**    | Indexer manager for Radarr and Sonarr                                                  | 9696  |
| **Bazarr**      | Subtitle manager for HD content                                                       | 6767  |
| **Bazarr 4K**   | Subtitle manager for 4K content                                                       | 6768  |
| **Bazarr Anime**| Subtitle manager for Anime content                                                    | 6769  |
| **Requestrr**   | Discord bot to allow users to request content                                         | 4545  |
| **Overseerr**   | Web request interface for Movies and TV Shows                                         | 5055  |
| **Overseerr Anime**| Web request interface for Anime content                                           | 5056  |
| **Tautulli**    | Plex monitoring dashboard                                                             | 8181  |
| **Maintainerr** | Service health dashboard                                                              | 6246  |

---

## 📦 Requirements

- **Docker Engine** (>=20.10)
- **Docker Compose** (>=2.0)
- **Media Files** stored under `/mnt`
- Proper permissions (`PUID=1000`, `PGID=1000`)

---

Notes: 
Watchtower Integration: Several services are configured with the watchtower label to enable automatic updates.

Custom Scripts: You can mount automation scripts to /opt/scripts.

Rclone: Bind-mounted to allow remote storage integrations (optional).

----

## 🚀 Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/yourrepo.git
   cd yourrepo

2. Adjust the paths and environment variables in the docker-compose.yml as needed.
3. docker compose up -d
4. Access services at http://<your-server-ip>:<port> as per the table above

❤️ Credits 
- [Plex](https://www.plex.tv/)
- [Radarr](https://radarr.video/)
- [Sonarr](https://sonarr.tv/)
- [Prowlarr](https://github.com/Prowlarr/Prowlarr)
- [Bazarr](https://www.bazarr.media/)
- [Requestrr](https://github.com/davestephens/Requestrr)
- [Overseerr](https://overseerr.dev/)
- [Tautulli](https://tautulli.com/)
- [Maintainerr](https://github.com/jorenn92/maintainerr)


