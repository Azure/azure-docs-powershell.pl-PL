---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 17ace5a209a34fc65d79efaac0bfb477e00b2472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709218"
---
# <span data-ttu-id="8b10e-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8b10e-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="8b10e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b10e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b10e-103">Tworzy wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b10e-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="8b10e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b10e-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b10e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b10e-105">DESCRIPTION</span></span>
<span data-ttu-id="8b10e-106">Tworzy nowy zasób usługi Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="8b10e-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="8b10e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b10e-107">EXAMPLES</span></span>

### <span data-ttu-id="8b10e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b10e-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="8b10e-109">Powyższy obszar utworzy grupę zasobów "testRG" w regionie "Zachodnia USA" oraz wirtualną sieć WAN w usłudze Azure z gałęzią do ruchu w gałęzi dozwolonym w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8b10e-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="8b10e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b10e-110">PARAMETERS</span></span>

### <span data-ttu-id="8b10e-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="8b10e-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="8b10e-112">Zezwalanie na odgałęzienie do ruchu w oddziale dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="8b10e-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="8b10e-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="8b10e-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="8b10e-114">Zezwól sieci wirtualnej na ruch w sieci VNET dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="8b10e-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="8b10e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b10e-115">-AsJob</span></span>
<span data-ttu-id="8b10e-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8b10e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b10e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b10e-117">-DefaultProfile</span></span>
<span data-ttu-id="8b10e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b10e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b10e-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8b10e-119">-Location</span></span>
<span data-ttu-id="8b10e-120">Lokalizacja zasobu VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="8b10e-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b10e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b10e-121">-Name</span></span>
<span data-ttu-id="8b10e-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8b10e-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b10e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b10e-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b10e-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b10e-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b10e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b10e-125">-Tag</span></span>
<span data-ttu-id="8b10e-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b10e-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8b10e-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b10e-127">-Confirm</span></span>
<span data-ttu-id="8b10e-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b10e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b10e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b10e-129">-WhatIf</span></span>
<span data-ttu-id="8b10e-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b10e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b10e-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b10e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b10e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b10e-132">CommonParameters</span></span>
<span data-ttu-id="8b10e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b10e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b10e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b10e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b10e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b10e-135">INPUTS</span></span>

### <span data-ttu-id="8b10e-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8b10e-136">None</span></span>

## <span data-ttu-id="8b10e-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b10e-137">OUTPUTS</span></span>

### <span data-ttu-id="8b10e-138">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8b10e-138">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="8b10e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b10e-139">NOTES</span></span>

## <span data-ttu-id="8b10e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b10e-140">RELATED LINKS</span></span>

[<span data-ttu-id="8b10e-141">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8b10e-141">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="8b10e-142">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8b10e-142">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="8b10e-143">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8b10e-143">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
