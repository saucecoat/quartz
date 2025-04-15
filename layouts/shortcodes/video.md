<video 
  src="{{ .Get "src" }}" 
  type="{{ .Get "type" | default "video/mp4" }}" 
  preload="{{ .Get "preload" | default "auto" }}"
  controls 
  width="600" 
  playsinline
>
  Dein Browser unterstützt kein HTML5-Video.
</video>
