---
title: ETF Information Overview
description: OpenBB Platform Data Model
---

<!-- markdownlint-disable MD012 MD031 MD033 -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

---

## Implementation details

### Class names

| Model name | Parameters class | Data class |
| ---------- | ---------------- | ---------- |
| `EtfInfo` | `EtfInfoQueryParams` | `EtfInfoData` |

### Import Statement

```python
from openbb_core.provider.standard_models.etf_info import (
EtfInfoData,
EtfInfoQueryParams,
)
```

## Parameters

<Tabs>
<TabItem value="standard" label="Standard">

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| symbol | Union[str, List[str]] | Symbol to get data for. (ETF) |  | False |
| provider | Literal['fmp'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fmp' if there is no default. | fmp | True |
</TabItem>

</Tabs>

## Data

<Tabs>
<TabItem value="standard" label="Standard">

| Name | Type | Description |
| ---- | ---- | ----------- |
| symbol | str | Symbol representing the entity requested in the data. (ETF) |
| name | str | Name of the ETF. |
| inception_date | str | Inception date of the ETF. |
</TabItem>

<TabItem value='fmp' label='fmp'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| symbol | str | Symbol representing the entity requested in the data. (ETF) |
| name | str | Name of the ETF. |
| inception_date | str | Inception date of the ETF. |
| asset_class | str | Asset class of the ETF. |
| aum | float | Assets under management. |
| avg_volume | float | Average trading volume of the ETF. |
| cusip | str | CUSIP of the ETF. |
| description | str | Description of the ETF. |
| domicile | str | Domicile of the ETF. |
| etf_company | str | Company of the ETF. |
| expense_ratio | float | Expense ratio of the ETF. |
| isin | str | ISIN of the ETF. |
| nav | float | Net asset value of the ETF. |
| nav_currency | str | Currency of the ETF's net asset value. |
| website | str | Website link of the ETF. |
| holdings_count | int | Number of holdings in the ETF. |
</TabItem>

</Tabs>
