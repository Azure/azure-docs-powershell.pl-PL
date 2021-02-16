---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 04611df4dd315c972d9e32b280d635a6ecd0ed21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197483"
---
# <span data-ttu-id="77522-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="77522-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="77522-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77522-102">SYNOPSIS</span></span>
<span data-ttu-id="77522-103">Aktualizowanie właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="77522-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="77522-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="77522-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77522-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="77522-105">DESCRIPTION</span></span>
<span data-ttu-id="77522-106">Polecenie **cmdlet Update-AzStorageAccountNetworkRuleSet** aktualizuje właściwość NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="77522-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="77522-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="77522-107">EXAMPLES</span></span>

### <span data-ttu-id="77522-108">Przykład 1. Aktualizowanie wszystkich właściwości właściwości NetworkRule, reguł wprowadzania przy użyciu JSON</span><span class="sxs-lookup"><span data-stu-id="77522-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="77522-109">To polecenie aktualizuje wszystkie właściwości polecenia NetworkRule, czyli reguły wprowadzania z wartością JSON.</span><span class="sxs-lookup"><span data-stu-id="77522-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="77522-110">Przykład 2. Aktualizowanie właściwości Obejścia dla właściwości NetworkRule</span><span class="sxs-lookup"><span data-stu-id="77522-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="77522-111">To polecenie aktualizuj właściwość Obejścia dla właściwości NetworkRule (inne właściwości nie zmienią się).</span><span class="sxs-lookup"><span data-stu-id="77522-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="77522-112">Przykład 3. Oczyszczanie reguł NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="77522-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="77522-113">To polecenie oczyszcza reguły NetworkRule konta magazynu (inne właściwości się nie zmieniają).</span><span class="sxs-lookup"><span data-stu-id="77522-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="77522-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77522-114">PARAMETERS</span></span>

### <span data-ttu-id="77522-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="77522-115">-AsJob</span></span>
<span data-ttu-id="77522-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="77522-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77522-117">— Obejście</span><span class="sxs-lookup"><span data-stu-id="77522-117">-Bypass</span></span>
<span data-ttu-id="77522-118">Wartość obejścia do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="77522-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="77522-119">Dozwolona wartość nie jest dowolną kombinacją: • Rejestrowanie • Metryki • Usługi Azure</span><span class="sxs-lookup"><span data-stu-id="77522-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77522-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="77522-120">-DefaultAction</span></span>
<span data-ttu-id="77522-121">Wartość Akcji Domyślnej do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="77522-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="77522-122">Dozwolone opcje: • Zezwalaj • Odmów</span><span class="sxs-lookup"><span data-stu-id="77522-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77522-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77522-123">-DefaultProfile</span></span>
<span data-ttu-id="77522-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="77522-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77522-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="77522-125">-IPRule</span></span>
<span data-ttu-id="77522-126">Tablica obiektów IpRule, które mają być aktualizowane na właściwość NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="77522-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77522-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="77522-127">-Name</span></span>
<span data-ttu-id="77522-128">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="77522-128">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77522-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77522-129">-ResourceGroupName</span></span>
<span data-ttu-id="77522-130">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="77522-130">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77522-131">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="77522-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="77522-132">Tablica obiektów VirtualNetworkRule w celu zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="77522-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77522-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77522-133">-Confirm</span></span>
<span data-ttu-id="77522-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="77522-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77522-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77522-135">-WhatIf</span></span>
<span data-ttu-id="77522-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77522-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77522-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="77522-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77522-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77522-138">CommonParameters</span></span>
<span data-ttu-id="77522-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77522-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77522-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77522-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77522-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77522-141">INPUTS</span></span>

### <span data-ttu-id="77522-142">System.String</span><span class="sxs-lookup"><span data-stu-id="77522-142">System.String</span></span>

### <span data-ttu-id="77522-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="77522-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="77522-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="77522-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="77522-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77522-145">OUTPUTS</span></span>

### <span data-ttu-id="77522-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="77522-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="77522-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="77522-147">NOTES</span></span>

## <span data-ttu-id="77522-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77522-148">RELATED LINKS</span></span>
