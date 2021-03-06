
---
title: "GetSaml"
title_tag: "Function GetSaml | Module idp | Package Okta"
meta_desc: "Explore the GetSaml function of the idp module, including examples, input properties, output properties, and supporting types. Use this data source to retrieve a SAML IdP from Okta."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to retrieve a SAML IdP from Okta.



{{% examples %}}
## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}

{{% example csharp %}}
```csharp
using Pulumi;
using Okta = Pulumi.Okta;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(Okta.Idp.GetSaml.InvokeAsync(new Okta.Idp.GetSamlArgs
        {
            Label = "Example App",
        }));
    }

}
```
{{% /example %}}

{{% example go %}}
Coming soon!
{{% /example %}}

{{% example python %}}
```python
import pulumi
import pulumi_okta as okta

example = okta.idp.get_saml(label="Example App")
```
{{% /example %}}

{{% example typescript %}}
```typescript
import * as pulumi from "@pulumi/pulumi";
import * as okta from "@pulumi/okta";

const example = pulumi.output(okta.idp.getSaml({
    label: "Example App",
}, { async: true }));
```
{{% /example %}}

{{% /examples %}}


## Using GetSaml {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getSaml<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/idp/#GetSamlArgs">GetSamlArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/idp/#GetSamlResult">GetSamlResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">function </span> get_saml(</span>id=None<span class="p">, </span>name=None<span class="p">, </span>opts=None<span class="p">)</span></code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupSaml<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">args</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/v2/go/okta/idp?tab=doc#LookupSamlArgs">LookupSamlArgs</a></span><span class="p">, </span><span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v2/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/v2/go/okta/idp?tab=doc#LookupSamlResult">LookupSamlResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupSaml` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetSaml </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.Idp.GetSamlResult.html">GetSamlResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.Idp.GetSamlArgs.html">GetSamlArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The id of the idp to retrieve, conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the idp to retrieve, conflicts with `id`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The id of the idp to retrieve, conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the idp to retrieve, conflicts with `id`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The id of the idp to retrieve, conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}The name of the idp to retrieve, conflicts with `id`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The id of the idp to retrieve, conflicts with `name`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}The name of the idp to retrieve, conflicts with `id`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## GetSaml Result {#result}

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="acsbinding_csharp">
<a href="#acsbinding_csharp" style="color: inherit; text-decoration: inherit;">Acs<wbr>Binding</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}HTTP binding used to receive a SAMLResponse message from the IdP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="acstype_csharp">
<a href="#acstype_csharp" style="color: inherit; text-decoration: inherit;">Acs<wbr>Type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}Determines whether to publish an instance-specific (trust) or organization (shared) ACS endpoint in the SAML metadata.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="audience_csharp">
<a href="#audience_csharp" style="color: inherit; text-decoration: inherit;">Audience</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}URI that identifies the target Okta IdP instance (SP)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="issuer_csharp">
<a href="#issuer_csharp" style="color: inherit; text-decoration: inherit;">Issuer</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}URI that identifies the issuer (IdP).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="issuermode_csharp">
<a href="#issuermode_csharp" style="color: inherit; text-decoration: inherit;">Issuer<wbr>Mode</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}indicates whether Okta uses the original Okta org domain URL, or a custom domain URL in the request to the IdP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="kid_csharp">
<a href="#kid_csharp" style="color: inherit; text-decoration: inherit;">Kid</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}Key ID reference to the IdP's X.509 signature certificate.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="ssobinding_csharp">
<a href="#ssobinding_csharp" style="color: inherit; text-decoration: inherit;">Sso<wbr>Binding</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}single sign on binding.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="ssodestination_csharp">
<a href="#ssodestination_csharp" style="color: inherit; text-decoration: inherit;">Sso<wbr>Destination</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}SSO request binding, HTTP-POST or HTTP-REDIRECT.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="ssourl_csharp">
<a href="#ssourl_csharp" style="color: inherit; text-decoration: inherit;">Sso<wbr>Url</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}single sign on url.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="subjectfilter_csharp">
<a href="#subjectfilter_csharp" style="color: inherit; text-decoration: inherit;">Subject<wbr>Filter</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}regular expression pattern used to filter untrusted IdP usernames.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="subjectformats_csharp">
<a href="#subjectformats_csharp" style="color: inherit; text-decoration: inherit;">Subject<wbr>Formats</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">List&lt;string&gt;</a></span>
    </dt>
    <dd>{{% md %}}Expression to generate or transform a unique username for the IdP user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}type of idp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}id of idp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span>
    </dt>
    <dd>{{% md %}}name of the idp.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="acsbinding_go">
