---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 5e1cbec98e2b501a71f022766f7248c3209d590f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991747"
---
# <span data-ttu-id="3ea59-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ea59-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="3ea59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ea59-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea59-103">Otrzymuje interfejs API.</span><span class="sxs-lookup"><span data-stu-id="3ea59-103">Gets an API.</span></span>

## <span data-ttu-id="3ea59-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3ea59-104">SYNTAX</span></span>

### <span data-ttu-id="3ea59-105">GetAllApis (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3ea59-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ea59-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="3ea59-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ea59-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="3ea59-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ea59-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="3ea59-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ea59-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="3ea59-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ea59-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="3ea59-110">DESCRIPTION</span></span>
<span data-ttu-id="3ea59-111">Polecenie **cmdlet Get-AzApiManagementApi** otrzymuje co najmniej jeden interfejs API usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="3ea59-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="3ea59-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3ea59-112">EXAMPLES</span></span>

### <span data-ttu-id="3ea59-113">Przykład 1. Uzyskiwanie wszystkich interfejsów API zarządzania</span><span class="sxs-lookup"><span data-stu-id="3ea59-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="3ea59-114">To polecenie pobiera wszystkie interfejsy API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="3ea59-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="3ea59-115">Przykład 2. Uzyskiwanie interfejsu API zarządzania według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="3ea59-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="3ea59-116">To polecenie pobiera interfejs API o określonym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="3ea59-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="3ea59-117">Przykład 3. Uzyskiwanie interfejsu API zarządzania według nazwy</span><span class="sxs-lookup"><span data-stu-id="3ea59-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="3ea59-118">To polecenie pobiera interfejs API o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="3ea59-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="3ea59-119">Przykład 4. Uzyskiwanie interfejsu API zarządzania według bramy GatewayId</span><span class="sxs-lookup"><span data-stu-id="3ea59-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="3ea59-120">To polecenie pobiera interfejs API dla określonego wartości GatewayId.</span><span class="sxs-lookup"><span data-stu-id="3ea59-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="3ea59-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ea59-121">PARAMETERS</span></span>

### <span data-ttu-id="3ea59-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3ea59-122">-ApiId</span></span>
<span data-ttu-id="3ea59-123">Określa identyfikator interfejsu API do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="3ea59-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="3ea59-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="3ea59-124">-ApiRevision</span></span>
<span data-ttu-id="3ea59-125">Identyfikator poprawek określonej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="3ea59-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="3ea59-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3ea59-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ea59-127">— kontekst</span><span class="sxs-lookup"><span data-stu-id="3ea59-127">-Context</span></span>
<span data-ttu-id="3ea59-128">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3ea59-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3ea59-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea59-129">-DefaultProfile</span></span>
<span data-ttu-id="3ea59-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea59-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ea59-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3ea59-131">-GatewayId</span></span>
<span data-ttu-id="3ea59-132">Jeśli zostanie określona, spróbuje uzyskać wszystkie interfejsy API bramy.</span><span class="sxs-lookup"><span data-stu-id="3ea59-132">If specified will try to get all Gateway APIs.</span></span>

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

### <span data-ttu-id="3ea59-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3ea59-133">-Name</span></span>
<span data-ttu-id="3ea59-134">Określa nazwę interfejsu API do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="3ea59-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="3ea59-135">- ProductId</span><span class="sxs-lookup"><span data-stu-id="3ea59-135">-ProductId</span></span>
<span data-ttu-id="3ea59-136">Określa identyfikator produktu, dla którego ma być uzyskiwanie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="3ea59-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="3ea59-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea59-137">CommonParameters</span></span>
<span data-ttu-id="3ea59-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea59-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea59-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ea59-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea59-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ea59-140">INPUTS</span></span>

### <span data-ttu-id="3ea59-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ea59-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3ea59-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3ea59-142">System.String</span></span>

## <span data-ttu-id="3ea59-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ea59-143">OUTPUTS</span></span>

### <span data-ttu-id="3ea59-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ea59-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="3ea59-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3ea59-145">NOTES</span></span>

## <span data-ttu-id="3ea59-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ea59-146">RELATED LINKS</span></span>

[<span data-ttu-id="3ea59-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ea59-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="3ea59-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ea59-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="3ea59-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ea59-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="3ea59-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ea59-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="3ea59-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3ea59-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


