## Découpage symétrique du réseau

Répartition équitable des adresses IP dans tout le réseau :
Pour tous les pôles : 2^6-2 = 62 donc on peut adresser 62 machines par réseau.
- CIDR = 32-6 = 26

| Pôle          | Adresse réseau  | Adresse broadcast | Début de plage  | Fin de plage    |
| ------------- | --------------- | ----------------- | --------------- | --------------- |
| Informatique  | 172.16.1.0/26   | 172.16.1.63/26    | 172.16.1.1/26   | 172.16.1.62/26  |
| Développement | 172.16.1.64/26  | 172.16.1.127/26   | 172.16.1.65/26  | 172.16.1.126/26 |
| Administratif | 172.16.1.128/26 | 172.16.1.191/26   | 172.16.1.129/26 | 172.16.1.190/26 |
| Technicien    | 172.16.1.192/26 | 172.16.1.255/26   | 172.16.1.193/26 | 172.16.1.254/26 |

## Découpage asymétrique du réseau

Allocation de plus d'adresses aux pôles ayant plus d'équipements :
- Pôle informatique : 2^6-2 = 64-2 = 62
- Pôle développement : 2^4-2 = 16-2 = 14
- Pôle administratif : 2^5-2 = 32-2 = 30
- Pôle technicien : 2^5-2 = 32-2 = 30

| Pôle          | Adresse réseau  | Adresse broadcast | Début de plage  | Fin de plage    |
| ------------- | --------------- | ----------------- | --------------- | --------------- |
| Informatique  | 172.16.1.0/26   | 172.16.1.63/26    | 172.16.1.1/26   | 172.16.1.62/26  |
| Développement | 172.16.1.64/28  | 172.16.1.80/28   | 172.16.1.65/28  | 172.16.1.79/28 |
| Administratif | 172.16.1.81/27 | 172.16.1.113/27   | 172.16.1.82/27 | 172.16.1.112/27 |
| Technicien    | 172.16.1.114/27 | 172.16.1.146/27   | 172.16.1.115/27 | 172.16.1.145/27 |
