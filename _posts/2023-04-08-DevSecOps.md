---
title: DevSecOps - De Confianza, SASTs e IAs
layout: post
categories: [DevSecOps]
image: /assets/img/buho.jpg
description: "DevSecOps - De Confianza, SASTs e IAs"
---

Partamos de un hecho que no por más repetido es menos cierto: La herramienta básica y principal con la que "Sec" trabaja en un entorno DevSecOps es la confianza. A partir de ahí, y sólo a partir de ahí, se puede construir todo lo demás, mucho o poco.

Un aspecto peculiar de la confianza es que es bastante difícil conseguirla y extremadamente fácil perderla, por lo que trabajarla suele convertirse en una tarea poco grata. Sobre todo en entornos donde la confianza tradicionalmente se ha impuesto por galones. Esto último tanto en la acepción referente a los distintivos y atribuciones del ejército, como a la medida de capacidad en galones (métricos) de vulnerabilidades por segundo que se le pueden enviar a los equipos de desarrollo hasta que vomitan. Los pobres.

Hace tiempo cayó en mis manos un trabajo publicado en 2020 por la universidad de la Rioja: [“Benchmarking approach to compare web applications static analysis tools detecting OWASP top ten security vulnerabilities.”](https://techscience.com/cmc/v64n3/39444) En el que se hacía una comparativa de diferentes analizadores estáticos de código, su ratio de falsos positivos y, en consecuencia, la mayor o menor necesidad de un equipo experto (hasta ahora, necesariamente, humano y por aquí van algunos tiros del artículo) para realizar triaje de los resultados y que fuesen útiles. Los resultados, bastante afinados, por mi experiencia, sobre vulnerabilidades de OWASP Top Ten, son de aproximadamente entre un 30%-40% de falsos positivos en escaneos de aplicaciones web. Esto significa que un tercio del trabajo que obligamos a "retrabajar" a un desarrollador si no se ha hecho un triaje y se han limpiado esos falsos positivos del informe antes de hacérselo llegar serán directamente mentira. Independientemente de la herramienta técnica que utilicemos, todas se mueven en un ratio similar.

¿Cual es el problema? ¿Que hay que hacer triaje? Pues ya se dice en La-Mancha: "¡¡Gente y sogas que se me ha caído la llueca al río!!" (He decidido no traducir este artículo como se puede observar). Pero el mundo era más fácil cuando sólo se trataba de tirar de sogas que ahora con esto de los triajes. Primero, porque no hay gente. Después, porque para poder descartar falsos positivos, bien, es necesario tener conocimiento de las aplicaciones: De su lógica de negocio, sus librerías, sus frameworks, arquetipos, porqués, por cuántos y por cuándos (¿he oído legacy?). Y eso, lamentablemente, es difícil.

Entonces, qué hacer. ¿Aceptamos ya que DevSecOps no funciona, que vamos a tener muchas vulnerabilidades y que los análisis estáticos nos van a ayudar de una manera muy limitada y directamente proporcional al número de expertos que puedan leer sus resultados? No, claro que no. Mis hijas tienen que comer. Vamos a la raíz de DevSecOps. Las personas. Y oye, que lo hemos dicho antes y seguro que vuestra capacidad retentiva no está mermada a base de torrijas aún. La confianza.

Trabajando un nivel de confianza adecuado con las personas, en el que se puedan explicar las cosas con total libertad y en el que todo el mundo quiere aprender, donde se quiere trabajar bien y, sobre todo, en el que se entiende que la seguridad de los desarrollos es un aspecto fundamental de la calidad de los mismos, será fácil que todo el mundo entienda que la utilidad de herramientas como SAST es incontestable enmarcándolas dentro de un entorno en el que todo el mundo entiende que el 60-70% de las cosas que aparecen ahí son importantes para todos. Que de los informes de 100 páginas, unas 60-70 son tesoros que es mejor que encontremos nosotros antes que los que quieren vulnerarnos. Que el proceso de "afinado" de las herramientas es progresivo y depende de todos. Que cuanto más pegado estés al desarrollo más importante eres para que el proceso salga bien. Porque es posible que no sepas tanto de seguridad como el friki este de las vulnerabilidades, pero sabes del otro 60% que decide si de verdad eso es un problema en el código o no y puedes ayudar a que en el próximo informe eso no aparezca, si no tiene que aparecer. O aparezca con mayor criticidad. Además esto tiene que venir desde el alto management presionando en los lugares adecuados, pero eso es objeto de otro post.

El último problema es que no sólo de confianza se vive, ya que esta raramente corrige bugs. El triaje se tiene que seguir haciendo para que el número de falsos positivos a analizar sea el mínimo posible y, durante el tiempo, se adapten las herramientas para que vaya disminuyendo de forma automatizada. Como el número de personas no parece que aumente pronto, hoy sabemos que el futuro a corto plazo nos pide apalancarnos en dos pilares fundamentales:

- **Programas de capacitación en ciberseguridad continuos para los equipos de desarrollo.** Ya sea a través de iniciativas tipo "Security Champion" o con formaciones continuas adaptadas a los equipos más pegados al desarrollo para hacer esa, ya no primera línea, sino línea cero de defensa. Que el código se escriba lo mejor posible desde los IDE.

- **Utilización de algoritmos de LLM/Inteligencia artificial** que sean capaces de entender el contexto de las aplicaciones de manera similar a como lo haría un analista y pueda hacer ese triaje. En este sentido, prácticamente la totalidad de las herramientas SAST están trabajando hoy. Me ha gustado este artículo de SemGrep (https://semgrep.dev/blog/2023/gpt4-and-semgrep-detailed) que me ha recordado el trabajo de la Universidad de la Rioja que citaba al principio y por el que he escrito esta entrada.

Seguiremos hablando de todo esto.

¡Buen fin de Semana Santa!



* hello
{:toc}