# Transformer Model
    - Mask
        - Purpose: Prevent certain elements from contributing to computations
        - Types
            - Padding Mask
                - Purpose: Ignore padding tokens in input sequences
                - Use Case: Sequence-to-sequence tasks with varying sequence lengths
            - Look-ahead Mask (Future Mask)
                - Purpose: Prevent model from looking into future tokens
                - Use Case: Language modeling tasks where future information should not influence current prediction
