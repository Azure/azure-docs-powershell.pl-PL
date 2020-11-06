---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
ms.openlocfilehash: 8d514ae4f01709d499c7685958cf13671e9b0c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553484"
---
# <span data-ttu-id="6ae32-101">New-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ae32-101">New-AzureRmVirtualWan</span></span>

## <span data-ttu-id="6ae32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ae32-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae32-103">Tworzy wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae32-103">Creates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ae32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ae32-104">SYNTAX</span></span>

```
New-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ae32-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ae32-105">DESCRIPTION</span></span>
<span data-ttu-id="6ae32-106">Tworzy nowy zasób usługi Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="6ae32-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="6ae32-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ae32-107">EXAMPLES</span></span>

### <span data-ttu-id="6ae32-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ae32-108">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="6ae32-109">Powyższy obszar utworzy grupę zasobów "testRG" w regionie "Zachodnia USA" oraz wirtualną sieć WAN w usłudze Azure z gałęzią do ruchu w gałęzi dozwolonym w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae32-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="6ae32-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ae32-110">PARAMETERS</span></span>

### <span data-ttu-id="6ae32-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="6ae32-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="6ae32-112">Zezwalanie na odgałęzienie do ruchu w oddziale dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="6ae32-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="6ae32-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="6ae32-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="6ae32-114">Zezwól sieci wirtualnej na ruch w sieci VNET dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="6ae32-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="6ae32-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ae32-115">-AsJob</span></span>
<span data-ttu-id="6ae32-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6ae32-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ae32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae32-117">-DefaultProfile</span></span>
<span data-ttu-id="6ae32-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae32-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae32-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6ae32-119">-Location</span></span>
<span data-ttu-id="6ae32-120">Lokalizacja zasobu VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="6ae32-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="6ae32-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ae32-121">-Name</span></span>
<span data-ttu-id="6ae32-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="6ae32-122">The resource name.</span></span>

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

### <span data-ttu-id="6ae32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ae32-123">-ResourceGroupName</span></span>
<span data-ttu-id="6ae32-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ae32-124">The resource group name.</span></span>

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

### <span data-ttu-id="6ae32-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ae32-125">-Tag</span></span>
<span data-ttu-id="6ae32-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ae32-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6ae32-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ae32-127">-Confirm</span></span>
<span data-ttu-id="6ae32-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ae32-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ae32-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ae32-129">-WhatIf</span></span>
<span data-ttu-id="6ae32-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ae32-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ae32-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ae32-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ae32-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae32-132">CommonParameters</span></span>
<span data-ttu-id="6ae32-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ae32-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae32-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ae32-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae32-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ae32-135">INPUTS</span></span>

### <span data-ttu-id="6ae32-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6ae32-136">System.String</span></span>

### <span data-ttu-id="6ae32-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ae32-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6ae32-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ae32-138">OUTPUTS</span></span>

### <span data-ttu-id="6ae32-139">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="6ae32-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="6ae32-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ae32-140">NOTES</span></span>

## <span data-ttu-id="6ae32-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ae32-141">RELATED LINKS</span></span>
