# decoupage adresse IP

**Découpage réseaux de manière symétrique**
Nombre d'adresses disponibles = 2^(Nombre de bits de sous-réseau) - 2
- Le Pôle Informatique (6 bureaux, environ 50 équipements au total) -> 2^6-2 = 64-2 = 62 adresses hosts disponibles
- Le Pôle Administratif (4 bureaux, environ 20 équipements au total) -> 2^6-2 = 64-2 = 62 adresses hosts disponibles
- Le Pôle Technicien (4 bureaux, environ 15 équipements au total) -> 2^6-2 = 64-2 = 62 adresses hosts disponibles
- Le Pôle Développement (6 bureaux, environ 12 équipements au total) -> 2^6-2 = 64-2 = 62 adresses hosts disponibles



**Découpage réseaux de manière asymétrique**

- Le Pôle Informatique (6 bureaux, environ 50 équipements au total) -> 2^6-2 = 64-2 = 62 adresses hosts disponibles
- Le Pôle Administratif (4 bureaux, environ 20 équipements au total) -> 2^5-2 = 32-2 = 30 adresses hosts disponibles
- Le Pôle Technicien (4 bureaux, environ 15 équipements au total) -> 2^5-2 = 32-2 = 30 adresses hosts disponibles
- Le Pôle Développement (6 bureaux, environ 12 équipements au total) -> 2^4-2 = 16-2 = 14 adresses hosts disponibles


# Découpage symétrique

Réseau : 172.16.1.0/24

| Pôle           | Plage d'adresses   | Masque de sous-réseau | Adresse réseau | Adresse de broadcast | Adresse de début de plage | Adresse de fin de plage |
|----------------|--------------------|-----------------------|----------------|-----------------------|--------------------------|------------------------|
| Informatique   | 172.16.1.0 - 172.16.1.63 | /26 (255.255.255.192) | 172.16.1.0/26  | 172.16.1.63/26       | 172.16.1.1               | 172.16.1.62            |
| Développement  | 172.16.1.64 - 172.16.1.127 | /26 (255.255.255.192) | 172.16.1.64/26 | 172.16.1.127/26      | 172.16.1.65              | 172.16.1.126           |
| Administratif  | 172.16.1.128 - 172.16.1.191 | /26 (255.255.255.192) | 172.16.1.128/26 | 172.16.1.191/26      | 172.16.1.129             | 172.16.1.190           |
| Technicien     | 172.16.1.192 - 172.16.1.255 | /26 (255.255.255.192) | 172.16.1.192/26 | 172.16.1.255/26      | 172.16.1.193             | 172.16.1.254           |

# Découpage asymétrique

Réseau : 172.16.1.0/24

| Pôle           | Plage d'adresses   | Masque de sous-réseau | Adresse réseau | Adresse de broadcast | Adresse de début de plage | Adresse de fin de plage |
|----------------|--------------------|-----------------------|----------------|-----------------------|--------------------------|------------------------|
| Informatique   | 172.16.1.0 - 172.16.1.63 | /26 (255.255.255.192) | 172.16.1.0/26  | 172.16.1.63/26       | 172.16.1.1               | 172.16.1.62            |
| Développement  | 172.16.1.64 - 172.16.1.79 | /27 (255.255.255.224) | 172.16.1.64/27 | 172.16.1.79/27       | 172.16.1.65              | 172.16.1.78            |
| Administratif  | 172.16.1.80 - 172.16.1.111 | /26 (255.255.255.192) | 172.16.1.80/26 | 172.16.1.111/26      | 172.16.1.81              | 172.16.1.110           |
| Technicien     | 172.16.1.112 - 172.16.1.127 | /27 (255.255.255.224) | 172.16.1.112/27 | 172.16.1.127/27      | 172.16.1.113             | 172.16.1.126           |

