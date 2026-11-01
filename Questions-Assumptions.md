# Questions, Assumptions & Contradictions

## 1. Questions

1. **Section 7.12 – Rental Agreements:** How should additional drivers be modeled? Should they be stored as separate records, or should their details be recorded directly for each rental?

2. **Section 7.12 – Rental Agreements:** Should the late fee amount be stored in the rental record, or calculated when the vehicle is returned?

3. **Section 7.15 – Maintenance and Parts:** Should every job card have at least one mechanic assigned to it, or can a job card exist without an assigned mechanic?

4. **Section 7.16 – Payments:** The SRS states that corporate clients usually receive one invoice at the end of each month instead of paying per rental. Should we model a separate INVOICE entity? If yes, should one invoice cover multiple rentals, and should payments be linked to invoices rather than individual rentals?

## 2. Assumptions

1. **Section 7.2 – Training:** An `AttemptNo` attribute is used to distinguish multiple enrollment attempts by the same employee for the same course.

2. **Section 7.3 – Fleet and Pricing:** A separate `SPECIAL_PRICE` entity is used to store individual car model prices and their validity periods.

3. **Section 7.7 – Customers:** `AUTHORIZED_DRIVER` is modeled as a weak entity because authorized drivers are identified within their corporate customer, and their driver numbers are unique only within that company.

4. **Section 7.7 – Customers:** `BLACKLIST_RECORD` is modeled as a separate entity to store the reason, date, and employee responsible for blacklisting a customer.

5. **Section 7.12 – Rental Agreements:** Rental extensions are modeled using a recursive relationship between `RENTAL` entities. Each rental can be directly extended by at most one rental.

6. **Section 7.15 – Maintenance and Parts:** The `WorksOn` relationship has partial participation on both sides. A job card may exist without an assigned mechanic.

## 3. Contradictions

- No contradictions have been identified in the reviewed SRS sections.