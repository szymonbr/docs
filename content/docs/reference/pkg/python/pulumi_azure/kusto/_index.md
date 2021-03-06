---
title: Module kusto
title_tag: Module kusto | Package pulumi_azure | Python SDK
linktitle: kusto
notitle: true
block_external_search_index: true
---

{{< resource-docs-alert "azure" >}}

<div class="section" id="kusto">
<h1>kusto<a class="headerlink" href="#kusto" title="Permalink to this headline">¶</a></h1>
<blockquote>
<div><p>This provider is a derived work of the <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm">Terraform Provider</a> distributed under
<a class="reference external" href="https://www.mozilla.org/en-US/MPL/2.0/">MPL 2.0</a>. If you encounter a bug or missing feature, first check the
<a class="reference external" href="https://github.com/pulumi/pulumi-azure/issues">pulumi/pulumi-azure repo</a>; however, if that doesn’t turn up
anything, please consult the source <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm/issues">terraform-providers/terraform-provider-azurerm repo</a>.</p>
</div></blockquote>
<span class="target" id="module-pulumi_azure.kusto"></span><dl class="py class">
<dt id="pulumi_azure.kusto.AwaitableGetClusterResult">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.kusto.</code><code class="sig-name descname">AwaitableGetClusterResult</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">data_ingestion_uri</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">uri</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.AwaitableGetClusterResult" title="Permalink to this definition">¶</a></dt>
<dd></dd></dl>

<dl class="py class">
<dt id="pulumi_azure.kusto.Cluster">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.kusto.</code><code class="sig-name descname">Cluster</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">enable_disk_encryption</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">enable_streaming_ingest</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">sku</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.Cluster" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages a Kusto (also known as Azure Data Explorer) Cluster</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">rg</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">ResourceGroup</span><span class="p">(</span><span class="s2">&quot;rg&quot;</span><span class="p">,</span> <span class="n">location</span><span class="o">=</span><span class="s2">&quot;East US&quot;</span><span class="p">)</span>
<span class="n">example</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">Cluster</span><span class="p">(</span><span class="s2">&quot;example&quot;</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">sku</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="s2">&quot;Standard_D13_v2&quot;</span><span class="p">,</span>
        <span class="s2">&quot;capacity&quot;</span><span class="p">:</span> <span class="mi">2</span><span class="p">,</span>
    <span class="p">},</span>
    <span class="n">tags</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;Environment&quot;</span><span class="p">:</span> <span class="s2">&quot;Production&quot;</span><span class="p">,</span>
    <span class="p">})</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>enable_disk_encryption</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Specifies if the cluster’s disks are encrypted.</p></li>
