# 快速启动

```bash
cd DIKWP_PACT_OPEN_AUDIT_PROJECT_v0.1.0
python -m pip install -e .
dikwp-pact validate benchmark/scenarios.jsonl
dikwp-pact run-baselines benchmark/scenarios.jsonl --out outputs
python -m unittest discover -s tests -v
```

双击 `prototype/index.html` 可打开离线驾驶舱。

公开前请先阅读：`PROJECT_CHARTER.md`、`governance/RELEASE_GATES.md`、`paper/PREREGISTRATION.md`。
