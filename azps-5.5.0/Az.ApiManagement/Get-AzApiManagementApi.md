---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176515"
---
# <span data-ttu-id="9e508-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9e508-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="9e508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e508-102">SYNOPSIS</span></span>
<span data-ttu-id="9e508-103">Otrzymuje interfejs API.</span><span class="sxs-lookup"><span data-stu-id="9e508-103">Gets an API.</span></span>

## <span data-ttu-id="9e508-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e508-104">SYNTAX</span></span>

### <span data-ttu-id="9e508-105">GetAllApis (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9e508-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e508-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="9e508-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e508-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="9e508-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e508-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="9e508-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e508-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="9e508-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e508-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e508-110">DESCRIPTION</span></span>
<span data-ttu-id="9e508-111">Polecenie **cmdlet Get-AzApiManagementApi** otrzymuje co najmniej jeden interfejs API usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9e508-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="9e508-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e508-112">EXAMPLES</span></span>

### <span data-ttu-id="9e508-113">Przykład 1. Uzyskiwanie wszystkich interfejsów API zarządzania</span><span class="sxs-lookup"><span data-stu-id="9e508-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="9e508-114">To polecenie pobiera wszystkie interfejsy API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="9e508-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="9e508-115">Przykład 2. Uzyskiwanie interfejsu API zarządzania według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="9e508-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="9e508-116">To polecenie pobiera interfejs API o określonym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="9e508-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="9e508-117">Przykład 3. Uzyskiwanie interfejsu API zarządzania według nazwy</span><span class="sxs-lookup"><span data-stu-id="9e508-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="9e508-118">To polecenie pobiera interfejs API o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="9e508-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="9e508-119">Przykład 4. Uzyskiwanie interfejsu API zarządzania według bramy GatewayId</span><span class="sxs-lookup"><span data-stu-id="9e508-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="9e508-120">To polecenie pobiera interfejs API dla określonego wartości GatewayId.</span><span class="sxs-lookup"><span data-stu-id="9e508-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="9e508-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e508-121">PARAMETERS</span></span>

### <span data-ttu-id="9e508-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9e508-122">-ApiId</span></span>
<span data-ttu-id="9e508-123">Określa identyfikator interfejsu API do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="9e508-123">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e508-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="9e508-124">-ApiRevision</span></span>
<span data-ttu-id="9e508-125">Identyfikator poprawek określonej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9e508-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="9e508-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9e508-126">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e508-127">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9e508-127">-Context</span></span>
<span data-ttu-id="9e508-128">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="9e508-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e508-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e508-129">-DefaultProfile</span></span>
<span data-ttu-id="9e508-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e508-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e508-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9e508-131">-GatewayId</span></span>
<span data-ttu-id="9e508-132">Jeśli zostanie określona, spróbuje uzyskać wszystkie interfejsy API bramy.</span><span class="sxs-lookup"><span data-stu-id="9e508-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e508-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9e508-133">-Name</span></span>
<span data-ttu-id="9e508-134">Określa nazwę interfejsu API do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="9e508-134">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e508-135">- ProductId</span><span class="sxs-lookup"><span data-stu-id="9e508-135">-ProductId</span></span>
<span data-ttu-id="9e508-136">Określa identyfikator produktu, dla którego ma być uzyskiwanie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9e508-136">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e508-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e508-137">CommonParameters</span></span>
<span data-ttu-id="9e508-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e508-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e508-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e508-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e508-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e508-140">INPUTS</span></span>

### <span data-ttu-id="9e508-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9e508-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e508-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9e508-142">System.String</span></span>

## <span data-ttu-id="9e508-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e508-143">OUTPUTS</span></span>

### <span data-ttu-id="9e508-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9e508-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9e508-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e508-145">NOTES</span></span>

## <span data-ttu-id="9e508-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e508-146">RELATED LINKS</span></span>

[<span data-ttu-id="9e508-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9e508-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="9e508-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9e508-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="9e508-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9e508-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="9e508-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9e508-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="9e508-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9e508-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


