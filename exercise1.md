# 11.1 Warming up

Think about a hypothetical situation where we have an application being worked on by a team of about 6 people. The application is in active development and will be released soon.

Let us assume that the application is coded with some other language than JavaScript/TypeScript, e.g. in Python, Java, or Ruby. You can freely pick the language. This might even be a language you do not know much yourself.

Write a short text, say 200-300 words, where you answer or discuss some of the points below. You can check the length with <https://wordcounter.net/>. Save your answer to the file named exercise1.md in the root of the repository that you shall create in exercise 11.2.

The points to discuss:

Some common steps in a CI setup include linting, testing, and building. What are the specific tools for taking care of these steps in the ecosystem of the language you picked? You can search for the answers by Google.

What alternatives are there to set up the CI besides Jenkins and GitHub Actions? Again, you can ask Google!

Would this setup be better in a self-hosted or a cloud-based environment? Why? What information would you need to make that decision?
Remember that there are no 'right' answers to the above!

## Answer - Spanish Version

Considerando el escenario de una aplicación desarrollada en Python por un equipo de 6 personas que se encuentra en desarrollo activo y pronta a liberarse, es necesario asegurar que el equipo en su conjunto haga uso de alguna de herramienta de linting única con una configuración acordada por todos que evite conflictos tanto a nivel de los desarrolladores (uso de mayúsculas, tipo de case usado, etc.) como del repositorio (evitar diferencias de código fuente asociadas solo a diferentes formatos de código). Para ello, se podría usar PyLint, asumiendo que se usa el IDE de facto en la actualidad, Visual Studio Code, el cual se configurará con un archivo único el cual se dejará respaldado dentro del mismo repositorio del proyecto para acceso de cualquier desarrollador.

Para las pruebas, es posible usar Pytest ya que es una extensión soportada de forma nativa por el mismo VS Code, que permite implementar las pruebas unitarias como parte del mismo código fuente de la aplicación y usando el mismo lenguaje.

Para el build de la aplicación, se hace necesario generar scripts (bash), para poder usar la estructura de la aplicación e indicar el comando que inicia la aplicación desde el archivo que es el punto de entrada de la misma. Todo esto debe ser manejado dentro de algún contenedor Docker, el cual se configure con todas las dependencias necesarias.

Respecto a alternativas a usar para levantar CI de la aplicación, están CircleCI, TravisCI y CodeShip, entre muchas otras.

Esta configuración podría ser usada tanto en Cloud como en Local, ya que el uso de Docker y herramientas universales como son scripts bash, hacen que sea soportado por una gran cantidad de configuraciones posibles. Sin embargo, se requiere saber muchas más cosas para poder tomar la decisión de cual es la mejor alternativa, como por ejemplo, acceso a la aplicación, público objetivo, disponibilidad que debe tener, cantidad de usuarios concurrentes, presupuesto disponible para la implementación, entre muchas otras variables.

## Answer - English Version

Considering the scenario of an application developed in Python by a team of six people that is in active development and ready for release, it is necessary to ensure that the team as a whole uses a single linting tool with a configuration agreed upon by all to avoid conflicts at both the developer level (case usage, case type used, etc.) and the repository level (avoiding source code differences associated only with different code formats). To achieve this, PyLint could be used, assuming the current de facto IDE, Visual Studio Code, is used. This IDE will be configured with a single file that will be backed up within the project repository for any developer to access.

For testing, Pytest can be used, as it is an extension natively supported by VS Code itself, allowing unit tests to be implemented as part of the application's source code and using the same language.

To build the application, it is necessary to generate scripts (bash) to use the application structure and specify the command that launches the application from the file that is its entry point. All of this must be managed within a Docker container, which is configured with all the necessary dependencies.

Regarding alternatives to use to launch CI for the application, there are CircleCI, TravisCI, and CodeShip, among many others.

This configuration could be used both in the Cloud and on-premises, since the use of Docker and universal tools such as bash scripts allows it to support a large number of possible configurations. However, it requires a lot more knowledge to be able to decide which is the best option, such as access to the application, target audience, availability, number of concurrent users, available budget for implementation, among many other variables.
