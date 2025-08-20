{{ define "main" }}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>{{ .Site.Title }}</title>
  <link rel="stylesheet" href="/css/style.css">
</head>
<body>
  <header>
    <h1>{{ .Site.Title }}</h1>
    <p>Portfólio de projetos, POCs e posts DevOps</p>
  </header>

  <section id="projects">
    <h2>Projetos Recentes</h2>
    <ul>
      {{ range .Site.RegularPages }}
      <li>
        <a href="{{ .RelPermalink }}">{{ .Title }}</a> - {{ .Date.Format "Jan 2, 2006" }}
      </li>
      {{ end }}
    </ul>
  </section>
</body>
</html>
{{ end }}
