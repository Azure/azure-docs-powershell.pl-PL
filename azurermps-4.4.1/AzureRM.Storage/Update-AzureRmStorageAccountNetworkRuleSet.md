---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 09619247f41acb60180a7d3045afdcd689d5c183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718671"
---
# <span data-ttu-id="6ad2c-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ad2c-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="6ad2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ad2c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad2c-103">Aktualizowanie właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6ad2c-103">Update the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ad2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ad2c-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ad2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ad2c-105">DESCRIPTION</span></span>
<span data-ttu-id="6ad2c-106">Polecenie cmdlet **Update-AzureRmStorageAccountNetworkRuleSet** aktualizuje właściwość NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6ad2c-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="6ad2c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ad2c-107">EXAMPLES</span></span>

### <span data-ttu-id="6ad2c-108">Przykład 1: aktualizowanie wszystkich właściwości NetworkRule, reguły wprowadzania za pomocą notacji JSON</span><span class="sxs-lookup"><span data-stu-id="6ad2c-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="6ad2c-109">To polecenie aktualizuje wszystkie właściwości NetworkRule, reguły wprowadzania za pomocą notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="6ad2c-110">Przykład 2: aktualizowanie właściwości Bypass dla NetworkRule</span><span class="sxs-lookup"><span data-stu-id="6ad2c-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="6ad2c-111">To polecenie umożliwia zaktualizowanie właściwości Bypass NetworkRule (inne właściwości nie zostaną zmienione).</span><span class="sxs-lookup"><span data-stu-id="6ad2c-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="6ad2c-112">Przykład 3: porządkowanie reguł NetworkRule z konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6ad2c-112">Example 3: Clean up rules of NetworkRule of a Storage Account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="6ad2c-113">To polecenie czyści reguły NetworkRule konta magazynu (inne właściwości nie zmieniają się).</span><span class="sxs-lookup"><span data-stu-id="6ad2c-113">This command clean up rules of NetworkRule of a Storage Account (other properties not change).</span></span>

## <span data-ttu-id="6ad2c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ad2c-114">PARAMETERS</span></span>

### <span data-ttu-id="6ad2c-115">-Bypass</span><span class="sxs-lookup"><span data-stu-id="6ad2c-115">-Bypass</span></span>
<span data-ttu-id="6ad2c-116">Wartość pomijania do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-116">The Bypass value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="6ad2c-117">Dozwolona wartość to brak lub dowolna kombinacja: â € ¢ rejestrowanie â € ¢ metryki â € ¢ Azureservices</span><span class="sxs-lookup"><span data-stu-id="6ad2c-117">The allowed value are none or any combination of: â€¢ Logging â€¢ Metrics â€¢ Azureservices</span></span>

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

### <span data-ttu-id="6ad2c-118">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="6ad2c-118">-DefaultAction</span></span>
<span data-ttu-id="6ad2c-119">Wartość DefaultAction do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-119">The DefaultAction value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="6ad2c-120">Dozwolone opcje: â € ¢ Zezwalaj na â € ¢ odmowa</span><span class="sxs-lookup"><span data-stu-id="6ad2c-120">The allowed Options: â€¢ Allow â€¢ Deny</span></span>

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

### <span data-ttu-id="6ad2c-121">-IPRule</span><span class="sxs-lookup"><span data-stu-id="6ad2c-121">-IPRule</span></span>
<span data-ttu-id="6ad2c-122">Tablica obiektów IpRule, które mają zostać zaktualizowane do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-122">The Array of IpRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

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

### <span data-ttu-id="6ad2c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ad2c-123">-Name</span></span>
<span data-ttu-id="6ad2c-124">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-124">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="6ad2c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad2c-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ad2c-126">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-126">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="6ad2c-127">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6ad2c-127">-VirtualNetworkRule</span></span>
<span data-ttu-id="6ad2c-128">Tablica obiektów VirtualNetworkRule, które mają zostać zaktualizowane do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-128">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

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

### <span data-ttu-id="6ad2c-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ad2c-129">-Confirm</span></span>
<span data-ttu-id="6ad2c-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad2c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad2c-131">-WhatIf</span></span>
<span data-ttu-id="6ad2c-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad2c-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad2c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad2c-134">-DefaultProfile</span></span>
<span data-ttu-id="6ad2c-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ad2c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad2c-136">CommonParameters</span></span>
<span data-ttu-id="6ad2c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad2c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad2c-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad2c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad2c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ad2c-139">INPUTS</span></span>

### <span data-ttu-id="6ad2c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad2c-140">System.String</span></span>
<span data-ttu-id="6ad2c-141">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="6ad2c-141">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="6ad2c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ad2c-142">OUTPUTS</span></span>

### <span data-ttu-id="6ad2c-143">Microsoft. Azure. Commands. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ad2c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="6ad2c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ad2c-144">NOTES</span></span>

## <span data-ttu-id="6ad2c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ad2c-145">RELATED LINKS</span></span>

