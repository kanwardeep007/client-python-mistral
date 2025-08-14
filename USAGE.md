<!-- Start SDK Example Usage [usage] -->
### Create Chat Completions

This example shows how to create chat completions.

```python
# Synchronous Example
from kdmistralai import KdMistral
import os


with KdMistral(
    api_key=os.getenv("MISTRAL_API_KEY", ""),
) as kd_mistral:

    res = kd_mistral.chat.complete(model="mistral-small-latest", messages=[
        {
            "content": "Who is the best French painter? Answer in one short sentence.",
            "role": "user",
        },
    ], stream=False)

    # Handle response
    print(res)
```

</br>

The same SDK client can also be used to make asynchronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
from kdmistralai import KdMistral
import os

async def main():

    async with KdMistral(
        api_key=os.getenv("MISTRAL_API_KEY", ""),
    ) as kd_mistral:

        res = await kd_mistral.chat.complete_async(model="mistral-small-latest", messages=[
            {
                "content": "Who is the best French painter? Answer in one short sentence.",
                "role": "user",
            },
        ], stream=False)

        # Handle response
        print(res)

asyncio.run(main())
```

### Upload a file

This example shows how to upload a file.

```python
# Synchronous Example
from kdmistralai import KdMistral
import os


with KdMistral(
    api_key=os.getenv("MISTRAL_API_KEY", ""),
) as kd_mistral:

    res = kd_mistral.files.upload(file={
        "file_name": "example.file",
        "content": open("example.file", "rb"),
    })

    # Handle response
    print(res)
```

</br>

The same SDK client can also be used to make asynchronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
from kdmistralai import KdMistral
import os

async def main():

    async with KdMistral(
        api_key=os.getenv("MISTRAL_API_KEY", ""),
    ) as kd_mistral:

        res = await kd_mistral.files.upload_async(file={
            "file_name": "example.file",
            "content": open("example.file", "rb"),
        })

        # Handle response
        print(res)

asyncio.run(main())
```

### Create Agents Completions

This example shows how to create agents completions.

```python
# Synchronous Example
from kdmistralai import KdMistral
import os


with KdMistral(
    api_key=os.getenv("MISTRAL_API_KEY", ""),
) as kd_mistral:

    res = kd_mistral.agents.complete(messages=[
        {
            "content": "Who is the best French painter? Answer in one short sentence.",
            "role": "user",
        },
    ], agent_id="<id>", stream=False)

    # Handle response
    print(res)
```

</br>

The same SDK client can also be used to make asynchronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
from kdmistralai import KdMistral
import os

async def main():

    async with KdMistral(
        api_key=os.getenv("MISTRAL_API_KEY", ""),
    ) as kd_mistral:

        res = await kd_mistral.agents.complete_async(messages=[
            {
                "content": "Who is the best French painter? Answer in one short sentence.",
                "role": "user",
            },
        ], agent_id="<id>", stream=False)

        # Handle response
        print(res)

asyncio.run(main())
```

### Create Embedding Request

This example shows how to create embedding request.

```python
# Synchronous Example
from kdmistralai import KdMistral
import os


with KdMistral(
    api_key=os.getenv("MISTRAL_API_KEY", ""),
) as kd_mistral:

    res = kd_mistral.embeddings.create(model="mistral-embed", inputs=[
        "Embed this sentence.",
        "As well as this one.",
    ])

    # Handle response
    print(res)
```

</br>

The same SDK client can also be used to make asynchronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
from kdmistralai import KdMistral
import os

async def main():

    async with KdMistral(
        api_key=os.getenv("MISTRAL_API_KEY", ""),
    ) as kd_mistral:

        res = await kd_mistral.embeddings.create_async(model="mistral-embed", inputs=[
            "Embed this sentence.",
            "As well as this one.",
        ])

        # Handle response
        print(res)

asyncio.run(main())
```
<!-- End SDK Example Usage [usage] -->