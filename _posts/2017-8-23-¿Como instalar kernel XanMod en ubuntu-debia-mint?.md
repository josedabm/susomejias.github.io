---
layout: post
title:  "¿Cómo instalar kernel XanMod en ubuntu/debian/mint?"
date:   2017-08-23 01:30:13 +0800
categories: Linux
tags: Linux Kernel XanMod Ubuntu
comments: 1
---

Muy buenas chicos/as, hoy os voy a enseñar a instalar un kernel modificado en vuestra distribucción linux, cabe decir que debe ser una distribucción basada en debian/ubuntu, ya que la instalación requiere añadir
unos repositorios, los cuáles obviamente no van a servir para distribucciones que no se basen en debian/ubuntu, también decir que <b>¡¡¡no me hago responsable de cualquier daño o perjuicio causado a tu equipo realiza el tutorial bajo tu responsabilidad, dicho esto comenzemos!!!</b><br/>

![_config.yml]({{ site.baseurl }}/assets/res/XanModKernel.png)
<br/>

Vale y os preguntaréis <b>¿Qué me aportaría un kernel modificado?</b> , pues la respuesta es bien sencilla, <b>eso si cabe decir que es una opinión personal basada en mi uso</b>, yo básicamente lo llevo por tener los ultimos parches del kernel de linux y porque en <b>"teoría"</b> están preparados para ofrecer un mejor rendimiento del equipo, esto dependerá en gran medida del equipo en el cuál lo instales, si es un equipo muy potente probablemente no notéis mucho la diferencia.

Bien comencemos con la instalación, en primer lugar deberemos <b>añadir el repositorio</b> del cual bajaremos el kernel, para ello usaremos el siguiente comando:
<br/>
<br/>

```
echo 'deb http://deb.xanmod.org releases main' | sudo tee /etc/apt/sources.list.d/xanmod-kernel.list && wget -qO - http://deb.xanmod.org/gpg.key | sudo apt-key add -  
```
<br/>
<br/>


Ahora procederemos a <b>actualizar los respositorios, e instalar el kernel, tengo que decir, que depende de cuando veáis este tuto, obviamente la versión del kernel va a ir actualizandose, deberemos cambiar la versión del kernel la cual queremos instalar en mi caso a dia de hoy la ultima versión disponible es la 4.12.8</b>, por tanto usaré los siguiente comandos para actualizar e instalar el kernel:
<br/>
<br/>


```

sudo apt update && sudo apt install linux-xanmod-4.

```


<br/>
<br/>

Una vez actualizados los repositorios e instalado el kernel, es recomendable instalar los <b>Microcodes</b> de tu procesador ya sea <b>Intel</b> o <b>AMD</b>, tan simple como copiar el comando adecuado al procesador de tu equipo:
<br/>
<br/>

__*Para procesadores Intel:*__

<br/>
<br/>

```

sudo apt install intel-microcode iucode-tool

```

<br/>
<br/>

__*Para procesadores AMD (64 bits):*__

<br/>
<br/>

```

sudo apt install amd64-microcode

```
<br/>
<br/>

<b>Una vez realizados todos los pasos con éxito, solo queda reiniciar el equipo</b> y el siguiente arranque, usará el nuevo kernel <b>XanMod</b> para el arranque del sistema.<br/>

<b>Cualquier duda o sugerencia es bienvenida en los comentarios, un saludo y espero que os haya gustado.</b>

<br/>
<br/>

<b>Fuente original:</b> <https://xanmod.org/>
<br/>
<br/>
<b>Link para la descarga del wallpaper oficial de XanMod:</b> <https://xanmod.org/_detail/xanmod_wallpaper.png?id=download>

<br/>
<br/>
