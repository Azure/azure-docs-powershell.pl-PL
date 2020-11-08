---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053633"
---
# <span data-ttu-id="d09fb-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d09fb-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="d09fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d09fb-102">SYNOPSIS</span></span>
<span data-ttu-id="d09fb-103">Usuwanie IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d09fb-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="d09fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d09fb-104">SYNTAX</span></span>

### <span data-ttu-id="d09fb-105">NetWorkRuleString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d09fb-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d09fb-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="d09fb-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d09fb-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="d09fb-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d09fb-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="d09fb-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d09fb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d09fb-109">DESCRIPTION</span></span>
<span data-ttu-id="d09fb-110">Polecenie cmdlet **Remove-AzStorageAccountNetworkRule** usuwa IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d09fb-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="d09fb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d09fb-111">EXAMPLES</span></span>

### <span data-ttu-id="d09fb-112">Przykład 1: Usuwanie kilku IpRules za pomocą IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d09fb-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="d09fb-113">To polecenie umożliwia usunięcie kilku IpRules z IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="d09fb-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="d09fb-114">Przykład 2: usuwanie VirtualNetworkRule z wejściowym obiektem VirtualNetworkRule w formacie JSON</span><span class="sxs-lookup"><span data-stu-id="d09fb-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="d09fb-115">To polecenie usuwa VirtualNetworkRule z danymi wejściowymi obiektu VirtualNetworkRule w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="d09fb-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="d09fb-116">Przykład 3: usuwanie pierwszego IpRule za pomocą rurociągu</span><span class="sxs-lookup"><span data-stu-id="d09fb-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="d09fb-117">To polecenie usuwa pierwszą IpRule z rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="d09fb-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="d09fb-118">Przykład 4: Usuwanie kilku VirtualNetworkRules za pomocą VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="d09fb-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="d09fb-119">To polecenie umożliwia usunięcie kilku VirtualNetworkRules z VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="d09fb-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="d09fb-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d09fb-120">PARAMETERS</span></span>

### <span data-ttu-id="d09fb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d09fb-121">-AsJob</span></span>
<span data-ttu-id="d09fb-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d09fb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d09fb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d09fb-123">-DefaultProfile</span></span>
<span data-ttu-id="d09fb-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d09fb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d09fb-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d09fb-125">-IPAddressOrRange</span></span>
<span data-ttu-id="d09fb-126">Tablica IpAddressOrRange, która usunie IpRule z tym samym IpAddressOrRange z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="d09fb-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d09fb-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="d09fb-127">-IPRule</span></span>
<span data-ttu-id="d09fb-128">Tablica obiektów IpRule do usunięcia z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="d09fb-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d09fb-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d09fb-129">-Name</span></span>
<span data-ttu-id="d09fb-130">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d09fb-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d09fb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d09fb-131">-ResourceGroupName</span></span>
<span data-ttu-id="d09fb-132">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d09fb-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d09fb-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d09fb-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="d09fb-134">Tablica VirtualNetworkResourceId, która usunie VirtualNetworkRule z tym samym VirtualNetworkResourceId z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="d09fb-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d09fb-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d09fb-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="d09fb-136">Tablica obiektów VirtualNetworkRule do usunięcia z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="d09fb-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d09fb-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d09fb-137">-Confirm</span></span>
<span data-ttu-id="d09fb-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d09fb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d09fb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d09fb-139">-WhatIf</span></span>
<span data-ttu-id="d09fb-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d09fb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d09fb-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d09fb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d09fb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d09fb-142">CommonParameters</span></span>
<span data-ttu-id="d09fb-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d09fb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d09fb-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d09fb-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d09fb-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d09fb-145">INPUTS</span></span>

### <span data-ttu-id="d09fb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d09fb-146">System.String</span></span>

### <span data-ttu-id="d09fb-147">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="d09fb-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="d09fb-148">Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="d09fb-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="d09fb-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d09fb-149">OUTPUTS</span></span>

### <span data-ttu-id="d09fb-150">Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d09fb-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="d09fb-151">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="d09fb-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="d09fb-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d09fb-152">NOTES</span></span>

## <span data-ttu-id="d09fb-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d09fb-153">RELATED LINKS</span></span>
