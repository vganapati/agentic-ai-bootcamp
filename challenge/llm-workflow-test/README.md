# LLM-WORKFLOW-TEST

## Commands

====================
# Note for accessing python and uv binaries in a Jupyter notebook when selecting the "Agentic AI Bootcamp" kernel
import sys
from pathlib import Path

# this is the python binary
!{sys.executable} 
# expected output: /global/cfs/cdirs/training/2026/agentic-ai-bootcamp/agentic-ai-env/bin/python

# this is the uv binary
!{Path(sys.executable).parent / "uv"}
# expected output: /global/cfs/cdirs/training/2026/agentic-ai-bootcamp/agentic-ai-env/bin/uv

======================

# Note for accessing python and uv binarties in a Jupyter terminal

perlmutter~> module load python
perlmutter~> source /global/cfs/cdirs/training/2026/agentic-ai-bootcamp/agentic-ai-env/bin/activate
(agentic-ai-env) (nersc-python) perlmutter:~> which python
/global/cfs/cdirs/training/2026/agentic-ai-bootcamp/agentic-ai-env/bin/python
(agentic-ai-env) (nersc-python) perlmutter:~> which uv
/global/cfs/cdirs/training/2026/agentic-ai-bootcamp/agentic-ai-env/bin/uv

======================

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