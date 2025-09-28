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