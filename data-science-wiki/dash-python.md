# Dash-Python Tutorial 🚀

> Created by @jl33-ai 👦🏻

A comprehensive notebook to help you get started with Dash for Python.

**Tags:** #Python #Dash #DataScience #Plotly

## Introduction 📜

Dash, built on top of Flask, React and Plotly, is designed for developing interactive analytical web applications within Python - no HTML or Js required. Let's jump in and learn how to get started!

## How to Install Dash 🐍

It's straightforward to install Dash. Simply use pip:
```bash
pip install dash==1.20.0
```

Ensure you have the necessary version by checking:
```bash
pip freeze | grep dash==1.20.0
```

## Simple Dash App Example 👨‍💻

Here's a simple Dash app:

```python
import dash
import dash_core_components as dcc
import dash_html_components as html

app = dash.Dash(__name__)

app.layout = html.Div(children=[
    html.H1(children='Hello Dash'),

    html.Div(children='''
        Dash: A web application framework for Python.
    '''),

    dcc.Graph(
        id='example-graph',
        figure={
            'data': [
                {'x': [1, 2, 3], 'y': [4, 1, 2], 'type': 'bar', 'name': 'SF'},
                {'x': [1, 2, 3], 'y': [2, 4, 5], 'type': 'bar', 'name': u'Montréal'},
            ],
            'layout': {
                'title': 'Dash Data Visualization'
            }
        }
    )
])

if __name__ == '__main__':
    app.run_server(debug=True)
```
When you run this, it creates a webserver that serves this page. It live updates as you modify and save your Python code.

## Dash Components 🧩

- Dash provides a suite of abstracted user interface components with Python wrappers for creating user interfaces.
- Components are categorized under dash_core_components and dash_html_components modules.

## Adding Dash Callbacks 🔙

Callbacks functions in Dash apps add interactivity. Inputs and outputs of our application interface are mapped to these callback functions through decorators.

Here is a simple callback Example:

```python
import dash
from dash.dependencies import Input, Output
import dash_core_components as dcc
import dash_html_components as html

app = dash.Dash(__name__)

app.layout = html.Div([
    html.H6("Change the value in the text box to see callbacks in action!"),
    html.Div(["Input: ",
              dcc.Input(id='my-input', value='initial value', type='text')]),
    html.Br(),
    html.Div(id='my-output'),

])


@app.callback(
    Output(component_id='my-output', component_property='children'),
    [Input(component_id='my-input', component_property='value')]
)
def update_output_div(input_value):
    return 'Output: {}'.format(input_value)


if __name__ == '__main__':
    app.run_server(debug=True)
```
Here, whenever value of the Input element changes, the function `update_output_div` gets triggered and the returned value gets displayed in the 'my-output' component. 

And that's it! You have now seen the basics of creating a web app with Dash and Python. Enjoy creating your own Dash apps! 💫🎉