<li><p><strong>enable_streaming_ingest</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Specifies if the streaming ingest is enabled.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The location where the Kusto Cluster should be created. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Kusto Cluster to create. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the Resource Group where the Kusto Cluster should exist. Changing this forces a new resource to be created.</p></li>
<li><p><strong>sku</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">sku</span></code> block as defined below.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>sku</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">capacity</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies the node count for the cluster. Boundaries depend on the sku name.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The name of the SKU. Valid values are: <code class="docutils literal notranslate"><span class="pre">Dev(No</span> <span class="pre">SLA)_Standard_D11_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D11_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D12_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D13_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D14_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS13_v2+1TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS13_v2+2TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS14_v2+3TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS14_v2+4TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_L16s</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_L4s</span></code> and <code class="docutils literal notranslate"><span class="pre">Standard_L8s</span></code></p></li>
</ul>
<dl class="py attribute">
<dt id="pulumi_azure.kusto.Cluster.data_ingestion_uri">
<code class="sig-name descname">data_ingestion_uri</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Cluster.data_ingestion_uri" title="Permalink to this definition">¶</a></dt>
<dd><p>The Kusto Cluster URI to be used for data ingestion.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Cluster.enable_disk_encryption">
<code class="sig-name descname">enable_disk_encryption</code><em class="property">: pulumi.Output[bool]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Cluster.enable_disk_encryption" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies if the cluster’s disks are encrypted.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Cluster.enable_streaming_ingest">
<code class="sig-name descname">enable_streaming_ingest</code><em class="property">: pulumi.Output[bool]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Cluster.enable_streaming_ingest" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies if the streaming ingest is enabled.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Cluster.location">
<code class="sig-name descname">location</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Cluster.location" title="Permalink to this definition">¶</a></dt>
<dd><p>The location where the Kusto Cluster should be created. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Cluster.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Cluster.name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the Kusto Cluster to create. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Cluster.resource_group_name">
<code class="sig-name descname">resource_group_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Cluster.resource_group_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the Resource Group where the Kusto Cluster should exist. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Cluster.sku">
<code class="sig-name descname">sku</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Cluster.sku" title="Permalink to this definition">¶</a></dt>
<dd><p>A <code class="docutils literal notranslate"><span class="pre">sku</span></code> block as defined below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">capacity</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - Specifies the node count for the cluster. Boundaries depend on the sku name.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">name</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The name of the SKU. Valid values are: <code class="docutils literal notranslate"><span class="pre">Dev(No</span> <span class="pre">SLA)_Standard_D11_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D11_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D12_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D13_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D14_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS13_v2+1TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS13_v2+2TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS14_v2+3TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS14_v2+4TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_L16s</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_L4s</span></code> and <code class="docutils literal notranslate"><span class="pre">Standard_L8s</span></code></p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Cluster.tags">
<code class="sig-name descname">tags</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Cluster.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags to assign to the resource.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Cluster.uri">
<code class="sig-name descname">uri</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Cluster.uri" title="Permalink to this definition">¶</a></dt>
<dd><p>The FQDN of the Azure Kusto Cluster.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.Cluster.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">data_ingestion_uri</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">enable_disk_encryption</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">enable_streaming_ingest</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">sku</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">uri</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.Cluster.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Cluster resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>data_ingestion_uri</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Kusto Cluster URI to be used for data ingestion.</p></li>
<li><p><strong>enable_disk_encryption</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Specifies if the cluster’s disks are encrypted.</p></li>
<li><p><strong>enable_streaming_ingest</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Specifies if the streaming ingest is enabled.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The location where the Kusto Cluster should be created. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Kusto Cluster to create. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the Resource Group where the Kusto Cluster should exist. Changing this forces a new resource to be created.</p></li>
<li><p><strong>sku</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A <code class="docutils literal notranslate"><span class="pre">sku</span></code> block as defined below.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
<li><p><strong>uri</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The FQDN of the Azure Kusto Cluster.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>sku</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">capacity</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - Specifies the node count for the cluster. Boundaries depend on the sku name.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The name of the SKU. Valid values are: <code class="docutils literal notranslate"><span class="pre">Dev(No</span> <span class="pre">SLA)_Standard_D11_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D11_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D12_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D13_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_D14_v2</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS13_v2+1TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS13_v2+2TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS14_v2+3TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_DS14_v2+4TB_PS</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_L16s</span></code>, <code class="docutils literal notranslate"><span class="pre">Standard_L4s</span></code> and <code class="docutils literal notranslate"><span class="pre">Standard_L8s</span></code></p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.Cluster.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.Cluster.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.Cluster.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.Cluster.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

</dd></dl>

<dl class="py class">
<dt id="pulumi_azure.kusto.Database">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.kusto.</code><code class="sig-name descname">Database</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">cluster_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">hot_cache_period</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">soft_delete_period</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.Database" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages a Kusto (also known as Azure Data Explorer) Database</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">rg</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">ResourceGroup</span><span class="p">(</span><span class="s2">&quot;rg&quot;</span><span class="p">,</span> <span class="n">location</span><span class="o">=</span><span class="s2">&quot;East US&quot;</span><span class="p">)</span>
<span class="n">cluster</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">Cluster</span><span class="p">(</span><span class="s2">&quot;cluster&quot;</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">sku</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="s2">&quot;Standard_D13_v2&quot;</span><span class="p">,</span>
        <span class="s2">&quot;capacity&quot;</span><span class="p">:</span> <span class="mi">2</span><span class="p">,</span>
    <span class="p">})</span>
