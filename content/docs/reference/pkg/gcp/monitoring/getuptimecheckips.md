
---
title: "GetUptimeCheckIPs"
title_tag: "Function GetUptimeCheckIPs | Module monitoring | Package GCP"
meta_desc: "Explore the GetUptimeCheckIPs function of the monitoring module, including examples, input properties, output properties, and supporting types. Returns the list of IP addresses that checkers run from. For more information see"
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Returns the list of IP addresses that checkers run from. For more information see
the [official documentation](https://cloud.google.com/monitoring/uptime-checks#get-ips).


{{% examples %}}
## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}

{{% example csharp %}}
```csharp
using Pulumi;
using Gcp = Pulumi.Gcp;

class MyStack : Stack
{
    public MyStack()
    {
        var ips = Output.Create(Gcp.Monitoring.GetUptimeCheckIPs.InvokeAsync());
        this.IpList = ips.Apply(ips => ips.UptimeCheckIps);
    }

    [Output("ipList")]
    public Output<string> IpList { get; set; }
}
```
{{% /example %}}

{{% example go %}}
Coming soon!
{{% /example %}}

{{% example python %}}
```python
import pulumi
import pulumi_gcp as gcp

ips = gcp.monitoring.get_uptime_check_i_ps()
pulumi.export("ipList", ips.uptime_check_ips)
```
{{% /example %}}

{{% example typescript %}}
```typescript
import * as pulumi from "@pulumi/pulumi";
import * as gcp from "@pulumi/gcp";

const ips = gcp.monitoring.getUptimeCheckIPs({});
export const ipList = ips.then(ips => ips.uptimeCheckIps);
```
{{% /example %}}

{{% /examples %}}


## Using GetUptimeCheckIPs {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getUptimeCheckIPs<span class="p">(</span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gcp/monitoring/#GetUptimeCheckIPsResult">GetUptimeCheckIPsResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_uptime_check_i_ps(</span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetUptimeCheckIPs<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/v3/go/gcp/monitoring?tab=doc#GetUptimeCheckIPsResult">GetUptimeCheckIPsResult</a></span>, error)</span></code></pre></div>

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetUptimeCheckIPs </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Monitoring.GetUptimeCheckIPsResult.html">GetUptimeCheckIPsResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}




## GetUptimeCheckIPs Result {#result}

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="uptimecheckips_csharp">
<a href="#uptimecheckips_csharp" style="color: inherit; text-decoration: inherit;">Uptime<wbr>Check<wbr>Ips</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getuptimecheckipsuptimecheckip">List&lt;Get<wbr>Uptime<wbr>Check<wbr>IPs<wbr>Uptime<wbr>Check<wbr>Ip&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of uptime check IPs used by Stackdriver Monitoring. Each `uptime_check_ip` contains:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="uptimecheckips_go">
<a href="#uptimecheckips_go" style="color: inherit; text-decoration: inherit;">Uptime<wbr>Check<wbr>Ips</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getuptimecheckipsuptimecheckip">[]Get<wbr>Uptime<wbr>Check<wbr>IPs<wbr>Uptime<wbr>Check<wbr>Ip</a></span>
    </dt>
    <dd>{{% md %}}A list of uptime check IPs used by Stackdriver Monitoring. Each `uptime_check_ip` contains:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="uptimecheckips_nodejs">
<a href="#uptimecheckips_nodejs" style="color: inherit; text-decoration: inherit;">uptime<wbr>Check<wbr>Ips</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getuptimecheckipsuptimecheckip">Get<wbr>Uptime<wbr>Check<wbr>IPs<wbr>Uptime<wbr>Check<wbr>Ip[]</a></span>
    </dt>
    <dd>{{% md %}}A list of uptime check IPs used by Stackdriver Monitoring. Each `uptime_check_ip` contains:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="uptime_check_ips_python">
<a href="#uptime_check_ips_python" style="color: inherit; text-decoration: inherit;">uptime_<wbr>check_<wbr>ips</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getuptimecheckipsuptimecheckip">List[Get<wbr>Uptime<wbr>Check<wbr>IPs<wbr>Uptime<wbr>Check<wbr>Ip]</a></span>
    </dt>
    <dd>{{% md %}}A list of uptime check IPs used by Stackdriver Monitoring. Each `uptime_check_ip` contains:
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Supporting Types


<h4 id="getuptimecheckipsuptimecheckip">Get<wbr>Uptime<wbr>Check<wbr>IPs<wbr>Uptime<wbr>Check<wbr>Ip</h4>
{{% choosable language nodejs %}}
> See the   <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/output/#GetUptimeCheckIPsUptimeCheckIp">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the   <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/v3/go/gcp/monitoring?tab=doc#GetUptimeCheckIPsUptimeCheckIp">output</a> API doc for this type.
{{% /choosable %}}
{{% choosable language csharp %}}
> See the   <a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Monitoring.Outputs.GetUptimeCheckIPsUptimeCheckIp.html">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="ipaddress_csharp">
<a href="#ipaddress_csharp" style="color: inherit; text-decoration: inherit;">Ip<wbr>Address</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The IP address from which the Uptime check originates. This is a fully specified IP address
(not an IP address range). Most IP addresses, as of this publication, are in IPv4 format; however, one should not
rely on the IP addresses being in IPv4 format indefinitely, and should support interpreting this field in either
IPv4 or IPv6 format.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}A more specific location within the region that typically encodes a particular city/town/metro
(and its containing state/province or country) within the broader umbrella region category.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="region_csharp">
<a href="#region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}A broad region category in which the IP address is located.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="ipaddress_go">
<a href="#ipaddress_go" style="color: inherit; text-decoration: inherit;">Ip<wbr>Address</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The IP address from which the Uptime check originates. This is a fully specified IP address
(not an IP address range). Most IP addresses, as of this publication, are in IPv4 format; however, one should not
rely on the IP addresses being in IPv4 format indefinitely, and should support interpreting this field in either
IPv4 or IPv6 format.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}A more specific location within the region that typically encodes a particular city/town/metro
(and its containing state/province or country) within the broader umbrella region category.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="region_go">
<a href="#region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}A broad region category in which the IP address is located.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="ipaddress_nodejs">
<a href="#ipaddress_nodejs" style="color: inherit; text-decoration: inherit;">ip<wbr>Address</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The IP address from which the Uptime check originates. This is a fully specified IP address
(not an IP address range). Most IP addresses, as of this publication, are in IPv4 format; however, one should not
rely on the IP addresses being in IPv4 format indefinitely, and should support interpreting this field in either
IPv4 or IPv6 format.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}A more specific location within the region that typically encodes a particular city/town/metro
(and its containing state/province or country) within the broader umbrella region category.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="region_nodejs">
<a href="#region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}A broad region category in which the IP address is located.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span id="ip_address_python">
<a href="#ip_address_python" style="color: inherit; text-decoration: inherit;">ip_<wbr>address</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The IP address from which the Uptime check originates. This is a fully specified IP address
(not an IP address range). Most IP addresses, as of this publication, are in IPv4 format; however, one should not
rely on the IP addresses being in IPv4 format indefinitely, and should support interpreting this field in either
IPv4 or IPv6 format.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}A more specific location within the region that typically encodes a particular city/town/metro
(and its containing state/province or country) within the broader umbrella region category.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span id="region_python">
<a href="#region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}A broad region category in which the IP address is located.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-gcp">https://github.com/pulumi/pulumi-gcp</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>This Pulumi package is based on the [`google-beta` Terraform Provider](https://github.com/terraform-providers/terraform-provider-google-beta).</dd>
</dl>

