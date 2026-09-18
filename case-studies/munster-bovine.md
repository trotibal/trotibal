# Munster Bovine

## Making catalogue search useful across customer profiles

Munster Bovine's frontend includes React applications integrated into an Umbraco website. My recent contributions focused on global catalogue search and selecting the relevant profile for a result.

### The challenge

A result can have different profiles depending on the customer's farming system. The interface needs to help customers find an animal, narrow the results, and reach the appropriate profile without treating every profile as an unrelated item.

### My contribution

I worked on API-driven global search, responsive result cards, pagination, media handling, and profile-selection interactions. The implementation uses React, JavaScript, styled-components, and react-select within the existing application structure.

### Decision: separate API data from presentation

The search integration maps dairy and beef profile collections into a common UI shape. Media handling distinguishes images from video and accommodates missing values. Result cards get a consistent structure while retaining category information for navigation.

This places response normalization at the integration boundary instead of requiring every presentation component to understand each upstream variation.

### Decision: ask for the relevant profile

For applicable results, the interface offers a profile choice and remembers the customer's preference. The same result can then lead to the profile appropriate to that choice. My commits include the selection modal and refinements following client feedback.

Filtering and page-size changes reset pagination to the first page, avoiding a later page that no longer exists after the result set changes. Initial, loading, and empty states explain what to do or why results are not currently available.

### Outcome and verification limits

The source and commit history show the search, result-card, and profile-selection implementation. I do not have analytics establishing reduced search time or increased conversion.

A further accessibility pass should verify keyboard operation, focus management, and dialog semantics in the profile selector. The existing implementation should not be presented as proof of full accessibility compliance.

### What this demonstrates

- Building interactive React interfaces around an existing API and CMS.
- Normalizing data for reusable presentation components.
- Managing related search, filter, pagination, and preference state.
- Iterating on a customer-facing workflow after feedback.

This was a team project. This account describes my recent frontend contributions, not sole ownership of the catalogue or backend.