<span class="n">database</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">Database</span><span class="p">(</span><span class="s2">&quot;database&quot;</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">cluster_name</span><span class="o">=</span><span class="n">cluster</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">hot_cache_period</span><span class="o">=</span><span class="s2">&quot;P7D&quot;</span><span class="p">,</span>
    <span class="n">soft_delete_period</span><span class="o">=</span><span class="s2">&quot;P31D&quot;</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>cluster_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Kusto Cluster this database will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>hot_cache_period</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The time the data that should be kept in cache for fast queries as ISO 8601 timespan. Default is unlimited. For more information see: <a class="reference external" href="https://en.wikipedia.org/wiki/ISO_8601#Durations">ISO 8601 Timespan</a></p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The location where the Kusto Database should be created. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Kusto Database to create. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the Resource Group where the Kusto Database should exist. Changing this forces a new resource to be created.</p></li>
<li><p><strong>soft_delete_period</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The time the data should be kept before it stops being accessible to queries as ISO 8601 timespan. Default is unlimited. For more information see: <a class="reference external" href="https://en.wikipedia.org/wiki/ISO_8601#Durations">ISO 8601 Timespan</a></p>
</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_azure.kusto.Database.cluster_name">
<code class="sig-name descname">cluster_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Database.cluster_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the Kusto Cluster this database will be added to. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Database.hot_cache_period">
<code class="sig-name descname">hot_cache_period</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Database.hot_cache_period" title="Permalink to this definition">¶</a></dt>
<dd><p>The time the data that should be kept in cache for fast queries as ISO 8601 timespan. Default is unlimited. For more information see: <a class="reference external" href="https://en.wikipedia.org/wiki/ISO_8601#Durations">ISO 8601 Timespan</a></p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Database.location">
<code class="sig-name descname">location</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Database.location" title="Permalink to this definition">¶</a></dt>
<dd><p>The location where the Kusto Database should be created. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Database.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Database.name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the Kusto Database to create. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Database.resource_group_name">
<code class="sig-name descname">resource_group_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Database.resource_group_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the Resource Group where the Kusto Database should exist. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Database.size">
<code class="sig-name descname">size</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Database.size" title="Permalink to this definition">¶</a></dt>
<dd><p>The size of the database in bytes.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.Database.soft_delete_period">
<code class="sig-name descname">soft_delete_period</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.Database.soft_delete_period" title="Permalink to this definition">¶</a></dt>
<dd><p>The time the data should be kept before it stops being accessible to queries as ISO 8601 timespan. Default is unlimited. For more information see: <a class="reference external" href="https://en.wikipedia.org/wiki/ISO_8601#Durations">ISO 8601 Timespan</a></p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.Database.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">cluster_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">hot_cache_period</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">size</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">soft_delete_period</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.Database.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Database resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>cluster_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Kusto Cluster this database will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>hot_cache_period</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The time the data that should be kept in cache for fast queries as ISO 8601 timespan. Default is unlimited. For more information see: <a class="reference external" href="https://en.wikipedia.org/wiki/ISO_8601#Durations">ISO 8601 Timespan</a></p>
</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The location where the Kusto Database should be created. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Kusto Database to create. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the Resource Group where the Kusto Database should exist. Changing this forces a new resource to be created.</p></li>
<li><p><strong>size</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The size of the database in bytes.</p></li>
<li><p><strong>soft_delete_period</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The time the data should be kept before it stops being accessible to queries as ISO 8601 timespan. Default is unlimited. For more information see: <a class="reference external" href="https://en.wikipedia.org/wiki/ISO_8601#Durations">ISO 8601 Timespan</a></p>
</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.Database.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.Database.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.Database.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.Database.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

