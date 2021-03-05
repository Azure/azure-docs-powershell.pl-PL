---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 295f79f48ffa966024561486745cdcf52ec8e38f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973329"
---
# <span data-ttu-id="9bf32-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9bf32-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="9bf32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bf32-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf32-103">Usuwanie wartości IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="9bf32-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="9bf32-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9bf32-104">SYNTAX</span></span>

### <span data-ttu-id="9bf32-105">NetWorkRuleString (domyślna)</span><span class="sxs-lookup"><span data-stu-id="9bf32-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bf32-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="9bf32-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf32-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9bf32-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf32-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="9bf32-108">ResourceAccessRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf32-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="9bf32-109">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf32-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="9bf32-110">ResourceAccessRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bf32-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="9bf32-111">DESCRIPTION</span></span>
<span data-ttu-id="9bf32-112">Polecenie cmdlet **Remove-AzStorageAccountNetworkRule** usuwa wartości IpRules lub VirtualNetworkRules z właściwości NetWorkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="9bf32-112">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="9bf32-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9bf32-113">EXAMPLES</span></span>

### <span data-ttu-id="9bf32-114">Przykład 1. Usuwanie kilku adresów IpRules za pomocą adresu IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9bf32-114">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="9bf32-115">To polecenie usuwa kilka adresów IpRules z adresem IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="9bf32-115">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="9bf32-116">Przykład 2. Usuwanie ciągu VirtualNetworkRule za pomocą danych wejściowych obiektu VirtualNetworkRule z JSON</span><span class="sxs-lookup"><span data-stu-id="9bf32-116">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="9bf32-117">To polecenie usuwa polecenie VirtualNetworkRule z wprowadzeniem obiektu VirtualNetworkRule z JSON.</span><span class="sxs-lookup"><span data-stu-id="9bf32-117">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="9bf32-118">Przykład 3. Usuwanie pierwszego ciągu IpRule z potokiem</span><span class="sxs-lookup"><span data-stu-id="9bf32-118">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="9bf32-119">To polecenie usuwa pierwszy adres IpRule z potokiem.</span><span class="sxs-lookup"><span data-stu-id="9bf32-119">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="9bf32-120">Przykład 4. Usuwanie kilku przycisków VirtualNetworkRules za pomocą funkcji VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="9bf32-120">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="9bf32-121">To polecenie usuwa kilka ręcznych esejów (VirtualNetworkRules) za pomocą funkcji VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="9bf32-121">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="9bf32-122">Przykład 5. Usuwanie reguły dostępu do zasobów przy użyciu reguł TenantId i ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9bf32-122">Example 5: Remove a resource access rule with TenantId and ResourceId.</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"  -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="9bf32-123">To polecenie usuwa regułę dostępu do zasobów z polem TenantId i ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9bf32-123">This command removes a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="9bf32-124">Przykład 6. Usuwanie pierwszych 3 reguł dostępu do zasobów z konta magazynu</span><span class="sxs-lookup"><span data-stu-id="9bf32-124">Example 6: Remove the first 3 resource access rules from a storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount").ResourceAccessRules | Select-Object -First 3 | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="9bf32-125">To polecenie usuwa pierwsze 3 reguły dostępu do zasobów z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9bf32-125">This command removes the first 3 resource access rules from a storage account.</span></span>

## <span data-ttu-id="9bf32-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bf32-126">PARAMETERS</span></span>

### <span data-ttu-id="9bf32-127">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9bf32-127">-AsJob</span></span>
<span data-ttu-id="9bf32-128">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9bf32-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bf32-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf32-129">-DefaultProfile</span></span>
<span data-ttu-id="9bf32-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf32-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf32-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9bf32-131">-IPAddressOrRange</span></span>
<span data-ttu-id="9bf32-132">Tablica IpAddressOrRange, spowoduje usunięcie właściwości IpRule z taką samą wartością IpAddressOrRange z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="9bf32-132">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="9bf32-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="9bf32-133">-IPRule</span></span>
<span data-ttu-id="9bf32-134">Tablica obiektów IpRule do usunięcia z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="9bf32-134">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="9bf32-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9bf32-135">-Name</span></span>
<span data-ttu-id="9bf32-136">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9bf32-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9bf32-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="9bf32-137">-ResourceAccessRule</span></span>
<span data-ttu-id="9bf32-138">Konto magazynu NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="9bf32-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: ResourceAccessRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf32-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf32-139">-ResourceGroupName</span></span>
<span data-ttu-id="9bf32-140">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="9bf32-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="9bf32-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf32-141">-ResourceId</span></span>
<span data-ttu-id="9bf32-142">Konto magazynu ResourceAccessRule ResourceId w ciągu.</span><span class="sxs-lookup"><span data-stu-id="9bf32-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf32-143">- TenantId</span><span class="sxs-lookup"><span data-stu-id="9bf32-143">-TenantId</span></span>
<span data-ttu-id="9bf32-144">Konto magazynu ResourceAccessRule TenantId w ciągu.</span><span class="sxs-lookup"><span data-stu-id="9bf32-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf32-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf32-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="9bf32-146">Tablica virtualNetworkResourceId, spowoduje usunięcie właściwości VirtualNetworkRule z tym samym virtualNetworkResourceId z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="9bf32-146">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="9bf32-147">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9bf32-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="9bf32-148">Tablica obiektów VirtualNetworkRule do usunięcia z właściwości NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="9bf32-148">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="9bf32-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9bf32-149">-Confirm</span></span>
<span data-ttu-id="9bf32-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9bf32-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf32-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf32-151">-WhatIf</span></span>
<span data-ttu-id="9bf32-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf32-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf32-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9bf32-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf32-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf32-154">CommonParameters</span></span>
<span data-ttu-id="9bf32-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf32-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf32-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf32-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf32-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bf32-157">INPUTS</span></span>

### <span data-ttu-id="9bf32-158">System.String</span><span class="sxs-lookup"><span data-stu-id="9bf32-158">System.String</span></span>

### <span data-ttu-id="9bf32-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="9bf32-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="9bf32-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="9bf32-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="9bf32-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bf32-161">OUTPUTS</span></span>

### <span data-ttu-id="9bf32-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9bf32-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="9bf32-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="9bf32-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="9bf32-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9bf32-164">NOTES</span></span>

## <span data-ttu-id="9bf32-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bf32-165">RELATED LINKS</span></span>
