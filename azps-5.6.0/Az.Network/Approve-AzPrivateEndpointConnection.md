---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 3768bc8769d81056dc8f2de4f42f9f1783f89728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979642"
---
# <span data-ttu-id="dbd36-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dbd36-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="dbd36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd36-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd36-103">Zatwierdza prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="dbd36-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="dbd36-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dbd36-104">SYNTAX</span></span>

### <span data-ttu-id="dbd36-105">ByResourceId (Default)</span><span class="sxs-lookup"><span data-stu-id="dbd36-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbd36-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="dbd36-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbd36-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dbd36-107">DESCRIPTION</span></span>
<span data-ttu-id="dbd36-108">Polecenie cmdlet **Approve-AzPrivateEndpointConnection** zatwierdza prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="dbd36-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="dbd36-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dbd36-109">EXAMPLES</span></span>

### <span data-ttu-id="dbd36-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dbd36-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="dbd36-111">Ten przykład zatwierdza prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="dbd36-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="dbd36-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbd36-112">PARAMETERS</span></span>

### <span data-ttu-id="dbd36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd36-113">-DefaultProfile</span></span>
<span data-ttu-id="dbd36-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd36-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="dbd36-115">-Description</span></span>
<span data-ttu-id="dbd36-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="dbd36-116">The reason of action.</span></span>

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

### <span data-ttu-id="dbd36-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dbd36-117">-Name</span></span>
<span data-ttu-id="dbd36-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="dbd36-118">The resource name.</span></span>

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

### <span data-ttu-id="dbd36-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="dbd36-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="dbd36-120">Typ zasobu linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="dbd36-120">The private link resource type.</span></span>

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

### <span data-ttu-id="dbd36-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd36-121">-ResourceGroupName</span></span>
<span data-ttu-id="dbd36-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dbd36-122">The resource group name.</span></span>

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

### <span data-ttu-id="dbd36-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbd36-123">-ResourceId</span></span>
<span data-ttu-id="dbd36-124">Identyfikator menedżera zasobów platformy Azure prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="dbd36-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="dbd36-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dbd36-125">-ServiceName</span></span>
<span data-ttu-id="dbd36-126">Nazwa usługi prywatnego linku.</span><span class="sxs-lookup"><span data-stu-id="dbd36-126">The private link service name.</span></span>

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


### <span data-ttu-id="dbd36-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd36-127">CommonParameters</span></span>
<span data-ttu-id="dbd36-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd36-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd36-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbd36-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd36-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbd36-130">INPUTS</span></span>

### <span data-ttu-id="dbd36-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dbd36-131">System.String</span></span>

## <span data-ttu-id="dbd36-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbd36-132">OUTPUTS</span></span>

### <span data-ttu-id="dbd36-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dbd36-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="dbd36-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dbd36-134">NOTES</span></span>

## <span data-ttu-id="dbd36-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbd36-135">RELATED LINKS</span></span>

[<span data-ttu-id="dbd36-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dbd36-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="dbd36-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dbd36-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="dbd36-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dbd36-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="dbd36-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dbd36-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)