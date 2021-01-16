---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344173"
---
# <span data-ttu-id="7afed-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7afed-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="7afed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7afed-102">SYNOPSIS</span></span>
<span data-ttu-id="7afed-103">Aktualizuje stan połączenia prywatnego punktu końcowego w usłudze linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="7afed-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="7afed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7afed-104">SYNTAX</span></span>

### <span data-ttu-id="7afed-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7afed-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7afed-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="7afed-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7afed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7afed-107">DESCRIPTION</span></span>
<span data-ttu-id="7afed-108">Polecenie cmdlet **Set-AzPrivateEndpointConnection** aktualizuje stan połączenia prywatnego punktu końcowego w usłudze linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="7afed-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="7afed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7afed-109">EXAMPLES</span></span>

### <span data-ttu-id="7afed-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7afed-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="7afed-111">W tym przykładzie Zaktualizowano stan połączenia prywatnego punktu końcowego na zatwierdzony.</span><span class="sxs-lookup"><span data-stu-id="7afed-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="7afed-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7afed-112">PARAMETERS</span></span>

### <span data-ttu-id="7afed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7afed-113">-DefaultProfile</span></span>
<span data-ttu-id="7afed-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7afed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7afed-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="7afed-115">-Description</span></span>
<span data-ttu-id="7afed-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="7afed-116">The reason of action.</span></span>

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

### <span data-ttu-id="7afed-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7afed-117">-Name</span></span>
<span data-ttu-id="7afed-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7afed-118">The resource name.</span></span>

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

### <span data-ttu-id="7afed-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="7afed-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="7afed-120">Typ zasobu link prywatny.</span><span class="sxs-lookup"><span data-stu-id="7afed-120">The private link resource type.</span></span>

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

### <span data-ttu-id="7afed-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="7afed-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="7afed-122">Zatwierdzono lub odrzucił zasób.</span><span class="sxs-lookup"><span data-stu-id="7afed-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="7afed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7afed-123">-ResourceGroupName</span></span>
<span data-ttu-id="7afed-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7afed-124">The resource group name.</span></span>

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

### <span data-ttu-id="7afed-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7afed-125">-ResourceId</span></span>
<span data-ttu-id="7afed-126">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="7afed-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7afed-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7afed-127">-ServiceName</span></span>
<span data-ttu-id="7afed-128">Nazwa usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="7afed-128">The private link service name.</span></span>

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

### <span data-ttu-id="7afed-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7afed-129">CommonParameters</span></span>
<span data-ttu-id="7afed-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7afed-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7afed-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7afed-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7afed-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7afed-132">INPUTS</span></span>

### <span data-ttu-id="7afed-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7afed-133">System.String</span></span>

## <span data-ttu-id="7afed-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7afed-134">OUTPUTS</span></span>

### <span data-ttu-id="7afed-135">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7afed-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="7afed-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7afed-136">NOTES</span></span>

## <span data-ttu-id="7afed-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7afed-137">RELATED LINKS</span></span>

[<span data-ttu-id="7afed-138">Zatwierdzanie — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7afed-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7afed-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7afed-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7afed-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7afed-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7afed-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7afed-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)