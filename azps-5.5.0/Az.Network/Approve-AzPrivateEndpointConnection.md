---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241066"
---
# <span data-ttu-id="424bb-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="424bb-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="424bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424bb-102">SYNOPSIS</span></span>
<span data-ttu-id="424bb-103">Zatwierdza prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="424bb-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="424bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="424bb-104">SYNTAX</span></span>

### <span data-ttu-id="424bb-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="424bb-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="424bb-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="424bb-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="424bb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="424bb-107">DESCRIPTION</span></span>
<span data-ttu-id="424bb-108">Polecenie cmdlet **Approve-AzPrivateEndpointConnection** zatwierdza prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="424bb-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="424bb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="424bb-109">EXAMPLES</span></span>

### <span data-ttu-id="424bb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="424bb-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="424bb-111">Ten przykład zatwierdza prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="424bb-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="424bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="424bb-112">PARAMETERS</span></span>

### <span data-ttu-id="424bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424bb-113">-DefaultProfile</span></span>
<span data-ttu-id="424bb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="424bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424bb-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="424bb-115">-Description</span></span>
<span data-ttu-id="424bb-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="424bb-116">The reason of action.</span></span>

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

### <span data-ttu-id="424bb-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="424bb-117">-Name</span></span>
<span data-ttu-id="424bb-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="424bb-118">The resource name.</span></span>

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

### <span data-ttu-id="424bb-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="424bb-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="424bb-120">Typ zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="424bb-120">The private link resource type.</span></span>

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

### <span data-ttu-id="424bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="424bb-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="424bb-122">The resource group name.</span></span>

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

### <span data-ttu-id="424bb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="424bb-123">-ResourceId</span></span>
<span data-ttu-id="424bb-124">Identyfikator menedżera zasobów platformy Azure prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="424bb-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="424bb-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="424bb-125">-ServiceName</span></span>
<span data-ttu-id="424bb-126">Nazwa usługi prywatnego linku.</span><span class="sxs-lookup"><span data-stu-id="424bb-126">The private link service name.</span></span>

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


### <span data-ttu-id="424bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424bb-127">CommonParameters</span></span>
<span data-ttu-id="424bb-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424bb-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="424bb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424bb-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="424bb-130">INPUTS</span></span>

### <span data-ttu-id="424bb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="424bb-131">System.String</span></span>

## <span data-ttu-id="424bb-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="424bb-132">OUTPUTS</span></span>

### <span data-ttu-id="424bb-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="424bb-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="424bb-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="424bb-134">NOTES</span></span>

## <span data-ttu-id="424bb-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="424bb-135">RELATED LINKS</span></span>

[<span data-ttu-id="424bb-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="424bb-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="424bb-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="424bb-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="424bb-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="424bb-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="424bb-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="424bb-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)