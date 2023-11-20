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
- 10.13.13.101 (Matrix Machine)
- 10.13.13.102 (My virtual machine)
- 10.13.13.104 (Ubunttu Desktop 22.04)
- 10.13.13.105 (Metasplotable 2.0.0)

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

### Resultados 10.13.13.101

<image src="https://github.com/jgrisalescode/nmap/blob/main/10.13.13.101%20info.png" alt="10.13.13.101">

### Resultados 10.13.13.104

<image src="https://github.com/jgrisalescode/nmap/blob/main/10.13.13.104%20info.png" alt="10.13.13.104">

### Resultados 10.13.13.105

<image src="https://github.com/jgrisalescode/nmap/blob/main/10.13.13.105%20info.png" alt="10.13.13.105">

Como podemos ver la maquina con direccion ip ```10.13.13.105``` es la que más vectores de ataque posible tiene.
