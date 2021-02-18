---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190755"
---
# <span data-ttu-id="7eb01-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7eb01-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="7eb01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eb01-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb01-103">Usuwanie wartości IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="7eb01-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="7eb01-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7eb01-104">SYNTAX</span></span>

### <span data-ttu-id="7eb01-105">NetWorkRuleString (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="7eb01-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7eb01-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="7eb01-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb01-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="7eb01-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb01-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="7eb01-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb01-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7eb01-109">DESCRIPTION</span></span>
<span data-ttu-id="7eb01-110">Polecenie cmdlet **Remove-AzStorageAccountNetworkRule** usuwa wartości IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="7eb01-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="7eb01-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7eb01-111">EXAMPLES</span></span>

### <span data-ttu-id="7eb01-112">Przykład 1. Usuwanie kilku adresów IpRules za pomocą adresu IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7eb01-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="7eb01-113">To polecenie usuwa kilka poleceń IpRules z adresem IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="7eb01-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="7eb01-114">Przykład 2. Usuwanie ciągu VirtualNetworkRule za pomocą danych wejściowych obiektu VirtualNetworkRule z JSON</span><span class="sxs-lookup"><span data-stu-id="7eb01-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="7eb01-115">To polecenie usuwa polecenie VirtualNetworkRule z wprowadzeniem obiektu VirtualNetworkRule z JSON.</span><span class="sxs-lookup"><span data-stu-id="7eb01-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="7eb01-116">Przykład 3. Usuwanie pierwszego ciągu IpRule z potokiem</span><span class="sxs-lookup"><span data-stu-id="7eb01-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="7eb01-117">To polecenie umożliwia usunięcie pierwszego polecenia IpRule z potokiem.</span><span class="sxs-lookup"><span data-stu-id="7eb01-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="7eb01-118">Przykład 4. Usuwanie kilku przycisków VirtualNetworkRules za pomocą funkcji VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="7eb01-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="7eb01-119">To polecenie usuwa kilka ręcznych esejów (VirtualNetworkRules) za pomocą funkcji VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="7eb01-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="7eb01-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eb01-120">PARAMETERS</span></span>

### <span data-ttu-id="7eb01-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7eb01-121">-AsJob</span></span>
<span data-ttu-id="7eb01-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7eb01-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7eb01-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb01-123">-DefaultProfile</span></span>
<span data-ttu-id="7eb01-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7eb01-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb01-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7eb01-125">-IPAddressOrRange</span></span>
<span data-ttu-id="7eb01-126">Tablica IpAddressOrRange, spowoduje usunięcie właściwości IpRule z taką samą wartością IpAddressOrRange z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="7eb01-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="7eb01-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="7eb01-127">-IPRule</span></span>
<span data-ttu-id="7eb01-128">Tablica obiektów IpRule do usunięcia z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="7eb01-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="7eb01-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7eb01-129">-Name</span></span>
<span data-ttu-id="7eb01-130">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7eb01-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="7eb01-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb01-131">-ResourceGroupName</span></span>
<span data-ttu-id="7eb01-132">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="7eb01-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="7eb01-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="7eb01-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="7eb01-134">Tablica virtualNetworkResourceId, spowoduje usunięcie właściwości VirtualNetworkRule z tym samym virtualNetworkResourceId z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="7eb01-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="7eb01-135">- VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7eb01-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="7eb01-136">Tablica obiektów VirtualNetworkRule do usunięcia z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="7eb01-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="7eb01-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7eb01-137">-Confirm</span></span>
<span data-ttu-id="7eb01-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7eb01-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb01-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb01-139">-WhatIf</span></span>
<span data-ttu-id="7eb01-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eb01-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb01-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7eb01-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb01-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb01-142">CommonParameters</span></span>
<span data-ttu-id="7eb01-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb01-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb01-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb01-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb01-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eb01-145">INPUTS</span></span>

### <span data-ttu-id="7eb01-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7eb01-146">System.String</span></span>

### <span data-ttu-id="7eb01-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="7eb01-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="7eb01-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="7eb01-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="7eb01-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7eb01-149">OUTPUTS</span></span>

### <span data-ttu-id="7eb01-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7eb01-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="7eb01-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="7eb01-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="7eb01-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7eb01-152">NOTES</span></span>

## <span data-ttu-id="7eb01-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7eb01-153">RELATED LINKS</span></span>
