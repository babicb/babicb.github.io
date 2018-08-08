---
layout: page
title: Teaching
---

Here you will find information about my teaching experience and graphical summaries of quantitative student feedback.

**Califoria Institute of Technology**

_Upcoming_

  * Probability Evidence and Belief (Spring 2019) 
  * Knowledge & Reality (Spring 2019) 
  * Introduction to Philosophy of Science (Winter 2019) 

_Previous_ 

  * Probability Evidence and Belief (Spring 2018) Syllabus PDF 
  * Seminar in Ethics, Statistics, and Law (Spring 2018) Syllabus PDF 
  * Knowledge & Reality (Fall 2017) Syllabus PDF 

**University of Michigan, Ann Arbor (primary instructor)**

  * Nature of Science (Fall 2016) Syllabus PDF
  * Knowledge & Reality (Summer 2016) Syllabus PDF 

**University of Michigan, Ann Arbor (TA)**

  * Philosophy, Politics & Economics (Fall 2015)
  * Philosophy, Politics & Economics (Winter 2015) 
  * Intermediate Logic (Fall 2014)

## Quantitative Feedback

<!DOCTYPE html>
<html>
<head>
  <style>
    .vega-actions a {
        margin-right: 12px;
        color: #757575;
        font-weight: normal;
        font-size: 13px;
    }
    .error {
        color: red;
    }
  </style>

<script src="https://cdn.jsdelivr.net/npm//vega@3.3.1"></script>
<script src="https://cdn.jsdelivr.net/npm//vega-lite@2.4.3"></script>
<script src="https://cdn.jsdelivr.net/npm//vega-embed@3.11"></script>

</head>
<body>
  <div id="vis"></div>
  <script type="text/javascript">
    var spec = {"config": {"view": {"width": 400, "height": 300}, "scale": {"rangeStep": 40}, "tick": {"bandSize": 35, "thickness": 2}}, "layer": [{"mark": "bar", "encoding": {"x": {"type": "nominal", "field": "course"}, "y": {"type": "quantitative", "field": "average"}}}, {"mark": {"type": "rule", "color": "red"}, "encoding": {"size": {"value": 3}, "y": {"type": "quantitative", "field": "university average"}}}], "data": {"values": [{"course": "a", "average": 25, "university average": 30}, {"course": "b", "average": 57, "university average": 30}, {"course": "c", "average": 23, "university average": 30}, {"course": "d", "average": 19, "university average": 30}, {"course": "e", "average": 8, "university average": 30}, {"course": "f", "average": 47, "university average": 30}, {"course": "g", "average": 8, "university average": 30}]}, "$schema": "https://vega.github.io/schema/vega-lite/v2.4.3.json"};
    var embed_opt = {"mode": "vega-lite"};

    function showError(el, error){
        el.innerHTML = ('<div class="error">'
                        + '<p>JavaScript Error: ' + error.message + '</p>'
                        + "<p>This usually means there's a typo in your chart specification. "
                        + "See the javascript console for the full traceback.</p>"
                        + '</div>');
        throw error;
    }
    const el = document.getElementById('vis');
    vegaEmbed("#vis", spec, embed_opt)
      .catch(error => showError(el, error));
  </script>
</body>
</html>
