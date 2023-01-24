### GTM Container Template for Cookiebot

GTM Blocking Triggers
- Blocking - preferences consent
- Blocking - marketing consent is not given
- Blocking - statistics consent is not given
- Custom - cookie_consent_preferences
- Custom - cookie_consent_statistics
- Custom - cookie_consent_marketing

```json
{
    "exportFormatVersion": 2,
    "exportTime": "2023-01-24 20:09:50",
    "containerVersion": {
        "path": "accounts/6056368634/containers/100958787/versions/0",
        "accountId": "6056368634",
        "containerId": "100958787",
        "containerVersionId": "0",
        "container": {
            "path": "accounts/6056368634/containers/100958787",
            "accountId": "6056368634",
            "containerId": "100958787",
            "name": "Cookiebot container",
            "publicId": "GTM-W9DPB6W",
            "usageContext": [
                "WEB"
            ],
            "fingerprint": "1674590938408",
            "tagManagerUrl": "https://tagmanager.google.com/#/container/accounts/6056368634/containers/100958787/workspaces?apiLink=container",
            "features": {
                "supportUserPermissions": true,
                "supportEnvironments": true,
                "supportWorkspaces": true,
                "supportGtagConfigs": false,
                "supportBuiltInVariables": true,
                "supportClients": false,
                "supportFolders": true,
                "supportTags": true,
                "supportTemplates": true,
                "supportTriggers": true,
                "supportVariables": true,
                "supportVersions": true,
                "supportZones": true
            },
            "tagIds": [
                "GTM-W9DPB6W"
            ]
        },
        "tag": [
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "tagId": "9",
                "name": "Cookiebot",
                "type": "cvt_100958787_8",
                "parameter": [
                    {
                        "type": "TEMPLATE",
                        "key": "serial",
                        "value": "{{ENTER YOUR DOMAIN GROUP ID}}"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "iabFramework",
                        "value": "false"
                    },
                    {
                        "type": "TEMPLATE",
                        "key": "language",
                        "value": "auto"
                    }
                ],
                "fingerprint": "1674590968896",
                "firingTriggerId": [
                    "2147479553"
                ],
                "tagFiringOption": "ONCE_PER_EVENT",
                "monitoringMetadata": {
                    "type": "MAP"
                },
                "consentSettings": {
                    "consentStatus": "NOT_SET"
                }
            }
        ],
        "trigger": [
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "triggerId": "5",
                "name": "Blocking - preferences consent is not given",
                "type": "CUSTOM_EVENT",
                "customEventFilter": [
                    {
                        "type": "MATCH_REGEX",
                        "parameter": [
                            {
                                "type": "TEMPLATE",
                                "key": "arg0",
                                "value": "{{_event}}"
                            },
                            {
                                "type": "TEMPLATE",
                                "key": "arg1",
                                "value": ".*"
                            }
                        ]
                    }
                ],
                "filter": [
                    {
                        "type": "EQUALS",
                        "parameter": [
                            {
                                "type": "TEMPLATE",
                                "key": "arg0",
                                "value": "{{Regex - consent to preferences cookies}}"
                            },
                            {
                                "type": "TEMPLATE",
                                "key": "arg1",
                                "value": "false"
                            }
                        ]
                    }
                ],
                "fingerprint": "1674590968893"
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "triggerId": "7",
                "name": "Custom - cookie_consent_preferences",
                "type": "CUSTOM_EVENT",
                "customEventFilter": [
                    {
                        "type": "EQUALS",
                        "parameter": [
                            {
                                "type": "TEMPLATE",
                                "key": "arg0",
                                "value": "{{_event}}"
                            },
                            {
                                "type": "TEMPLATE",
                                "key": "arg1",
                                "value": "cookie_consent_preferences"
                            }
                        ]
                    }
                ],
                "fingerprint": "1674590968894"
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "triggerId": "10",
                "name": "Blocking - marketing consent is not given",
                "type": "CUSTOM_EVENT",
                "customEventFilter": [
                    {
                        "type": "MATCH_REGEX",
                        "parameter": [
                            {
                                "type": "TEMPLATE",
                                "key": "arg0",
                                "value": "{{_event}}"
                            },
                            {
                                "type": "TEMPLATE",
                                "key": "arg1",
                                "value": ".*"
                            }
                        ]
                    }
                ],
                "filter": [
                    {
                        "type": "EQUALS",
                        "parameter": [
                            {
                                "type": "TEMPLATE",
                                "key": "arg0",
                                "value": "{{Regex - consent to marketing cookies}}"
                            },
                            {
                                "type": "TEMPLATE",
                                "key": "arg1",
                                "value": "false"
                            }
                        ]
                    }
                ],
                "fingerprint": "1674590968896"
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "triggerId": "12",
                "name": "Blocking - statistics consent is not given",
                "type": "CUSTOM_EVENT",
                "customEventFilter": [
                    {
                        "type": "MATCH_REGEX",
                        "parameter": [
                            {
                                "type": "TEMPLATE",
                                "key": "arg0",
                                "value": "{{_event}}"
                            },
                            {
                                "type": "TEMPLATE",
                                "key": "arg1",
                                "value": ".*"
                            }
                        ]
                    }
                ],
                "filter": [
                    {
                        "type": "EQUALS",
                        "parameter": [
                            {
                                "type": "TEMPLATE",
                                "key": "arg0",
                                "value": "{{Regex - consent to statistics cookies}}"
                            },
                            {
                                "type": "TEMPLATE",
                                "key": "arg1",
                                "value": "false"
                            }
                        ]
                    }
                ],
                "fingerprint": "1674590968897"
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "triggerId": "13",
                "name": "Custom - cookie_consent_statistics",
                "type": "CUSTOM_EVENT",
                "customEventFilter": [
                    {
                        "type": "EQUALS",
                        "parameter": [
                            {
                                "type": "TEMPLATE",
                                "key": "arg0",
                                "value": "{{_event}}"
                            },
                            {
                                "type": "TEMPLATE",
                                "key": "arg1",
                                "value": "cookie_consent_statistics"
                            }
                        ]
                    }
                ],
                "fingerprint": "1674590968897"
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "triggerId": "14",
                "name": "Custom - cookie_consent_marketing",
                "type": "CUSTOM_EVENT",
                "customEventFilter": [
                    {
                        "type": "EQUALS",
                        "parameter": [
                            {
                                "type": "TEMPLATE",
                                "key": "arg0",
                                "value": "{{_event}}"
                            },
                            {
                                "type": "TEMPLATE",
                                "key": "arg1",
                                "value": "cookie_consent_marketing"
                            }
                        ]
                    }
                ],
                "fingerprint": "1674590968898"
            }
        ],
        "variable": [
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "variableId": "3",
                "name": "Cookie - CookieConsent",
                "type": "k",
                "parameter": [
                    {
                        "type": "BOOLEAN",
                        "key": "decodeCookie",
                        "value": "false"
                    },
                    {
                        "type": "TEMPLATE",
                        "key": "name",
                        "value": "CookieConsent"
                    }
                ],
                "fingerprint": "1674590968892",
                "formatValue": {}
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "variableId": "4",
                "name": "Regex - consent to preferences cookies",
                "type": "remm",
                "parameter": [
                    {
                        "type": "BOOLEAN",
                        "key": "setDefaultValue",
                        "value": "true"
                    },
                    {
                        "type": "TEMPLATE",
                        "key": "input",
                        "value": "{{Cookie - CookieConsent}}"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "fullMatch",
                        "value": "false"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "replaceAfterMatch",
                        "value": "false"
                    },
                    {
                        "type": "TEMPLATE",
                        "key": "defaultValue",
                        "value": "false"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "ignoreCase",
                        "value": "true"
                    },
                    {
                        "type": "LIST",
                        "key": "map",
                        "list": [
                            {
                                "type": "MAP",
                                "map": [
                                    {
                                        "type": "TEMPLATE",
                                        "key": "key",
                                        "value": "preferences:true"
                                    },
                                    {
                                        "type": "TEMPLATE",
                                        "key": "value",
                                        "value": "true"
                                    }
                                ]
                            }
                        ]
                    }
                ],
                "fingerprint": "1674590968892",
                "formatValue": {}
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "variableId": "6",
                "name": "Regex - consent to marketing cookies",
                "type": "remm",
                "parameter": [
                    {
                        "type": "BOOLEAN",
                        "key": "setDefaultValue",
                        "value": "true"
                    },
                    {
                        "type": "TEMPLATE",
                        "key": "input",
                        "value": "{{Cookie - CookieConsent}}"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "fullMatch",
                        "value": "false"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "replaceAfterMatch",
                        "value": "false"
                    },
                    {
                        "type": "TEMPLATE",
                        "key": "defaultValue",
                        "value": "false"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "ignoreCase",
                        "value": "true"
                    },
                    {
                        "type": "LIST",
                        "key": "map",
                        "list": [
                            {
                                "type": "MAP",
                                "map": [
                                    {
                                        "type": "TEMPLATE",
                                        "key": "key",
                                        "value": "marketing:true"
                                    },
                                    {
                                        "type": "TEMPLATE",
                                        "key": "value",
                                        "value": "true"
                                    }
                                ]
                            }
                        ]
                    }
                ],
                "fingerprint": "1674590968894",
                "formatValue": {}
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "variableId": "11",
                "name": "Regex - consent to statistics cookies",
                "type": "remm",
                "parameter": [
                    {
                        "type": "BOOLEAN",
                        "key": "setDefaultValue",
                        "value": "true"
                    },
                    {
                        "type": "TEMPLATE",
                        "key": "input",
                        "value": "{{Cookie - CookieConsent}}"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "fullMatch",
                        "value": "false"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "replaceAfterMatch",
                        "value": "false"
                    },
                    {
                        "type": "TEMPLATE",
                        "key": "defaultValue",
                        "value": "false"
                    },
                    {
                        "type": "BOOLEAN",
                        "key": "ignoreCase",
                        "value": "true"
                    },
                    {
                        "type": "LIST",
                        "key": "map",
                        "list": [
                            {
                                "type": "MAP",
                                "map": [
                                    {
                                        "type": "TEMPLATE",
                                        "key": "key",
                                        "value": "statistics:true"
                                    },
                                    {
                                        "type": "TEMPLATE",
                                        "key": "value",
                                        "value": "true"
                                    }
                                ]
                            }
                        ]
                    }
                ],
                "fingerprint": "1674590968897",
                "formatValue": {}
            }
        ],
        "builtInVariable": [
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "type": "PAGE_URL",
                "name": "Page URL"
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "type": "PAGE_HOSTNAME",
                "name": "Page Hostname"
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "type": "PAGE_PATH",
                "name": "Page Path"
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "type": "REFERRER",
                "name": "Referrer"
            },
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "type": "EVENT",
                "name": "Event"
            }
        ],
        "fingerprint": "1674590990734",
        "tagManagerUrl": "https://tagmanager.google.com/#/versions/accounts/6056368634/containers/100958787/versions/0?apiLink=version",
        "customTemplate": [
            {
                "accountId": "6056368634",
                "containerId": "100958787",
                "templateId": "8",
                "name": "Cookiebot CMP",
                "fingerprint": "1674590968895",
                "templateData": "___TERMS_OF_SERVICE___\n\nBy creating or modifying this file you agree to Google Tag Manager's Community\nTemplate Gallery Developer Terms of Service available at\nhttps://developers.google.com/tag-manager/gallery-tos (or such other URL as\nGoogle may provide), as modified from time to time.\n\n\n___INFO___\n\n{\n  \"displayName\": \"Cookiebot CMP\",\n  \"description\": \"Cookiebot is a Consent Management Provider (CMP) that helps make your use of cookies and online tracking GDPR and ePR compliant by obtaining consent from website users. More on https://cookiebot.com.\",\n  \"categories\": [\n    \"TAG_MANAGEMENT\",\n    \"PERSONALIZATION\"\n  ],\n  \"securityGroups\": [],\n  \"id\": \"cvt_temp_public_id\",\n  \"type\": \"TAG\",\n  \"version\": 1,\n  \"brand\": {\n    \"thumbnail\": \"data:image/png;base64,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\",\n    \"displayName\": \"cybotcorp\",\n    \"id\": \"github.com_cybotcorp\"\n  },\n  \"containerContexts\": [\n    \"WEB\"\n  ]\n}\n\n\n___TEMPLATE_PARAMETERS___\n\n[\n  {\n    \"notSetText\": \"Please enter the \\u0027Domain Group ID\\u0027 found under the tab named \\u0027Your Scripts\\u0027 in Cookiebot in the format \\u0027XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX\\u0027\",\n    \"help\": \"Create an account on Cookiebot.com and copy \\u0027Domain Group ID\\u0027 from the tab \\u0027Your Scripts\\u0027 in Cookiebot.\",\n    \"valueValidators\": [\n      {\n        \"args\": [\n          \"^(\\\\{){0,1}[0-9a-fA-F]{8}\\\\-[0-9a-fA-F]{4}\\\\-[0-9a-fA-F]{4}\\\\-[0-9a-fA-F]{4}\\\\-[0-9a-fA-F]{12}(\\\\}){0,1}$\"\n        ],\n        \"type\": \"REGEX\"\n      },\n      {\n        \"type\": \"NON_EMPTY\"\n      }\n    ],\n    \"displayName\": \"Cookiebot ID\",\n    \"simpleValueType\": true,\n    \"name\": \"serial\",\n    \"type\": \"TEXT\",\n    \"valueHint\": \"Your Cookiebot Domain Group ID\"\n  },\n  {\n    \"help\": \"Select how Cookiebot determines the language of the consent banner.\",\n    \"selectItems\": [\n      {\n        \"displayValue\": \"Default (auto-detect)\",\n        \"value\": \"auto\"\n      },\n      {\n        \"displayValue\": \"By GTM variable\",\n        \"value\": \"variable\"\n      }\n    ],\n    \"displayName\": \"Language\",\n    \"simpleValueType\": true,\n    \"name\": \"language\",\n    \"type\": \"SELECT\"\n  },\n  {\n    \"help\": \"Select a variable that returns a two-letter ISO 639-1 language code, e.g. from current URL. In Cookiebot, create matching content versions for all languages supported on your site.\",\n    \"enablingConditions\": [\n      {\n        \"paramName\": \"language\",\n        \"type\": \"EQUALS\",\n        \"paramValue\": \"variable\"\n      }\n    ],\n    \"valueValidators\": [\n      {\n        \"type\": \"NON_EMPTY\"\n      }\n    ],\n    \"displayName\": \"Language Variable\",\n    \"simpleValueType\": true,\n    \"name\": \"languageVariable\",\n    \"type\": \"TEXT\"\n  },\n  {\n    \"help\": \"Enabled IAB Europe\\u0027s Transparency \\u0026 Consent Framework if your site is displaying ads from one or more IAB Vendors.\",\n    \"simpleValueType\": true,\n    \"name\": \"iabFramework\",\n    \"checkboxText\": \"Enable IAB Transparency and Consent Framework\",\n    \"type\": \"CHECKBOX\"\n  }\n]\n\n\n___SANDBOXED_JS_FOR_WEB_TEMPLATE___\n\nconst injectScript = require('injectScript');\nconst encodeUriComponent = require('encodeUriComponent');\nconst queryPermission = require('queryPermission');\nconst cookiebotSerial = data.serial;\nconst IABEnabled = data.iabFramework;\nconst language = data.language;\n\nlet scriptUrl = 'https://consent.cookiebot.com/uc.js?cbid=' + encodeUriComponent(cookiebotSerial);\n\nif (language === 'variable')\n{\n  scriptUrl += '&culture=' + encodeUriComponent(data.languageVariable);\n}\n\nif(IABEnabled)\n{\n  scriptUrl += '&framework=IAB';\n}\n\nif (queryPermission('inject_script', scriptUrl)) {\n  injectScript(scriptUrl, data.gtmOnSuccess, data.gtmOnFailure);\n} else {\n  data.gtmOnFailure();\n}\n\n\n___WEB_PERMISSIONS___\n\n[\n  {\n    \"instance\": {\n      \"key\": {\n        \"publicId\": \"inject_script\",\n        \"versionId\": \"1\"\n      },\n      \"param\": [\n        {\n          \"key\": \"urls\",\n          \"value\": {\n            \"type\": 2,\n            \"listItem\": [\n              {\n                \"type\": 1,\n                \"string\": \"https://*.cookiebot.com/\"\n              }\n            ]\n          }\n        }\n      ]\n    },\n    \"clientAnnotations\": {\n      \"isEditedByUser\": true\n    },\n    \"isRequired\": true\n  }\n]\n\n\n___NOTES___\n\nCreated on 23.8.2019 08.53.59\n\n\n",
                "galleryReference": {
                    "host": "github.com",
                    "owner": "cybotcorp",
                    "repository": "gtm-templates-cookiebot-cmp",
                    "version": "e262384",
                    "signature": "7ecb3ef52763b57e9f786e088c374387fe4dad0707e068744bb57076443d3da3"
                }
            }
        ]
    }
}
```
