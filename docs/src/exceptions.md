# Exceptions


* [mPulseAPIException](exceptions.md#datatype-mpulseapiexception)
* [mPulseAPIAuthException](exceptions.md#datatype-mpulseapiauthexception)
* [mPulseAPIRequestException](exceptions.md#datatype-mpulseapirequestexception)
* [mPulseAPIResultFormatException](exceptions.md#datatype-mpulseapiresultformatexception)
## Exported Types
### datatype `mPulseAPIException`
[exceptions.jl#20-23](https://github.com/SOASTA/mPulseAPI.jl/tree/master/src/exceptions.jl#L20-L23){: .source-link}

Thrown when the REST API has a problem and returns something other than a 2xx response.

#### Fields
`msg::AbstractString`
:    The error message

`response::Response`
:    The response object from the REST API call.  You can inspect headers, data, cookies, redirects, and the initiating request.


---

### datatype `mPulseAPIAuthException`
[exceptions.jl#36-41](https://github.com/SOASTA/mPulseAPI.jl/tree/master/src/exceptions.jl#L36-L41){: .source-link}

Thrown when the token used to authenticate with the REST API is invalid or has expired

#### Fields
`msg::AbstractString`
:    This message is always set to "Error Authenticating with REST API"

`response::Response`
:    The response object from the REST API call.  You can inspect headers, data, cookies, redirects, and the initiating request.


---

### datatype `mPulseAPIRequestException`
[exceptions.jl#63-69](https://github.com/SOASTA/mPulseAPI.jl/tree/master/src/exceptions.jl#L63-L69){: .source-link}

Thrown when a request parameter is invalid

#### Fields
`msg::AbstractString`
:    The error message sent from the mPulse server

`code::AbstractString`
:    The error code sent from the mPulse server

`parameter::AbstractString`
:    The parameter that the mPulse server had a problem with

`value::AbstractString`
:    The value of the parameter that the mPulse server had a problem with

`response::Response`
:    The response object from the REST API call.  You can inspect headers, data, cookies, redirects, and the initiating request.


---

### datatype `mPulseAPIResultFormatException`
[exceptions.jl#82-85](https://github.com/SOASTA/mPulseAPI.jl/tree/master/src/exceptions.jl#L82-L85){: .source-link}

Thrown when the result returned by an API call was not in the expected format

#### Fields
`msg::AbstractString`
:    The error message

`data::Any`
:    The actual data returned


---

