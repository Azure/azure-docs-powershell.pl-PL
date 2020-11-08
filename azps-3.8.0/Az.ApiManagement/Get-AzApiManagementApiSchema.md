---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 7b28a9ff44251e84656411d6322eb87eac9f4991
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050915"
---
# <span data-ttu-id="3e1a1-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3e1a1-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="3e1a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1a1-103">Uzyskiwanie szczegółowych informacji o schemacie API</span><span class="sxs-lookup"><span data-stu-id="3e1a1-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="3e1a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e1a1-104">SYNTAX</span></span>

### <span data-ttu-id="3e1a1-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e1a1-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e1a1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e1a1-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e1a1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3e1a1-107">DESCRIPTION</span></span>
<span data-ttu-id="3e1a1-108">Polecenie cmdlet **Get-AzApiManagementApiSchema** pobiera szczegóły schematu API</span><span class="sxs-lookup"><span data-stu-id="3e1a1-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="3e1a1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e1a1-109">EXAMPLES</span></span>

### <span data-ttu-id="3e1a1-110">Przykład 1: uzyskiwanie szczegółów dotyczących wszystkich schematów API interfejsu API</span><span class="sxs-lookup"><span data-stu-id="3e1a1-110">Example 1 : Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="3e1a1-111">To polecenie pobiera wszystkie schematy API skojarzone z interfejsem API `swagger-petstore-extensive` dla określonego kontekstu ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="3e1a1-112">Przykład 2: uzyskiwanie określonego schematu skojarzonego z interfejsem API</span><span class="sxs-lookup"><span data-stu-id="3e1a1-112">Example 2 : Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="3e1a1-113">To polecenie uzyskuje schemat API `5cc9cf67e6ed3b1154e638bd` skojarzony z interfejsem API `swagger-petstore-extensive` dla określonego kontekstu ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="3e1a1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e1a1-114">PARAMETERS</span></span>

### <span data-ttu-id="3e1a1-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3e1a1-115">-ApiId</span></span>
<span data-ttu-id="3e1a1-116">Identyfikator API do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-116">API identifier to look for.</span></span>
<span data-ttu-id="3e1a1-117">Jeśli zostanie określona, spróbuje uzyskać interfejs API o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="3e1a1-118">-Context</span><span class="sxs-lookup"><span data-stu-id="3e1a1-118">-Context</span></span>
<span data-ttu-id="3e1a1-119">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3e1a1-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-120">This parameter is required.</span></span>

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

### <span data-ttu-id="3e1a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1a1-121">-DefaultProfile</span></span>
<span data-ttu-id="3e1a1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e1a1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e1a1-123">-ResourceId</span></span>
<span data-ttu-id="3e1a1-124">Identyfikator zasobu ARM schematu API.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="3e1a1-125">Jeśli zostanie określona, spróbuje znaleźć schemat API o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="3e1a1-126">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-126">This parameter is required.</span></span>

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

### <span data-ttu-id="3e1a1-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="3e1a1-127">-SchemaId</span></span>
<span data-ttu-id="3e1a1-128">Identyfikator schematu.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="3e1a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1a1-129">CommonParameters</span></span>
<span data-ttu-id="3e1a1-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1a1-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e1a1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1a1-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e1a1-132">INPUTS</span></span>

### <span data-ttu-id="3e1a1-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e1a1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3e1a1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3e1a1-134">System.String</span></span>

## <span data-ttu-id="3e1a1-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e1a1-135">OUTPUTS</span></span>

### <span data-ttu-id="3e1a1-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3e1a1-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="3e1a1-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e1a1-137">NOTES</span></span>

## <span data-ttu-id="3e1a1-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e1a1-138">RELATED LINKS</span></span>

[<span data-ttu-id="3e1a1-139">Nowe — AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3e1a1-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="3e1a1-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3e1a1-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="3e1a1-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3e1a1-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)