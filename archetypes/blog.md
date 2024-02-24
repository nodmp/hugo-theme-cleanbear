+++
title = "{{ replace .Name "-" " " | title }}"
date = "{{ .Date }}"
slug = "{{ replace .Name "-" "-" | title }}"
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."
description = ""
tags = [{{ range $plural, $terms := .Site.Taxonomies }}{{ range $term, $val := $terms }}"{{ printf "%s" $term }}",{{ end }}{{ end }}]
+++

This is a page about »{{ replace .Name "-" " " | title }}«.
