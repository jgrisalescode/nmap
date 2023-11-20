**Author:** Julian Grisales

**Date Created:** 20.11.2023

**Date Modified:** 20.11.2023

**Description**

Escaneo de máquinas virtuales instaladas en un laboratio de Virtualbox configuradas en una red interna.

- **Ubuntu Server 22.04 (Máquina atacante)**
- Matrix Machine (Vulnerable)
- Ubuntu Desktop 22.04
- Metasplotable 2.0.0

```bash
# Escaneo de posibles máquinas en la red
nmap -sn 10.13.13.0/24

# Resultaddo
- 10.13.13.101
- 10.13.13.102 (My virtual machine)
- 10.13.13.104
- 10.13.13.105

# Escaneo basico de puertos
sudo nmap -sS 10.13.13.101
sudo nmap -sS 10.13.13.104
sudo nmap -sS 10.13.13.105

# Ahora haremos un escaneo un poco más profundo
- Puertos
- Estados
- Versión del servicio
- Sistema Operativo

sudo nmao -sS 10.13.13.101 -sV -O
sudo nmao -sS 10.13.13.104 -sV -O
sudo nmao -sS 10.13.13.105 -sV -O
```
