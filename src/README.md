# PoisonGuard

ML-Based Data Poisoning Defense for Intrusion Detection Systems, evaluated on the CICIoMT2024 dataset with Random Forest and Logistic Regression.

This repository includes a Streamlit dashboard (`app.py`) that shows the dataset setup, the effect of label-flipping attacks, the defended model performance, the detection results and the defense workflow.

## Dashboard pages

1. Project Overview
2. Dataset & Poisoning
3. Model Performance
4. Detection Results
5. Defense Workflow
6. Threshold Comparison

## How to open the dashboard from Google Colab

Streamlit runs on a Google server, so the `localhost` and `External URL` links it prints will not open from your browser. A tunnel gives the dashboard a public link.

Open a new Colab notebook and run the cells below in order, each in its own cell. Start from a fresh runtime first (**Runtime → Restart session**) so nothing old is still running.

### Cell 1: install the libraries

```python
!pip install -q streamlit altair pandas
```

### Cell 2: create `app.py`

The first line must be `%%writefile app.py`. Paste the full code of `app.py` underneath it, then run the cell. You should see `Writing app.py`.

```python
%%writefile app.py
# paste the full app.py code here
```

Alternatively, upload `app.py` with the folder icon on the left of Colab (Upload), or clone this repository and move into it:

```python
!git clone https://github.com/<your-username>/<your-repo>.git
%cd <your-repo>
```

### Cell 3: check the file saved

```python
!ls -l app.py
!python -m py_compile app.py && echo "app.py OK"
```

It should print `app.py OK`. If it prints an error, the code was cut off while pasting. Paste it into Cell 2 again.

### Cell 4: start Streamlit in the background

```python
!streamlit run app.py --server.port 8501 --server.headless true --server.enableCORS false --server.enableXsrfProtection false &>/content/logs.txt &
```

### Cell 5: confirm it started

```python
!sleep 6; cat /content/logs.txt
```

You should see `You can now view your Streamlit app`. Do not open the links it prints, because they will not work from your browser.

### Cell 6: download the tunnel tool

```python
!wget -q https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64 -O cloudflared
!chmod +x cloudflared
```

### Cell 7: open the tunnel

```python
!./cloudflared tunnel --url http://localhost:8501
```

After a few seconds the cell prints a link that ends in `trycloudflare.com`. **Click that link** to open the dashboard. Keep this cell running while you use the dashboard. Closing it ends the link, and a new run creates a new link.

If Colab disconnects, `app.py` is deleted. Run Cells 1 to 7 again to get it back.

## Moving between pages

Use the arrow at the **upper left** of the dashboard:

1. Click the arrow to open the sidebar.
2. Pick a page from the list to move to it.
3. Click the arrow again to close the sidebar, so the page fills the whole screen.
