---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240507"
---
# <span data-ttu-id="3d31f-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3d31f-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="3d31f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d31f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d31f-103">Aktualizuje wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d31f-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="3d31f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3d31f-104">SYNTAX</span></span>

### <span data-ttu-id="3d31f-105">ByVirtualWanName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3d31f-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d31f-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="3d31f-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d31f-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="3d31f-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d31f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3d31f-108">DESCRIPTION</span></span>
<span data-ttu-id="3d31f-109">Aktualizuje wirtualną sieć WAN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d31f-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="3d31f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3d31f-110">EXAMPLES</span></span>

### <span data-ttu-id="3d31f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3d31f-111">Example 1</span></span>

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

<span data-ttu-id="3d31f-112">Powyższe spowoduje utworzenie grupy zasobów "testRG" w regionie "Zachód Usa" i wirtualnej sieci WAN platformy Azure w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="3d31f-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="3d31f-113">VirtualWan został zaktualizowany o nowe właściwości.</span><span class="sxs-lookup"><span data-stu-id="3d31f-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="3d31f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d31f-114">PARAMETERS</span></span>

### <span data-ttu-id="3d31f-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="3d31f-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="3d31f-116">Zezwalaj na ruch gałęzi do rozgałęzienia dla VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="3d31f-116">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="3d31f-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="3d31f-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="3d31f-118">Zezwalaj na ruch w sieci vnet dla virtualWan.</span><span class="sxs-lookup"><span data-stu-id="3d31f-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="3d31f-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3d31f-119">-AsJob</span></span>
<span data-ttu-id="3d31f-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3d31f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d31f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d31f-121">-DefaultProfile</span></span>
<span data-ttu-id="3d31f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d31f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d31f-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3d31f-123">-Force</span></span>
<span data-ttu-id="3d31f-124">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="3d31f-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3d31f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d31f-125">-InputObject</span></span>
<span data-ttu-id="3d31f-126">Obiekt wirtualny wan do modyfikacji</span><span class="sxs-lookup"><span data-stu-id="3d31f-126">The virtual wan object to be modified</span></span>

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

### <span data-ttu-id="3d31f-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3d31f-127">-Name</span></span>
<span data-ttu-id="3d31f-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3d31f-128">The resource name.</span></span>

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

### <span data-ttu-id="3d31f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d31f-129">-ResourceGroupName</span></span>
<span data-ttu-id="3d31f-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d31f-130">The resource group name.</span></span>

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

### <span data-ttu-id="3d31f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d31f-131">-ResourceId</span></span>
<span data-ttu-id="3d31f-132">Identyfikator zasobu Azure dla wirtualnej sieci Wan.</span><span class="sxs-lookup"><span data-stu-id="3d31f-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="3d31f-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="3d31f-133">-Tag</span></span>
<span data-ttu-id="3d31f-134">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d31f-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3d31f-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="3d31f-135">-VirtualWANType</span></span>
<span data-ttu-id="3d31f-136">Typ wirtualnej sieci Wan.</span><span class="sxs-lookup"><span data-stu-id="3d31f-136">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="3d31f-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d31f-137">-Confirm</span></span>
<span data-ttu-id="3d31f-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3d31f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d31f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d31f-139">-WhatIf</span></span>
<span data-ttu-id="3d31f-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d31f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d31f-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3d31f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d31f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d31f-142">CommonParameters</span></span>
<span data-ttu-id="3d31f-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d31f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d31f-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d31f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d31f-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d31f-145">INPUTS</span></span>

### <span data-ttu-id="3d31f-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3d31f-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="3d31f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3d31f-147">System.String</span></span>

## <span data-ttu-id="3d31f-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d31f-148">OUTPUTS</span></span>

### <span data-ttu-id="3d31f-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3d31f-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="3d31f-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3d31f-150">NOTES</span></span>

## <span data-ttu-id="3d31f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d31f-151">RELATED LINKS</span></span>

[<span data-ttu-id="3d31f-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3d31f-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="3d31f-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3d31f-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="3d31f-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="3d31f-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
