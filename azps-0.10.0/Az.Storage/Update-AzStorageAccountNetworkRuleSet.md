---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: b92da8f6128ecc58a8e85d5e8f3f92347fd8dce1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891977"
---
# <span data-ttu-id="28430-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="28430-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="28430-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28430-102">SYNOPSIS</span></span>
<span data-ttu-id="28430-103">Aktualizowanie właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="28430-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="28430-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28430-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28430-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28430-105">DESCRIPTION</span></span>
<span data-ttu-id="28430-106">Polecenie cmdlet **Update-AzStorageAccountNetworkRuleSet** aktualizuje właściwość NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="28430-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="28430-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28430-107">EXAMPLES</span></span>

### <span data-ttu-id="28430-108">Przykład 1: aktualizowanie wszystkich właściwości NetworkRule, reguły wprowadzania za pomocą notacji JSON</span><span class="sxs-lookup"><span data-stu-id="28430-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="28430-109">To polecenie aktualizuje wszystkie właściwości NetworkRule, reguły wprowadzania za pomocą notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="28430-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="28430-110">Przykład 2: aktualizowanie właściwości Bypass dla NetworkRule</span><span class="sxs-lookup"><span data-stu-id="28430-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="28430-111">To polecenie umożliwia zaktualizowanie właściwości Bypass NetworkRule (inne właściwości nie zostaną zmienione).</span><span class="sxs-lookup"><span data-stu-id="28430-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="28430-112">Przykład 3: porządkowanie reguł NetworkRule z konta magazynu</span><span class="sxs-lookup"><span data-stu-id="28430-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="28430-113">To polecenie czyści reguły NetworkRule konta magazynu (inne właściwości nie zmieniają się).</span><span class="sxs-lookup"><span data-stu-id="28430-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="28430-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28430-114">PARAMETERS</span></span>

### <span data-ttu-id="28430-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28430-115">-AsJob</span></span>
<span data-ttu-id="28430-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="28430-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28430-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="28430-117">-Bypass</span></span>
<span data-ttu-id="28430-118">Wartość pomijania do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="28430-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="28430-119">Dozwolona wartość to brak lub dowolna kombinacja: • rejestrowanie • metryki • Azureservices</span><span class="sxs-lookup"><span data-stu-id="28430-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="28430-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="28430-120">-DefaultAction</span></span>
<span data-ttu-id="28430-121">Wartość DefaultAction do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="28430-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="28430-122">Dozwolone opcje: • Zezwalaj • Odmawiaj</span><span class="sxs-lookup"><span data-stu-id="28430-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28430-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28430-123">-DefaultProfile</span></span>
<span data-ttu-id="28430-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28430-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28430-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="28430-125">-IPRule</span></span>
<span data-ttu-id="28430-126">Tablica obiektów IpRule, które mają zostać zaktualizowane do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="28430-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="28430-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28430-127">-Name</span></span>
<span data-ttu-id="28430-128">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="28430-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="28430-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28430-129">-ResourceGroupName</span></span>
<span data-ttu-id="28430-130">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="28430-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="28430-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="28430-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="28430-132">Tablica obiektów VirtualNetworkRule, które mają zostać zaktualizowane do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="28430-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="28430-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28430-133">-Confirm</span></span>
<span data-ttu-id="28430-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28430-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28430-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28430-135">-WhatIf</span></span>
<span data-ttu-id="28430-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28430-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28430-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28430-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28430-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28430-138">CommonParameters</span></span>
<span data-ttu-id="28430-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28430-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28430-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28430-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28430-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28430-141">INPUTS</span></span>

### <span data-ttu-id="28430-142">System. String</span><span class="sxs-lookup"><span data-stu-id="28430-142">System.String</span></span>

### <span data-ttu-id="28430-143">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="28430-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="28430-144">Parametry: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28430-144">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="28430-145">Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="28430-145">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="28430-146">Parametry: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28430-146">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="28430-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28430-147">OUTPUTS</span></span>

### <span data-ttu-id="28430-148">Microsoft. Azure. Commands. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="28430-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="28430-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28430-149">NOTES</span></span>

## <span data-ttu-id="28430-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28430-150">RELATED LINKS</span></span>
