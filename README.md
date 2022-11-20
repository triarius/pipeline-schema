Buildkite Pipeline Schema
===

Typescript Schema for buildkite generated from https://github.com/buildkite/pipeline-schema


```typescript
import { Pipeline, isPipeline } from  "@triarius/pipeline-schema";

# you can read this from the filesystem
const pipeline: Pipeline = `
steps:
  - name: hello_world
    command: echo Hello, World!
`;

# and check the pipeline is valid here
if (!isPipeline(pipeline)) {
  throw new Error("not a pipeline");
}
```
