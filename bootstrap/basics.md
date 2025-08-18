
### ✅ Bootstrap Form Syntaxes & Use Cases

1. **Basic Label + Input**

   ```html
   <label for="email" class="form-label">Email</label>
   <input type="email" id="email" class="form-control">
   ```

   🔹 Use when you want a **normal input field with a label**.

---

2. **Readonly Input**

   ```html
   <input type="text" value="lakshmi.com" readonly class="form-control">
   ```

   🔹 Use when you want to **display text that cannot be changed**.

---

3. **Select Dropdown**

   ```html
   <select class="form-select form-select-lg">
     <option>lakshmi</option>
     <option>nidhishree</option>
     <option>sachin</option>
   </select>
   ```

   🔹 Use for **dropdown options** (single selection).

---

4. **Checkbox**

   ```html
   <input type="checkbox" class="form-check-input"> Option
   ```

   🔹 Use for **on/off multiple selections**.

---

5. **Switch (toggle style)**

   ```html
   <div class="form-check form-switch">
     <input class="form-check-input" type="checkbox" role="switch">
   </div>
   ```

   🔹 Use for a **toggle switch instead of a plain checkbox**.

---

6. **Input Group (with symbols / addons)**

   ```html
   <div class="input-group">
     <span class="input-group-text">$</span>
     <input type="number" class="form-control">
     <span class="input-group-text">.00</span>
   </div>
   ```

   🔹 Use to **add symbols/icons before or after input**.

---

7. **Floating Label**

   ```html
   <div class="form-floating">
     <input type="email" id="email" class="form-control" placeholder="Email">
     <label for="email">Email</label>
   </div>
   ```

   🔹 Use for **modern floating labels inside input fields**.

---

8. **Button**

   ```html
   <button type="submit" class="btn btn-primary">Submit</button>
   ```

   🔹 Use `btn btn-primary` for a **Bootstrap styled button**.

---

👉 If you **remember just these 8 syntaxes**, you can build **any kind of Bootstrap form**.

Would you like me to create a **cheat sheet table (syntax + screenshot of output + use case)** so you can revise it faster?
