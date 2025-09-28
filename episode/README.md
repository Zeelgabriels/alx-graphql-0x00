# Episode Queries - Task 2

## Objective
Write GraphQL queries to fetch episode details using pagination from the Rick and Morty API.
Key Learning Points

Episode Data Structure: Episodes contain id, name, air_date, and episode fields
Episode Pagination: Similar to character pagination, episodes are returned in pages
Cross-Domain Queries: Applied pagination concepts from characters to episodes
Episode Codes: Episodes use format like "S01E01" (Season 1, Episode 1)

## Query Pattern
graphqlquery {
  episodes(page: [PAGE_NUMBER]) {
    results {
      id
      name
      air_date
      episode
    }
  }
}

## Files Structure (Task 2)

episode-page-1.graphql with characters-page-1-output.json
characters-page-2.graphql with characters-page-2-output.json
characters-page-3.graphql with characters-page-3-output.json
characters-page-4.graphql with characters-page-4-output.json

## Note: File naming follows task requirements exactly as specified.
Episode Data Example
Episodes typically contain information like:

name: "Pilot" or "Lawnmower Dog"
air_date: "December 2, 2013"
episode: "S01E01" (Season/Episode code)

## Learning Outcome
Successfully demonstrated ability to apply GraphQL pagination patterns across different data types (characters → episodes).