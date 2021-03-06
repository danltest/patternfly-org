---
title: Sparkline
author: dlabrecq
layout: page-tabs
---
<div class="tab-content">
  <div role="tabpanel" class="tab-pane active" id="overview">
    <p>A sparkline is a small chart that helps users to analyze data and understand trends and patterns (e.g. CPU Utilization in an environment). Sparklines are commonly used in tables, reports and dashboards.</p>
    <h2 id="example-overview-1">Example</h2>
    <div class="example">
      <div class="row">
        <div class="col-md-5">
          <div class="example-pf">
            {% include widgets/charts/sparkline.html id="sparkline-chart-1" %}
          </div>
        </div>
      </div>
    </div>
  </div>
  <div role="tabpanel" class="tab-pane" id="design">
    <h2>Description</h2>
    <div class="row">
      <div class="col-md-5 col-lg-4">
        <img src="{{site.baseurl}}assets/img/sparkline_callout2.png" alt="sparkline_callout2"/>
      </div>
      <div class="col-md-7 col-lg-8">
        <ol>
        <li><b>Sparkline:</b> The sparkline is blue with a light blue fill, which helps to visually define the x axis.</li>
        <li><b>Tooltip:</b> Use a tooltip on hover to display additional information about exact points on the sparkline such as values or percentages. A vertical line and dot may be added to accentuate the user’s hover point.</li>
        <!--<li><b>X and Y Axis:</b> A visual representation of the X and Y axis (not shown) can be used if needed.-->
        </ol>
      </div>
    </div>
  </div>
  <div role="tabpanel" class="tab-pane" id="code">
    {% include nav-tabs-code.html %}
    <div class="tab-content">
      <div role="tabpanel" class="tab-pane nested active" id="html-css">
        <h2 id="example-code-1">Example</h2>
        <div class="example">
          <div class="row">
            <div class="col-md-5">
              <div class="example-pf" style="padding-bottom: 20px;">
                {% include widgets/charts/sparkline.html id="sparkline-chart-2" %}
              </div>
            </div>
          </div>
        </div>
        <p class="reference-markup"><a class="collapse-toggle" data-toggle="collapse" aria-expanded="true" aria-controls="markup-1" href="#markup-1">Reference Markup</a></p>
        <div class="collapse in" id="markup-1">
          <pre class="prettyprint">{% capture markup_include %}
<script src="components/c3/c3.min.js"></script>
<script src="components/d3/d3.min.js"></script>
{% include widgets/charts/sparkline.html id="sparkline-chart-2" %}
          {% endcapture %}{{ markup_include | xml_escape }}</pre>
        </div>
      </div>
      <div role="tabpanel" class="tab-pane nested" id="angular">
        <div ng-app="docsApp" ng-controller="DocsController" class="content">
          <div ng-include src="'/components/angular-patternfly/dist/docs/partials/api/patternfly.charts.directive.pfSparklineChart.html'"></div>
        </div>
      </div>
    </div>
  </div>
</div>
