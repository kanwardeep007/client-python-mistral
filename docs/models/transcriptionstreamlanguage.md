# TranscriptionStreamLanguage


## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `type`                                                       | *Optional[Literal["transcription.language"]]*                | :heavy_minus_sign:                                           | N/A                                                          |
| `data`                                                       | [models.AudioLanguageChunk](../models/audiolanguagechunk.md) | :heavy_check_mark:                                           | Language identifier, formatted as an ISO 639-1 tag.          |