</dd></dl>

<dl class="py class">
<dt id="pulumi_azure.kusto.DatabasePrincipal">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.kusto.</code><code class="sig-name descname">DatabasePrincipal</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">client_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">cluster_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">database_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">object_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">role</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages a Kusto (also known as Azure Data Explorer) Database Principal</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">current</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">get_client_config</span><span class="p">()</span>
<span class="n">rg</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">ResourceGroup</span><span class="p">(</span><span class="s2">&quot;rg&quot;</span><span class="p">,</span> <span class="n">location</span><span class="o">=</span><span class="s2">&quot;East US&quot;</span><span class="p">)</span>
<span class="n">cluster</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">Cluster</span><span class="p">(</span><span class="s2">&quot;cluster&quot;</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">sku</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="s2">&quot;Standard_D13_v2&quot;</span><span class="p">,</span>
        <span class="s2">&quot;capacity&quot;</span><span class="p">:</span> <span class="mi">2</span><span class="p">,</span>
    <span class="p">})</span>
<span class="n">database</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">Database</span><span class="p">(</span><span class="s2">&quot;database&quot;</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">cluster_name</span><span class="o">=</span><span class="n">cluster</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">hot_cache_period</span><span class="o">=</span><span class="s2">&quot;P7D&quot;</span><span class="p">,</span>
    <span class="n">soft_delete_period</span><span class="o">=</span><span class="s2">&quot;P31D&quot;</span><span class="p">)</span>
<span class="n">principal</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">DatabasePrincipal</span><span class="p">(</span><span class="s2">&quot;principal&quot;</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">cluster_name</span><span class="o">=</span><span class="n">cluster</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">database_name</span><span class="o">=</span><span class="n">azurerm_kusto_database</span><span class="p">[</span><span class="s2">&quot;test&quot;</span><span class="p">][</span><span class="s2">&quot;name&quot;</span><span class="p">],</span>
    <span class="n">role</span><span class="o">=</span><span class="s2">&quot;Viewer&quot;</span><span class="p">,</span>
    <span class="nb">type</span><span class="o">=</span><span class="s2">&quot;User&quot;</span><span class="p">,</span>
    <span class="n">client_id</span><span class="o">=</span><span class="n">current</span><span class="o">.</span><span class="n">tenant_id</span><span class="p">,</span>
    <span class="n">object_id</span><span class="o">=</span><span class="n">current</span><span class="o">.</span><span class="n">client_id</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>client_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Client ID that owns the specified <code class="docutils literal notranslate"><span class="pre">object_id</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>cluster_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Kusto Cluster this database principal will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>database_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specified the name of the Kusto Database this principal will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>object_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – An Object ID of a User, Group, or App. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the Resource Group where the Kusto Database Principal should exist. Changing this forces a new resource to be created.</p></li>
