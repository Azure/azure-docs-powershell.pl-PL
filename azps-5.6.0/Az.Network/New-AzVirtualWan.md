---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 3bb2a2d7c8e53cc7ba336234e3c5b24ad58e2faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995331"
---
# <span data-ttu-id="47f9f-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="47f9f-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="47f9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="47f9f-103">Tworzy wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47f9f-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="47f9f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47f9f-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47f9f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="47f9f-105">DESCRIPTION</span></span>
<span data-ttu-id="47f9f-106">Tworzy nowy zasób Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="47f9f-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="47f9f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47f9f-107">EXAMPLES</span></span>

### <span data-ttu-id="47f9f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47f9f-108">Example 1</span></span>

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

<span data-ttu-id="47f9f-109">Powyższe spowoduje utworzenie grupy zasobów "testRG" w regionie "Zachód Stanów Zjednoczonych" i wirtualnej sieci WAN platformy Azure z ruchem rozgałęzieniowym dozwolonym w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="47f9f-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="47f9f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47f9f-110">PARAMETERS</span></span>

### <span data-ttu-id="47f9f-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="47f9f-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="47f9f-112">Zezwalaj na ruch gałęzi dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="47f9f-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="47f9f-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="47f9f-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="47f9f-114">Zezwalaj na ruch w sieci vnet dla virtualWan.</span><span class="sxs-lookup"><span data-stu-id="47f9f-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="47f9f-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="47f9f-115">-AsJob</span></span>
<span data-ttu-id="47f9f-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="47f9f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47f9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f9f-117">-DefaultProfile</span></span>
<span data-ttu-id="47f9f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47f9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47f9f-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="47f9f-119">-Location</span></span>
<span data-ttu-id="47f9f-120">Lokalizacja zasobu VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="47f9f-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="47f9f-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="47f9f-121">-Name</span></span>
<span data-ttu-id="47f9f-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="47f9f-122">The resource name.</span></span>

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

### <span data-ttu-id="47f9f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f9f-123">-ResourceGroupName</span></span>
<span data-ttu-id="47f9f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47f9f-124">The resource group name.</span></span>

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

### <span data-ttu-id="47f9f-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="47f9f-125">-Tag</span></span>
<span data-ttu-id="47f9f-126">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="47f9f-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="47f9f-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="47f9f-127">-VirtualWANType</span></span>
<span data-ttu-id="47f9f-128">Typ wirtualnej sieci Wan.</span><span class="sxs-lookup"><span data-stu-id="47f9f-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="47f9f-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47f9f-129">-Confirm</span></span>
<span data-ttu-id="47f9f-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="47f9f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47f9f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47f9f-131">-WhatIf</span></span>
<span data-ttu-id="47f9f-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47f9f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47f9f-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="47f9f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47f9f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f9f-134">CommonParameters</span></span>
<span data-ttu-id="47f9f-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47f9f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f9f-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47f9f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f9f-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47f9f-137">INPUTS</span></span>

### <span data-ttu-id="47f9f-138">Brak</span><span class="sxs-lookup"><span data-stu-id="47f9f-138">None</span></span>

## <span data-ttu-id="47f9f-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47f9f-139">OUTPUTS</span></span>

### <span data-ttu-id="47f9f-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="47f9f-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="47f9f-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47f9f-141">NOTES</span></span>

## <span data-ttu-id="47f9f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47f9f-142">RELATED LINKS</span></span>

[<span data-ttu-id="47f9f-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="47f9f-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="47f9f-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="47f9f-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="47f9f-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="47f9f-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
