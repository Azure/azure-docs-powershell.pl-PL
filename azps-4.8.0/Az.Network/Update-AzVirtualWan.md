---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220464"
---
# <span data-ttu-id="c3fbc-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3fbc-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="c3fbc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fbc-103">Aktualizuje wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c3fbc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3fbc-104">SYNTAX</span></span>

### <span data-ttu-id="c3fbc-105">ByVirtualWanName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c3fbc-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fbc-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="c3fbc-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fbc-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="c3fbc-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3fbc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c3fbc-108">DESCRIPTION</span></span>
<span data-ttu-id="c3fbc-109">Aktualizuje wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c3fbc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3fbc-110">EXAMPLES</span></span>

### <span data-ttu-id="c3fbc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3fbc-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="c3fbc-112">Powyższy obszar utworzy grupę zasobów "testRG" w regionie "Zachodnia USA" oraz wirtualną sieć WAN platformy Azure w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="c3fbc-113">VirtualWan jest aktualizowany nowymi właściwościami.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="c3fbc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3fbc-114">PARAMETERS</span></span>

### <span data-ttu-id="c3fbc-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="c3fbc-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="c3fbc-116">Zezwalanie na odgałęzienie do ruchu w oddziale dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fbc-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="c3fbc-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="c3fbc-118">Zezwól sieci wirtualnej na ruch w sieci VNET dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fbc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3fbc-119">-AsJob</span></span>
<span data-ttu-id="c3fbc-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c3fbc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3fbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fbc-121">-DefaultProfile</span></span>
<span data-ttu-id="c3fbc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3fbc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c3fbc-123">-Force</span></span>
<span data-ttu-id="c3fbc-124">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="c3fbc-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c3fbc-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3fbc-125">-InputObject</span></span>
<span data-ttu-id="c3fbc-126">Wirtualny obiekt sieci WAN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="c3fbc-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fbc-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3fbc-127">-Name</span></span>
<span data-ttu-id="c3fbc-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fbc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3fbc-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3fbc-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fbc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3fbc-131">-ResourceId</span></span>
<span data-ttu-id="c3fbc-132">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fbc-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3fbc-133">-Tag</span></span>
<span data-ttu-id="c3fbc-134">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c3fbc-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="c3fbc-135">-VirtualWANType</span></span>
<span data-ttu-id="c3fbc-136">Typ wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-136">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="c3fbc-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3fbc-137">-Confirm</span></span>
<span data-ttu-id="c3fbc-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3fbc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3fbc-139">-WhatIf</span></span>
<span data-ttu-id="c3fbc-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3fbc-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3fbc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fbc-142">CommonParameters</span></span>
<span data-ttu-id="c3fbc-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3fbc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fbc-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3fbc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fbc-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3fbc-145">INPUTS</span></span>

### <span data-ttu-id="c3fbc-146">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3fbc-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="c3fbc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c3fbc-147">System.String</span></span>

## <span data-ttu-id="c3fbc-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3fbc-148">OUTPUTS</span></span>

### <span data-ttu-id="c3fbc-149">Microsoft. Azure. Commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3fbc-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="c3fbc-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3fbc-150">NOTES</span></span>

## <span data-ttu-id="c3fbc-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3fbc-151">RELATED LINKS</span></span>

[<span data-ttu-id="c3fbc-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3fbc-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="c3fbc-153">Nowe — AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3fbc-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="c3fbc-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c3fbc-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
