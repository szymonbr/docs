---
title: "Module cognitive"
title_tag: "Module cognitive | Package @pulumi/azure | Node.js SDK"
linktitle: "cognitive"
meta_desc: "Explore members of the cognitive module in the @pulumi/azure package."
git_sha: "38f39deade34d0e187626f1cb68bf0835bc2c2d0"
block_external_search_index: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

{{< resource-docs-alert "azure" >}}




<h3>Resources</h3>
<ul class="api">
    <li><a href="#Account"><span class="symbol resource"></span>Account</a></li>
</ul>


<h3>Others</h3>
<ul class="api">
    <li><a href="#AccountArgs"><span class="symbol api"></span>AccountArgs</a></li>
    <li><a href="#AccountState"><span class="symbol api"></span>AccountState</a></li>
</ul>


<h2 id="resources">Resources</h2>
<h3 class="pdoc-module-header" id="Account" data-link-title="Account">
    <a href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L30">
        Resource <strong>Account</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>class</span> <span class='nx'>Account</span> <span class='kr'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></code></pre>

Manages a Cognitive Services Account.

#### Example Usage



```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const exampleResourceGroup = new azure.core.ResourceGroup("exampleResourceGroup", {location: "West Europe"});
const exampleAccount = new azure.cognitive.Account("exampleAccount", {
    location: exampleResourceGroup.location,
    resourceGroupName: exampleResourceGroup.name,
    kind: "Face",
    skuName: "S0",
    tags: {
        Acceptance: "Test",
    },
});
```

<h4 class="pdoc-member-header" id="Account-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L97"> <b>constructor</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span><span class='kd'>new</span> Account(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#AccountArgs'>AccountArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</code></pre>


Create a Account resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h4 class="pdoc-member-header" id="Account-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L40">method <b>get</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#AccountState'>AccountState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Account'>Account</a></code></pre>


Get an existing Account resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h4 class="pdoc-member-header" id="Account-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L30">method <b>getProvider</b></a>
</h4>


<pre class="highlight"><code><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ProviderResource'>ProviderResource</a> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></code></pre>

<h4 class="pdoc-member-header" id="Account-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L51">method <b>isInstance</b></a>
</h4>


<pre class="highlight"><code><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): obj is Account</code></pre>


Returns true if the given object is an instance of Account.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

<h4 class="pdoc-member-header" id="Account-endpoint">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L61">property <b>endpoint</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>endpoint: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The endpoint used to connect to the Cognitive Service Account.

<h4 class="pdoc-member-header" id="Account-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L30">property <b>id</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</code></pre>

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h4 class="pdoc-member-header" id="Account-kind">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L65">property <b>kind</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>kind: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the type of Cognitive Service Account that should be created. Possible values are `Academic`, `Bing.Autosuggest`, `Bing.Autosuggest.v7`, `Bing.CustomSearch`, `Bing.Search`, `Bing.Search.v7`, `Bing.Speech`, `Bing.SpellCheck`, `Bing.SpellCheck.v7`, `CognitiveServices`, `ComputerVision`, `ContentModerator`, `CustomSpeech`, `CustomVision.Prediction`, `CustomVision.Training`, `Emotion`, `Face`,`FormRecognizer`, `ImmersiveReader`, `LUIS`, `LUIS.Authoring`, `QnAMaker`, `Recommendations`, `SpeakerRecognition`, `Speech`, `SpeechServices`, `SpeechTranslation`, `TextAnalytics`, `TextTranslation` and `WebLM`. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="Account-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L69">property <b>location</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>location: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="Account-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L73">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the name of the Cognitive Service Account. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="Account-primaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L77">property <b>primaryAccessKey</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>primaryAccessKey: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

A primary access key which can be used to connect to the Cognitive Service Account.

<h4 class="pdoc-member-header" id="Account-qnaRuntimeEndpoint">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L81">property <b>qnaRuntimeEndpoint</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>qnaRuntimeEndpoint: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

A URL to link a QnAMaker cognitive account to a QnA runtime.

<h4 class="pdoc-member-header" id="Account-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L85">property <b>resourceGroupName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>resourceGroupName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the resource group in which the Cognitive Service Account is created. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="Account-secondaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L89">property <b>secondaryAccessKey</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>secondaryAccessKey: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The secondary access key which can be used to connect to the Cognitive Service Account.

<h4 class="pdoc-member-header" id="Account-skuName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L93">property <b>skuName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>skuName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the SKU Name for this Cognitive Service Account. Possible values are `F0`, `F1`, `S0`, `S1`, `S2`, `S3`, `S4`, `S5`, `S6`, `P0`, `P1`, and `P2`.

<h4 class="pdoc-member-header" id="Account-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L97">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'>public </span>tags: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>} | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</code></pre>

A mapping of tags to assign to the resource.

<h4 class="pdoc-member-header" id="Account-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L30">property <b>urn</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</code></pre>

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.



<h2 id="apis">Others</h2>
<h3 class="pdoc-module-header" id="AccountArgs" data-link-title="AccountArgs">
    <a href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L203">
        interface <strong>AccountArgs</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>AccountArgs</span></code></pre>

