---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498782"
---
# <span data-ttu-id="3bc86-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3bc86-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="3bc86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bc86-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc86-103">Dodawanie elementu równorzędnego do usługi Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3bc86-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="3bc86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bc86-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bc86-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3bc86-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc86-106">Polecenie cmdlet **Add-AzVirtualRouterPeer** dodaje VirtualRouter peer do usługi Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3bc86-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="3bc86-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bc86-107">EXAMPLES</span></span>

### <span data-ttu-id="3bc86-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3bc86-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="3bc86-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bc86-109">PARAMETERS</span></span>

### <span data-ttu-id="3bc86-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bc86-110">-AsJob</span></span>
<span data-ttu-id="3bc86-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3bc86-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc86-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc86-112">-DefaultProfile</span></span>
<span data-ttu-id="3bc86-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc86-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc86-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3bc86-114">-Force</span></span>
<span data-ttu-id="3bc86-115">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="3bc86-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc86-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="3bc86-116">-PeerAsn</span></span>
<span data-ttu-id="3bc86-117">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="3bc86-117">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc86-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="3bc86-118">-PeerIp</span></span>
<span data-ttu-id="3bc86-119">Adres IP elementu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="3bc86-119">Peer Ip.</span></span>

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

### <span data-ttu-id="3bc86-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="3bc86-120">-PeerName</span></span>
<span data-ttu-id="3bc86-121">Nazwa węzła równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="3bc86-121">The name of the virtual router Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc86-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc86-122">-ResourceGroupName</span></span>
<span data-ttu-id="3bc86-123">Nazwa grupy zasobów wirtualnego routera/elementu równorzędnego.</span><span class="sxs-lookup"><span data-stu-id="3bc86-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="3bc86-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="3bc86-124">-VirtualRouterName</span></span>
<span data-ttu-id="3bc86-125">Router wirtualny, na którym znajduje się element równorzędny.</span><span class="sxs-lookup"><span data-stu-id="3bc86-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="3bc86-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bc86-126">-Confirm</span></span>
<span data-ttu-id="3bc86-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc86-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc86-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc86-128">-WhatIf</span></span>
<span data-ttu-id="3bc86-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc86-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bc86-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3bc86-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc86-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc86-131">CommonParameters</span></span>
<span data-ttu-id="3bc86-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc86-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc86-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bc86-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc86-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bc86-134">INPUTS</span></span>

### <span data-ttu-id="3bc86-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc86-135">System.String</span></span>

### <span data-ttu-id="3bc86-136">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="3bc86-136">System.UInt32</span></span>

## <span data-ttu-id="3bc86-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bc86-137">OUTPUTS</span></span>

### <span data-ttu-id="3bc86-138">Microsoft. Azure. Commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3bc86-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="3bc86-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bc86-139">NOTES</span></span>

## <span data-ttu-id="3bc86-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bc86-140">RELATED LINKS</span></span>
