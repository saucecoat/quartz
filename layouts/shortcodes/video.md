<video
  src="{{ .Get "src" }}"
  type="{{ .Get "type" | default "video/mp4" }}"
  preload="{{ .Get "preload" | default "auto" }}"
  {{ if .Get "controls" }}controls{{ end }}
  {{ if .Get "autoplay" }}autoplay{{ end }}
  {{ if .Get "muted" }}muted{{ end }}
  {{ if .Get "loop" }}loop{{ end }}
  playsinline
  style="width: {{ .Get "width" | default "100%" }}; height: {{ .Get "height" | default "auto" }};"
>
  Dein Browser unterstützt kein HTML5-Video.
</video>
