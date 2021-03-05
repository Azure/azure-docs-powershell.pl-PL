---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 0104c64bf65acc945609f4e2e0ae78ff288b142d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976177"
---
# <span data-ttu-id="3db93-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3db93-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="3db93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3db93-102">SYNOPSIS</span></span>
 <span data-ttu-id="3db93-103">Dodawanie wartości IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3db93-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3db93-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3db93-104">SYNTAX</span></span>

### <span data-ttu-id="3db93-105">NetWorkRuleString (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3db93-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3db93-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3db93-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db93-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="3db93-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db93-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="3db93-108">ResourceAccessRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db93-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="3db93-109">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db93-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="3db93-110">ResourceAccessRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3db93-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="3db93-111">DESCRIPTION</span></span>
<span data-ttu-id="3db93-112">Polecenie **cmdlet Add-AzStorageAccountNetworkRule** dodaje wartości IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3db93-112">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3db93-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3db93-113">EXAMPLES</span></span>

### <span data-ttu-id="3db93-114">Przykład 1. Dodawanie kilku adresów IpRules za pomocą adresu IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3db93-114">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="3db93-115">To polecenie pozwala dodać kilka poleceń IpRules z adresem IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="3db93-115">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="3db93-116">Przykład 2. Dodawanie dodatku VirtualNetworkRule z virtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="3db93-116">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="3db93-117">To polecenie pozwala dodać pole VirtualNetworkRule z polem VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="3db93-117">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="3db93-118">Przykład 3. Dodawanie obiektów VirtualNetworkRules za pomocą funkcji VirtualNetworkRule Objects z innego konta</span><span class="sxs-lookup"><span data-stu-id="3db93-118">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="3db93-119">To polecenie pozwala dodać obiekty VirtualNetworkRules z obiektami VirtualNetworkRule z innego konta.</span><span class="sxs-lookup"><span data-stu-id="3db93-119">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="3db93-120">Przykład 4. Dodawanie kilku adresów IpRule za pomocą obiektów IpRule, danych wejściowych za pomocą JSON</span><span class="sxs-lookup"><span data-stu-id="3db93-120">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="3db93-121">To polecenie pozwala dodać kilka obiektów IpRule z obiektami IpRule, dane wejściowe z wartością JSON.</span><span class="sxs-lookup"><span data-stu-id="3db93-121">This command add several IpRule with IpRule objects, input with JSON.</span></span>

### <span data-ttu-id="3db93-122">Przykład 5. Dodawanie reguły dostępu do zasobu</span><span class="sxs-lookup"><span data-stu-id="3db93-122">Example 5: Add a resource access rule</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="3db93-123">To polecenie dodaje regułę dostępu do zasobów z polem TenantId i ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3db93-123">This command adds a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="3db93-124">Przykład 6. Dodawanie wszystkich reguł dostępu do zasobów jednego konta magazynu do innego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3db93-124">Example 6: Add all resource access rules of one storage account to another storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1").ResourceAccessRules | Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2"
```

<span data-ttu-id="3db93-125">To polecenie pobiera wszystkie reguły dostępu do zasobów z jednego konta magazynu i dodaje je do innego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3db93-125">This command gets all resource access rules from one storage account, and adds them to another storage account.</span></span>

## <span data-ttu-id="3db93-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3db93-126">PARAMETERS</span></span>

### <span data-ttu-id="3db93-127">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3db93-127">-AsJob</span></span>
<span data-ttu-id="3db93-128">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3db93-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3db93-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db93-129">-DefaultProfile</span></span>
<span data-ttu-id="3db93-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3db93-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3db93-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3db93-131">-IPAddressOrRange</span></span>
<span data-ttu-id="3db93-132">Tablica IpAddressOrRange, dodaj wartości IpRules z wartością wejściową IpAddressOrRange i domyślną akcję Zezwalaj na właściwość NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="3db93-132">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="3db93-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3db93-133">-IPRule</span></span>
<span data-ttu-id="3db93-134">Tablica obiektów IpRule, które należy dodać do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="3db93-134">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="3db93-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3db93-135">-Name</span></span>
<span data-ttu-id="3db93-136">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3db93-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="3db93-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="3db93-137">-ResourceAccessRule</span></span>
<span data-ttu-id="3db93-138">Konto magazynu NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="3db93-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

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

### <span data-ttu-id="3db93-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db93-139">-ResourceGroupName</span></span>
<span data-ttu-id="3db93-140">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="3db93-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="3db93-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3db93-141">-ResourceId</span></span>
<span data-ttu-id="3db93-142">Konto magazynu ResourceAccessRule ResourceId w ciągu.</span><span class="sxs-lookup"><span data-stu-id="3db93-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

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

### <span data-ttu-id="3db93-143">- TenantId</span><span class="sxs-lookup"><span data-stu-id="3db93-143">-TenantId</span></span>
<span data-ttu-id="3db93-144">Konto magazynu ResourceAccessRule TenantId w ciągu.</span><span class="sxs-lookup"><span data-stu-id="3db93-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

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

### <span data-ttu-id="3db93-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3db93-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3db93-146">Tablica virtualNetworkResourceId, doda wartość VirtualNetworkRule z wartością "VirtualNetworkResourceId" i domyślną akcją zezwala na właściwość NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="3db93-146">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="3db93-147">— VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3db93-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="3db93-148">Tablica obiektów VirtualNetworkRule, które należy dodać do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="3db93-148">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="3db93-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3db93-149">-Confirm</span></span>
<span data-ttu-id="3db93-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3db93-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db93-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db93-151">-WhatIf</span></span>
<span data-ttu-id="3db93-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db93-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db93-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3db93-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db93-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db93-154">CommonParameters</span></span>
<span data-ttu-id="3db93-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db93-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db93-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db93-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db93-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3db93-157">INPUTS</span></span>

### <span data-ttu-id="3db93-158">System.String</span><span class="sxs-lookup"><span data-stu-id="3db93-158">System.String</span></span>

### <span data-ttu-id="3db93-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="3db93-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="3db93-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="3db93-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="3db93-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3db93-161">OUTPUTS</span></span>

### <span data-ttu-id="3db93-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3db93-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="3db93-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="3db93-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="3db93-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3db93-164">NOTES</span></span>

## <span data-ttu-id="3db93-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3db93-165">RELATED LINKS</span></span>
