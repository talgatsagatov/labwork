# LAB 4 – Distributed Transactions (2PC / 3PC)

This repository contains an implementation of Two-Phase Commit (2PC)
and Three-Phase Commit (3PC) protocols.

## How to run

Start participants:
python participant.py --id B --port 8001
python participant.py --id C --port 8002

Start coordinator:
python coordinator.py --port 8000 --participants http://localhost:8001,http://localhost:8002

Run client:
python client.py --coord http://localhost:8000 start TX1 2PC SET x 5
