
---
title: "IApp"
block_external_search_index: true
---



`f5bigip.sys.IApp` resource helps you to deploy Application Services template that can be used to automate and orchestrate Layer 4-7 applications service deployments using F5 Network.  

## Example Usage of Json file

```typescript
import * as pulumi from "@pulumi/pulumi";
```

 * `description` - User defined description.
 * `deviceGroup` - The name of the device group that the application service is assigned to.
 * `executeAction` - Run the specified template action associated with the application.
 * `inheritedDevicegroup`- Read-only. Shows whether the application folder will automatically remain with the same device-group as its parent folder. Use 'device-group default' or 'device-group non-default' to set this.
 * `inheritedTrafficGroup` - Read-only. Shows whether the application folder will automatically remain with the same traffic-group as its parent folder. Use 'traffic-group default' or 'traffic-group non-default' to set this.
 * `partition` - Displays the administrative partition within which the application resides.
 * `strictUpdates` - Specifies whether configuration objects contained in the application may be directly modified, outside the context of the system's application management interfaces.
 * `template` - The template defines the configuration for the application. This may be changed after the application has been created to move the application to a new template.
 * `templateModified` - Indicates that the application template used to deploy the application has been modified. The application should be updated to make use of the latest changes.
 * `templatePrerequisiteErrors` - Indicates any missing prerequisites associated with the template that defines this application.
 * `trafficGroup` - The name of the traffic group that the application service is assigned to.
 * `lists` - string values
 * `metadata` - User defined generic data for the application service. It is a name and value pair.
 * `tables` - Values provided like pool name, nodes etc.
 * `variables` - Name, values, encrypted or not

> This content is derived from https://github.com/terraform-providers/terraform-provider-bigip/blob/master/website/docs/r/bigip_sys_iapp.html.markdown.



## Create a IApp Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/sys/#IApp">IApp</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/sys/#IAppArgs">IAppArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">IApp</span><span class="p">(resource_name, opts=None, </span>description=None<span class="p">, </span>devicegroup=None<span class="p">, </span>execute_action=None<span class="p">, </span>inherited_devicegroup=None<span class="p">, </span>inherited_traffic_group=None<span class="p">, </span>jsonfile=None<span class="p">, </span>lists=None<span class="p">, </span>metadatas=None<span class="p">, </span>name=None<span class="p">, </span>partition=None<span class="p">, </span>strict_updates=None<span class="p">, </span>tables=None<span class="p">, </span>template=None<span class="p">, </span>template_modified=None<span class="p">, </span>template_prerequisite_errors=None<span class="p">, </span>traffic_group=None<span class="p">, </span>variables=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewIApp<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppArgs">IAppArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IApp">IApp</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.F5bigip/Pulumi.F5bigip.Sys.IApp.html">IApp</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.F5bigip/Pulumi.F5bigip.Sys.IAppArgs.html">IAppArgs</a></span>? <span class="nx">args = null<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

