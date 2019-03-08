# Efficient Frontier Explorer

Analyze Re's portfolio optimization component produces what is called a
multi-dimensional "Efficient Frontier" or "Pareto Frontier" of viable
solutions that satisfy certain optimization objectives and constraints. We
currently have the ability to visualize that frontier in Excel using 2D
plots of a selected pair of dimensions. The challenge is to provide an
innovative approach for conveying this information via a Web-based
solution, that potentially leverages different techniques for
visualization.

![](frontier-explorer.png)

## Objectives

- Conceptualize and prototype a Web UI that allows users to interactively
  explore the efficient frontier and get detailed information on each
  candidate solution
- Display additional information about each candidate by querying the
  Analyze Re API
- Allow for more than two optimization objectives (multi-dimensional)

## API Specification

The [Analyze Re REST API documentation](http://docs.analyzere.net/) describes how
[Optimizations](http://docs.analyzere.net/?http#optimization-views) are created
on the Analyze Re platform. It provides some examples code of how to initiated an optimization and retrieve the Efficient Frontier.

## Example Data Sets

There are preconfigured optimization results setup on an Analyze Re platform environment to get started with. There is are a smaller and a larger run. You can access these optimization results either via API or via our existing Excel-based Efficient Frontier Explorer.

- Small run via [API](https://hackaton-api.analyzere.net/optimization_views/4141f37e-5c28-4619-ab35-32f4d35bef1c) or via [Frontier Explorer](hackathon-frontier-explorer-small.xlsb)
- Large run via [API](https://hackaton-api.analyzere.net/optimization_views/6c596386-c496-48f2-b176-1c19f7207d53) or via [Frontier Explorer](hackathon-frontier-explorer-small.xlsb)

In order to open and interact with the Excel-based Frontier Explorer you will also need the Analyze Re Excel Add-In:

- [Analyze Re Excel Add-In 64-bit](https://analyzere.sharefile.com/d-s08223768c24463ab)
- [Analyze Re Excel Add-In 32-bit](https://analyzere.sharefile.com/d-s43fbb4d85d549c99)

## Useful Links

- [Analyze Re REST API Documentation](http://docs.analyzere.net/)
- [Angular JavaScript Framework](https://angular.io/)
- [React JavaScript Framework](https://reactjs.org/)
- [Bokeh](https://bokeh.pydata.org/en/latest/) - Interactive visualizations in Python
- [D3.js Data-Driven Documents](https://d3js.org/)
