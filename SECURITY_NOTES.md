2026-11-02

- Anonymous GET /recipes → 200 OK, returns all recipes including non-public data.

- Anonymous PATCH /recipes/3 → 200 OK, updates secret recipe title.

- Anonymous DELETE /recipes/3 → 204 No Content, recipe 3 removed from subsequent GET /recipes.