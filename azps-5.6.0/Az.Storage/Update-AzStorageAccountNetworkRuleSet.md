---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 03e6169a9e69b9f2faa3dfaccba934428f7db4e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973290"
---
# <span data-ttu-id="41845-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="41845-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="41845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41845-102">SYNOPSIS</span></span>
<span data-ttu-id="41845-103">Aktualizowanie właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="41845-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="41845-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="41845-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-ResourceAccessRule <PSResourceAccessRule[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41845-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="41845-105">DESCRIPTION</span></span>
<span data-ttu-id="41845-106">Polecenie **cmdlet Update-AzStorageAccountNetworkRuleSet** aktualizuje właściwość NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="41845-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="41845-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="41845-107">EXAMPLES</span></span>

### <span data-ttu-id="41845-108">Przykład 1. Aktualizowanie wszystkich właściwości właściwości NetworkRule, reguł wprowadzania przy użyciu JSON</span><span class="sxs-lookup"><span data-stu-id="41845-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"}) -ResourceAccessRule (@{ResourceId=$ResourceId1;TenantId=$tenantId1},@{ResourceId=$ResourceId2;TenantId=$tenantId1})
```

<span data-ttu-id="41845-109">To polecenie aktualizuje wszystkie właściwości właściwości NetworkRule, czyli reguł wprowadzania przy użyciu JSON.</span><span class="sxs-lookup"><span data-stu-id="41845-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="41845-110">Przykład 2. Aktualizowanie właściwości Obejścia dla właściwości NetworkRule</span><span class="sxs-lookup"><span data-stu-id="41845-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="41845-111">To polecenie aktualizuj właściwość Obejścia dla właściwości NetworkRule (inne właściwości nie zmienią się).</span><span class="sxs-lookup"><span data-stu-id="41845-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="41845-112">Przykład 3. Oczyszczanie reguł NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="41845-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @() -ResourceAccessRule @()
```

<span data-ttu-id="41845-113">To polecenie oczyszczanie reguł NetworkRule konta magazynu (inne właściwości nie zmieniają się).</span><span class="sxs-lookup"><span data-stu-id="41845-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="41845-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41845-114">PARAMETERS</span></span>

### <span data-ttu-id="41845-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="41845-115">-AsJob</span></span>
<span data-ttu-id="41845-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="41845-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41845-117">— Obejście</span><span class="sxs-lookup"><span data-stu-id="41845-117">-Bypass</span></span>
<span data-ttu-id="41845-118">Wartość obejścia do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="41845-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="41845-119">Dozwolona wartość nie jest dowolną kombinacją: • Rejestrowanie • Metryki • Usługi Azure</span><span class="sxs-lookup"><span data-stu-id="41845-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="41845-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="41845-120">-DefaultAction</span></span>
<span data-ttu-id="41845-121">Wartość Akcji Domyślnej do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="41845-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="41845-122">Dozwolone opcje: • Zezwalaj • Odmów</span><span class="sxs-lookup"><span data-stu-id="41845-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="41845-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41845-123">-DefaultProfile</span></span>
<span data-ttu-id="41845-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="41845-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41845-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="41845-125">-IPRule</span></span>
<span data-ttu-id="41845-126">Tablica obiektów IpRule, które mają być aktualizowane na właściwość NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="41845-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="41845-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="41845-127">-Name</span></span>
<span data-ttu-id="41845-128">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="41845-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="41845-129">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="41845-129">-ResourceAccessRule</span></span>
<span data-ttu-id="41845-130">Konto magazynu NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="41845-130">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41845-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41845-131">-ResourceGroupName</span></span>
<span data-ttu-id="41845-132">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="41845-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="41845-133">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="41845-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="41845-134">Tablica obiektów VirtualNetworkRule w celu zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="41845-134">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="41845-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41845-135">-Confirm</span></span>
<span data-ttu-id="41845-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="41845-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41845-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41845-137">-WhatIf</span></span>
<span data-ttu-id="41845-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41845-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41845-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="41845-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41845-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41845-140">CommonParameters</span></span>
<span data-ttu-id="41845-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41845-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41845-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41845-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41845-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41845-143">INPUTS</span></span>

### <span data-ttu-id="41845-144">System.String</span><span class="sxs-lookup"><span data-stu-id="41845-144">System.String</span></span>

### <span data-ttu-id="41845-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="41845-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="41845-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="41845-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="41845-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41845-147">OUTPUTS</span></span>

### <span data-ttu-id="41845-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="41845-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="41845-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="41845-149">NOTES</span></span>

## <span data-ttu-id="41845-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41845-150">RELATED LINKS</span></span>
