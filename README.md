# Nitro Schema Publish

A GitHub Action that publishes GraphQL schemas to the Nitro registry.

## Usage

```yaml
- uses: ChilliCream/nitro-schema-publish@v16
  with:
    tag: <tag>
    stage: <stage>
    api-id: <api-id>
    api-key: <api-key>
```

## Inputs

| Name                | Required | Description                                            |
| ------------------- | -------- | ------------------------------------------------------ |
| `tag`               | Yes      | The tag of the schema version                          |
| `stage`             | Yes      | The name of the stage                                  |
| `api-id`            | Yes      | The ID of the API                                      |
| `api-key`           | Yes      | API key for authentication                             |
| `force`             | No       | Will not ask for confirmation on deletes or overwrites |
| `wait-for-approval` | No       | Wait for approval                                      |
| `cloud-url`         | No       | The URL of the Nitro registry                          |

The action automatically attaches source metadata from the GitHub Actions runtime.

If you self-host Nitro or use a dedicated hosted instance, you can specify the `cloud-url` input to point to your instance.
