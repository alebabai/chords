---
{{- $fileNameParts := split .File.BaseFileName " - " }}
title: {{ index $fileNameParts 0 | title }}
{{- with index $fileNameParts 1 }}
artists: 
  - {{ . | title }}
{{- end }}
draft: true
---
