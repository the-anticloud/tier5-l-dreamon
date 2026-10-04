# Developer Cookbook — L_DREAMON
**Stack:** Python 3.11, PyTorch 2.10+, K_DREAMER4, stable-baselines3, PAX 27B, AIOSS_FORMAT
**Domain:** DreamOn: dream-based offline RL training using world model imagined experience

## Dream-based RL training
```python
from l_dreamon import DreamOnTrainer

trainer = DreamOnTrainer(
    world_model="./dreamer4_checkpoint/",
    current_policy="./robot_policy.pt",
    pax_model="./pax-27b-q4.gguf",
    aioss_chain="./dreamon.aioss"
)

# Generate and train on dreams
for epoch in range(100):
    dreams = trainer.generate_dreams(
        n_trajectories=1000,
        scenario_diversity="high"
    )
    policy_update = trainer.train_on_dreams(dreams)
    print(f"Epoch {epoch}: improvement={policy_update.improvement:.3f}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
