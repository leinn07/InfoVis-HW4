<div class="assignment-rubric">

# Assignment 4 Rubric

**Visualization Design | 100 points**

This rubric is suitable for sharing with students. Grade the Gradescope responses, uploaded figures, and source materials as evidence of design reasoning, accurate representation, and revision. Multiple visual solutions can earn full credit.

Apply the criterion points without adding a separate holistic score. Award full credit for complete, accurate, task-specific evidence; substantial partial credit for sound work with minor omissions; limited credit for a meaningful attempt with a consequential error; and little or no credit for missing or irrelevant evidence.

## Part 1 - Define the design brief (10 points)

| Criterion | Points | Full-credit evidence |
|---|---:|---|
| Audience and context | 4 | Distinguishes domain and graphical knowledge; connects standalone newsletter reading to concrete design requirements |
| Task and required comparison | 3 | Explains what readers should compare or identify and any emphasis within the supplied route and time comparison task |
| Data meaning | 3 | Correctly explains the mean of two sampled runs per route-week and a relevant limit of the sample |

## Part 2 - Explore two alternatives (25 points)

| Criterion | Points | Full-credit evidence |
|---|---:|---|
| Two plausible, distinct sketches | 10 | Shows different visual structures or encodings for the same task; labels marks, scales, legend intent, and how full coverage fits |
| Two Wheel profiles | 9 | Clearly identifies both designs on one or two wheels; marks the six dimension pairs with qualitative positions consistent with the sketches |
| Brief design selection | 6 | States which design will be developed and gives a relevant audience- or task-based reason in one or two sentences |

<div class="assignment-page-break"></div>

## Part 3 - Implement the design in Vega-Lite (30 points)

| Criterion | Points | Full-credit evidence |
|---|---:|---|
| Implementation and data | 12 | Submitted Vega-Lite code and data reproduce the final graphic with 96 correct means, eight routes, twelve ordered weeks, ties, and truthful geometry; explains any derived summary |
| Task fit and standalone reading | 10 | A readable single page supports route and temporal comparison; labels, units, synthetic sample context, source, title, and consistent scales make interpretation possible |
| Encoding explanation | 8 | Briefly explains how marks and channels represent weeks, routes, and mean delays; justifies one axis-scale or route-order choice and applies two L10 concepts to specific design strengths or limitations |

## Part 4 - Explain and test color (25 points)

| Criterion | Points | Full-credit evidence |
|---|---:|---|
| Color channels and mapping | 9 | Justifies the color channels used in relation to attributes and task; explains color meaning and distinguishability through the legend or labels, with clear numeric domain, normalization, direction, bins, or reference when used |
| Comparison of two color choices | 10 | Changes one color choice on the same data and layout; clearly shows both versions, explains the change, and uses one reading example to justify a choice |
| Color vision considerations | 6 | Explains a potential color-reading difficulty and a specific adjustment that supports a comparison, or explains how an existing design feature addresses that difficulty |

## Part 5 - Evaluate and revise (10 points)

| Criterion | Points | Full-credit evidence |
|---|---:|---|
| Three reading checks | 4 | Gives a CSV-supported finding for route, time, and persistence/concentration comparisons; explains how clearly the graphic communicates each finding |
| Evidence-based revision | 4 | Shows a specific before/after change linked to a finding and rechecks the affected question; final graphic incorporates the revision |
| Limits and disclosure | 2 | States a remaining limitation and a truthful assistance disclosure |

## Grading guardrails

- Accept different chart types, palettes, route orders, and Wheel profiles. Complexity, novelty, glyphs, and interaction are not required or rewarded by themselves.
- For Part 2B, assess the drawn profiles and brief selection reason against the sketches, audience, and task.
- Part 2 may be hand-drawn. Part 3 requires a working Vega-Lite implementation; a draft alone is insufficient. Award demonstrated design and explanation credit if code fails, and avoid duplicate deductions for one failure. Code complexity earns no extra credit.
- Accept color comparisons involving category identity, ordered values, emphasis, or grayscale, as appropriate to the design. Judge the explanation against the displayed example.
- For Part 4C, assess reasoning about a proposed adjustment or an existing feature that helps readers with color vision deficiency interpret the student's design.
- Accept the finding that higher delays persist and weekly shapes are shared. Preserve ties and overlaps; do not demand distinct trends absent from the data.
- Require an explicit rule for threshold claims. Do not impose a particular cutoff or accept an invented official target.
- The same figures or explanations may support multiple parts. A Part 4 comparison can also support Part 5: assess the color judgment in Part 4 and the demonstrated improvement and recheck in Part 5.
- Judge the revised design as final; documented weaknesses in earlier versions are useful evidence.
- Deduct an underlying error once under its main criterion, then assess other demonstrated reasoning separately.
- Assess readability and completeness of the uploaded figures and written responses. Part 3's final graphic should remain readable as a single page.
- AI assistance is permitted. Assess correctness, understanding, verification, and disclosure; the final implementation must use Vega-Lite.

</div>
