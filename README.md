
```markdown
# GraphQuest: Exploring and Implementing GraphQL (Part 1)

This project explores fundamental GraphQL concepts by constructing and executing queries against a GraphQL API [the API used)](https://rickandmortyapi.com/graphql). This is the first part of a two-part project focusing on GraphQL; the second part will involve a React application.

## Getting Started

This repository primarily contains GraphQL query examples.  You can execute these queries using a GraphQL playground or any GraphQL client of your choice.

* **API Endpoint:** `https://rickandmortyapi.com/graphql`

## Tasks and Queries

### Task 0: Get a Specific Character by ID

**Objective:** Retrieve a specific character's information using their ID.

**Query:**

```graphql
query GetCharacter($id: ID!) {
  character(id: $id) {
    id
    name
    status
    species
    image
  }
}

# Example variables:
# {
#   "id": 1
# }

```


### Task 1: Get a List of All Characters

**Objective:** Retrieve a paginated list of all characters.

**Query:**

```graphql
query GetCharacters($page: Int) {
  characters(page: $page) {
    info {
      count
      pages
      next
      prev
    }
    results {
      id
      name
      status
      species
      image
    }
  }
}

# Example variables:
# {
#   "page": 1
# }
```


### Task 2: Get a Specific Episode by ID

**Objective:** Fetch the details of a specific episode using its ID.

**Query:**

```graphql
query GetEpisode($id: ID!) {
  episode(id: $id) {
    id
    name
    air_date
    episode
    characters {
      id
      name
    }
  }
}


# Example variables:
# {
#   "id": 1
# }

```


## Future Work (Part 2)

The second part of this project will involve building a React application that integrates with this GraphQL API, allowing users to interact with the data dynamically.



```
