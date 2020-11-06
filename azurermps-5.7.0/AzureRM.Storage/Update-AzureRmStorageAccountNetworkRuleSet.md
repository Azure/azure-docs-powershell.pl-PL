---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 8851f7e2820e1c9a0a63b475544c49fe5c0c8ee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550476"
---
# <span data-ttu-id="5ef40-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ef40-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="5ef40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ef40-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef40-103">Aktualizowanie właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5ef40-103">Update the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ef40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ef40-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ef40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ef40-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef40-106">Polecenie cmdlet **Update-AzureRmStorageAccountNetworkRuleSet** aktualizuje właściwość NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5ef40-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="5ef40-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ef40-107">EXAMPLES</span></span>

### <span data-ttu-id="5ef40-108">Przykład 1: aktualizowanie wszystkich właściwości NetworkRule, reguły wprowadzania za pomocą notacji JSON</span><span class="sxs-lookup"><span data-stu-id="5ef40-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="5ef40-109">To polecenie aktualizuje wszystkie właściwości NetworkRule, reguły wprowadzania za pomocą notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="5ef40-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="5ef40-110">Przykład 2: aktualizowanie właściwości Bypass dla NetworkRule</span><span class="sxs-lookup"><span data-stu-id="5ef40-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="5ef40-111">To polecenie umożliwia zaktualizowanie właściwości Bypass NetworkRule (inne właściwości nie zostaną zmienione).</span><span class="sxs-lookup"><span data-stu-id="5ef40-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="5ef40-112">Przykład 3: porządkowanie reguł NetworkRule z konta magazynu</span><span class="sxs-lookup"><span data-stu-id="5ef40-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="5ef40-113">To polecenie czyści reguły NetworkRule konta magazynu (inne właściwości nie zmieniają się).</span><span class="sxs-lookup"><span data-stu-id="5ef40-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="5ef40-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ef40-114">PARAMETERS</span></span>

### <span data-ttu-id="5ef40-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ef40-115">-AsJob</span></span>
<span data-ttu-id="5ef40-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5ef40-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ef40-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="5ef40-117">-Bypass</span></span>
<span data-ttu-id="5ef40-118">Wartość pomijania do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ef40-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="5ef40-119">Dozwolona wartość to brak lub dowolna kombinacja: • rejestrowanie • metryki • Azureservices</span><span class="sxs-lookup"><span data-stu-id="5ef40-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef40-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="5ef40-120">-DefaultAction</span></span>
<span data-ttu-id="5ef40-121">Wartość DefaultAction do zaktualizowania do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ef40-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="5ef40-122">Dozwolone opcje: • Zezwalaj • Odmawiaj</span><span class="sxs-lookup"><span data-stu-id="5ef40-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef40-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef40-123">-DefaultProfile</span></span>
<span data-ttu-id="5ef40-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef40-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef40-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="5ef40-125">-IPRule</span></span>
<span data-ttu-id="5ef40-126">Tablica obiektów IpRule, które mają zostać zaktualizowane do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ef40-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef40-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ef40-127">-Name</span></span>
<span data-ttu-id="5ef40-128">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ef40-128">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef40-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef40-129">-ResourceGroupName</span></span>
<span data-ttu-id="5ef40-130">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ef40-130">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef40-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5ef40-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="5ef40-132">Tablica obiektów VirtualNetworkRule, które mają zostać zaktualizowane do właściwości NetworkRule konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ef40-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef40-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ef40-133">-Confirm</span></span>
<span data-ttu-id="5ef40-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ef40-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef40-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef40-135">-WhatIf</span></span>
<span data-ttu-id="5ef40-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ef40-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef40-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ef40-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef40-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef40-138">CommonParameters</span></span>
<span data-ttu-id="5ef40-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef40-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef40-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef40-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef40-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ef40-141">INPUTS</span></span>

### <span data-ttu-id="5ef40-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5ef40-142">System.String</span></span>
<span data-ttu-id="5ef40-143">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="5ef40-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="5ef40-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ef40-144">OUTPUTS</span></span>

### <span data-ttu-id="5ef40-145">Microsoft. Azure. Commands. Management. Storage. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ef40-145">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="5ef40-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ef40-146">NOTES</span></span>

## <span data-ttu-id="5ef40-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ef40-147">RELATED LINKS</span></span>