<li><p><strong>role</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the permissions the Principal will have. Valid values include <code class="docutils literal notranslate"><span class="pre">Admin</span></code>, <code class="docutils literal notranslate"><span class="pre">Ingestor</span></code>, <code class="docutils literal notranslate"><span class="pre">Monitor</span></code>, <code class="docutils literal notranslate"><span class="pre">UnrestrictedViewers</span></code>, <code class="docutils literal notranslate"><span class="pre">User</span></code>, <code class="docutils literal notranslate"><span class="pre">Viewer</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the type of object the principal is. Valid values include <code class="docutils literal notranslate"><span class="pre">App</span></code>, <code class="docutils literal notranslate"><span class="pre">Group</span></code>, <code class="docutils literal notranslate"><span class="pre">User</span></code>. Changing this forces a new resource to be created.</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.app_id">
<code class="sig-name descname">app_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.app_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The app id, if not empty, of the principal.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.client_id">
<code class="sig-name descname">client_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.client_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The Client ID that owns the specified <code class="docutils literal notranslate"><span class="pre">object_id</span></code>. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.cluster_name">
<code class="sig-name descname">cluster_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.cluster_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the Kusto Cluster this database principal will be added to. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.database_name">
<code class="sig-name descname">database_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.database_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specified the name of the Kusto Database this principal will be added to. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.email">
<code class="sig-name descname">email</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.email" title="Permalink to this definition">¶</a></dt>
<dd><p>The email, if not empty, of the principal.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.fully_qualified_name">
<code class="sig-name descname">fully_qualified_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.fully_qualified_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The fully qualified name of the principal.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the Kusto Database Principal.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.object_id">
<code class="sig-name descname">object_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.object_id" title="Permalink to this definition">¶</a></dt>
<dd><p>An Object ID of a User, Group, or App. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.resource_group_name">
<code class="sig-name descname">resource_group_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.resource_group_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the Resource Group where the Kusto Database Principal should exist. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.role">
<code class="sig-name descname">role</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.role" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the permissions the Principal will have. Valid values include <code class="docutils literal notranslate"><span class="pre">Admin</span></code>, <code class="docutils literal notranslate"><span class="pre">Ingestor</span></code>, <code class="docutils literal notranslate"><span class="pre">Monitor</span></code>, <code class="docutils literal notranslate"><span class="pre">UnrestrictedViewers</span></code>, <code class="docutils literal notranslate"><span class="pre">User</span></code>, <code class="docutils literal notranslate"><span class="pre">Viewer</span></code>. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.DatabasePrincipal.type">
<code class="sig-name descname">type</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.type" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the type of object the principal is. Valid values include <code class="docutils literal notranslate"><span class="pre">App</span></code>, <code class="docutils literal notranslate"><span class="pre">Group</span></code>, <code class="docutils literal notranslate"><span class="pre">User</span></code>. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.DatabasePrincipal.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">app_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">client_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">cluster_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">database_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">email</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">fully_qualified_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">object_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">role</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">type</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing DatabasePrincipal resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>app_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The app id, if not empty, of the principal.</p></li>
<li><p><strong>client_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Client ID that owns the specified <code class="docutils literal notranslate"><span class="pre">object_id</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>cluster_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Kusto Cluster this database principal will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>database_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specified the name of the Kusto Database this principal will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>email</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The email, if not empty, of the principal.</p></li>
<li><p><strong>fully_qualified_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The fully qualified name of the principal.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Kusto Database Principal.</p></li>
<li><p><strong>object_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – An Object ID of a User, Group, or App. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the Resource Group where the Kusto Database Principal should exist. Changing this forces a new resource to be created.</p></li>
<li><p><strong>role</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the permissions the Principal will have. Valid values include <code class="docutils literal notranslate"><span class="pre">Admin</span></code>, <code class="docutils literal notranslate"><span class="pre">Ingestor</span></code>, <code class="docutils literal notranslate"><span class="pre">Monitor</span></code>, <code class="docutils literal notranslate"><span class="pre">UnrestrictedViewers</span></code>, <code class="docutils literal notranslate"><span class="pre">User</span></code>, <code class="docutils literal notranslate"><span class="pre">Viewer</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the type of object the principal is. Valid values include <code class="docutils literal notranslate"><span class="pre">App</span></code>, <code class="docutils literal notranslate"><span class="pre">Group</span></code>, <code class="docutils literal notranslate"><span class="pre">User</span></code>. Changing this forces a new resource to be created.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.DatabasePrincipal.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.DatabasePrincipal.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.DatabasePrincipal.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

</dd></dl>

