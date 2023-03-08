# adept

Reinforcement learning abstractions for speed and simplicity.

## Design Overview

### Conventions
- Batch dimensions come before non-batch dimensions
- 

### `Space`
- Represents batched tensor dimensions
  - Operations accept `with_batch`
      - Sampling (interface)
      - Logit dimensions (interface)
      - Dimensions
      - Empty tensor
  - Set batch size

#### `Box`
- A bounded `Space` representing a continuous range of values
- Uniform sampling
- Flat logits

#### `Discrete`
- A categorical `Space` representing `n` unique choices in a category
- Uniform sampling
- Flat logits

#### `MultiDiscrete`
- A categorical `Space` representing `m` `Discrete` categories
- Uniform sampling from each category

### `Spec`
- A set of named or unnamed `Space`s. Used to define input/output relationships between TODO