---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051485"
---
# <span data-ttu-id="2c76f-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c76f-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="2c76f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c76f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c76f-103">Zatwierdza połączenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2c76f-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="2c76f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c76f-104">SYNTAX</span></span>

### <span data-ttu-id="2c76f-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2c76f-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c76f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="2c76f-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c76f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2c76f-107">DESCRIPTION</span></span>
<span data-ttu-id="2c76f-108">Polecenie cmdlet **zatwierdzanie — AzPrivateEndpointConnection** umożliwia zatwierdzenie prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2c76f-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="2c76f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c76f-109">EXAMPLES</span></span>

### <span data-ttu-id="2c76f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c76f-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="2c76f-111">W tym przykładzie zaakceptowano prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2c76f-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="2c76f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c76f-112">PARAMETERS</span></span>

### <span data-ttu-id="2c76f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c76f-113">-DefaultProfile</span></span>
<span data-ttu-id="2c76f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c76f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c76f-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="2c76f-115">-Description</span></span>
<span data-ttu-id="2c76f-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="2c76f-116">The reason of action.</span></span>

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

### <span data-ttu-id="2c76f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c76f-117">-Name</span></span>
<span data-ttu-id="2c76f-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2c76f-118">The resource name.</span></span>

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

### <span data-ttu-id="2c76f-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="2c76f-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="2c76f-120">Typ zasobu link prywatny.</span><span class="sxs-lookup"><span data-stu-id="2c76f-120">The private link resource type.</span></span>

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

### <span data-ttu-id="2c76f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c76f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2c76f-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c76f-122">The resource group name.</span></span>

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

### <span data-ttu-id="2c76f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c76f-123">-ResourceId</span></span>
<span data-ttu-id="2c76f-124">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="2c76f-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="2c76f-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2c76f-125">-ServiceName</span></span>
<span data-ttu-id="2c76f-126">Nazwa usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="2c76f-126">The private link service name.</span></span>

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


### <span data-ttu-id="2c76f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c76f-127">CommonParameters</span></span>
<span data-ttu-id="2c76f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c76f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c76f-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c76f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c76f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c76f-130">INPUTS</span></span>

### <span data-ttu-id="2c76f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2c76f-131">System.String</span></span>

## <span data-ttu-id="2c76f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c76f-132">OUTPUTS</span></span>

### <span data-ttu-id="2c76f-133">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2c76f-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="2c76f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c76f-134">NOTES</span></span>

## <span data-ttu-id="2c76f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c76f-135">RELATED LINKS</span></span>

[<span data-ttu-id="2c76f-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c76f-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2c76f-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c76f-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2c76f-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c76f-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2c76f-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c76f-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)