## 🚀 Quick Start (Local Setup)

This project uses [uv](https://github.com/astral-sh/uv) for extremely fast dependency management. Follow these steps to get running in seconds.

### 1. Install uv

If you don't have `uv` installed yet, run this (Mac/Linux):

**Bash**

```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

*(For Windows: `powershell -c "irm https://astral.sh/uv/install.ps1 | iex"`)*

### 2. Clone the Repository

### 3. Install Dependencies

This command will create a virtual environment and install all locked dependencies (Ray, NumPy, Jupyter, etc.) automatically.

**Bash**

```
uv sync
```

### 4. Run the Notebook

You don't need to manually activate the virtual environment. Just use `uv run` to launch Jupyter with the correct environment context:

**Bash**

```
uv run jupyter lab
```

*(Or `uv run jupyter notebook` if you prefer the classic interface)*

---

## 📂 Project Structure

* **`monte_carlo.ipynb`**: The main benchmark notebook containing the simulation logic and performance comparisons.
* **`pyproject.toml`**: Defines project metadata and dependencies.
* **`uv.lock`**: Ensures reproducible builds by locking exact package versions.

## ⚠️ A Note on `pip`

You might see `!pip install` commands inside the notebook. These are strictly for users running the code on **Google Colab**.

When running locally with `uv`, these cells are unnecessary because `uv sync` has already handled the installation. You can safely skip them.
