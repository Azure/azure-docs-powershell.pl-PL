---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052061"
---
# <span data-ttu-id="894a9-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="894a9-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="894a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="894a9-102">SYNOPSIS</span></span>
<span data-ttu-id="894a9-103">Aktualizuje stan połączenia prywatnego punktu końcowego w usłudze linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="894a9-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="894a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="894a9-104">SYNTAX</span></span>

### <span data-ttu-id="894a9-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="894a9-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="894a9-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="894a9-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="894a9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="894a9-107">DESCRIPTION</span></span>
<span data-ttu-id="894a9-108">Polecenie cmdlet **Set-AzPrivateEndpointConnection** aktualizuje stan połączenia prywatnego punktu końcowego w usłudze linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="894a9-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="894a9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="894a9-109">EXAMPLES</span></span>

### <span data-ttu-id="894a9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="894a9-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="894a9-111">W tym przykładzie Zaktualizowano stan połączenia prywatnego punktu końcowego na zatwierdzony.</span><span class="sxs-lookup"><span data-stu-id="894a9-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="894a9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="894a9-112">PARAMETERS</span></span>

### <span data-ttu-id="894a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894a9-113">-DefaultProfile</span></span>
<span data-ttu-id="894a9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="894a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="894a9-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="894a9-115">-Description</span></span>
<span data-ttu-id="894a9-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="894a9-116">The reason of action.</span></span>

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

### <span data-ttu-id="894a9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="894a9-117">-Name</span></span>
<span data-ttu-id="894a9-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="894a9-118">The resource name.</span></span>

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

### <span data-ttu-id="894a9-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="894a9-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="894a9-120">Typ zasobu link prywatny.</span><span class="sxs-lookup"><span data-stu-id="894a9-120">The private link resource type.</span></span>

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

### <span data-ttu-id="894a9-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="894a9-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="894a9-122">Zatwierdzono lub odrzucił zasób.</span><span class="sxs-lookup"><span data-stu-id="894a9-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="894a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="894a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="894a9-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="894a9-124">The resource group name.</span></span>

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

### <span data-ttu-id="894a9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="894a9-125">-ResourceId</span></span>
<span data-ttu-id="894a9-126">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="894a9-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="894a9-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="894a9-127">-ServiceName</span></span>
<span data-ttu-id="894a9-128">Nazwa usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="894a9-128">The private link service name.</span></span>

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

### <span data-ttu-id="894a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894a9-129">CommonParameters</span></span>
<span data-ttu-id="894a9-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894a9-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="894a9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894a9-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="894a9-132">INPUTS</span></span>

### <span data-ttu-id="894a9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="894a9-133">System.String</span></span>

## <span data-ttu-id="894a9-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="894a9-134">OUTPUTS</span></span>

### <span data-ttu-id="894a9-135">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="894a9-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="894a9-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="894a9-136">NOTES</span></span>

## <span data-ttu-id="894a9-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="894a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="894a9-138">Zatwierdzanie — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="894a9-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="894a9-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="894a9-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="894a9-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="894a9-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="894a9-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="894a9-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)