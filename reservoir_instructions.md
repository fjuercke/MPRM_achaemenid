## Instructions for loading the reservoir data into your GEE assets. 

Before running the script, please complete **three setup steps**:

### 1) Download the Reservoir Dataset

Download the reservoir dataset through the Global Dam Watch (GDW) database here: https://www.globaldamwatch.org/database

Extract the zip-file.

---

### **1) Upload the reservoir dataset to your GEE Assets**

This step is required so the script can access the reservoir polygons.

**To upload the shapefile:**

1. Open the **Assets** tab in the left-hand panel of the GEE Code Editor (next to **Scripts** and **Docs**).
2. Click **New**.
3. Select **Table upload → Shapefiles**.
4. Click **Select** under *Source files* and navigate to the GDW dataset you saved locally and extracted. Choose the GDW_reservoirs shapefile from the GDW_v_shp folder.
5. **(Optional)** Rename the asset.
6. Click **Upload** in the bottom-right corner.

The upload will appear in the **Tasks** tab on the right. Processing may take **several minutes**.

After the task is complete:

* Check that the asset appears under **Assets**.
* If it does not appear immediately, click the **refresh button** (circular arrows) above the asset list.

---

### **2) Update the FeatureCollection path in the script**

Once your asset is visible in your asset library:

1. Click the **asset name** (not the three small icons that appear when hovering).
2. A details window will open.
3. Copy the **Table ID**, which looks like:

   ```
   projects/USERNAME/assets/ASSET_NAME
   ```

**Next, update the script:**

1. Scroll to **line 190**.
2. Replace the placeholder with your Table ID.

Example:

```javascript
// Example original line
var reservoir_polygons = ee.FeatureCollection('projects/ee-fkjuercke/assets/GDW_reservoirs_v1_0');

// Replace with your asset:
var reservoir_polygons = ee.FeatureCollection('[YOUR_TABLE_ID]');
```

**Important:** Ensure the Table ID remains wrapped in **single quotation marks**.

Finally, **save the script** after inserting the correct path.

The script is now ready to run. 