<a href="#acsbinding_go" style="color: inherit; text-decoration: inherit;">Acs<wbr>Binding</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}HTTP binding used to receive a SAMLResponse message from the IdP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="acstype_go">
<a href="#acstype_go" style="color: inherit; text-decoration: inherit;">Acs<wbr>Type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}Determines whether to publish an instance-specific (trust) or organization (shared) ACS endpoint in the SAML metadata.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="audience_go">
<a href="#audience_go" style="color: inherit; text-decoration: inherit;">Audience</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}URI that identifies the target Okta IdP instance (SP)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="issuer_go">
<a href="#issuer_go" style="color: inherit; text-decoration: inherit;">Issuer</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}URI that identifies the issuer (IdP).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="issuermode_go">
<a href="#issuermode_go" style="color: inherit; text-decoration: inherit;">Issuer<wbr>Mode</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}indicates whether Okta uses the original Okta org domain URL, or a custom domain URL in the request to the IdP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="kid_go">
<a href="#kid_go" style="color: inherit; text-decoration: inherit;">Kid</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}Key ID reference to the IdP's X.509 signature certificate.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="ssobinding_go">
<a href="#ssobinding_go" style="color: inherit; text-decoration: inherit;">Sso<wbr>Binding</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}single sign on binding.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="ssodestination_go">
<a href="#ssodestination_go" style="color: inherit; text-decoration: inherit;">Sso<wbr>Destination</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}SSO request binding, HTTP-POST or HTTP-REDIRECT.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="ssourl_go">
<a href="#ssourl_go" style="color: inherit; text-decoration: inherit;">Sso<wbr>Url</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}single sign on url.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="subjectfilter_go">
<a href="#subjectfilter_go" style="color: inherit; text-decoration: inherit;">Subject<wbr>Filter</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}regular expression pattern used to filter untrusted IdP usernames.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="subjectformats_go">
<a href="#subjectformats_go" style="color: inherit; text-decoration: inherit;">Subject<wbr>Formats</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">[]string</a></span>
    </dt>
    <dd>{{% md %}}Expression to generate or transform a unique username for the IdP user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}type of idp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}id of idp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://golang.org/pkg/builtin/#string">string</a></span>
    </dt>
    <dd>{{% md %}}name of the idp.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="acsbinding_nodejs">
