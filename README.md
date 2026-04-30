<div align="center">

# Prefab 🎨

**The generative UI framework that even humans can use.**

<a href="https://prefab.prefect.io">
<img src="https://raw.githubusercontent.com/PrefectHQ/prefab/main/docs/assets/showcase.png" alt="Prefab" width="1000">
</a>

</div>
<div align="center">
<img src="https://raw.githubusercontent.com/PrefectHQ/prefab/main/docs/assets/hello-world-card.png" alt="Hello world card" width="400">
</div>
</br>

```python
from prefab_ui.components import *
from prefab_ui.rx import Rx

name = Rx("name").default("world")

with Card():
    with CardContent():
        with Column(gap=3):
            H3(f"Hello, {name}!")
            Muted("Type below and watch this update in real time.")
            Input(name="name", placeholder="Your name...")
    with CardFooter():
        with Row(gap=2):
            Badge(f"Name: {name}", variant="default")
            Badge("Prefab", variant="success")
```

## See the Dashboard using
- prefab serve examples/hitchhikers-guide/dashboard.py
## Installation
```bash
pip install prefab-ui
```
Requires Python 3.10+.