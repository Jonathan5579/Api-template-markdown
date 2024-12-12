## Create beautiful REST API docs authored in Markdown

- Adopted from: https://stubby4j.com/docs/admin_portal.html
- Inspired by Swagger API docs style & structure: https://petstore.swagger.io/#/pet
- Modified style to use colors
------------------------------------------------------------------------------------------

<style>

summary{
  color: white;
}

details{
  font-family: "Jetbrains Mono", Consolas,"courier new";
  color: white;
  border-radius: 6px;
  padding: 12px 16px 12px 16px;
  margin: 4px 0px 4px 0px;
}

.api_tag{
  style=' font-family: Consolas,"courier new";
  font-color: white;  
  color: white;
  padding: 6px 16px 6px 16px;
  font-size: 115%;
}


.post{
  background-color:rgba(64, 138, 70, 0.36);
}

code.post{
  background-color:rgb(73, 170, 82);
}

.get{
  background-color:rgba(56, 102, 170, 0.36);
}

code.get{
  background-color:rgb(68, 115, 187);
}

.put{
  background-color:rgba(189, 160, 82, 0.36);
}

code.put{
  background-color:rgb(187, 145, 68);
}

.delete{
  background-color:rgba(151, 74, 74, 0.36);
}

code.delete{
  background-color:rgb(187, 68, 68);
}
</style>






## Templates...

<details class='post'>
   <summary><code class='api_tag post'>POST</code><b> /</b> Post description</summary>

### Description

A short summary of what it does, and metadata needed.

### Parameters

> None

### Json
> Json

### Responses

> | http code     | description           | content-type              | response                                                            |
> |---------------|-----------------------| --------------------------|---------------------------------------------------------------------|
> | `200/300/400`         | description    | `application/json`        | `{"status": 500,"error": "6001","message": "locación no existe"}`    |

### Example 

> ```json
>   {Example to make a request}
> ```

</details>

<details class='get'>
 <summary><code class='api_tag get'>GET</code><b> /</b> Get description</summary>

### Description

A short summary of what it does, and metadata needed.

### Parameters

> None

### Json
> Json

### Responses

> | http code     | description           | content-type              | response                                                            |
> |---------------|-----------------------| --------------------------|---------------------------------------------------------------------|
> | `200/300/400`         | description    | `application/json`        | `{"status": 500,"error": "6001","message": "locación no existe"}`    |

### Example 

> ```json
>   {Example to make a request}
> ```

</details>

<details class='put'>
 <summary><code class='api_tag put'>PUT</code><b> /</b> Put description</summary>

### Description

A short summary of what it does, and metadata needed.

### Parameters

> None

### Json
> Json

### Responses

> | http code     | description           | content-type              | response                                                            |
> |---------------|-----------------------| --------------------------|---------------------------------------------------------------------|
> | `200/300/400`         | description    | `application/json`        | `{"status": 500,"error": "6001","message": "locación no existe"}`    |

### Example 

> ```json
>   {Example to make a request}
> ```

</details>


<details class='delete'>
 <summary><code class='api_tag delete'>DELETE</code><b> /</b> Delete description</summary>

### Description

A short summary of what it does, and metadata needed.

### Parameters

> None

### Json
> Json

### Responses

> | http code     | description           | content-type              | response                                                            |
> |---------------|-----------------------| --------------------------|---------------------------------------------------------------------|
> | `200/300/400`         | description    | `application/json`        | `{"status": 500,"error": "6001","message": "locación no existe"}`    |

### Example 

> ```json
>   {Example to make a request}
> ```

</details>


# Examples

## Creating new/overwriting existing stubs & proxy configs

<details class='post'>
 <summary><code class='api_tag post'>POST</code><b> /</b> (overwrites all in-memory stub and/or proxy-config)</summary>

### Parameters

> | name      |  type     | data type               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | None      |  required | object (JSON or YAML)   | N/A  |


### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `201`         | `text/plain;charset=UTF-8`        | `Configuration created successfully`                                |
> | `400`         | `application/json`                | `{"code":"400","message":"Bad Request"}`                            |
> | `405`         | `text/html;charset=utf-8`         | None                                                                |

### Example cURL

> ```javascript
>  curl -X POST -H "Content-Type: application/json" --data @post.json http://localhost:8889/
> ```

</details>

------------------------------------------------------------------------------------------

## Listing existing stubs & proxy configs as YAML string

<details class='post'>
   <summary><code class='api_tag post'>POST</code><b> /</b> (gets all in-memory stub & proxy configs)</summary>

### Parameters

> None

### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `text/plain;charset=UTF-8`        | YAML string                                                         |

### Example cURL

> ```javascript
>  curl -X GET -H "Content-Type: application/json" http://localhost:8889/
> ```

</details>

<details class='get'>
 <summary><code class='api_tag get'>GET</code><b> /</b> (gets stub by its resource-id-{stub_numeric_id} in the YAML config)</summary>
 

### Parameters

> | name              |  type     | data type      | description                         |
> |-------------------|-----------|----------------|-------------------------------------|
> | `stub_numeric_id` |  required | int ($int64)   | The specific stub numeric id        |

### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `text/plain;charset=UTF-8`        | YAML string                                                         |
> | `400`         | `application/json`                | `{"code":"400","message":"Bad Request"}`                            |

### Example cURL

> ```javascript
>  curl -X GET -H "Content-Type: application/json" http://localhost:8889/0
> ```

</details>

<details class='put'>
 <summary><code class='api_tag put'>PUT</code><b> /</b> (gets stub by its defined uuid property)</summary>

### Parameters

> | name   |  type      | data type      | description                                          |
> |--------|------------|----------------|------------------------------------------------------|
> | `uuid` |  required  | string         | The specific stub unique idendifier                  |

### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `text/plain;charset=UTF-8`        | YAML string                                                         |
> | `400`         | `application/json`                | `{"code":"400","message":"Bad Request"}`                            |

### Example cURL

> ```javascript
>  curl -X GET -H "Content-Type: application/json" http://localhost:8889/some-unique-uuid-string
> ```

</details>


<details class='delete'>
 <summary><code class='api_tag delete'>DELETE</code><b> /</b> (gets <b>default</b> proxy-config)</summary>

### Parameters

> None

### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `text/plain;charset=UTF-8`        | YAML string                                                         |
> | `400`         | `application/json`                | `{"code":"400","message":"Bad Request"}`                            |

### Example cURL

> ```javascript
>  curl -X GET -H "Content-Type: application/json" http://localhost:8889/proxy-config/default
> ```

</details>

------------------------------------------------------------------------------------------
