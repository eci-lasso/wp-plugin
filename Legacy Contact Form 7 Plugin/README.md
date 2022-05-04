<h1>WordPress Legacy Form Integration</h1>

<h3><a name="cf7-plugin">Contact Form 7</a></h3>
<p>To integrate a Contact Form 7 WordPress form:</p>
<ul>
<li>Download the WordPress plugin <a href="https://github.com/eci-lasso/wp-plugin/tree/main/Legacy%20Contact%20Form%207%20Plugin/cf7-lasso-v1.4.zip" download>cf7-lasso-v1.4.zip</a></li>
<li>Refer to the <a href="https://contactform7.com/getting-started-with-contact-form-7/" target="_blank">Getting started with Contact Form 7</a> article for instructions on setting up a Contact Form 7 WordPress form.</li>
<li>Add the Lasso integration settings under the <b>Additional Settings</b> tab as shown in <a href="https://github.com/eci-lasso/wp-plugin/blob/main/Legacy%20Contact%20Form%207%20Plugin/contact-form/additional-settings.txt" target="_blank">additional-settings.txt</a></li>
<li>Add the Lasso form fields under the <b>Form</b> tab as shown in <a href="https://github.com/eci-lasso/wp-plugin/blob/main/Legacy%20Contact%20Form%207%20Plugin/contact-form/form.html" target="_blank">form.html</a></li>
</ul>
<h3><a name="special-cases">Special Cases</a></h3>
<p>To submit to different projects based on an answer selection</p>
<ul>
<li>Remove the <code>ProjectID</code> from under the <b>Additional Settings</b> tab</li>
<li>Add the <code>ProjectID</code> under the <b>Form</b> tab as a question (examples below)</li>
</ul>
<pre>[radio ProjectID "Project One|1111" "Project Two|2222" "Project Three|3333"]<br />[checkbox ProjectIds "Project One|1111" "Project Two|2222" "Project Three|3333"]</pre>
