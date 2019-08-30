---
title: Module maps
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../">@pulumi/azure</a> &gt; maps

> This provider is a derived work of the [Terraform Provider](https://github.com/terraform-providers/terraform-provider-azurerm)
> distributed under [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/). If you encounter a bug or missing feature,
> first check the [`pulumi/pulumi-azure` repo](https://github.com/pulumi/pulumi-azure/issues); however, if that doesn't turn up anything,
> please consult the source [`terraform-providers/terraform-provider-azurerm` repo](https://github.com/terraform-providers/terraform-provider-azurerm/issues).



<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#Account">class Account</a></li>
<li><a href="#getAccount">function getAccount</a></li>
<li><a href="#AccountArgs">interface AccountArgs</a></li>
<li><a href="#AccountState">interface AccountState</a></li>
<li><a href="#GetAccountArgs">interface GetAccountArgs</a></li>
<li><a href="#GetAccountResult">interface GetAccountResult</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts">maps/account.ts</a> <a href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts">maps/getAccount.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="Account">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L32">class <b>Account</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

Manages an Azure Maps Account.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const testResourceGroup = new azure.core.ResourceGroup("test", {
    location: "West Europe",
    name: "example-resources",
});
const testAccount = new azure.maps.Account("test", {
    name: "example-maps-account",
    resourceGroupName: testResourceGroup.name,
    skuName: "s1",
    tags: {
        environment: "Test",
    },
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/maps_account.html.markdown.

{{% /md %}}
<h3 class="pdoc-member-header" id="Account-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L86"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> Account(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#AccountArgs'>AccountArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>

{{% md %}}

Create a Account resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L41">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#AccountState'>AccountState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Account'>Account</a></pre>

{{% md %}}

Get an existing Account resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L32">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% md %}}
{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L52">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>

{{% md %}}

Returns true if the given object is an instance of Account.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L32">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L62">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Azure Maps Account. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-primaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L66">property <b>primaryAccessKey</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>primaryAccessKey: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The primary key used to authenticate and authorize access to the Maps REST APIs.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L70">property <b>resourceGroupName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>resourceGroupName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Resource Group in which the Azure Maps Account should exist. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-secondaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L74">property <b>secondaryAccessKey</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>secondaryAccessKey: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The secondary key used to authenticate and authorize access to the Maps REST APIs.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-skuName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L78">property <b>skuName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>skuName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The sku of the Azure Maps Account. Possible values are `s0` and `s1`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L82">property <b>tags</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>tags: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>}&gt;;</pre>
{{% md %}}

A mapping of tags to assign to the Azure Maps Account.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L32">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Account-xMsClientId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L86">property <b>xMsClientId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>xMsClientId: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

A unique identifier for the Maps Account.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="getAccount">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L26">function <b>getAccount</b></a>
</h2>
<div class="pdoc-module-contents">

<pre class="highlight"><span class='kd'></span>getAccount(args: <a href='#GetAccountArgs'>GetAccountArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetAccountResult'>GetAccountResult</a>&gt; &amp; <a href='#GetAccountResult'>GetAccountResult</a></pre>

{{% md %}}

Use this data source to access information about an existing Azure Maps Account.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const test = azure.maps.getAccount({
    name: "production",
    resourceGroupName: "maps",
});

export const mapsAccountId = test.id;
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/d/maps_account.html.markdown.

{{% /md %}}
</div>
<h2 class="pdoc-module-header" id="AccountArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L171">interface <b>AccountArgs</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

The set of arguments for constructing a Account resource.

{{% /md %}}
<h3 class="pdoc-member-header" id="AccountArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L175">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Azure Maps Account. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="AccountArgs-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L179">property <b>resourceGroupName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>resourceGroupName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Resource Group in which the Azure Maps Account should exist. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="AccountArgs-skuName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L183">property <b>skuName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>skuName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The sku of the Azure Maps Account. Possible values are `s0` and `s1`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="AccountArgs-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L187">property <b>tags</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>}&gt;;</pre>
{{% md %}}

A mapping of tags to assign to the Azure Maps Account.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="AccountState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L137">interface <b>AccountState</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

Input properties used for looking up and filtering Account resources.

{{% /md %}}
<h3 class="pdoc-member-header" id="AccountState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L141">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Azure Maps Account. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="AccountState-primaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L145">property <b>primaryAccessKey</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>primaryAccessKey?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The primary key used to authenticate and authorize access to the Maps REST APIs.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="AccountState-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L149">property <b>resourceGroupName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>resourceGroupName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Resource Group in which the Azure Maps Account should exist. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="AccountState-secondaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L153">property <b>secondaryAccessKey</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>secondaryAccessKey?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The secondary key used to authenticate and authorize access to the Maps REST APIs.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="AccountState-skuName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L157">property <b>skuName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>skuName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The sku of the Azure Maps Account. Possible values are `s0` and `s1`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="AccountState-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L161">property <b>tags</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>}&gt;;</pre>
{{% md %}}

A mapping of tags to assign to the Azure Maps Account.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="AccountState-xMsClientId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/account.ts#L165">property <b>xMsClientId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>xMsClientId?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

A unique identifier for the Maps Account.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="GetAccountArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L46">interface <b>GetAccountArgs</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

A collection of arguments for invoking getAccount.

{{% /md %}}
<h3 class="pdoc-member-header" id="GetAccountArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L50">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

Specifies the name of the Maps Account.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetAccountArgs-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L54">property <b>resourceGroupName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>resourceGroupName: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

Specifies the name of the Resource Group in which the Maps Account is located.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetAccountArgs-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L55">property <b>tags</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>tags?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | {[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>};</pre>
</div>
</div>
<h2 class="pdoc-module-header" id="GetAccountResult">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L61">interface <b>GetAccountResult</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

A collection of values returned by getAccount.

{{% /md %}}
<h3 class="pdoc-member-header" id="GetAccountResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L84">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetAccountResult-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L62">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="GetAccountResult-primaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L66">property <b>primaryAccessKey</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>primaryAccessKey: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

The primary key used to authenticate and authorize access to the Maps REST APIs.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetAccountResult-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L67">property <b>resourceGroupName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>resourceGroupName: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="GetAccountResult-secondaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L71">property <b>secondaryAccessKey</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>secondaryAccessKey: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

The primary key used to authenticate and authorize access to the Maps REST APIs. The second key is given to provide seamless key regeneration.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetAccountResult-skuName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L75">property <b>skuName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>skuName: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

The sku of the Azure Maps Account.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetAccountResult-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L76">property <b>tags</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>tags: {[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>};</pre>
</div>
<h3 class="pdoc-member-header" id="GetAccountResult-xMsClientId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/864ed91accb1f4f050abbb968cf0aae95f222f36/sdk/nodejs/maps/getAccount.ts#L80">property <b>xMsClientId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>xMsClientId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

A unique identifier for the Maps Account.

{{% /md %}}
</div>
</div>