<dl class="py class">
<dt id="pulumi_azure.kusto.EventhubDataConnection">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.kusto.</code><code class="sig-name descname">EventhubDataConnection</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">cluster_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">consumer_group</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">data_format</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">database_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">eventhub_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">mapping_rule_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">table_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages a Kusto (also known as Azure Data Explorer) EventHub Data Connection</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">rg</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">ResourceGroup</span><span class="p">(</span><span class="s2">&quot;rg&quot;</span><span class="p">,</span> <span class="n">location</span><span class="o">=</span><span class="s2">&quot;East US&quot;</span><span class="p">)</span>
<span class="n">cluster</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">Cluster</span><span class="p">(</span><span class="s2">&quot;cluster&quot;</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">sku</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;name&quot;</span><span class="p">:</span> <span class="s2">&quot;Standard_D13_v2&quot;</span><span class="p">,</span>
        <span class="s2">&quot;capacity&quot;</span><span class="p">:</span> <span class="mi">2</span><span class="p">,</span>
    <span class="p">})</span>
<span class="n">database</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">Database</span><span class="p">(</span><span class="s2">&quot;database&quot;</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">cluster_name</span><span class="o">=</span><span class="n">cluster</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">hot_cache_period</span><span class="o">=</span><span class="s2">&quot;P7D&quot;</span><span class="p">,</span>
    <span class="n">soft_delete_period</span><span class="o">=</span><span class="s2">&quot;P31D&quot;</span><span class="p">)</span>
<span class="n">eventhub_ns</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">eventhub</span><span class="o">.</span><span class="n">EventHubNamespace</span><span class="p">(</span><span class="s2">&quot;eventhubNs&quot;</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">sku</span><span class="o">=</span><span class="s2">&quot;Standard&quot;</span><span class="p">)</span>
<span class="n">eventhub</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">eventhub</span><span class="o">.</span><span class="n">EventHub</span><span class="p">(</span><span class="s2">&quot;eventhub&quot;</span><span class="p">,</span>
    <span class="n">namespace_name</span><span class="o">=</span><span class="n">eventhub_ns</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">partition_count</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span>
    <span class="n">message_retention</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">consumer_group</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">eventhub</span><span class="o">.</span><span class="n">ConsumerGroup</span><span class="p">(</span><span class="s2">&quot;consumerGroup&quot;</span><span class="p">,</span>
    <span class="n">namespace_name</span><span class="o">=</span><span class="n">eventhub_ns</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">eventhub_name</span><span class="o">=</span><span class="n">eventhub</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">)</span>
<span class="n">eventhub_connection</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">EventhubDataConnection</span><span class="p">(</span><span class="s2">&quot;eventhubConnection&quot;</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">location</span><span class="o">=</span><span class="n">rg</span><span class="o">.</span><span class="n">location</span><span class="p">,</span>
    <span class="n">cluster_name</span><span class="o">=</span><span class="n">cluster</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">database_name</span><span class="o">=</span><span class="n">database</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">eventhub_id</span><span class="o">=</span><span class="n">azurerm_eventhub</span><span class="p">[</span><span class="s2">&quot;evenhub&quot;</span><span class="p">][</span><span class="s2">&quot;id&quot;</span><span class="p">],</span>
    <span class="n">consumer_group</span><span class="o">=</span><span class="n">consumer_group</span><span class="o">.</span><span class="n">name</span><span class="p">,</span>
    <span class="n">table_name</span><span class="o">=</span><span class="s2">&quot;my-table&quot;</span><span class="p">,</span>
    <span class="n">mapping_rule_name</span><span class="o">=</span><span class="s2">&quot;my-table-mapping&quot;</span><span class="p">,</span>
    <span class="n">data_format</span><span class="o">=</span><span class="s2">&quot;JSON&quot;</span><span class="p">)</span>
