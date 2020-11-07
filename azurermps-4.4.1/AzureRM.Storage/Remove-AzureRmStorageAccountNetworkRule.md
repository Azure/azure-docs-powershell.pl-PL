---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: abfd6f06a0d3f81c84f79e4a5fa6870ad60ba18d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717559"
---
# <span data-ttu-id="aa83d-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aa83d-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="aa83d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa83d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa83d-103">Usuwanie IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="aa83d-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa83d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa83d-104">SYNTAX</span></span>

### <span data-ttu-id="aa83d-105">NetWorkRuleString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa83d-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa83d-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="aa83d-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa83d-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="aa83d-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa83d-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="aa83d-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa83d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="aa83d-109">DESCRIPTION</span></span>
<span data-ttu-id="aa83d-110">Polecenie cmdlet **Remove-AzureRmStorageAccountNetworkRule** usuwa IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="aa83d-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage Account</span></span>

## <span data-ttu-id="aa83d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa83d-111">EXAMPLES</span></span>

### <span data-ttu-id="aa83d-112">Przykład 1: Usuwanie kilku IpRules za pomocą IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="aa83d-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="aa83d-113">To polecenie umożliwia usunięcie kilku IpRules z IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="aa83d-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="aa83d-114">Przykład 2: usuwanie VirtualNetworkRule z wejściowym obiektem VirtualNetworkRule w formacie JSON</span><span class="sxs-lookup"><span data-stu-id="aa83d-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="aa83d-115">To polecenie usuwa VirtualNetworkRule z danymi wejściowymi obiektu VirtualNetworkRule w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="aa83d-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="aa83d-116">Przykład 3: usuwanie pierwszego IpRule za pomocą rurociągu</span><span class="sxs-lookup"><span data-stu-id="aa83d-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="aa83d-117">To polecenie usuwa pierwszą IpRule z rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="aa83d-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="aa83d-118">Przykład 4: Usuwanie kilku VirtualNetworkRules za pomocą VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="aa83d-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="aa83d-119">To polecenie umożliwia usunięcie kilku VirtualNetworkRules z VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="aa83d-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="aa83d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa83d-120">PARAMETERS</span></span>

### <span data-ttu-id="aa83d-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="aa83d-121">-IPAddressOrRange</span></span>
<span data-ttu-id="aa83d-122">Tablica IpAddressOrRange, która usunie IpRule z tym samym IpAddressOrRange z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="aa83d-122">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="aa83d-123">-IPRule</span><span class="sxs-lookup"><span data-stu-id="aa83d-123">-IPRule</span></span>
<span data-ttu-id="aa83d-124">Tablica obiektów IpRule do usunięcia z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="aa83d-124">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="aa83d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa83d-125">-Name</span></span>
<span data-ttu-id="aa83d-126">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa83d-126">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="aa83d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa83d-127">-ResourceGroupName</span></span>
<span data-ttu-id="aa83d-128">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa83d-128">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="aa83d-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="aa83d-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="aa83d-130">Tablica VirtualNetworkResourceId, która usunie VirtualNetworkRule z tym samym VirtualNetworkResourceId z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="aa83d-130">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="aa83d-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aa83d-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="aa83d-132">Tablica obiektów VirtualNetworkRule do usunięcia z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="aa83d-132">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="aa83d-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa83d-133">-Confirm</span></span>
<span data-ttu-id="aa83d-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa83d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa83d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa83d-135">-WhatIf</span></span>
<span data-ttu-id="aa83d-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa83d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa83d-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa83d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa83d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa83d-138">-DefaultProfile</span></span>
<span data-ttu-id="aa83d-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa83d-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa83d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa83d-140">CommonParameters</span></span>
<span data-ttu-id="aa83d-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa83d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa83d-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa83d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa83d-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa83d-143">INPUTS</span></span>

### <span data-ttu-id="aa83d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="aa83d-144">System.String</span></span>
<span data-ttu-id="aa83d-145">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="aa83d-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="aa83d-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa83d-146">OUTPUTS</span></span>

### <span data-ttu-id="aa83d-147">Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aa83d-147">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="aa83d-148">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="aa83d-148">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="aa83d-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa83d-149">NOTES</span></span>

## <span data-ttu-id="aa83d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa83d-150">RELATED LINKS</span></span>

