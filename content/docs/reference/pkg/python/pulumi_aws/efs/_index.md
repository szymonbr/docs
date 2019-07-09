---
---

<div class="section" id="module-pulumi_aws.efs">
<span id="efs"></span><h1>efs<a class="headerlink" href="#module-pulumi_aws.efs" title="Permalink to this headline">¶</a></h1>
<dl class="class">
<dt id="pulumi_aws.efs.FileSystem">
<em class="property">class </em><code class="descclassname">pulumi_aws.efs.</code><code class="descname">FileSystem</code><span class="sig-paren">(</span><em>resource_name</em>, <em>opts=None</em>, <em>creation_token=None</em>, <em>encrypted=None</em>, <em>kms_key_id=None</em>, <em>performance_mode=None</em>, <em>provisioned_throughput_in_mibps=None</em>, <em>tags=None</em>, <em>throughput_mode=None</em>, <em>__name__=None</em>, <em>__opts__=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.FileSystem" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an Elastic File System (EFS) resource.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</li>
<li><strong>encrypted</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – If true, the disk will be encrypted.</li>
<li><strong>kms_key_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ARN for the KMS encryption key. When specifying kms_key_id, encrypted needs to be set to true.</li>
<li><strong>performance_mode</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The file system performance mode. Can be either <code class="docutils literal notranslate"><span class="pre">&quot;generalPurpose&quot;</span></code> or <code class="docutils literal notranslate"><span class="pre">&quot;maxIO&quot;</span></code> (Default: <code class="docutils literal notranslate"><span class="pre">&quot;generalPurpose&quot;</span></code>).</li>
<li><strong>provisioned_throughput_in_mibps</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The throughput, measured in MiB/s, that you want to provision for the file system. Only applicable with <code class="docutils literal notranslate"><span class="pre">throughput_mode</span></code> set to <code class="docutils literal notranslate"><span class="pre">provisioned</span></code>.</li>
<li><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the file system.</li>
<li><strong>throughput_mode</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Throughput mode for the file system. Defaults to <code class="docutils literal notranslate"><span class="pre">bursting</span></code>. Valid values: <code class="docutils literal notranslate"><span class="pre">bursting</span></code>, <code class="docutils literal notranslate"><span class="pre">provisioned</span></code>. When using <code class="docutils literal notranslate"><span class="pre">provisioned</span></code>, also set <code class="docutils literal notranslate"><span class="pre">provisioned_throughput_in_mibps</span></code>.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<blockquote>
<div>This content is derived from <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/efs_file_system.html.markdown">https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/efs_file_system.html.markdown</a>.</div></blockquote>
<dl class="attribute">
<dt id="pulumi_aws.efs.FileSystem.arn">
<code class="descname">arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.FileSystem.arn" title="Permalink to this definition">¶</a></dt>
<dd><p>Amazon Resource Name of the file system.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.FileSystem.dns_name">
<code class="descname">dns_name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.FileSystem.dns_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The DNS name for the filesystem per <a class="reference external" href="http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html">documented convention</a>.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.FileSystem.encrypted">
<code class="descname">encrypted</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.FileSystem.encrypted" title="Permalink to this definition">¶</a></dt>
<dd><p>If true, the disk will be encrypted.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.FileSystem.kms_key_id">
<code class="descname">kms_key_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.FileSystem.kms_key_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The ARN for the KMS encryption key. When specifying kms_key_id, encrypted needs to be set to true.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.FileSystem.performance_mode">
<code class="descname">performance_mode</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.FileSystem.performance_mode" title="Permalink to this definition">¶</a></dt>
<dd><p>The file system performance mode. Can be either <code class="docutils literal notranslate"><span class="pre">&quot;generalPurpose&quot;</span></code> or <code class="docutils literal notranslate"><span class="pre">&quot;maxIO&quot;</span></code> (Default: <code class="docutils literal notranslate"><span class="pre">&quot;generalPurpose&quot;</span></code>).</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.FileSystem.provisioned_throughput_in_mibps">
<code class="descname">provisioned_throughput_in_mibps</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.FileSystem.provisioned_throughput_in_mibps" title="Permalink to this definition">¶</a></dt>
<dd><p>The throughput, measured in MiB/s, that you want to provision for the file system. Only applicable with <code class="docutils literal notranslate"><span class="pre">throughput_mode</span></code> set to <code class="docutils literal notranslate"><span class="pre">provisioned</span></code>.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.FileSystem.tags">
<code class="descname">tags</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.FileSystem.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags to assign to the file system.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.FileSystem.throughput_mode">
<code class="descname">throughput_mode</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.FileSystem.throughput_mode" title="Permalink to this definition">¶</a></dt>
<dd><p>Throughput mode for the file system. Defaults to <code class="docutils literal notranslate"><span class="pre">bursting</span></code>. Valid values: <code class="docutils literal notranslate"><span class="pre">bursting</span></code>, <code class="docutils literal notranslate"><span class="pre">provisioned</span></code>. When using <code class="docutils literal notranslate"><span class="pre">provisioned</span></code>, also set <code class="docutils literal notranslate"><span class="pre">provisioned_throughput_in_mibps</span></code>.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.efs.FileSystem.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.FileSystem.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><strong>prop</strong> (<em>str</em>) – A property name.</td>
</tr>
<tr class="field-even field"><th class="field-name">Returns:</th><td class="field-body">A potentially transformed property name.</td>
</tr>
<tr class="field-odd field"><th class="field-name">Return type:</th><td class="field-body">str</td>
</tr>
</tbody>
</table>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.efs.FileSystem.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.FileSystem.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><strong>prop</strong> (<em>str</em>) – A property name.</td>
</tr>
<tr class="field-even field"><th class="field-name">Returns:</th><td class="field-body">A potentially transformed property name.</td>
</tr>
<tr class="field-odd field"><th class="field-name">Return type:</th><td class="field-body">str</td>
</tr>
</tbody>
</table>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.efs.GetFileSystemResult">
<em class="property">class </em><code class="descclassname">pulumi_aws.efs.</code><code class="descname">GetFileSystemResult</code><span class="sig-paren">(</span><em>arn=None</em>, <em>creation_token=None</em>, <em>dns_name=None</em>, <em>encrypted=None</em>, <em>file_system_id=None</em>, <em>kms_key_id=None</em>, <em>performance_mode=None</em>, <em>tags=None</em>, <em>id=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.GetFileSystemResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getFileSystem.</p>
<dl class="attribute">
<dt id="pulumi_aws.efs.GetFileSystemResult.arn">
<code class="descname">arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetFileSystemResult.arn" title="Permalink to this definition">¶</a></dt>
<dd><p>Amazon Resource Name of the file system.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetFileSystemResult.dns_name">
<code class="descname">dns_name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetFileSystemResult.dns_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The DNS name for the filesystem per <a class="reference external" href="http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html">documented convention</a>.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetFileSystemResult.encrypted">
<code class="descname">encrypted</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetFileSystemResult.encrypted" title="Permalink to this definition">¶</a></dt>
<dd><p>Whether EFS is encrypted.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetFileSystemResult.kms_key_id">
<code class="descname">kms_key_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetFileSystemResult.kms_key_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The ARN for the KMS encryption key.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetFileSystemResult.performance_mode">
<code class="descname">performance_mode</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetFileSystemResult.performance_mode" title="Permalink to this definition">¶</a></dt>
<dd><p>The PerformanceMode of the file system.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetFileSystemResult.tags">
<code class="descname">tags</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetFileSystemResult.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>The list of tags assigned to the file system.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetFileSystemResult.id">
<code class="descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetFileSystemResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>id is the provider-assigned unique ID for this managed resource.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.efs.GetMountTargetResult">
<em class="property">class </em><code class="descclassname">pulumi_aws.efs.</code><code class="descname">GetMountTargetResult</code><span class="sig-paren">(</span><em>dns_name=None</em>, <em>file_system_arn=None</em>, <em>file_system_id=None</em>, <em>ip_address=None</em>, <em>mount_target_id=None</em>, <em>network_interface_id=None</em>, <em>security_groups=None</em>, <em>subnet_id=None</em>, <em>id=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.GetMountTargetResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getMountTarget.</p>
<dl class="attribute">
<dt id="pulumi_aws.efs.GetMountTargetResult.dns_name">
<code class="descname">dns_name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetMountTargetResult.dns_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The DNS name for the given subnet/AZ per <a class="reference external" href="http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html">documented convention</a>.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetMountTargetResult.file_system_arn">
<code class="descname">file_system_arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetMountTargetResult.file_system_arn" title="Permalink to this definition">¶</a></dt>
<dd><p>Amazon Resource Name of the file system for which the mount target is intended.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetMountTargetResult.file_system_id">
<code class="descname">file_system_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetMountTargetResult.file_system_id" title="Permalink to this definition">¶</a></dt>
<dd><p>ID of the file system for which the mount target is intended.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetMountTargetResult.ip_address">
<code class="descname">ip_address</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetMountTargetResult.ip_address" title="Permalink to this definition">¶</a></dt>
<dd><p>Address at which the file system may be mounted via the mount target.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetMountTargetResult.network_interface_id">
<code class="descname">network_interface_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetMountTargetResult.network_interface_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The ID of the network interface that Amazon EFS created when it created the mount target.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetMountTargetResult.security_groups">
<code class="descname">security_groups</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetMountTargetResult.security_groups" title="Permalink to this definition">¶</a></dt>
<dd><p>List of VPC security group IDs attached to the mount target.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetMountTargetResult.subnet_id">
<code class="descname">subnet_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetMountTargetResult.subnet_id" title="Permalink to this definition">¶</a></dt>
<dd><p>ID of the mount target’s subnet.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.GetMountTargetResult.id">
<code class="descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.GetMountTargetResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>id is the provider-assigned unique ID for this managed resource.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.efs.MountTarget">
<em class="property">class </em><code class="descclassname">pulumi_aws.efs.</code><code class="descname">MountTarget</code><span class="sig-paren">(</span><em>resource_name</em>, <em>opts=None</em>, <em>file_system_id=None</em>, <em>ip_address=None</em>, <em>security_groups=None</em>, <em>subnet_id=None</em>, <em>__name__=None</em>, <em>__opts__=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.MountTarget" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an Elastic File System (EFS) mount target.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</li>
<li><strong>file_system_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ID of the file system for which the mount target is intended.</li>
<li><strong>ip_address</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The address (within the address range of the specified subnet) at
which the file system may be mounted via the mount target.</li>
<li><strong>security_groups</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of up to 5 VPC security group IDs (that must
be for the same VPC as subnet specified) in effect for the mount target.</li>
<li><strong>subnet_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ID of the subnet to add the mount target in.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<blockquote>
<div>This content is derived from <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/efs_mount_target.html.markdown">https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/efs_mount_target.html.markdown</a>.</div></blockquote>
<dl class="attribute">
<dt id="pulumi_aws.efs.MountTarget.dns_name">
<code class="descname">dns_name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.MountTarget.dns_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The DNS name for the given subnet/AZ per <a class="reference external" href="http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html">documented convention</a>.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.MountTarget.file_system_arn">
<code class="descname">file_system_arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.MountTarget.file_system_arn" title="Permalink to this definition">¶</a></dt>
<dd><p>Amazon Resource Name of the file system.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.MountTarget.file_system_id">
<code class="descname">file_system_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.MountTarget.file_system_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The ID of the file system for which the mount target is intended.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.MountTarget.ip_address">
<code class="descname">ip_address</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.MountTarget.ip_address" title="Permalink to this definition">¶</a></dt>
<dd><p>The address (within the address range of the specified subnet) at
which the file system may be mounted via the mount target.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.MountTarget.network_interface_id">
<code class="descname">network_interface_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.MountTarget.network_interface_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The ID of the network interface that Amazon EFS created when it created the mount target.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.MountTarget.security_groups">
<code class="descname">security_groups</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.MountTarget.security_groups" title="Permalink to this definition">¶</a></dt>
<dd><p>A list of up to 5 VPC security group IDs (that must
be for the same VPC as subnet specified) in effect for the mount target.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.efs.MountTarget.subnet_id">
<code class="descname">subnet_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.efs.MountTarget.subnet_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The ID of the subnet to add the mount target in.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.efs.MountTarget.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.MountTarget.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><strong>prop</strong> (<em>str</em>) – A property name.</td>
</tr>
<tr class="field-even field"><th class="field-name">Returns:</th><td class="field-body">A potentially transformed property name.</td>
</tr>
<tr class="field-odd field"><th class="field-name">Return type:</th><td class="field-body">str</td>
</tr>
</tbody>
</table>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.efs.MountTarget.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.MountTarget.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><strong>prop</strong> (<em>str</em>) – A property name.</td>
</tr>
<tr class="field-even field"><th class="field-name">Returns:</th><td class="field-body">A potentially transformed property name.</td>
</tr>
<tr class="field-odd field"><th class="field-name">Return type:</th><td class="field-body">str</td>
</tr>
</tbody>
</table>
</dd></dl>

</dd></dl>

<dl class="function">
<dt id="pulumi_aws.efs.get_file_system">
<code class="descclassname">pulumi_aws.efs.</code><code class="descname">get_file_system</code><span class="sig-paren">(</span><em>creation_token=None</em>, <em>file_system_id=None</em>, <em>tags=None</em>, <em>opts=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.get_file_system" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides information about an Elastic File System (EFS).</p>
<blockquote>
<div>This content is derived from <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/d/efs_file_system.html.markdown">https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/d/efs_file_system.html.markdown</a>.</div></blockquote>
</dd></dl>

<dl class="function">
<dt id="pulumi_aws.efs.get_mount_target">
<code class="descclassname">pulumi_aws.efs.</code><code class="descname">get_mount_target</code><span class="sig-paren">(</span><em>mount_target_id=None</em>, <em>opts=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.efs.get_mount_target" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides information about an Elastic File System Mount Target (EFS).</p>
<blockquote>
<div>This content is derived from <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/d/efs_mount_target.html.markdown">https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/d/efs_mount_target.html.markdown</a>.</div></blockquote>
</dd></dl>

</div>