<span class="c1">#(Optional)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>cluster_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Kusto Cluster this data connection will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>consumer_group</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the EventHub consumer group this data connection will use for ingestion. Changing this forces a new resource to be created.</p></li>
<li><p><strong>data_format</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the data format of the EventHub messages. Allowed values: <code class="docutils literal notranslate"><span class="pre">AVRO</span></code>, <code class="docutils literal notranslate"><span class="pre">CSV</span></code>, <code class="docutils literal notranslate"><span class="pre">JSON</span></code>, <code class="docutils literal notranslate"><span class="pre">MULTIJSON</span></code>, <code class="docutils literal notranslate"><span class="pre">PSV</span></code>, <code class="docutils literal notranslate"><span class="pre">RAW</span></code>, <code class="docutils literal notranslate"><span class="pre">SCSV</span></code>, <code class="docutils literal notranslate"><span class="pre">SINGLEJSON</span></code>, <code class="docutils literal notranslate"><span class="pre">SOHSV</span></code>, <code class="docutils literal notranslate"><span class="pre">TSV</span></code> and <code class="docutils literal notranslate"><span class="pre">TXT</span></code></p></li>
<li><p><strong>database_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Kusto Database this data connection will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>eventhub_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the resource id of the EventHub this data connection will use for ingestion. Changing this forces a new resource to be created.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The location where the Kusto Database should be created. Changing this forces a new resource to be created.</p></li>
<li><p><strong>mapping_rule_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the mapping rule used for the message ingestion. Mapping rule must exist before resource is created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Kusto EventHub Data Connection to create. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the Resource Group where the Kusto Database should exist. Changing this forces a new resource to be created.</p></li>
<li><p><strong>table_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the target table name used for the message ingestion. Table must exist before resource is created.</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.cluster_name">
<code class="sig-name descname">cluster_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.cluster_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the Kusto Cluster this data connection will be added to. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.consumer_group">
<code class="sig-name descname">consumer_group</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.consumer_group" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the EventHub consumer group this data connection will use for ingestion. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.data_format">
<code class="sig-name descname">data_format</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.data_format" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the data format of the EventHub messages. Allowed values: <code class="docutils literal notranslate"><span class="pre">AVRO</span></code>, <code class="docutils literal notranslate"><span class="pre">CSV</span></code>, <code class="docutils literal notranslate"><span class="pre">JSON</span></code>, <code class="docutils literal notranslate"><span class="pre">MULTIJSON</span></code>, <code class="docutils literal notranslate"><span class="pre">PSV</span></code>, <code class="docutils literal notranslate"><span class="pre">RAW</span></code>, <code class="docutils literal notranslate"><span class="pre">SCSV</span></code>, <code class="docutils literal notranslate"><span class="pre">SINGLEJSON</span></code>, <code class="docutils literal notranslate"><span class="pre">SOHSV</span></code>, <code class="docutils literal notranslate"><span class="pre">TSV</span></code> and <code class="docutils literal notranslate"><span class="pre">TXT</span></code></p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.database_name">
<code class="sig-name descname">database_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.database_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the Kusto Database this data connection will be added to. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.eventhub_id">
<code class="sig-name descname">eventhub_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.eventhub_id" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the resource id of the EventHub this data connection will use for ingestion. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.location">
<code class="sig-name descname">location</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.location" title="Permalink to this definition">¶</a></dt>
<dd><p>The location where the Kusto Database should be created. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.mapping_rule_name">
<code class="sig-name descname">mapping_rule_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.mapping_rule_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the mapping rule used for the message ingestion. Mapping rule must exist before resource is created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the Kusto EventHub Data Connection to create. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.resource_group_name">
<code class="sig-name descname">resource_group_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.resource_group_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the Resource Group where the Kusto Database should exist. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.EventhubDataConnection.table_name">
<code class="sig-name descname">table_name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.table_name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the target table name used for the message ingestion. Table must exist before resource is created.</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.EventhubDataConnection.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">cluster_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">consumer_group</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">data_format</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">database_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">eventhub_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">mapping_rule_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">table_name</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing EventhubDataConnection resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>cluster_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Kusto Cluster this data connection will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>consumer_group</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the EventHub consumer group this data connection will use for ingestion. Changing this forces a new resource to be created.</p></li>
<li><p><strong>data_format</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the data format of the EventHub messages. Allowed values: <code class="docutils literal notranslate"><span class="pre">AVRO</span></code>, <code class="docutils literal notranslate"><span class="pre">CSV</span></code>, <code class="docutils literal notranslate"><span class="pre">JSON</span></code>, <code class="docutils literal notranslate"><span class="pre">MULTIJSON</span></code>, <code class="docutils literal notranslate"><span class="pre">PSV</span></code>, <code class="docutils literal notranslate"><span class="pre">RAW</span></code>, <code class="docutils literal notranslate"><span class="pre">SCSV</span></code>, <code class="docutils literal notranslate"><span class="pre">SINGLEJSON</span></code>, <code class="docutils literal notranslate"><span class="pre">SOHSV</span></code>, <code class="docutils literal notranslate"><span class="pre">TSV</span></code> and <code class="docutils literal notranslate"><span class="pre">TXT</span></code></p></li>
<li><p><strong>database_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Kusto Database this data connection will be added to. Changing this forces a new resource to be created.</p></li>
<li><p><strong>eventhub_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the resource id of the EventHub this data connection will use for ingestion. Changing this forces a new resource to be created.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The location where the Kusto Database should be created. Changing this forces a new resource to be created.</p></li>
<li><p><strong>mapping_rule_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the mapping rule used for the message ingestion. Mapping rule must exist before resource is created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Kusto EventHub Data Connection to create. Changing this forces a new resource to be created.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the Resource Group where the Kusto Database should exist. Changing this forces a new resource to be created.</p></li>
<li><p><strong>table_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the target table name used for the message ingestion. Table must exist before resource is created.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.EventhubDataConnection.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_azure.kusto.EventhubDataConnection.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.EventhubDataConnection.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

