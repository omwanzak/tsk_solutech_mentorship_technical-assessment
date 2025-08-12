## 🧠 Section A: Logical Thinking & System Design

**Scenario:**  
You're building a system to track borrowed library books. Think through how you'd structure the data and design the system to handle scale and prevent errors.

---

### ✍️ Challenge Instructions

Answer the following questions **briefly and clearly**. Use bullet points or short sentences where helpful.

---

### 📚 1. Three pieces of data to store for each book:
- What key information would help identify and manage each book?
   - Unique identifier like the book id.
   - The title of the book and Author
   - Inventory of the books-availablity status.


### 🚫 2. How to prevent the same book from being borrowed twice:
- What logic or system check would you implement?
   - Check the availability status before allowing a borrow action.
    - Use a transactional lock or validation logic to ensure only one active borrow per book.
    - Update status to "borrowed" immediately after a successful borrow.
---

### 📈 3. Scaling to 10,000 books and 1,000 users — what needs to change:
- What would you update in your design or infrastructure to handle this growth?

    - Implement pagination and search filters.
    - Cache frequent reads.
    - Use a relational database with indexing for easier data retrieving.
    - Implementing role based access control.

### 🔄 4. Store book info and borrowing record together or separately — why?
- Share your reasoning for how you'd structure the data.

    - I would store separately because:
        - It is easy to track borrowing history without duplicating book data.
        - Book info is static; borrowing records are dynamic.
        - Separation improves data integrity, query performance, and scalability

Take your time to think through each part. We're looking for clarity, logic, and practical design thinking. Good luck!
