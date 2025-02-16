# Custom Sawmill Recipes for Wooden Utilities Mod  

This guide explains how to create custom sawmill recipes for the **Wooden Utilities** mod in Minecraft. Follow the steps carefully to configure your recipes properly.

---

# 📌 How to Add Custom Recipes  

## 1️⃣ Edit the `Wooden Utilities.toml` Config  
1. Navigate to the `config` folder in your Minecraft directory.  
2. Open the file **`Wooden Utilities.toml`**.  
3. Find the setting:  
   ```toml
   Auto Regenerate Crafting Recipes = true
   ```  
4. Change it to:  
   ```toml
   Auto Regenerate Crafting Recipes = false
   ```  
   This prevents the game from overwriting your custom recipes.  

---

## 2️⃣ Create the Custom Recipe Folder  
1. Go back to the `config` folder.  
2. Create a new folder named:  
   ```
   wooden_utilities
   ```

---

## 3️⃣ Add a Custom Recipe File  
1. Inside the `wooden_utilities` folder, create a new file.  
2. Name it using this format:  
   ```
   {recipe_id}_{page}sawmillrecipe.json
   ```
   - **`recipe_id`**: A unique number for the recipe.  
   - **`page`**: The page number in the sawmill GUI.  
   - **Example**: `1_1sawmillrecipe.json` (First recipe on page 1).  

⚠️ **Note:** You **cannot** use the same `recipe_id` and `page` for multiple recipes of the same item.

---

## 4️⃣ Write the Recipe JSON  
Inside your `1_1sawmillrecipe.json` file, add the following structure:

```json
{
  "Needed Item ID Or Tag": "minecraft:oak_log",
  "Result slot 1 item ID": "minecraft:planks",
  "Result slot 2 item ID": "minecraft:stick",
  "Result slot 3 item ID": "",
  "Result slot 4 item ID": "",
  "Result slot 5 item ID": "",
  "Result slot 6 item ID": "",
  "Result slot 7 item ID": "",
  "Result slot 8 item ID": "",
  "Result slot 9 item ID": "",
  "Result slot 10 item ID": "",
  "Result slot 11 item ID": "",
  "Result slot 12 item ID": ""
}
```

#### 🔹 Explanation:  
- `"Needed Item ID Or Tag"`: The required input item. Example:  
  - `"minecraft:oak_log"` (specific item)  
  - `"forge:strings"` (tag-based input)  
- `"Result slot X item ID"`: The output items in each of the **12 possible slots**. If a slot is empty, leave it as `""`.  

---

## ✅ Example Recipes  
Here are a few examples:  

## **Example 1: Oak Log to Planks & Sticks**
```json
{
  "Needed Item ID Or Tag": "minecraft:oak_log",
  "Result slot 1 item ID": "minecraft:oak_planks",
  "Result slot 2 item ID": "minecraft:oak_planks",
  "Result slot 3 item ID": "minecraft:stick",
  "Result slot 4 item ID": "minecraft:stick",
  "Result slot 5 item ID": "",
  "Result slot 6 item ID": "",
  "Result slot 7 item ID": "",
  "Result slot 8 item ID": "",
  "Result slot 9 item ID": "",
  "Result slot 10 item ID": "",
  "Result slot 11 item ID": "",
  "Result slot 12 item ID": ""
}
```

## **Example 2: Logs to Charcoal**
```json
{
  "Needed Item ID Or Tag": "minecraft:birch_log",
  "Result slot 1 item ID": "minecraft:charcoal",
  "Result slot 2 item ID": "minecraft:charcoal",
  "Result slot 3 item ID": "",
  "Result slot 4 item ID": "",
  "Result slot 5 item ID": "",
  "Result slot 6 item ID": "",
  "Result slot 7 item ID": "",
  "Result slot 8 item ID": "",
  "Result slot 9 item ID": "",
  "Result slot 10 item ID": "",
  "Result slot 11 item ID": "",
  "Result slot 12 item ID": ""
}
```

---

## ⚠️ Important Notes  
- **Each recipe must have a unique `recipe_id` and `page` combination.**  
- **Leave empty slots as `""`** (do not remove them).  
- **If a recipe isn’t working, check the config settings and folder structure.**  

---

📌 **Created for the Wooden Utilities Mod** – Happy Crafting! 🎉  
```
