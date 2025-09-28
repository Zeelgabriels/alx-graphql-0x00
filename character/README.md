# GraphQL Character Queries - Task 0

## Objective
Write GraphQL queries to retrieve specific character information using their IDs from the Rick and Morty API.

## API Endpoint
- **GraphQL Endpoint**: https://rickandmortyapi.com/graphql

## Task Description
This task involves creating GraphQL queries to fetch character details for IDs 1, 2, 3, and 4. Each query retrieves the following fields:
- `id` - Character's unique identifier
- `name` - Character's name  
- `status` - Character's current status (Alive, Dead, Unknown)
- `species` - Character's species (Human, Alien, etc.)
- `type` - Character's subspecies or specific type
- `gender` - Character's gender

## Files Structure
- `character-id-1.graphql` / `character-id-1-output.json` - Rick Sanchez
- `character-id-2.graphql` / `character-id-2-output.json` - Morty Smith  
- `character-id-3.graphql` / `character-id-3-output.json` - Summer Smith
- `character-id-4.graphql` / `character-id-4-output.json` - Beth Smith

## Query Pattern
All queries follow the same structure, only changing the ID parameter:

```graphql
query {
  character(id: [ID_NUMBER]) {
    id
    name
    status
    species
    type
    gender
  }
}
```

## Learning Outcomes
- Understanding GraphQL query syntax
- Using arguments in GraphQL queries  
- Requesting specific fields to avoid over-fetching
- Working with the Rick and Morty GraphQL API

Task 1 - Character Pagination Queries
Objective
Create GraphQL queries to retrieve paginated lists of characters from the Rick and Morty API, demonstrating how to handle multiple records and pagination patterns.
Key Concepts Learned

Pagination: Splitting large datasets into manageable pages (20 characters per page)
Plural vs Singular Queries: characters(page: Int) vs character(id: ID!)
Results Wrapper: Multiple records are returned within a results array
Field Selection: Requesting only necessary fields (id, name, status, image)

Query Pattern for Pagination
graphqlquery {
  characters(page: [PAGE_NUMBER]) {
    results {
      id
      name
      status
      image
    }
  }
}
Files Added (Task 1)

characters-page-1.graphql / characters-page-1-output.json - Characters 1-20
characters-page-2.graphql / characters-page-2-output.json - Characters 21-40
characters-page-3.graphql / characters-page-3-output.json - Characters 41-60
characters-page-4.graphql / characters-page-4-output.json - Characters 61-80

Response Structure Difference
Task 0 (Single Character):
json{
  "data": {
    "character": {
      "id": "1",
      "name": "Rick Sanchez"
    }
  }
}
Task 1 (Multiple Characters):
json{
  "data": {
    "characters": {
      "results": [
        {
          "id": "1", 
          "name": "Rick Sanchez"
        },
        {
          "id": "2",
          "name": "Morty Smith"
        }
        // ... 18 more characters
      ]
    }
  }
}
Learning Outcomes

Understanding pagination in GraphQL APIs
Working with array responses (results)
Recognizing patterns in query structure
Efficient data fetching for large datasets
Difference between singular and plural GraphQL operations