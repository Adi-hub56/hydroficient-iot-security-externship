# Week 2: Learning Python for IoT Security

## Objective
Learn Python fundamentals for working with IoT sensor data — Pandas, JSON
parsing (including nested JSON), and building a mock data generator that
produces realistic HYDROLOGIC sensor readings.

## What's Inside
- [`sensor_generator.ipynb`](./sensor_generator.ipynb) — the complete
  `WaterSensor` class, built from scratch, including normal readings and
  three anomaly simulations (leak, blockage, stuck sensor)
- [`sensor_data.json`](./sensor_data.json) — 100 generated sensor readings
  (97 normal, 3 anomalies), used as test data for later projects (MQTT
  publishing, TLS, replay attack defense, and the security dashboard)

## Skills Covered
- Pandas: loading, cleaning, and flattening tabular data
- Parsing flat and nested JSON with Python's `json` library and
  `pandas.json_normalize()`
- Building a Python class with instance state (`self.counter`,
  timestamp generation)
- Simulating realistic sensor drift vs. anomalous readings for security
  testing purposes

## Key Concept
Every reading includes a `timestamp` and an incrementing `counter` —
these two fields are the foundation for detecting replay attacks in a
later project (an attacker resending a captured "shutoff" command).
