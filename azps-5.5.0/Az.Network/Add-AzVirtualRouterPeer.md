---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241083"
---
# <span data-ttu-id="e7a14-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="e7a14-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="e7a14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a14-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a14-103">Dodawanie elementu równorzędnego do programu Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e7a14-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="e7a14-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7a14-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7a14-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7a14-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a14-106">Polecenie **cmdlet Add-AzVirtualRouterPeer** dodaje element równorzędny VirtualRouter do elementu Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e7a14-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="e7a14-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7a14-107">EXAMPLES</span></span>

### <span data-ttu-id="e7a14-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7a14-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="e7a14-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7a14-109">PARAMETERS</span></span>

### <span data-ttu-id="e7a14-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e7a14-110">-AsJob</span></span>
<span data-ttu-id="e7a14-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e7a14-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7a14-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a14-112">-DefaultProfile</span></span>
<span data-ttu-id="e7a14-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a14-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a14-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e7a14-114">-Force</span></span>
<span data-ttu-id="e7a14-115">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="e7a14-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e7a14-116">- PeerAsn</span><span class="sxs-lookup"><span data-stu-id="e7a14-116">-PeerAsn</span></span>
<span data-ttu-id="e7a14-117">Równorzędna asn.</span><span class="sxs-lookup"><span data-stu-id="e7a14-117">Peer ASN.</span></span>

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

### <span data-ttu-id="e7a14-118">— Komunikacja równorzędna</span><span class="sxs-lookup"><span data-stu-id="e7a14-118">-PeerIp</span></span>
<span data-ttu-id="e7a14-119">Adres IP współpracownika.</span><span class="sxs-lookup"><span data-stu-id="e7a14-119">Peer Ip.</span></span>

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

### <span data-ttu-id="e7a14-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="e7a14-120">-PeerName</span></span>
<span data-ttu-id="e7a14-121">Nazwa komputera równorzędnego routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="e7a14-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="e7a14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a14-122">-ResourceGroupName</span></span>
<span data-ttu-id="e7a14-123">Nazwa grupy zasobów routera/elementu równorzędnego wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="e7a14-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="e7a14-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="e7a14-124">-VirtualRouterName</span></span>
<span data-ttu-id="e7a14-125">Router wirtualny, na którym istnieje serwer równorzędny.</span><span class="sxs-lookup"><span data-stu-id="e7a14-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="e7a14-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7a14-126">-Confirm</span></span>
<span data-ttu-id="e7a14-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7a14-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a14-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a14-128">-WhatIf</span></span>
<span data-ttu-id="e7a14-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a14-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a14-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e7a14-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a14-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a14-131">CommonParameters</span></span>
<span data-ttu-id="e7a14-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a14-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a14-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7a14-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a14-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7a14-134">INPUTS</span></span>

### <span data-ttu-id="e7a14-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e7a14-135">System.String</span></span>

### <span data-ttu-id="e7a14-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="e7a14-136">System.UInt32</span></span>

## <span data-ttu-id="e7a14-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7a14-137">OUTPUTS</span></span>

### <span data-ttu-id="e7a14-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e7a14-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e7a14-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7a14-139">NOTES</span></span>

## <span data-ttu-id="e7a14-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7a14-140">RELATED LINKS</span></span>
