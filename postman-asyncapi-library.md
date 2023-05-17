# Postman AsyncAPI Library

Easily design and document your asynchronous API
Build your own guidelines with this library covering a wide range of topics. 
These rules aim to help you design and document your asynchronous API.

- [API information should contain contact information](#info-contact-defined)
- [API information should contain a contact email or url](#info-contact-email-or-url-defined)
- [API information should contain a contact email](#info-contact-email-defined)
- [API information should contain a contact name](#info-contact-name-defined)
- [API information should contain a contact url](#info-contact-url-defined)
- [API information should contain a description](#info-description-defined)
- [API information should contain license information](#info-license-defined)
- [API information should contain a license url](#info-license-url-defined)
- [API information should contain a terms of service url](#info-termsofservice-defined)
- [The minimum and maximum number of items of an array should be indicated](#schema-array-length-defined)
- [The minimum and maximum length of a string should be indicated](#schema-string-length-defined)
- [The schema of a message header should be a reference to a reusable schema](#schema-not-inline-message-headers)
- [The schema of a message trait header should be a reference to a reusable schema](#schema-not-inline-message-trait-headers)
- [The schema of a message payload should be a reference to a reusable schema](#schema-not-inline-payload)
- [The schema of a parameter should be a reference to a reusable schema](#schema-not-inline-parameter)
- [A property should have a description if its name and context are not explicit enough](#property-description-defined)
- [A reusable schema property should have a description if its name is not explicit enough](#reusable-schema-description-defined)
- [An operation should have a summary](#operation-summary-defined)
- [A summary shouldn't end with a period](#summary-period-none)
- [A parameter should have a description if name and context are not explicit enough](#parameter-description-defined)
- [A parameter should have at least one example](#parameters-examples-defined)
- [A message should have at least one example](#message-examples-defined)
- [A message trait should have at least one example](#messagetrait-examples-defined)

## <a name="info-contact-defined"></a>API information should contain contact information


### Issue

No contact object is defined in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}

```

An empty contact object is defined in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact: {}
channels: {}

```
### Resolution

A non-empty contact object is defined in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    name: a contact name
channels: {}

```

## <a name="info-contact-email-or-url-defined"></a>API information should contain a contact email or url


### Issue

No email or url property are defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact: {}
channels: {}

```
### Resolution

An email property is defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    name: a contact name
    email: contact@somewhere.come
channels: {}

```

A url property is defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    name: a contact name
    url: https://somewhere.com
channels: {}

```

A url and an email property are defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    name: a contact name
    url: https://somewhere.com
    email: contact@somewhere.come
channels: {}

```

## <a name="info-contact-email-defined"></a>API information should contain a contact email


### Issue

No email property is defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    name: a contact name
channels: {}

```
### Resolution

An email property is defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    name: a contact name
    email: contact@somewhere.come
channels: {}

```

## <a name="info-contact-name-defined"></a>API information should contain a contact name


### Issue

No name property is defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    url: https://somewhere.com/support
channels: {}

```
### Resolution

A name property is defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    name: a contact name
    url: https://somewhere.com/support
channels: {}

```

## <a name="info-contact-url-defined"></a>API information should contain a contact url


### Issue

No url property is defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    name: a contact name
channels: {}

```
### Resolution

A url property is defined in info.contact.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  contact:
    name: a contact name
    url: https://somewhere.com
channels: {}

```

## <a name="info-description-defined"></a>API information should contain a description


### Issue

No description property is defined in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}

```
### Resolution

A description property is defined in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  description: an api description
channels: {}

```

## <a name="info-license-defined"></a>API information should contain license information


### Issue

No license object is defined in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}

```
### Resolution

A license object is defined in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  description: an api description
  license:
    name: Apache 2.0
    url: https://opensource.org/licenses/Apache-2.0
channels: {}

```

## <a name="info-license-url-defined"></a>API information should contain a license url


### Issue

There's no url property in license.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  license:
    name: Apache 2.0
channels: {}

```
### Resolution

There's a url property in license.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  description: an api description
  license:
    name: Apache 2.0
    url: https://opensource.org/licenses/Apache-2.0
channels: {}

```

There's no license property in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}

```

## <a name="info-termsofservice-defined"></a>API information should contain a terms of service url


### Issue

No termsOfService property is defined in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}

```
### Resolution

A termsOfService property is defined in info.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
  termsOfService: https://somewhere.com/tos
channels: {}

```

## <a name="schema-array-length-defined"></a>The minimum and maximum number of items of an array should be indicated


### Issue

MinItems and maxItems are not defined in array property.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  schemas:
    Schema:
      properties:
        anArray:
          type: array
          items:
            type: string

```
### Resolution

MinItems and maxItems are defined in array property.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  schemas:
    Schema:
      properties:
        anArray:
          type: array
          minItems: 0
          maxItems: 10
          items:
            type: string

```

## <a name="schema-string-length-defined"></a>The minimum and maximum length of a string should be indicated


### Issue

The minLength and maxLength properties are not defined in a string schema.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  schemas:
    Schema:
      properties:
        aString:
          type: string

```
### Resolution

The minLength and maxLength properties are defined in a string schema.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  schemas:
    Schema:
      properties:
        aString:
          type: string
          minLength: 0
          maxLength: 10

```

## <a name="schema-not-inline-message-headers"></a>The schema of a message header should be a reference to a reusable schema


### Issue

The headers schema is defined inline.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  messages:
    ReusableMessage:
      headers:
        type: object

```
### Resolution

The headers schema is a $ref.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  messages:
    ReusableMessage:
      headers:
        $ref: "#/components/schemas/HeaderSchema"
  schemas:
    HeaderSchema:
      type: object

```

## <a name="schema-not-inline-message-trait-headers"></a>The schema of a message trait header should be a reference to a reusable schema


### Issue

The headers schema is defined inline.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  messageTraits:
    ReusableMessageTrait:
      headers:
        type: object

```
### Resolution

The headers schema is a $ref.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  messageTraits:
    ReusableMessageTrait:
      headers:
        $ref: "#/components/schemas/HeaderSchema"
  schemas:
    HeaderSchema:
      type: object

```

## <a name="schema-not-inline-payload"></a>The schema of a message payload should be a reference to a reusable schema


### Issue

The payload schema is defined inline.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    publish:
      message:
        payload:
          type: object

```
### Resolution

The payload schema is a $ref.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    publish:
      message:
        payload:
          $ref: "#/components/schemas/PayloadSchema"
components:
  schemas:
    PayloadSchema:
      type: object

```

## <a name="schema-not-inline-parameter"></a>The schema of a parameter should be a reference to a reusable schema


### Issue

The parameter schema is defined inline.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    parameters:
      aParameter:
        schema:
          type: object

```
### Resolution

The parameter schema is a $ref.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    parameters:
      aParameter:
        schema:
          $ref: "#/components/schemas/ParameterSchema"
components:
  schemas:
    ParameterSchema:
      type: object

```

## <a name="property-description-defined"></a>A property should have a description if its name and context are not explicit enough


### Issue

No description is defined in property.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  schemas:
    Schema:
      properties:
        aProperty:
          type: string

```
### Resolution

A description is defined in property.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  schemas:
    Schema:
      properties:
        aProperty:
          description: a property
          type: string

```

## <a name="reusable-schema-description-defined"></a>A reusable schema property should have a description if its name is not explicit enough


### Issue

No description is defined in reusable schema.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  schemas:
    Schema: {}

```
### Resolution

A description is defined in reusable schema.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  schemas:
    Schema:
      description: a schema

```

## <a name="operation-summary-defined"></a>An operation should have a summary


### Issue

No summary is defined in operation.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    publish: {}

```
### Resolution

Summary is defined in operation.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    publish:
      summary: an operation

```

## <a name="summary-period-none"></a>A summary shouldn't end with a period


### Issue

The summary ends with a period.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    publish:
      summary: a summary.

```
### Resolution

The summary doesn't end with a period.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    publish:
      summary: a summary

```

## <a name="parameter-description-defined"></a>A parameter should have a description if name and context are not explicit enough


### Issue

No description is defined in parameter.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    parameters:
      aParameter: {}

```
### Resolution

A description is defined in parameter.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    parameters:
      aParameter:
        description: a parameter

```

## <a name="parameters-examples-defined"></a>A parameter should have at least one example


### Issue

No examples is defined in parameter.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    parameters:
      aParameter:
        schema:
          type: string

```

An empty examples is defined in parameter.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    parameters:
      aParameter:
        schema:
          type: string
          examples: []

```
### Resolution

A non empty examples is defined in parameter.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    parameters:
      aParameter:
        schema:
          type: string
          examples:
            - example

```

## <a name="message-examples-defined"></a>A message should have at least one example


### Issue

No examples is defined in message.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    publish:
      message: {}

```

An empty examples is defined found in message.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    publish:
      message:
        examples: []

```
### Resolution

Non empty examples is defined in message.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels:
  a-channel:
    publish:
      message:
        examples:
          - payload:
              anExampleProperty: an example value

```

## <a name="messagetrait-examples-defined"></a>A message trait should have at least one example


### Issue

No examples is defined in message trait.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  messageTraits:
    ReusableMessageTrait: {}

```

An empty examples is defined in message trait.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  messageTraits:
    ReusableMessageTrait:
      examples: []

```
### Resolution

A non empty example is defined in message trait.

```yaml
asyncapi: 2.6.0
info:
  title: an api name
  version: "1.0"
channels: {}
components:
  messageTraits:
    ReusableMessageTrait:
      examples:
        - payload:
            anExampleProperty: an example value

```
