
| Protection | Request / Evidence | Result |
| :--- | :--- | :--- |
| Password storage | `SELECT * FROM users;` (hashes present) | Pass |
| Anonymous create | `POST /recipes` w/o token → 401 | Pass |
| Owner read/write | `ashlyn` token → `POST/GET /recipes/:id` | Pass |
| Cross-user modify/delete | `testuser1` → 403, state unchanged | Pass |
| Admin delete | `recipeadmin` → 204, then 404 on GET | Pass |
| Old exploit regression | Old anonymous POST → 401 or 404 | Pass |
