---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
ms.openlocfilehash: 3f62cf755ac06efe9ed5f04a6657a36cfe612abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541652"
---
# <span data-ttu-id="db302-101">Update-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="db302-101">Update-AzureRmVirtualWan</span></span>

## <span data-ttu-id="db302-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db302-102">SYNOPSIS</span></span>
<span data-ttu-id="db302-103">Aktualizuje wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="db302-103">Updates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db302-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db302-104">SYNTAX</span></span>

### <span data-ttu-id="db302-105">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="db302-105">ByVirtualWanName (Default)</span></span>
```
Update-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db302-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="db302-106">ByVirtualWanObject</span></span>
```
Update-AzureRmVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db302-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="db302-107">ByVirtualWanResourceId</span></span>
```
Update-AzureRmVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db302-108">Opis</span><span class="sxs-lookup"><span data-stu-id="db302-108">DESCRIPTION</span></span>
<span data-ttu-id="db302-109">Aktualizuje wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="db302-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="db302-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db302-110">EXAMPLES</span></span>

### <span data-ttu-id="db302-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="db302-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="db302-112">Powyższy obszar utworzy grupę zasobów "testRG" w regionie "Zachodnia USA" oraz wirtualną sieć WAN platformy Azure w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="db302-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="db302-113">VirtualWan jest aktualizowany nowymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="db302-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="db302-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db302-114">PARAMETERS</span></span>

### <span data-ttu-id="db302-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="db302-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="db302-116">Zezwalanie na odgałęzienie do ruchu w oddziale dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="db302-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db302-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="db302-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="db302-118">Zezwól sieci wirtualnej na ruch w sieci VNET dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="db302-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db302-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db302-119">-AsJob</span></span>
<span data-ttu-id="db302-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="db302-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db302-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db302-121">-DefaultProfile</span></span>
<span data-ttu-id="db302-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db302-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db302-123">-Force</span><span class="sxs-lookup"><span data-stu-id="db302-123">-Force</span></span>
<span data-ttu-id="db302-124">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="db302-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="db302-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="db302-125">-InputObject</span></span>
<span data-ttu-id="db302-126">Wirtualny obiekt sieci WAN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="db302-126">The virtual wan object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db302-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db302-127">-Name</span></span>
<span data-ttu-id="db302-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="db302-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db302-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db302-129">-ResourceGroupName</span></span>
<span data-ttu-id="db302-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="db302-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db302-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db302-131">-ResourceId</span></span>
<span data-ttu-id="db302-132">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="db302-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db302-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="db302-133">-Tag</span></span>
<span data-ttu-id="db302-134">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="db302-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db302-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="db302-135">-Confirm</span></span>
<span data-ttu-id="db302-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db302-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db302-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db302-137">-WhatIf</span></span>
<span data-ttu-id="db302-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db302-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db302-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="db302-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db302-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db302-140">CommonParameters</span></span>
<span data-ttu-id="db302-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db302-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db302-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db302-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db302-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db302-143">INPUTS</span></span>

### <span data-ttu-id="db302-144">System. String</span><span class="sxs-lookup"><span data-stu-id="db302-144">System.String</span></span>

### <span data-ttu-id="db302-145">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="db302-145">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="db302-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="db302-146">System.Collections.Hashtable</span></span>

## <span data-ttu-id="db302-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db302-147">OUTPUTS</span></span>

### <span data-ttu-id="db302-148">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="db302-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="db302-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db302-149">NOTES</span></span>

## <span data-ttu-id="db302-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db302-150">RELATED LINKS</span></span>
