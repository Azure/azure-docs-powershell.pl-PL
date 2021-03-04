---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 87647d504d47bf3f53b775d68b42ab617485f73d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979722"
---
# <span data-ttu-id="2073a-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2073a-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="2073a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2073a-102">SYNOPSIS</span></span>
<span data-ttu-id="2073a-103">Dodawanie elementu równorzędnego do programu Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2073a-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="2073a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2073a-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2073a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2073a-105">DESCRIPTION</span></span>
<span data-ttu-id="2073a-106">Polecenie **cmdlet Add-AzVirtualRouterPeer** dodaje element równorzędny VirtualRouter do elementu Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2073a-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="2073a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2073a-107">EXAMPLES</span></span>

### <span data-ttu-id="2073a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2073a-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="2073a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2073a-109">PARAMETERS</span></span>

### <span data-ttu-id="2073a-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2073a-110">-AsJob</span></span>
<span data-ttu-id="2073a-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2073a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2073a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2073a-112">-DefaultProfile</span></span>
<span data-ttu-id="2073a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2073a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2073a-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2073a-114">-Force</span></span>
<span data-ttu-id="2073a-115">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="2073a-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2073a-116">- PeerAsn</span><span class="sxs-lookup"><span data-stu-id="2073a-116">-PeerAsn</span></span>
<span data-ttu-id="2073a-117">Równorzędna asn.</span><span class="sxs-lookup"><span data-stu-id="2073a-117">Peer ASN.</span></span>

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

### <span data-ttu-id="2073a-118">— Komunikacja równorzędna</span><span class="sxs-lookup"><span data-stu-id="2073a-118">-PeerIp</span></span>
<span data-ttu-id="2073a-119">Adres IP współpracownika.</span><span class="sxs-lookup"><span data-stu-id="2073a-119">Peer Ip.</span></span>

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

### <span data-ttu-id="2073a-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2073a-120">-PeerName</span></span>
<span data-ttu-id="2073a-121">Nazwa komputera równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="2073a-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="2073a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2073a-122">-ResourceGroupName</span></span>
<span data-ttu-id="2073a-123">Nazwa grupy zasobów routera/elementu równorzędnego wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="2073a-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="2073a-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="2073a-124">-VirtualRouterName</span></span>
<span data-ttu-id="2073a-125">Router wirtualny, na którym istnieje serwer równorzędny.</span><span class="sxs-lookup"><span data-stu-id="2073a-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="2073a-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2073a-126">-Confirm</span></span>
<span data-ttu-id="2073a-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2073a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2073a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2073a-128">-WhatIf</span></span>
<span data-ttu-id="2073a-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2073a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2073a-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2073a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2073a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2073a-131">CommonParameters</span></span>
<span data-ttu-id="2073a-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2073a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2073a-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2073a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2073a-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2073a-134">INPUTS</span></span>

### <span data-ttu-id="2073a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2073a-135">System.String</span></span>

### <span data-ttu-id="2073a-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="2073a-136">System.UInt32</span></span>

## <span data-ttu-id="2073a-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2073a-137">OUTPUTS</span></span>

### <span data-ttu-id="2073a-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2073a-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="2073a-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2073a-139">NOTES</span></span>

## <span data-ttu-id="2073a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2073a-140">RELATED LINKS</span></span>
