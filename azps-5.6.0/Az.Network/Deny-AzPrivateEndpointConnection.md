---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 1522e8d9c66ccd2429ab331e1f39d26c06da5930
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978410"
---
# <span data-ttu-id="05829-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05829-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="05829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05829-102">SYNOPSIS</span></span>
<span data-ttu-id="05829-103">odmawia prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="05829-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="05829-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="05829-104">SYNTAX</span></span>

### <span data-ttu-id="05829-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="05829-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05829-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="05829-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05829-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="05829-107">DESCRIPTION</span></span>
<span data-ttu-id="05829-108">Polecenie cmdlet **Deny-AzPrivateEndpointConnection** odrzuca prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="05829-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="05829-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="05829-109">EXAMPLES</span></span>

### <span data-ttu-id="05829-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05829-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="05829-111">W tym przykładzie jest odrzucane prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="05829-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="05829-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05829-112">PARAMETERS</span></span>

### <span data-ttu-id="05829-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05829-113">-DefaultProfile</span></span>
<span data-ttu-id="05829-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="05829-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05829-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="05829-115">-Description</span></span>
<span data-ttu-id="05829-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="05829-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05829-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="05829-117">-Name</span></span>
<span data-ttu-id="05829-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="05829-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05829-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="05829-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="05829-120">Typ zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="05829-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05829-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05829-121">-ResourceGroupName</span></span>
<span data-ttu-id="05829-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05829-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05829-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05829-123">-ResourceId</span></span>
<span data-ttu-id="05829-124">Identyfikator menedżera zasobów platformy Azure prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="05829-124">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05829-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="05829-125">-ServiceName</span></span>
<span data-ttu-id="05829-126">Nazwa usługi, do której należy prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="05829-126">The name of service that private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05829-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05829-127">CommonParameters</span></span>
<span data-ttu-id="05829-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05829-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05829-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05829-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05829-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05829-130">INPUTS</span></span>

### <span data-ttu-id="05829-131">System.String</span><span class="sxs-lookup"><span data-stu-id="05829-131">System.String</span></span>

## <span data-ttu-id="05829-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05829-132">OUTPUTS</span></span>

### <span data-ttu-id="05829-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="05829-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="05829-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="05829-134">NOTES</span></span>

## <span data-ttu-id="05829-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05829-135">RELATED LINKS</span></span>

[<span data-ttu-id="05829-136">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05829-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="05829-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05829-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="05829-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05829-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="05829-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05829-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)