# Adeel S Calculator

```ts
const adeelSCalculatorController = new AdeelSCalculatorController(client);
```

## Class Name

`AdeelSCalculatorController`


# Calculate

```ts
async calculate(
  operation: OperationsTypeEnum,
  x: number,
  y: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<number>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `operation` | [`OperationsTypeEnum`](../../doc/models/operations-type-enum.md) | Template, Required | operation of the calculator |
| `x` | `number` | Query, Required | first operant |
| `y` | `number` | Query, Required | second operant |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

`number`

## Example Usage

```ts
const operation = OperationsTypeEnum.ADD;

const x = 222.14;

const y = 165.14;

try {
  // @ts-expect-error: unused variables
  // eslint-disable-next-line @typescript-eslint/no-unused-vars
  const { result, ...httpResponse } = await adeelSCalculatorController.calculate(
  operation,
  x,
  y
);
  // Get more response info...
  // const { statusCode, headers } = httpResponse;
} catch (error) {
  if (error instanceof ApiError) {
    // @ts-expect-error: unused variables
    // eslint-disable-next-line @typescript-eslint/no-unused-vars
    const errors = error.result;
    // const { statusCode, headers } = error;
  }
}
```

