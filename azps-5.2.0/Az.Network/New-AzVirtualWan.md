---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362677"
---
# <span data-ttu-id="ae163-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae163-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="ae163-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae163-102">SYNOPSIS</span></span>
<span data-ttu-id="ae163-103">Tworzy wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ae163-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="ae163-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae163-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae163-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae163-105">DESCRIPTION</span></span>
<span data-ttu-id="ae163-106">Tworzy nowy zasób usługi Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="ae163-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="ae163-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae163-107">EXAMPLES</span></span>

### <span data-ttu-id="ae163-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae163-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="ae163-109">Powyższy obszar utworzy grupę zasobów "testRG" w regionie "Zachodnia USA" oraz wirtualną sieć WAN w usłudze Azure z gałęzią do ruchu w gałęzi dozwolonym w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ae163-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="ae163-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae163-110">PARAMETERS</span></span>

### <span data-ttu-id="ae163-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="ae163-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="ae163-112">Zezwalanie na odgałęzienie do ruchu w oddziale dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="ae163-112">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="ae163-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="ae163-114">Zezwól sieci wirtualnej na ruch w sieci VNET dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="ae163-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae163-115">-AsJob</span></span>
<span data-ttu-id="ae163-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ae163-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae163-117">-DefaultProfile</span></span>
<span data-ttu-id="ae163-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae163-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ae163-119">-Location</span></span>
<span data-ttu-id="ae163-120">Lokalizacja zasobu VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="ae163-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae163-121">-Name</span></span>
<span data-ttu-id="ae163-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ae163-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae163-123">-ResourceGroupName</span></span>
<span data-ttu-id="ae163-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae163-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae163-125">-Tag</span></span>
<span data-ttu-id="ae163-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae163-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="ae163-127">-VirtualWANType</span></span>
<span data-ttu-id="ae163-128">Typ wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="ae163-128">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae163-129">-Confirm</span></span>
<span data-ttu-id="ae163-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae163-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae163-131">-WhatIf</span></span>
<span data-ttu-id="ae163-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae163-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae163-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae163-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae163-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae163-134">CommonParameters</span></span>
<span data-ttu-id="ae163-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae163-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae163-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae163-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae163-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae163-137">INPUTS</span></span>

### <span data-ttu-id="ae163-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ae163-138">None</span></span>

## <span data-ttu-id="ae163-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae163-139">OUTPUTS</span></span>

### <span data-ttu-id="ae163-140">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae163-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="ae163-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae163-141">NOTES</span></span>

## <span data-ttu-id="ae163-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae163-142">RELATED LINKS</span></span>

[<span data-ttu-id="ae163-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae163-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="ae163-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae163-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="ae163-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae163-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
