# LLM-WORKFLOW-TEST

## Commands

=============
# Some notes for accessing python and uv binaries in a Jupyter notebook when selecting the "Agentic AI Bootcamp" kernel
import sys
from pathlib import Path

# this is the python binary
!{sys.executable} --version
# this is the uv binary
!{Path(sys.executable).parent / "uv"} --version

=================

# Note for accessing python and uv binarties in a Jupyter terminal




==================

Start invoice mcp server

```
cd mcp-servers/invoice
uv run mcp-server-invoice \
    --mcp-server-qna-path ../qna \
    --inf-url https://integrate.api.nvidia.com/v1 \
    --nvidia-api-key <your api key>
```

Run your test cases

```
cd llm-workflow-test
uv run main.py
```