</dd></dl>

<dl class="py class">
<dt id="pulumi_azure.kusto.GetClusterResult">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.kusto.</code><code class="sig-name descname">GetClusterResult</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">data_ingestion_uri</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">location</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">tags</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">uri</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.GetClusterResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getCluster.</p>
<dl class="py attribute">
<dt id="pulumi_azure.kusto.GetClusterResult.data_ingestion_uri">
<code class="sig-name descname">data_ingestion_uri</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.GetClusterResult.data_ingestion_uri" title="Permalink to this definition">¶</a></dt>
<dd><p>The Kusto Cluster URI to be used for data ingestion.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.GetClusterResult.id">
<code class="sig-name descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.GetClusterResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>The provider-assigned unique ID for this managed resource.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_azure.kusto.GetClusterResult.uri">
<code class="sig-name descname">uri</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.kusto.GetClusterResult.uri" title="Permalink to this definition">¶</a></dt>
<dd><p>The FQDN of the Azure Kusto Cluster.</p>
</dd></dl>

</dd></dl>

<dl class="py function">
<dt id="pulumi_azure.kusto.get_cluster">
<code class="sig-prename descclassname">pulumi_azure.kusto.</code><code class="sig-name descname">get_cluster</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_group_name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.kusto.get_cluster" title="Permalink to this definition">¶</a></dt>
<dd><p>Use this data source to access information about an existing Kusto (also known as Azure Data Explorer) Cluster</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_azure</span> <span class="k">as</span> <span class="nn">azure</span>

<span class="n">example</span> <span class="o">=</span> <span class="n">azure</span><span class="o">.</span><span class="n">kusto</span><span class="o">.</span><span class="n">get_cluster</span><span class="p">(</span><span class="n">name</span><span class="o">=</span><span class="s2">&quot;kustocluster&quot;</span><span class="p">,</span>
    <span class="n">resource_group_name</span><span class="o">=</span><span class="s2">&quot;test_resource_group&quot;</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>name</strong> (<em>str</em>) – Specifies the name of the Kusto Cluster.</p></li>
<li><p><strong>resource_group_name</strong> (<em>str</em>) – The name of the Resource Group where the Kusto Cluster exists.</p></li>
</ul>
</dd>
</dl>
</dd></dl>

</div>
