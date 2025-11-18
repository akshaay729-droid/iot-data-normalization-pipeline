# 🏭 IoT Data Normalization Pipeline

This repository contains the core logic for normalizing diverse IoT telemetry messages into a single, standardized JSON format for downstream processing and analytics.

The solution addresses inconsistent data inputs from two different vendor formats (Format 1 and Format 2) and uses Python unit tests to ensure a unified, accurate output.

---

## Project Structure

* **`copy_of_json_data_transformation.py`**: The main Python script containing the transformation functions (`convertFromFormat1`, `convertFromFormat2`) and the `unittest` suite to verify accuracy.
* **`data-1.json`**: Example input data for Vendor **Format 1**.
* **`data-2.json`**: Example input data for Vendor **Format 2** (uses ISO timestamp).
* **`data-result.json`**: The expected, unified JSON output structure.

---

## 🚀 How to Run the Tests

To confirm the data transformations are working correctly, you can clone the repository and run the Python script locally.

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/akshaay729-droid/iot-data-normalization-pipeline.git](https://github.com/akshaay729-droid/iot-data-normalization-pipeline.git)
    cd iot-data-normalization-pipeline
    ```
2.  **Execute the Test Script:**
    ```bash
    python3 copy_of_json_data_transformation.py
    ```
    If successful, the output will display: `All tests passed successfully! 🎉`

---

## Final Normalized Data Goal

All incoming data is transformed to match this unified structure:

```json
{
    "deviceID": "g35v_xyz_789",
    "deviceType": "AssemblyRobot",
    "timestamp": 1731675600000,
    "location": {
        "country": "germany",
        "city": "bavaria",
        "area": "munich-tech-park",
        "factory": "automation-werk-a",
        "section": "tooling-bay"
    },
    "data": {
        "status": "maintenance_due",
        "temperature": 28.5
    }
}
