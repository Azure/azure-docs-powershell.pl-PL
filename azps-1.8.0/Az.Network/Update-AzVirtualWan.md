---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: 3a1d30f3ae44b0e6893682cf0c1d700207682803
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708889"
---
# <span data-ttu-id="8a6b1-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8a6b1-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="8a6b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6b1-103">Aktualizuje wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="8a6b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a6b1-104">SYNTAX</span></span>

### <span data-ttu-id="8a6b1-105">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a6b1-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6b1-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="8a6b1-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6b1-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="8a6b1-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a6b1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8a6b1-108">DESCRIPTION</span></span>
<span data-ttu-id="8a6b1-109">Aktualizuje wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="8a6b1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a6b1-110">EXAMPLES</span></span>

### <span data-ttu-id="8a6b1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a6b1-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="8a6b1-112">Powyższy obszar utworzy grupę zasobów "testRG" w regionie "Zachodnia USA" oraz wirtualną sieć WAN platformy Azure w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="8a6b1-113">VirtualWan jest aktualizowany nowymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="8a6b1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a6b1-114">PARAMETERS</span></span>

### <span data-ttu-id="8a6b1-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="8a6b1-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="8a6b1-116">Zezwalanie na odgałęzienie do ruchu w oddziale dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-116">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="8a6b1-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="8a6b1-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="8a6b1-118">Zezwól sieci wirtualnej na ruch w sieci VNET dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="8a6b1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a6b1-119">-AsJob</span></span>
<span data-ttu-id="8a6b1-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8a6b1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a6b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6b1-121">-DefaultProfile</span></span>
<span data-ttu-id="8a6b1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a6b1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8a6b1-123">-Force</span></span>
<span data-ttu-id="8a6b1-124">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="8a6b1-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="8a6b1-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8a6b1-125">-InputObject</span></span>
<span data-ttu-id="8a6b1-126">Wirtualny obiekt sieci WAN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="8a6b1-126">The virtual wan object to be modified</span></span>

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

### <span data-ttu-id="8a6b1-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a6b1-127">-Name</span></span>
<span data-ttu-id="8a6b1-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-128">The resource name.</span></span>

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

### <span data-ttu-id="8a6b1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6b1-129">-ResourceGroupName</span></span>
<span data-ttu-id="8a6b1-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-130">The resource group name.</span></span>

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

### <span data-ttu-id="8a6b1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a6b1-131">-ResourceId</span></span>
<span data-ttu-id="8a6b1-132">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="8a6b1-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a6b1-133">-Tag</span></span>
<span data-ttu-id="8a6b1-134">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8a6b1-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a6b1-135">-Confirm</span></span>
<span data-ttu-id="8a6b1-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a6b1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a6b1-137">-WhatIf</span></span>
<span data-ttu-id="8a6b1-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a6b1-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a6b1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6b1-140">CommonParameters</span></span>
<span data-ttu-id="8a6b1-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a6b1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6b1-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a6b1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6b1-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a6b1-143">INPUTS</span></span>

### <span data-ttu-id="8a6b1-144">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8a6b1-144">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="8a6b1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8a6b1-145">System.String</span></span>

## <span data-ttu-id="8a6b1-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a6b1-146">OUTPUTS</span></span>

### <span data-ttu-id="8a6b1-147">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8a6b1-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="8a6b1-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a6b1-148">NOTES</span></span>

## <span data-ttu-id="8a6b1-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a6b1-149">RELATED LINKS</span></span>

[<span data-ttu-id="8a6b1-150">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8a6b1-150">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="8a6b1-151">Nowe — AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8a6b1-151">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="8a6b1-152">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="8a6b1-152">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
