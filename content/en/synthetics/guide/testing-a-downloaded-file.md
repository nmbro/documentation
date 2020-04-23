---
title: Test a downloaded file
kind: guide
further_reading:
    - link: 'https://www.datadoghq.com/blog/introducing-synthetic-monitoring/'
      tag: 'Blog'
      text: 'Introducing Datadog Synthetics'
    - link: 'synthetics/'
      tag: 'Documentation'
      text: 'Manage your checks'
    - link: 'synthetics/browser_tests'
      tag: 'Documentation'
      text: 'Configure a Browser Test'
---

A web application journey often involves downloading files such as an order confirmation from an e-commerce website or the PDF or CSV export history of bank account transactions.

Datadog’s browser tests and the `Test a downloaded file` assertion allow you to verify that downloadable files from your web application are correctly being served (for example, from your FTP server). With this assertion, downloadable files, such as a PDF receipt from an e-commerce website or a CSV history of banking transactions, can be tested to ensure they have the correct file name, size, and data. Note that you can also [record the uploading of a file][1] as an action into your browser test.

To setup a browser test with this assertion:

1. **Record the step that generates the file download** in your browser test. The example below shows how to record a click on a button that triggers the download of a `.docx` file:

    {{< img src="synthetics/guide/testing-a-downloaded-file/recording_step.mp4" alt="Recording steps" video="true">}}

2. **Add a `Test a downloaded file` assertion** to confirm that the file was correctly downloaded:

    {{< img src="synthetics/guide/testing-a-downloaded-file/adding_assertion.mp4" alt="Adding assertions" video="true">}}

     If needed, you can perform some more advanced verifications, for instance on your filename, on its size, and even on its integrity using a md5 string:

    {{< img src="synthetics/guide/testing-a-downloaded-file/advanced_verifications.mp4" alt="Advanced verification" video="true">}}

     See the full list of [Browser test assertions][2] to learn more on the `Test a downloaded file` assertion.

3. **Confirm that the file was downloaded** and matched the requirements you set up in your assertion by looking at the generated test result:

    {{< img src="synthetics/guide/testing-a-downloaded-file/tests_results.png" alt="Test results" >}}

## Further Reading

{{< partial name="whats-next/whats-next.html" >}}

[1]: /synthetics/browser_tests/actions/#upload
[2]: /synthetics/browser_tests/actions/#assertion