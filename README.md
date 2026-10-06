# 🥋 SRE Dojo: Interactive Kubernetes & Linux Break-Fix Scenarios

Welcome to the SRE Dojo. This repository contains hands-on, reproducible scenarios where things are broken on purpose. Your mission is to diagnose, debug, and fix them using standard observability tools.

## How It Works
Each directory contains a broken scenario. 
1. `kubectl apply -f deploy.yaml` (or use the provided makefile/script) to spin up the broken environment.
2. Use `kubectl`, `journalctl`, and your wits to find the root cause.
3. Check `SOLUTION.md` when you are ready.

## Scenarios
- [x] **Scenario 01:** The Silent Crash (Pod pending forever)
- [ ] **Scenario 02:** The DNS Blackhole
- [ ] **Scenario 03:** CPU Throttling Nightmare

**Want to contribute?** We welcome new break-fix scenarios!
