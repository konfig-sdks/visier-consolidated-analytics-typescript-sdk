<div align="center">

[![Visit Visier](./header.png)](https://visier.com)

# [Visier](https://visier.com)<a id="visier"></a>

Visier APIs for managing consolidated analytics (CA) tenants.

</div>

## Table of Contents<a id="table-of-contents"></a>

<!-- toc -->

- [Installation](#installation)
- [Getting Started](#getting-started)
- [Reference](#reference)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.addExcludedSources`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alphaaddexcludedsources)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.addSourceTenants`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alphaaddsourcetenants)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.createTenant`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alphacreatetenant)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.listExcludedSources`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alphalistexcludedsources)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.listSourceTenants`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alphalistsourcetenants)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.listTenants`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alphalisttenants)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.removeExcludedSources`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alpharemoveexcludedsources)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.removeSourceTenants`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alpharemovesourcetenants)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.setExcludedSources`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alphasetexcludedsources)
  * [`visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.setSourceTenants`](#visierconsolidatedanalyticsconsolidatedanalyticsv1alphasetsourcetenants)

<!-- tocstop -->

## Installation<a id="installation"></a>
<div align="center">
  <a href="https://konfigthis.com/sdk-sign-up?company=Visier&serviceName=ConsolidatedAnalytics&language=TypeScript">
    <img src="https://raw.githubusercontent.com/konfig-dev/brand-assets/HEAD/cta-images/typescript-cta.png" width="70%">
  </a>
</div>

## Getting Started<a id="getting-started"></a>

```typescript
import { VisierConsolidatedAnalytics } from "visier-consolidated-analytics-typescript-sdk";

const visierconsolidatedanalytics = new VisierConsolidatedAnalytics({
  // Defining the base path is optional and defaults to https://vanity.api.visier.io
  // basePath: "https://vanity.api.visier.io",
});

const addExcludedSourcesResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.addExcludedSources(
    {}
  );

console.log(addExcludedSourcesResponse);
```

## Reference<a id="reference"></a>


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.addExcludedSources`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alphaaddexcludedsources"></a>

This API adds excluded sources to the list of excluded sources for a consolidated analytics tenant.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const addExcludedSourcesResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.addExcludedSources(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### excludedSources: `string`[]<a id="excludedsources-string"></a>

A list of a CA tenant\\\'s excluded sources.

##### tenantId: `string`<a id="tenantid-string"></a>

The ID of the tenant. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}  is the consolidated analytic tenant code.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPIExcludedSourcesListDTO](./models/consolidated-analytics-apiexcluded-sources-list-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants/:tenantId/excluded-sources` `PATCH`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.addSourceTenants`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alphaaddsourcetenants"></a>

This API adds source tenants to the list of source tenants for a consolidated analytics tenant.

 If successful, the response returns an updated list of source tenants.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const addSourceTenantsResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.addSourceTenants(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### tenantCodes: `string`[]<a id="tenantcodes-string"></a>

A list of a CA tenant\\\'s source tenants codes. The maximum length is 1000.

##### tenantId: `string`<a id="tenantid-string"></a>

The ID of the tenant. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}  is the consolidated analytic tenant code.

##### limit: `number`<a id="limit-number"></a>

The maximum number of source tenants to return. The maximum value is 1000. Default is 400.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPISourceTenantListDTO](./models/consolidated-analytics-apisource-tenant-list-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants/:tenantId/source-tenants` `PATCH`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.createTenant`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alphacreatetenant"></a>

This API allows you to create a consolidated analytics tenant.

 A new CA tenant has no source tenants and no excluded sources.

 **Note:** CA tenant codes must have a prefix of CA. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}
 is the consolidated analytic tenant code.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const createTenantResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.createTenant(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### tenantCode: `string`<a id="tenantcode-string"></a>

The ID of the tenant. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}  is the consolidated analytic tenant code.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPITenantCreateRequestDTO](./models/consolidated-analytics-apitenant-create-request-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants` `POST`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.listExcludedSources`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alphalistexcludedsources"></a>

This API allows you to retrieve a CA tenant's excluded sources.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const listExcludedSourcesResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.listExcludedSources(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### tenantId: `string`<a id="tenantid-string"></a>

The ID of the tenant. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}  is the consolidated analytic tenant code.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPIExcludedSourcesListDTO](./models/consolidated-analytics-apiexcluded-sources-list-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants/:tenantId/excluded-sources` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.listSourceTenants`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alphalistsourcetenants"></a>

This API allows you to retrieve a CA tenant's source tenants.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const listSourceTenantsResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.listSourceTenants(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### tenantId: `string`<a id="tenantid-string"></a>

The ID of the tenant. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}  is the consolidated analytic tenant code.

##### limit: `number`<a id="limit-number"></a>

The maximum number of source tenants to return. The maximum value is 1000. Default is 400.

##### start: `number`<a id="start-number"></a>

The starting index of the first source tenant to return. Default is 0.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPISourceTenantListDTO](./models/consolidated-analytics-apisource-tenant-list-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants/:tenantId/source-tenants` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.listTenants`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alphalisttenants"></a>

This API allows you to retrieve the full list of consolidated analytics tenants in your administrating tenant.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const listTenantsResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.listTenants(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### limit: `number`<a id="limit-number"></a>

The maximum number of tenants to return. The maximum value is 1000. Default is 400.

##### start: `number`<a id="start-number"></a>

The starting index of the first tenant to return. Default is 0.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPITenantListResponseDTO](./models/consolidated-analytics-apitenant-list-response-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.removeExcludedSources`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alpharemoveexcludedsources"></a>

This API removes excluded sources from the list of excluded sources for a consolidated analytics tenant.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const removeExcludedSourcesResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.removeExcludedSources(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### excludedSources: `string`[]<a id="excludedsources-string"></a>

A list of a CA tenant\\\'s excluded sources.

##### tenantId: `string`<a id="tenantid-string"></a>

The ID of the tenant. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}  is the consolidated analytic tenant code.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPIExcludedSourcesListDTO](./models/consolidated-analytics-apiexcluded-sources-list-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants/:tenantId/excluded-sources` `DELETE`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.removeSourceTenants`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alpharemovesourcetenants"></a>

This API removes source tenants from the list of source tenants for a consolidated analytics tenant.

 If successful, the response returns an updated list of source tenants.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const removeSourceTenantsResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.removeSourceTenants(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### tenantCodes: `string`[]<a id="tenantcodes-string"></a>

A list of a CA tenant\\\'s source tenants codes. The maximum length is 1000.

##### tenantId: `string`<a id="tenantid-string"></a>

The ID of the tenant. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}  is the consolidated analytic tenant code.

##### limit: `number`<a id="limit-number"></a>

The maximum number of source tenants to return. The maximum value is 1000. Default is 400.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPISourceTenantListDTO](./models/consolidated-analytics-apisource-tenant-list-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants/:tenantId/source-tenants` `DELETE`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.setExcludedSources`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alphasetexcludedsources"></a>

This API defines the excluded sources for a consolidated analytics tenant.

 After you create a CA tenant, you may optionally define a list of excluded sources. The excluded sources are the sources whose data is excluded from the CA tenant.
 You can also use this API to replace the list of excluded sources for an existing CA tenant.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const setExcludedSourcesResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.setExcludedSources(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### excludedSources: `string`[]<a id="excludedsources-string"></a>

A list of a CA tenant\\\'s excluded sources.

##### tenantId: `string`<a id="tenantid-string"></a>

The ID of the tenant. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}  is the consolidated analytic tenant code.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPIExcludedSourcesListDTO](./models/consolidated-analytics-apiexcluded-sources-list-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants/:tenantId/excluded-sources` `PUT`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.setSourceTenants`<a id="visierconsolidatedanalyticsconsolidatedanalyticsv1alphasetsourcetenants"></a>

This API defines the source tenants for a consolidated analytics tenant.

 After you create a CA tenant, you must define a list of its source tenants. The source tenants are the tenants whose data is aggregated in the CA tenant.
 You can also use this API to replace the list of source tenants for an existing CA tenant.

 If successful, the response returns an updated list of source tenants.

 <br>**Note:** <em>This API is in **alpha**. While in alpha, APIs may change in a breaking way without notice; functionality may be removed, and no deprecation notices will be issued.
 If you are interested in using this API, please contact your Customer Success Manager (CSM).</em>

#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const setSourceTenantsResponse =
  await visierconsolidatedanalytics.consolidatedAnalyticsV1Alpha.setSourceTenants(
    {}
  );
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### tenantCodes: `string`[]<a id="tenantcodes-string"></a>

A list of a CA tenant\\\'s source tenants codes. The maximum length is 1000.

##### tenantId: `string`<a id="tenantid-string"></a>

The ID of the tenant. For example, WFF_{XXX}~CA{YYY} where {XXX} is the administrating tenant code and {YYY}  is the consolidated analytic tenant code.

##### limit: `number`<a id="limit-number"></a>

The maximum number of source tenants to return. The maximum value is 1000. Default is 400.

#### 🔄 Return<a id="🔄-return"></a>

[ConsolidatedAnalyticsAPISourceTenantListDTO](./models/consolidated-analytics-apisource-tenant-list-dto.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1alpha/admin/consolidated-analytics/tenants/:tenantId/source-tenants` `PUT`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


## Author<a id="author"></a>
This TypeScript package is automatically generated by [Konfig](https://konfigthis.com)
