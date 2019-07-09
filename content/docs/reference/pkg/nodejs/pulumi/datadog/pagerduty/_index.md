---
title: Module pagerduty
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../">@pulumi/datadog</a> &gt; pagerduty

> This provider is a derived work of the [Terraform Provider](https://github.com/terraform-providers/terraform-provider-datadog)
> distributed under [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/). If you encounter a bug or missing feature,
> first check the [`pulumi/pulumi-datadog` repo](https://github.com/pulumi/pulumi-datadog/issues); however, if that doesn't turn up anything,
> please consult the source [`terraform-providers/terraform-provider-datadog` repo](https://github.com/terraform-providers/terraform-provider-datadog/issues).



<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#Integration">class Integration</a></li>
<li><a href="#IntegrationArgs">interface IntegrationArgs</a></li>
<li><a href="#IntegrationState">interface IntegrationState</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts">pagerduty/integration.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="Integration">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L12">class <b>Integration</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

Provides a Datadog - PagerDuty resource. This can be used to create and manage Datadog - PagerDuty integration.

> This content is derived from https://github.com/terraform-providers/terraform-provider-datadog/blob/master/website/docs/r/integration_pagerduty.html.markdown.

{{% /md %}}
<h3 class="pdoc-member-header" id="Integration-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L54"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> Integration(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#IntegrationArgs'>IntegrationArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>


Create a Integration resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Integration-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L21">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#IntegrationState'>IntegrationState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Integration'>Integration</a></pre>


Get an existing Integration resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Integration-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L19">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Integration-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L32">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>


Returns true if the given object is an instance of Integration.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Integration-apiToken">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L42">property <b>apiToken</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>apiToken: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
{{% md %}}

Your PagerDuty API token.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Integration-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L187">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Integration-schedules">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L46">property <b>schedules</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>schedules: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[] | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
{{% md %}}

Array of your schedule URLs.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Integration-services">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L50">property <b>services</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>services: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{
    serviceKey: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;
    serviceName: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;
}[]&gt;;</pre>
{{% md %}}

Array of PagerDuty service objects.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Integration-subdomain">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L54">property <b>subdomain</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>subdomain: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Your PagerDuty account’s personalized subdomain name.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Integration-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L17">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="IntegrationArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L114">interface <b>IntegrationArgs</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

The set of arguments for constructing a Integration resource.

{{% /md %}}
<h3 class="pdoc-member-header" id="IntegrationArgs-apiToken">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L118">property <b>apiToken</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>apiToken?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Your PagerDuty API token.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="IntegrationArgs-schedules">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L122">property <b>schedules</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>schedules?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;[]&gt;;</pre>
{{% md %}}

Array of your schedule URLs.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="IntegrationArgs-services">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L126">property <b>services</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>services: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{
    serviceKey: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
    serviceName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
}&gt;[]&gt;;</pre>
{{% md %}}

Array of PagerDuty service objects.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="IntegrationArgs-subdomain">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L130">property <b>subdomain</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>subdomain: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Your PagerDuty account’s personalized subdomain name.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="IntegrationState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L92">interface <b>IntegrationState</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

Input properties used for looking up and filtering Integration resources.

{{% /md %}}
<h3 class="pdoc-member-header" id="IntegrationState-apiToken">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L96">property <b>apiToken</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>apiToken?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Your PagerDuty API token.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="IntegrationState-schedules">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L100">property <b>schedules</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>schedules?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;[]&gt;;</pre>
{{% md %}}

Array of your schedule URLs.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="IntegrationState-services">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L104">property <b>services</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>services?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{
    serviceKey: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
    serviceName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
}&gt;[]&gt;;</pre>
{{% md %}}

Array of PagerDuty service objects.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="IntegrationState-subdomain">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-datadog/blob/0127400decf44f1c0713cd7a31395750b862fb1d/sdk/nodejs/pagerduty/integration.ts#L108">property <b>subdomain</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>subdomain?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Your PagerDuty account’s personalized subdomain name.

{{% /md %}}
</div>
</div>