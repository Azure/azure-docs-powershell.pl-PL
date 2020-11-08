---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233318"
---
# <span data-ttu-id="e8ea1-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e8ea1-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="e8ea1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ea1-103">Zatwierdza połączenie prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="e8ea1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8ea1-104">SYNTAX</span></span>

### <span data-ttu-id="e8ea1-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8ea1-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ea1-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="e8ea1-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ea1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e8ea1-107">DESCRIPTION</span></span>
<span data-ttu-id="e8ea1-108">Polecenie cmdlet **zatwierdzanie — AzPrivateEndpointConnection** umożliwia zatwierdzenie prywatnego połączenia punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="e8ea1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8ea1-109">EXAMPLES</span></span>

### <span data-ttu-id="e8ea1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8ea1-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="e8ea1-111">W tym przykładzie zaakceptowano prywatne połączenie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="e8ea1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8ea1-112">PARAMETERS</span></span>

### <span data-ttu-id="e8ea1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ea1-113">-DefaultProfile</span></span>
<span data-ttu-id="e8ea1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ea1-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="e8ea1-115">-Description</span></span>
<span data-ttu-id="e8ea1-116">Przyczyna działania.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-116">The reason of action.</span></span>

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

### <span data-ttu-id="e8ea1-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8ea1-117">-Name</span></span>
<span data-ttu-id="e8ea1-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-118">The resource name.</span></span>

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

### <span data-ttu-id="e8ea1-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="e8ea1-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="e8ea1-120">Typ zasobu link prywatny.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-120">The private link resource type.</span></span>

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

### <span data-ttu-id="e8ea1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ea1-121">-ResourceGroupName</span></span>
<span data-ttu-id="e8ea1-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-122">The resource group name.</span></span>

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

### <span data-ttu-id="e8ea1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8ea1-123">-ResourceId</span></span>
<span data-ttu-id="e8ea1-124">Identyfikator Menedżera zasobów platformy Azure połączenia z prywatnym punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="e8ea1-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e8ea1-125">-ServiceName</span></span>
<span data-ttu-id="e8ea1-126">Nazwa usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-126">The private link service name.</span></span>

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


### <span data-ttu-id="e8ea1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ea1-127">CommonParameters</span></span>
<span data-ttu-id="e8ea1-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ea1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ea1-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8ea1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ea1-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8ea1-130">INPUTS</span></span>

### <span data-ttu-id="e8ea1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ea1-131">System.String</span></span>

## <span data-ttu-id="e8ea1-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8ea1-132">OUTPUTS</span></span>

### <span data-ttu-id="e8ea1-133">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e8ea1-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="e8ea1-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8ea1-134">NOTES</span></span>

## <span data-ttu-id="e8ea1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8ea1-135">RELATED LINKS</span></span>

[<span data-ttu-id="e8ea1-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e8ea1-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e8ea1-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e8ea1-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e8ea1-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e8ea1-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e8ea1-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e8ea1-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)