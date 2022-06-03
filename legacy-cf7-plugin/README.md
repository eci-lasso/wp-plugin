<h1>WordPress Legacy Form Integration</h1>
<p>Please note that this WordPress plugin is <b>outdated and no longer supported</b>. The most recent <a href="https://github.com/eci-lasso/wp-plugin" target="_blank">Lasso Bridge Plugin</a> is recommended instead.</p>

<h3><a name="cf7-plugin">Contact Form 7 Integration</a></h3>
<p>To integrate a Contact Form 7 WordPress form:</p>
<ul>
<li>Download the WordPress plugin <a href="https://github.com/eci-lasso/wp-plugin/blob/main/legacy-cf7-plugin/cf7-lasso-v1.4.zip" download>cf7-lasso-v1.4.zip</a></li>
<li>Add the Lasso integration settings under the <b>Additional Settings</b> tab as shown in <a href="https://github.com/eci-lasso/wp-plugin/blob/main/legacy-cf7-plugin/contact-form/additional-settings.txt" target="_blank">additional-settings.txt</a></li>
<li>Add the Lasso form fields under the <b>Form</b> tab as shown in <a href="https://github.com/eci-lasso/wp-plugin/blob/main/legacy-cf7-plugin/contact-form/form.html" target="_blank">form.html</a></li>
<li>Refer to the <a href="https://constructionsupport.ecisolutions.com/s/article/Lasso-Integrations-Integrate-Contact-Form-7-with-Lasso" target="_blank">Integrate Contact Form 7 with Lasso</a> help article for full instructions</li>
</ul>

<h3><a name="multi-project">Multi-project Submissions</a></h3>
<p>To submit to different projects based on an answer selection:</p>
<ul>
<li>Remove the <code>ProjectID</code> from under the <b>Additional Settings</b> tab</li>
<li>Add <code>ProjectID</code> or <code>ProjectIds</code> under the <b>Form</b> tab as a required single- or multi-select question</li>
</ul>
<pre>[radio* ProjectID "Project One|1111" "Project Two|2222" "Project Three|3333"]<br />[checkbox* ProjectIds "Project One|1111" "Project Two|2222" "Project Three|3333"]</pre>

<h3><a name="sales-details">Sales Details as Form Fields</a></h3>
<p>To set Source Type and Follow-up Process as form fields and assign values based on selections:</p>
<ul>
<li>Remove the <code>SourceTypeID</code> and/or <code>followUpProcessId</code> from under the <b>Additional Settings</b> tab</li>
<li>Add the <code>SourceTypeID</code> and/or <code>followUpProcessId</code> under the <b>Form</b> tab in a single-select question format</li>
</ul>
<pre>[radio SourceTypeID "Source Type One|1111" "Source Type Two|2222" "Source Type Three|3333"]<br />[select followUpProcessId "Follow-up Process One|1111" "Follow-up Process Two|2222" "Follow-up Process Three|3333"]</pre>

<h3><a name="dynamic-fields">Capturing Dynamic Fields</a></h3>
<p>To capture dynamic fields and submit to Lasso:</p>
<ul>
<li>Install and activate the <a href="https://sevenspark.com/goods/contact-form-7-dynamic-text-extension" target="_blank">Contact Form 7 - Dynamic Text Extension</a> plugin</li>
<li>Add the hidden manual input question fields under the <b>Form</b> tab</li>
</ul>
<pre>[dynamichidden Questions-1111 "CF7_URL"]
[dynamichidden Questions-2222 "CF7_get_post_var key='title'"]
[dynamichidden Questions-3333 "CF7_get_post_var key='slug'"]</pre>

<h3><a name="dynamic-fields">Capturing UTM Information</a></h3>
<p>To capture UTM information and submit to Lasso:</p>
<ul>
<li>Install and activate the premium version of the <a href="https://utmgrabber.com/" target="_blank">HandL UTM Grabber</a> plugin</li>
<li>Add the manual input question fields under the <b>Form</b> tab</li>
</ul>
<pre>[utm_campaign_i]&lt;input type="hidden" name="question-1111" value="%s" /&gt;[/utm_campaign_i]
[utm_content_i]&lt;input type="hidden" name="question-2222" value="%s" /&gt;[/utm_content_i]
[utm_source_i]&lt;input type="hidden" name="question-5555" value="%s" /&gt;[/utm_source_i]
[utm_term_i]&lt;input type="hidden" name="question-6666" value="%s" /&gt;[/utm_term_i]</pre>
