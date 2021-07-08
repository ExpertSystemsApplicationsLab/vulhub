<!-- markdownlint-disable first-line-heading -->
<p align="center">
  <img src=".github/assets/logo.svg" alt="Vulhub" height="300" />
  <p align="center">
    <a href="https://github.com/vulhub/vulhub/blob/master/LICENSE">
      <img src="https://img.shields.io/github/license/vulhub/vulhub.svg" alt="GitHub">
    </a>
    <a href="https://www.wangan.com/vulhub">
      <img src="https://img.shields.io/badge/Official-Community-blue.svg" alt="Official Community">
    </a>
    <a href="https://discord.gg/GhMB3Z">
      <img src="https://img.shields.io/discord/485505185167179778.svg" alt="Chat on Discord">
    </a>
    <a href="https://www.patreon.com/phith0n">
      <img src="https://img.shields.io/badge/sponsor-patreon-73d6a1.svg" alt="Backers and sponors on Patreon">
    </a>
    <a href="https://opencollective.com/vulhub#backer">
      <img src="https://img.shields.io/badge/backer-opencollective-f89a76.svg" alt="Backers and sponors on Opencollective">
    </a>
  </p>
</p>

Vulhub es una colección de código abierto de entornos de Docker vulnerables prediseñados. No se requieren conocimientos previos de Docker, simplemente ejecutar dos comandos simples y tendrá un entorno vulnerable. Este repositorio se ha creado a partir de un fork del original https://github.com/vulhub/vulhub

[中文版本(Version China)](README.zh-cn.md)

## Instalación

Instalar el docker/docker-compose en Ubuntu 20.04:

```bash
# Install pip
curl -s https://bootstrap.pypa.io/get-pip.py | python3

# Install the latest version docker
curl -s https://get.docker.com/ | sh

# Run docker service
systemctl start docker

# Install docker compose
pip install docker-compose
```

Los pasos de instalación de docker y docker-compose para otros sistemas operativos pueden ser ligeramente diferentes, consulte la [documentación de docker] (https://docs.docker.com/) para obtener más detalles.

## Uso

```bash
# Download project
wget https://github.com/vulhub/vulhub/archive/master.zip -O vulhub-master.zip
unzip vulhub-master.zip
cd vulhub-master

# Enter the directory of vulnerability/environment
cd flask/ssti

# Compile environment
docker-compose build

# Run environment
docker-compose up -d
```

Hay un documento ** README ** en cada directorio de entorno; lea este archivo para conocer las pruebas y el uso de vulnerabilidades / entornos.

Después de la prueba, elimine el entorno con el siguiente comando.

```
docker-compose down -v
```

Se recomienda utilizar un VPS de al menos 1 GB de memoria para crear un entorno de vulnerabilidad. El `your-ip` mencionado en la documentación se refiere a la dirección IP de su VPS. Si está utilizando una máquina virtual, se refiere a la IP de su máquina virtual, no a la IP dentro del contenedor de la ventana acoplable

**¡Todos los entornos de este proyecto son solo para fines de prueba y no deben utilizarse como entorno de producción!**

## Aviso

1. Para evitar errores de permisos, es mejor utilizar el usuario root para ejecutar los comandos docker y docker-compose.
2. Algunas imágenes de la ventana acoplable no admiten la ejecución en máquinas ARM.

## Contribución

Este proyecto se basa en docker. Por lo tanto, cualquier error durante la compilación y la ejecución lo arroja la ventana acoplable y los programas relacionados. Primero, busque usted mismo la causa del error. Si se determina que el dockerfile está escrito incorrectamente (o el código es incorrecto en vulhub), envíe el problema. Más detalles, por favor 👉 [Razones comunes para fallas en la compilación] (https://github.com/phith0n/vulhub/wiki/%E7%BC%96%E8%AF%91%E5%A4%B1%E8%B4%A5%E7%9A%84%E5%8E%9F%E5%9B%A0), espero que pueda ayudarte.

Si tiene más preguntas, comuníquese con:

- [Chinese Community](https://www.wangan.com/vulhub)
- [Discord](https://discord.gg/GhMB3Z)
- [Twitter](https://twitter.com/vulhub)


Gracias a los siguientes contribuyentes:

[![](https://opencollective.com/vulhub/contributors.svg?width=890&button=false)](https://github.com/vulhub/vulhub/graphs/contributors)

Más contribuyentes：[Contributors List](contributors.md)

## Socios

Nuestros socios y usuarios:

<p>
  <a href="https://www.wangan.com/vulhub" target="_blank"><img src="https://vulhub.org/img/sponsor/wangan.png" width="200"></a>
  <a href="https://www.cvebase.com" target="_blank"><img src="https://vulhub.org/img/sponsor/cvebase.png" width="200"></a>
  <a href="https://www.huoxian.cn" target="_blank"><img src="https://vulhub.org/img/sponsor/huoxian.png" width="200"></a>
  <a href="https://www.chaitin.cn" target="_blank"><img src="https://vulhub.org/img/sponsor/chaitin.png" width="200"></a>
  <a href="https://xianzhi.aliyun.com/" target="_blank"><img src="https://vulhub.org/img/sponsor/aliyun.svg" width="200"></a>
</p>

Patrocinador vulhub en patreon 🙏

<a href="https://www.patreon.com/bePatron?u=12677520"><img src="https://vulhub.org/img/sponsor/patreon.png" width="150"></a>

Patrocinador vulhub en opencollective 🙏

<p>
  <a href="https://opencollective.com/vulhub#backer"><img src="https://opencollective.com/vulhub/backers.svg?width=138"></a>
  <a href="https://opencollective.com/vulhub#sponsor"><img src="https://opencollective.com/vulhub/sponsors.svg?width=138"></a>
</p>

Más [Donate](http://vulhub.org/#/docs/donate/).

## Licencia


Vulhub tiene la licencia MIT. Ver [LICENSE](LICENSE) para obtener el texto completo de la licencia.
