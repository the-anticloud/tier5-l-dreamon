# Deploy Guide — L_DREAMON
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, PyTorch 2.10+, K_DREAMER4, stable-baselines3, PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, K_DREAMER4 trained world model, stable-baselines3, T4 GPU.

## Environment
T4 GPU. K_DREAMER4 world model checkpoint required. 32GB RAM.

## AIOSS Integration
```bash
aioss init --module L_DREAMON --output ./l_dreamon.aioss
aioss append --chain ./l_dreamon.aioss --payload ./output.bin --module L_DREAMON
aioss verify --chain ./l_dreamon.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_DREAMON",
    aioss_chain="./L_DREAMON.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_DREAMON.aioss --verbose
python -m L_DREAMON.tests.smoke
```
