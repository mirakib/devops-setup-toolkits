### Apache Main Config File Locations (Ubuntu/Debian-based systems)

```

/etc/apache2/
│
├── apache2.conf              → Main configuration file
├── ports.conf                → Defines which ports Apache listens on (80, 443)
├── envvars                   → Environment variables
│
├── sites-available/          → All available VirtualHost configurations
│   ├── 000-default.conf
│   ├── example.com.conf
│
├── sites-enabled/            → Active VirtualHost configurations (symlinks)
│   ├── 000-default.conf → ../sites-available/000-default.conf
│
├── mods-available/           → All modules available
├── mods-enabled/             → Active modules (symlinks)
│
└── conf-available/ & conf-enabled/ → Optional configuration snippets

```

### Nginx Main Config File Locations (Ubuntu/Debian-based systems):

```
/etc/nginx/
│
├── nginx.conf                → Main configuration file
│
├── conf.d/                   → Extra configuration snippets (global)
│   ├── proxy.conf
│   ├── gzip.conf
│
├── sites-available/          → Available server blocks (virtual hosts)
│   ├── default
│   ├── example.com.conf
│
├── sites-enabled/            → Active server blocks (symlinks)
│   ├── example.com.conf → ../sites-available/example.com.conf
│
└── snippets/                 → Reusable small configuration parts
    ├── ssl.conf
    ├── fastcgi-php.conf

```
