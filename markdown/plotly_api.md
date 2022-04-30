# Embedding Interactive Plotly graphs in PowerPoint

1. Sign up for a Plotly account

[Plotly | Make charts and dashboards online](https://chart-studio.plotly.com/feed)

2. Install chart studio package

```python
pip install chart_studio
```

3. From python file, import chart studio

```python
import chart_studio
import chart_studio.plotly as py
import chart_studio.tools as tls
```

4. Define username and api_key variables, using API key from plotly account settings

```python
username = 'your name'
api_key = 'your api key'
```

```{note}
Be careful where you store this! You don't want to push these to GitHub. I have a separate file which I read these values from, that way they're never saved in GitHub.
```

5. Log into Plotly account from your python file

```python
chart_studio.tools.set_credentials_file(username=username,api_key=api_key)
```

6. Generate some Plotly graph

```python
fig = pd_df.plot.scatter(x='x_data',y='y_data')
```

7. Upload graph to your Plotly account

```python
py.plot(fig,filename='figureName', auto_open = False)
```

8. Go to your Plotly account, open your figure with ‘viewer’ and copy the URL

```python
ex. https://chart-studio.plotly.com/~username/1
```

9. Install “Web Viewer” add-in on Microsoft PowerPoint, and add a new Web Viewer element
10. Use the URL of your Plotly file