#### Resource Arguments




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Execute<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inherited<wbr>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inherited<wbr>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">List&lt;IApp<wbr>List<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">List&lt;IApp<wbr>Metadata<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strict<wbr>Updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">List&lt;IApp<wbr>Table<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template<wbr>Modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template<wbr>Prerequisite<wbr>Errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">List&lt;IApp<wbr>Variable<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Execute<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inherited<wbr>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inherited<wbr>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">[]IApp<wbr>List</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">[]IApp<wbr>Metadata</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strict<wbr>Updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">[]IApp<wbr>Table</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template<wbr>Modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template<wbr>Prerequisite<wbr>Errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">[]IApp<wbr>Variable</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>execute<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inherited<wbr>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inherited<wbr>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">IApp<wbr>List[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">IApp<wbr>Metadata[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strict<wbr>Updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">IApp<wbr>Table[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template<wbr>Modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template<wbr>Prerequisite<wbr>Errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">IApp<wbr>Variable[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>execute_<wbr>action</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inherited_<wbr>devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inherited_<wbr>traffic_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">List[IApp<wbr>List]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">List[IApp<wbr>Metadata]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strict_<wbr>updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">List[IApp<wbr>Table]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template_<wbr>modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template_<wbr>prerequisite_<wbr>errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>traffic_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">List[IApp<wbr>Variable]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## IApp Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Execute<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Inherited<wbr>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Inherited<wbr>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">List&lt;IApp<wbr>List&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">List&lt;IApp<wbr>Metadata&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Strict<wbr>Updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">List&lt;IApp<wbr>Table&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Template<wbr>Modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Template<wbr>Prerequisite<wbr>Errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">List&lt;IApp<wbr>Variable&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Execute<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Inherited<wbr>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Inherited<wbr>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">[]IApp<wbr>List</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">[]IApp<wbr>Metadata</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Strict<wbr>Updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">[]IApp<wbr>Table</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Template<wbr>Modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Template<wbr>Prerequisite<wbr>Errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">[]IApp<wbr>Variable</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>execute<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>inherited<wbr>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>inherited<wbr>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">IApp<wbr>List[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">IApp<wbr>Metadata[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>strict<wbr>Updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">IApp<wbr>Table[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>template</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>template<wbr>Modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>template<wbr>Prerequisite<wbr>Errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">IApp<wbr>Variable[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>execute_<wbr>action</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>inherited_<wbr>devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>inherited_<wbr>traffic_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">List[IApp<wbr>List]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">List[IApp<wbr>Metadata]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>strict_<wbr>updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">List[IApp<wbr>Table]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>template</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>template_<wbr>modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>template_<wbr>prerequisite_<wbr>errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>traffic_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">List[IApp<wbr>Variable]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing IApp Resource

Get an existing IApp resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/sys/#IAppState">IAppState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/sys/#IApp">IApp</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>description=None<span class="p">, </span>devicegroup=None<span class="p">, </span>execute_action=None<span class="p">, </span>inherited_devicegroup=None<span class="p">, </span>inherited_traffic_group=None<span class="p">, </span>jsonfile=None<span class="p">, </span>lists=None<span class="p">, </span>metadatas=None<span class="p">, </span>name=None<span class="p">, </span>partition=None<span class="p">, </span>strict_updates=None<span class="p">, </span>tables=None<span class="p">, </span>template=None<span class="p">, </span>template_modified=None<span class="p">, </span>template_prerequisite_errors=None<span class="p">, </span>traffic_group=None<span class="p">, </span>variables=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetIApp<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppState">IAppState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IApp">IApp</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.F5bigip/Pulumi.F5bigip.Sys.IApp.html">IApp</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.F5bigip/Pulumi.F5bigip.Sys.IAppState.html">IAppState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Execute<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inherited<wbr>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inherited<wbr>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">List&lt;IApp<wbr>List<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">List&lt;IApp<wbr>Metadata<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strict<wbr>Updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">List&lt;IApp<wbr>Table<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template<wbr>Modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template<wbr>Prerequisite<wbr>Errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">List&lt;IApp<wbr>Variable<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Execute<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inherited<wbr>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Inherited<wbr>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">[]IApp<wbr>List</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">[]IApp<wbr>Metadata</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Strict<wbr>Updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">[]IApp<wbr>Table</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template<wbr>Modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Template<wbr>Prerequisite<wbr>Errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">[]IApp<wbr>Variable</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>execute<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inherited<wbr>Devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inherited<wbr>Traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">IApp<wbr>List[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">IApp<wbr>Metadata[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strict<wbr>Updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">IApp<wbr>Table[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template<wbr>Modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template<wbr>Prerequisite<wbr>Errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>traffic<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">IApp<wbr>Variable[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>execute_<wbr>action</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inherited_<wbr>devicegroup</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>inherited_<wbr>traffic_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>jsonfile</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Refer to the Json file which will be deployed on F5 BIG-IP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>lists</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapplist">List[IApp<wbr>List]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metadatas</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappmetadata">List[IApp<wbr>Metadata]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>partition</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Address of the Iapp which needs to be Iappensed
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>strict_<wbr>updates</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptable">List[IApp<wbr>Table]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template_<wbr>modified</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>template_<wbr>prerequisite_<wbr>errors</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>traffic_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}BIG-IP password
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>variables</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iappvariable">List[IApp<wbr>Variable]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>IApp<wbr>List</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/input/#IAppList">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/output/#IAppList">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppListArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppListOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>IApp<wbr>Metadata</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/input/#IAppMetadata">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/output/#IAppMetadata">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppMetadataArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppMetadataOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Persists</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Persists</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>persists</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>persists</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>IApp<wbr>Table</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/input/#IAppTable">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/output/#IAppTable">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppTableArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppTableOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Column<wbr>Names</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Encrypted<wbr>Columns</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rows</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptablerow">List&lt;IApp<wbr>Table<wbr>Row<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Column<wbr>Names</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Encrypted<wbr>Columns</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rows</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptablerow">[]IApp<wbr>Table<wbr>Row</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>column<wbr>Names</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>encrypted<wbr>Columns</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rows</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptablerow">IApp<wbr>Table<wbr>Row[]?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>column<wbr>Names</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>encrypted<wbr>Columns</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rows</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#iapptablerow">List[IApp<wbr>Table<wbr>Row]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>IApp<wbr>Table<wbr>Row</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/input/#IAppTableRow">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/output/#IAppTableRow">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppTableRowArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppTableRowOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Rows</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Rows</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>rows</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>rows</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>IApp<wbr>Variable</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/input/#IAppVariable">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/f5bigip/types/output/#IAppVariable">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppVariableArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-f5bigip/sdk/go/f5bigip/sys?tab=doc#IAppVariableOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>encrypted</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the iApp.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-f5bigip">https://github.com/pulumi/pulumi-f5bigip</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>