The set of arguments for constructing a Account resource.

<h4 class="pdoc-member-header" id="AccountArgs-kind">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L207">property <b>kind</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>kind: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the type of Cognitive Service Account that should be created. Possible values are `Academic`, `Bing.Autosuggest`, `Bing.Autosuggest.v7`, `Bing.CustomSearch`, `Bing.Search`, `Bing.Search.v7`, `Bing.Speech`, `Bing.SpellCheck`, `Bing.SpellCheck.v7`, `CognitiveServices`, `ComputerVision`, `ContentModerator`, `CustomSpeech`, `CustomVision.Prediction`, `CustomVision.Training`, `Emotion`, `Face`,`FormRecognizer`, `ImmersiveReader`, `LUIS`, `LUIS.Authoring`, `QnAMaker`, `Recommendations`, `SpeakerRecognition`, `Speech`, `SpeechServices`, `SpeechTranslation`, `TextAnalytics`, `TextTranslation` and `WebLM`. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="AccountArgs-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L211">property <b>location</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>location?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="AccountArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L215">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the name of the Cognitive Service Account. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="AccountArgs-qnaRuntimeEndpoint">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L219">property <b>qnaRuntimeEndpoint</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>qnaRuntimeEndpoint?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

A URL to link a QnAMaker cognitive account to a QnA runtime.

<h4 class="pdoc-member-header" id="AccountArgs-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L223">property <b>resourceGroupName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>resourceGroupName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the resource group in which the Cognitive Service Account is created. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="AccountArgs-skuName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L227">property <b>skuName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>skuName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the SKU Name for this Cognitive Service Account. Possible values are `F0`, `F1`, `S0`, `S1`, `S2`, `S3`, `S4`, `S5`, `S6`, `P0`, `P1`, and `P2`.

<h4 class="pdoc-member-header" id="AccountArgs-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L231">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;}&gt;;</code></pre>

A mapping of tags to assign to the resource.

<h3 class="pdoc-module-header" id="AccountState" data-link-title="AccountState">
    <a href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L157">
        interface <strong>AccountState</strong>
    </a>
</h3>

<pre class="highlight"><code><span class='kr'>interface</span> <span class='nx'>AccountState</span></code></pre>

Input properties used for looking up and filtering Account resources.

<h4 class="pdoc-member-header" id="AccountState-endpoint">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L161">property <b>endpoint</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>endpoint?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The endpoint used to connect to the Cognitive Service Account.

<h4 class="pdoc-member-header" id="AccountState-kind">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L165">property <b>kind</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>kind?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the type of Cognitive Service Account that should be created. Possible values are `Academic`, `Bing.Autosuggest`, `Bing.Autosuggest.v7`, `Bing.CustomSearch`, `Bing.Search`, `Bing.Search.v7`, `Bing.Speech`, `Bing.SpellCheck`, `Bing.SpellCheck.v7`, `CognitiveServices`, `ComputerVision`, `ContentModerator`, `CustomSpeech`, `CustomVision.Prediction`, `CustomVision.Training`, `Emotion`, `Face`,`FormRecognizer`, `ImmersiveReader`, `LUIS`, `LUIS.Authoring`, `QnAMaker`, `Recommendations`, `SpeakerRecognition`, `Speech`, `SpeechServices`, `SpeechTranslation`, `TextAnalytics`, `TextTranslation` and `WebLM`. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="AccountState-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L169">property <b>location</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>location?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the supported Azure location where the resource exists. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="AccountState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L173">property <b>name</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the name of the Cognitive Service Account. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="AccountState-primaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L177">property <b>primaryAccessKey</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>primaryAccessKey?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

A primary access key which can be used to connect to the Cognitive Service Account.

<h4 class="pdoc-member-header" id="AccountState-qnaRuntimeEndpoint">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L181">property <b>qnaRuntimeEndpoint</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>qnaRuntimeEndpoint?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

A URL to link a QnAMaker cognitive account to a QnA runtime.

<h4 class="pdoc-member-header" id="AccountState-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L185">property <b>resourceGroupName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>resourceGroupName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The name of the resource group in which the Cognitive Service Account is created. Changing this forces a new resource to be created.

<h4 class="pdoc-member-header" id="AccountState-secondaryAccessKey">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L189">property <b>secondaryAccessKey</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>secondaryAccessKey?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

The secondary access key which can be used to connect to the Cognitive Service Account.

<h4 class="pdoc-member-header" id="AccountState-skuName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L193">property <b>skuName</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>skuName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</code></pre>

Specifies the SKU Name for this Cognitive Service Account. Possible values are `F0`, `F1`, `S0`, `S1`, `S2`, `S3`, `S4`, `S5`, `S6`, `P0`, `P1`, and `P2`.

<h4 class="pdoc-member-header" id="AccountState-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/38f39deade34d0e187626f1cb68bf0835bc2c2d0/sdk/nodejs/cognitive/account.ts#L197">property <b>tags</b></a>
</h4>

<pre class="highlight"><code><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;}&gt;;</code></pre>

A mapping of tags to assign to the resource.

