---
{{- $fileNameParts := split .File.BaseFileName " - " }}
title: {{ index $fileNameParts 1 }}
{{- with index $fileNameParts 0 }}
artists: 
  - {{ . }}
{{- end }}
date: {{ .Date }}
draft: true
---

{{% chords %}}  
<!-- put intro here -->
{{% /chords %}}

{{% chords lyrics %}}  
<!-- put lyrics here -->
{{% /chords %}}
