---
title: 'Latexify.jl, translating mathematical Julia objects to renderable equations and tables.'
tags:
  - Julia
  - LaTeX
  - Markdown
  - equations
  - rendering
authors:
  - name: Niklas Korsbo
    orcid: 0000-0001-9811-3190
    affiliation: "1, 2"
affiliations:
 - name: The Sainsbury Laboratory, Cambridge University
   index: 1
 - name: Department of Applied Mathematics and Theoretical Physics, Cambridge University
   index: 2
date: 27 January 2020
bibliography: paper.bib

---

# Summary

Human-understandable representation and visualisation of data and objects is
important for understanding and communicating the results of scientific
software. 

Latexify.jl is a tool for converting Julia [@julia] objects to humanly
accessible and renderable equations and tables.  It allows for the conversion
of multiple types to LaTeX or Markdown-formatted strings and, in many
development environments, for immediate rendering of the result. Among the
supported inputs is a class of Expressions that describe mathematical
equations. These can be translated into LaTeX formatted mathematics and can be
outputted as LaTeX environments such as align, equation or in-line equations.
The conversion can recurse through many container types, even if they contain
mixed types, and produce resulting tables, arrays or aligned equations for
LaTeX or Markdown. The output is configurable and a recipe system makes it easy
to extend Latexify.jl to work with custom types without having to modify
Latexify.jl itself. This becomes especially powerful in combination with
Julia's metaprogramming facilities and easily generated domain-specific
languages (DSLs). Latexify.jl can, for example, output the system of
differential equations (and much more) that is automatically generated by a
chemical reaction arrow DSL provided by Catalyst.jl [@diffeq].  

The package aims to support the scientific work-flow through facilitating
inspection, automation and representation. Simple inspection of the equations
that a computational model is ultimately simulating may increase
comprehensibility and improve troubleshooting.  It, furthermore, allows for
de-mystification of computational models generated using DSLs.  The
programmatic formatting of equations and tables enables their automatic
inclusion into generated documents, documentation, reports or posts (possibly
in combination with tools such as Weave.jl [@weave]). Such programmatic
translation can also help to ensure an accurate correspondence between what
software does and what reports or articles claim that they do.  It is also just
rather convenient.


# Acknowledgements

I acknowledge the contributions from the Julia programming community and
especially those who through issues and pull requests have improved
Latexify.jl. I would also like to acknowledge my PhD supervisor, Henrik
Jönsson, who supports me in my work while allowing me to allocate my efforts as
I see fit.

The development of this package was, in part, supported by the Gatsby
Charitable Foundation, grant GAT3395-PR4.

# References
