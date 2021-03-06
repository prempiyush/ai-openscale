---

copyright:
  years: 2018, 2019
lastupdated: "2019-02-04"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:important: .important}
{:note: .note}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# About
{: #in-ov}

{{site.data.keyword.aios_full}} is an enterprise-grade environment for AI-infused applications, providing enterprises visibility into how AI is being built, used, and delivering return on investment, at the scale of your business.
{: shortdesc}

## Implementation
{: #in-imp}

Here's how you will implement {{site.data.keyword.aios_short}}:

- **Configure {{site.data.keyword.aios_short}}**: With the easy-to-use graphical environment, [set up a payload logging database](/docs/services/ai-openscale/connect-db.html), and the [Watson Machine Learning instance](/docs/services/ai-openscale/connect-wml.html) where your AI models and deployments are stored.

- **Work with monitors**: For each deployment, configure how {{site.data.keyword.aios_short}} will monitor that deployment. You can monitor for:

    - [Fairness](/docs/services/ai-openscale/monitor-fairness.html)
    - [Accuracy](/docs/services/ai-openscale/monitor-accuracy.html)

- **View and edit monitored data**: The {{site.data.keyword.aios_short}} [dashboard](/docs/services/ai-openscale/insight-overview.html) lets you easily view key insights and identify issues for your deployments. Visualization of individual data points for each monitored feature provides additional detail.

## Limitations
{: #in-lim}

- The current release only supports one database, one Watson Machine Learning instance, and one instance of {{site.data.keyword.aios_short}}

- The database and Watson Machine Learning instance must be deployed in the same {{site.data.keyword.Bluemix_notm}} account.

- The Lite (free) plan has the following monthly limits:

    - Two deployed models monitored
    - 20 transactions explained
    - 50,000 payload records (cumulative)
    - 50,000 feedback records (cumulative)

- There is a license limit of 20 deployed models per instance of {{site.data.keyword.aios_short}}.

- Currently, explanations cannot be generated for images which are greater than 1 MB in size.

## Supported model types
{: #in-mod}

Table 1. Model support details

| Algorithms | **Fairness** | **Auto-debias** | **Explain** | **Accuracy** |
|:---|:---:|:---:|:---:|:---:|
| **Structured Classification** | Yes | Yes<sup>1</sup> | Yes | Yes |
| **Structured Regression**     | Yes | Coming soon | Yes | Yes |
| **Text Classification**       | No - active research topic | No - active research topic | Yes | No |
| **Image Classification**      | No - active research topic | No - active research topic | Yes | No ||
{: caption="Model support details" caption-side="top"}

<sup>1</sup> If your model / framework outputs prediction probabilities

## Supported frameworks
{: #in-fram}

Table 1. Framework support details

| Algorithms | **Out-of-the-box support** | **[Custom environment](/docs/services/ai-openscale/connect-other.html#co-works) or Python function support** |
|:---|:---:|:---:|
| **Structured Classification** | Spark mllib on WML, AWS Sagemaker Native, Azure ML Studio Native | Scikit-Learn, XGboost, SPSS, Keras, Tensorflow,  Pytorch, Caffe,  or any other framework of your choice |
| **Structured Regression**     | Spark mllib on WML, AWS Sagemaker Native, Azure ML Studio Native | Scikit-Learn, XGboost, SPSS, Keras, Tensorflow,  Pytorch, Caffe,  or any other framework of your choice |
| **Text Classification**       | Spark mllib on WML | Coming soon: Keras, Tensorflow, Pytorch, Caffe, and most others |
| **Image Classification**      | Keras on WML | Coming soon: Keras, Tensorflow, Pytorch, Caffe, and most others ||
{: caption="Framework support details" caption-side="top"}

## Browser support
{: #in-brw}

The {{site.data.keyword.aios_short}} service tooling requires the same level of browser software as is required by {{site.data.keyword.Bluemix_notm}}. See the {{site.data.keyword.Bluemix_notm}} [Prerequisites ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/docs/overview/prereqs.html#browsers){: new_window} topic for details.

## ModelOps CLI tool
{: #in-mop}

The [{{site.data.keyword.aios_short}} CLI model operations tool ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://github.com/IBM-Watson/aiopenscale-modelops-cli){: new_window} allows you to execute tasks related to the lifecycle management of machine learning models. This tool is complementary to the {{site.data.keyword.Bluemix_notm}} CLI tool, augmented with the [machine learning plugin ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/DSXDOC/analyze-data/ml_dlaas_environment.html){: new_window}.

## Python client
{: #in-pyc}

The [{{site.data.keyword.aios_short}} Python client ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ai-openscale-python-client.mybluemix.net/){: new_window} is a Python library that allows you to work directly with the {{site.data.keyword.aios_short}} service on {{site.data.keyword.Bluemix_notm}}. You can use the Python client, instead of the {{site.data.keyword.aios_short}} client UI, to directly configure a logging database, bind your machine learning engine, and select and monitor deployments. For an example using the Python client in this way, see both the [CARS4U action recommendation - model ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://github.com/pmservice/ai-openscale-tutorials/blob/master/notebooks/CARS4U%20action%20recommendation%20-%20model.ipynb) and the [Working with Watson Machine Learning Engine ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://github.com/pmservice/ai-openscale-tutorials/blob/master/notebooks/AI%20OpenScale%20and%20Watson%20ML%20Engine.ipynb) notebooks.

## Next steps
{: #in-next}

- [Get started](/docs/services/ai-openscale/getting-started.html) with the service.
- View the [API Reference material ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/apidocs/ai-openscale){: new_window}.

Still have questions? [Contact IBM ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/account/reg/us-en/signup?formid=MAIL-watson){: new_window}.
