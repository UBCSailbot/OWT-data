# OWT-data

Data from all the OWT so far.

Refer to the [deployment documentation](https://github.com/UBCSailbot/sailbot_workspace/blob/main/.devcontainer/release/README.md) for instructions on how to extract logs and rosbags.

Use `OWT-yyyy-mm-dd/ [EXAMPLE]` as a template folder for future OWTs. Feel free to delete the `.gitkeep` files inside.

## Notes

- `OWT-2026-03-15` only has a `...db.zip` file.
- Data from `OWT-2026-06-06` was recorded with the wrong timestamp (`2026-06-05`).
- Data from `OWT-2026-07-11` was recorded with the wrong timestamp (`2026-07-08`).
- `combined_can_frames.csv` contains all the can messages sent and recieved on the boat during the test.
    - This data is used for the mock can transceiver in Network system to test the Pathfinding system with real sensor data during the on-water test.
    - These files have been trimmed to only the window where the boat was actually in the water.
- `decoded_signals.csv` (the DBC-decoded form of `combined_can_frames.csv`) is **not** tracked in this repo. The files run to hundreds of MB each, which exceeds GitHub's 100 MB file size limit, so they are gitignored and regenerated locally from `combined_can_frames.csv` as needed.