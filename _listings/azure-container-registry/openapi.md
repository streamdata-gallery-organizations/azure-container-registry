---
swagger: "2.0"
x-collection-name: Azure Container Registry
x-complete: 1
info:
  title: ContainerRegistryManagementClient
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/providers/Microsoft.ContainerRegistry/checkNameAvailability:
    post:
      summary: Registries Check Name Availability
      description: Checks whether the container registry name is available for use.
        The name must contain only alphanumeric characters, be globally unique, and
        between 5 and 60 characters in length.
      operationId: Registries_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoftcontainerregistrychecknameavailability-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: registryNameCheckRequest
        description: The object containing information for the availability request
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Registries
  /providers/Microsoft.ContainerRegistry/operations:
    get:
      summary: Operations List
      description: Lists all of the available Azure Container Registry REST API operations.
      operationId: Operations_List
      x-api-path-slug: providersmicrosoftcontainerregistryoperations-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Operation
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ContainerRegistry/registries/{registryName}
  : get:
      summary: Registries Get
      description: Gets the properties of the specified container registry.
      operationId: Registries_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftcontainerregistryregistriesregistryname-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Registries
    put:
      summary: Registries Create
      description: Creates a container registry with the specified parameters.
      operationId: Registries_Create
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftcontainerregistryregistriesregistryname-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: registryCreateParameters
        description: The parameters for creating a container registry
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Registries
    delete:
      summary: Registries Delete
      description: Deletes a container registry.
      operationId: Registries_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftcontainerregistryregistriesregistryname-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Registries
    patch:
      summary: Registries Update
      description: Updates a container registry with the specified parameters.
      operationId: Registries_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftcontainerregistryregistriesregistryname-patch
      parameters:
      - in: query
        name: No Name
      - in: body
        name: registryUpdateParameters
        description: The parameters for updating a container registry
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Registries
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ContainerRegistry/registries:
    get:
      summary: Registries List By Resource Group
      description: Lists all the container registries under the specified resource
        group.
      operationId: Registries_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftcontainerregistryregistries-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Registries
  /subscriptions/{subscriptionId}/providers/Microsoft.ContainerRegistry/registries:
    get:
      summary: Registries List
      description: Lists all the container registries under the specified subscription.
      operationId: Registries_List
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoftcontainerregistryregistries-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Registries
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ContainerRegistry/registries/{registryName}/listCredentials
  : post:
      summary: Registries List Credentials
      description: Lists the login credentials for the specified container registry.
      operationId: Registries_ListCredentials
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftcontainerregistryregistriesregistrynamelistcredentials-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Registries
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ContainerRegistry/registries/{registryName}/regenerateCredential
  : post:
      summary: Registries Regenerate Credential
      description: Regenerates one of the login credentials for the specified container
        registry.
      operationId: Registries_RegenerateCredential
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftcontainerregistryregistriesregistrynameregeneratecredential-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: regenerateCredentialParameters
        description: Specifies name of the password which should be regenerated --
          password or password2
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Registries
---