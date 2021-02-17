---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193355"
---
# <span data-ttu-id="f2209-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2209-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="f2209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2209-102">SYNOPSIS</span></span>
<span data-ttu-id="f2209-103">Aktualizuje stan prywatnego połączenia punktu końcowego w prywatnej usłudze linków.</span><span class="sxs-lookup"><span data-stu-id="f2209-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="f2209-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2209-104">SYNTAX</span></span>

### <span data-ttu-id="f2209-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="f2209-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2209-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="f2209-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2209-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2209-107">DESCRIPTION</span></span>
<span data-ttu-id="f2209-108">Polecenie **cmdlet Set-AzPrivateEndpointConnection** aktualizuje stan prywatnego połączenia punktu końcowego w prywatnej usłudze łączenia</span><span class="sxs-lookup"><span data-stu-id="f2209-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="f2209-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2209-109">EXAMPLES</span></span>

### <span data-ttu-id="f2209-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2209-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="f2209-111">W tym przykładzie stan połączenia prywatnego punktu końcowego jest aktualizowany na zatwierdzony.</span><span class="sxs-lookup"><span data-stu-id="f2209-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="f2209-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2209-112">PARAMETERS</span></span>

### <span data-ttu-id="f2209-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2209-113">-DefaultProfile</span></span>
<span data-ttu-id="f2209-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2209-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2209-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="f2209-115">-Description</span></span>
<span data-ttu-id="f2209-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="f2209-116">The reason of action.</span></span>

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

### <span data-ttu-id="f2209-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f2209-117">-Name</span></span>
<span data-ttu-id="f2209-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f2209-118">The resource name.</span></span>

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

### <span data-ttu-id="f2209-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="f2209-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="f2209-120">Typ zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="f2209-120">The private link resource type.</span></span>

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

### <span data-ttu-id="f2209-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="f2209-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="f2209-122">Zatwierdzono lub odrzucono zasób.</span><span class="sxs-lookup"><span data-stu-id="f2209-122">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2209-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2209-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2209-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2209-124">The resource group name.</span></span>

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

### <span data-ttu-id="f2209-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2209-125">-ResourceId</span></span>
<span data-ttu-id="f2209-126">Identyfikator menedżera zasobów platformy Azure prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="f2209-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f2209-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f2209-127">-ServiceName</span></span>
<span data-ttu-id="f2209-128">Nazwa usługi prywatnego linku.</span><span class="sxs-lookup"><span data-stu-id="f2209-128">The private link service name.</span></span>

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

### <span data-ttu-id="f2209-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2209-129">CommonParameters</span></span>
<span data-ttu-id="f2209-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2209-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2209-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2209-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2209-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2209-132">INPUTS</span></span>

### <span data-ttu-id="f2209-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f2209-133">System.String</span></span>

## <span data-ttu-id="f2209-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2209-134">OUTPUTS</span></span>

### <span data-ttu-id="f2209-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f2209-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="f2209-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2209-136">NOTES</span></span>

## <span data-ttu-id="f2209-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2209-137">RELATED LINKS</span></span>

[<span data-ttu-id="f2209-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2209-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f2209-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2209-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f2209-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2209-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f2209-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f2209-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)