<a href="#acsbinding_nodejs" style="color: inherit; text-decoration: inherit;">acs<wbr>Binding</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}HTTP binding used to receive a SAMLResponse message from the IdP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="acstype_nodejs">
<a href="#acstype_nodejs" style="color: inherit; text-decoration: inherit;">acs<wbr>Type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}Determines whether to publish an instance-specific (trust) or organization (shared) ACS endpoint in the SAML metadata.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="audience_nodejs">
<a href="#audience_nodejs" style="color: inherit; text-decoration: inherit;">audience</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}URI that identifies the target Okta IdP instance (SP)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="issuer_nodejs">
<a href="#issuer_nodejs" style="color: inherit; text-decoration: inherit;">issuer</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}URI that identifies the issuer (IdP).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="issuermode_nodejs">
<a href="#issuermode_nodejs" style="color: inherit; text-decoration: inherit;">issuer<wbr>Mode</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}indicates whether Okta uses the original Okta org domain URL, or a custom domain URL in the request to the IdP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="kid_nodejs">
<a href="#kid_nodejs" style="color: inherit; text-decoration: inherit;">kid</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}Key ID reference to the IdP's X.509 signature certificate.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="ssobinding_nodejs">
<a href="#ssobinding_nodejs" style="color: inherit; text-decoration: inherit;">sso<wbr>Binding</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}single sign on binding.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="ssodestination_nodejs">
<a href="#ssodestination_nodejs" style="color: inherit; text-decoration: inherit;">sso<wbr>Destination</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}SSO request binding, HTTP-POST or HTTP-REDIRECT.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="ssourl_nodejs">
<a href="#ssourl_nodejs" style="color: inherit; text-decoration: inherit;">sso<wbr>Url</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}single sign on url.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="subjectfilter_nodejs">
<a href="#subjectfilter_nodejs" style="color: inherit; text-decoration: inherit;">subject<wbr>Filter</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}regular expression pattern used to filter untrusted IdP usernames.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="subjectformats_nodejs">
<a href="#subjectformats_nodejs" style="color: inherit; text-decoration: inherit;">subject<wbr>Formats</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string[]</a></span>
    </dt>
    <dd>{{% md %}}Expression to generate or transform a unique username for the IdP user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}type of idp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}id of idp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span>
    </dt>
    <dd>{{% md %}}name of the idp.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span id="acs_binding_python">
<a href="#acs_binding_python" style="color: inherit; text-decoration: inherit;">acs_<wbr>binding</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}HTTP binding used to receive a SAMLResponse message from the IdP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="acs_type_python">
<a href="#acs_type_python" style="color: inherit; text-decoration: inherit;">acs_<wbr>type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}Determines whether to publish an instance-specific (trust) or organization (shared) ACS endpoint in the SAML metadata.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="audience_python">
<a href="#audience_python" style="color: inherit; text-decoration: inherit;">audience</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}URI that identifies the target Okta IdP instance (SP)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="issuer_python">
<a href="#issuer_python" style="color: inherit; text-decoration: inherit;">issuer</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}URI that identifies the issuer (IdP).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="issuer_mode_python">
<a href="#issuer_mode_python" style="color: inherit; text-decoration: inherit;">issuer_<wbr>mode</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}indicates whether Okta uses the original Okta org domain URL, or a custom domain URL in the request to the IdP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="kid_python">
<a href="#kid_python" style="color: inherit; text-decoration: inherit;">kid</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}Key ID reference to the IdP's X.509 signature certificate.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="sso_binding_python">
<a href="#sso_binding_python" style="color: inherit; text-decoration: inherit;">sso_<wbr>binding</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}single sign on binding.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="sso_destination_python">
<a href="#sso_destination_python" style="color: inherit; text-decoration: inherit;">sso_<wbr>destination</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}SSO request binding, HTTP-POST or HTTP-REDIRECT.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="sso_url_python">
<a href="#sso_url_python" style="color: inherit; text-decoration: inherit;">sso_<wbr>url</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}single sign on url.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="subject_filter_python">
<a href="#subject_filter_python" style="color: inherit; text-decoration: inherit;">subject_<wbr>filter</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}regular expression pattern used to filter untrusted IdP usernames.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="subject_formats_python">
<a href="#subject_formats_python" style="color: inherit; text-decoration: inherit;">subject_<wbr>formats</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">List[str]</a></span>
    </dt>
    <dd>{{% md %}}Expression to generate or transform a unique username for the IdP user.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}type of idp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}id of idp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span> 
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://docs.python.org/3/library/stdtypes.html">str</a></span>
    </dt>
    <dd>{{% md %}}name of the idp.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-okta">https://github.com/pulumi/pulumi-okta</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>This Pulumi package is based on the [`okta` Terraform Provider](https://github.com/articulate/terraform-provider-okta).</dd>
</dl>

