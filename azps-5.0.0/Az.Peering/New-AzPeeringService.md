---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225003"
---
# <span data-ttu-id="8da44-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="8da44-101">New-AzPeeringService</span></span>

## <span data-ttu-id="8da44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8da44-102">SYNOPSIS</span></span>
<span data-ttu-id="8da44-103">Tworzy nową usługę peer.</span><span class="sxs-lookup"><span data-stu-id="8da44-103">Creates a new peering service.</span></span>

## <span data-ttu-id="8da44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8da44-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da44-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8da44-105">DESCRIPTION</span></span>
<span data-ttu-id="8da44-106">Tworzy usługę peer.</span><span class="sxs-lookup"><span data-stu-id="8da44-106">Creates peering service.</span></span>

## <span data-ttu-id="8da44-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8da44-107">EXAMPLES</span></span>

### <span data-ttu-id="8da44-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8da44-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="8da44-109">Tworzy obiekt usługi peer dla dostawców i lokalizacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="8da44-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="8da44-110">Używanie w conjuction z `Get-AzPeeringServiceProvider` i `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="8da44-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="8da44-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8da44-111">PARAMETERS</span></span>

### <span data-ttu-id="8da44-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8da44-112">-AsJob</span></span>
<span data-ttu-id="8da44-113">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="8da44-113">Run in the background.</span></span>

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

### <span data-ttu-id="8da44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da44-114">-DefaultProfile</span></span>
<span data-ttu-id="8da44-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8da44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8da44-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8da44-116">-Name</span></span>
<span data-ttu-id="8da44-117">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="8da44-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da44-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8da44-118">-PeeringLocation</span></span>
<span data-ttu-id="8da44-119">Lokalizacja fizyczna różna od obszaru Azure region.</span><span class="sxs-lookup"><span data-stu-id="8da44-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="8da44-120">Użyj Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="8da44-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da44-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="8da44-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="8da44-122">Nazwa dostawcy usługi Peer-Name.</span><span class="sxs-lookup"><span data-stu-id="8da44-122">The peering service provider name.</span></span>
<span data-ttu-id="8da44-123">Używanie polecenia cmdlet Get-AzPeeringServiceProvider dla listy</span><span class="sxs-lookup"><span data-stu-id="8da44-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da44-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da44-124">-ResourceGroupName</span></span>
<span data-ttu-id="8da44-125">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8da44-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da44-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="8da44-126">-Tag</span></span>
<span data-ttu-id="8da44-127">Tagi, które mają zostać skojarzone z usługą Microsoft Inputobject.</span><span class="sxs-lookup"><span data-stu-id="8da44-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da44-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8da44-128">-Confirm</span></span>
<span data-ttu-id="8da44-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da44-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da44-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da44-130">-WhatIf</span></span>
<span data-ttu-id="8da44-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da44-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8da44-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8da44-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da44-133">CommonParameters</span></span>
<span data-ttu-id="8da44-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da44-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8da44-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da44-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8da44-136">INPUTS</span></span>

### <span data-ttu-id="8da44-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8da44-137">None</span></span>

## <span data-ttu-id="8da44-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8da44-138">OUTPUTS</span></span>

### <span data-ttu-id="8da44-139">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="8da44-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="8da44-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8da44-140">NOTES</span></span>

## <span data-ttu-id="8da44-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8da44-141">RELATED LINKS</span></span>
