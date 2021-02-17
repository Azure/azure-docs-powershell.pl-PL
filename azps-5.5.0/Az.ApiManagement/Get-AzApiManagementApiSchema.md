---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192547"
---
# <span data-ttu-id="0df7f-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0df7f-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="0df7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0df7f-102">SYNOPSIS</span></span>
<span data-ttu-id="0df7f-103">Uzyskiwanie szczegółowych informacji o schemacie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0df7f-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="0df7f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0df7f-104">SYNTAX</span></span>

### <span data-ttu-id="0df7f-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0df7f-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0df7f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df7f-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0df7f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0df7f-107">DESCRIPTION</span></span>
<span data-ttu-id="0df7f-108">Polecenie **cmdlet Get-AzApiManagementApiSchema** pobiera szczegóły schematu interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0df7f-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="0df7f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0df7f-109">EXAMPLES</span></span>

### <span data-ttu-id="0df7f-110">Przykład 1. Uzyskiwanie szczegółów całego schematu interfejsu API interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0df7f-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="0df7f-111">To polecenie pobiera wszystkie schematy interfejsu API skojarzone z interfejsem API `swagger-petstore-extensive` dla określonego kontekstu ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0df7f-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="0df7f-112">Przykład 2. Uzyskiwanie określonego schematu skojarzonego z interfejsem API</span><span class="sxs-lookup"><span data-stu-id="0df7f-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="0df7f-113">To polecenie pobiera schemat interfejsu API skojarzony z interfejsem API dla określonego kontekstu `5cc9cf67e6ed3b1154e638bd` `swagger-petstore-extensive` ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0df7f-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="0df7f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0df7f-114">PARAMETERS</span></span>

### <span data-ttu-id="0df7f-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0df7f-115">-ApiId</span></span>
<span data-ttu-id="0df7f-116">Identyfikator API do wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="0df7f-116">API identifier to look for.</span></span>
<span data-ttu-id="0df7f-117">Jeśli zostanie określona, spróbuje uzyskać interfejs API za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="0df7f-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df7f-118">— kontekst</span><span class="sxs-lookup"><span data-stu-id="0df7f-118">-Context</span></span>
<span data-ttu-id="0df7f-119">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0df7f-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0df7f-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0df7f-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0df7f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df7f-121">-DefaultProfile</span></span>
<span data-ttu-id="0df7f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0df7f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df7f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0df7f-123">-ResourceId</span></span>
<span data-ttu-id="0df7f-124">Identyfikator zasobu arm schematu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0df7f-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="0df7f-125">Jeśli zostanie określona, spróbuje znaleźć schemat interfejsu API za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="0df7f-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="0df7f-126">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0df7f-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df7f-127">- SchemaId</span><span class="sxs-lookup"><span data-stu-id="0df7f-127">-SchemaId</span></span>
<span data-ttu-id="0df7f-128">Identyfikator schematu.</span><span class="sxs-lookup"><span data-stu-id="0df7f-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df7f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df7f-129">CommonParameters</span></span>
<span data-ttu-id="0df7f-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df7f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df7f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0df7f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df7f-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0df7f-132">INPUTS</span></span>

### <span data-ttu-id="0df7f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0df7f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0df7f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0df7f-134">System.String</span></span>

## <span data-ttu-id="0df7f-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0df7f-135">OUTPUTS</span></span>

### <span data-ttu-id="0df7f-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0df7f-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="0df7f-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0df7f-137">NOTES</span></span>

## <span data-ttu-id="0df7f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0df7f-138">RELATED LINKS</span></span>

[<span data-ttu-id="0df7f-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0df7f-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="0df7f-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0df7f-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="0df7f-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0df7f-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)