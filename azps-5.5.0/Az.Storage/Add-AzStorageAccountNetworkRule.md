---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195827"
---
# <span data-ttu-id="d7215-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d7215-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="d7215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7215-102">SYNOPSIS</span></span>
 <span data-ttu-id="d7215-103">Dodawanie wartości IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d7215-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d7215-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7215-104">SYNTAX</span></span>

### <span data-ttu-id="d7215-105">NetWorkRuleString (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d7215-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7215-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="d7215-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7215-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="d7215-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7215-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="d7215-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7215-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7215-109">DESCRIPTION</span></span>
<span data-ttu-id="d7215-110">Polecenie **cmdlet Add-AzStorageAccountNetworkRule** dodaje wartości IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d7215-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d7215-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7215-111">EXAMPLES</span></span>

### <span data-ttu-id="d7215-112">Przykład 1. Dodawanie kilku adresów IpRules za pomocą adresu IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d7215-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="d7215-113">To polecenie pozwala dodać kilka poleceń IpRules z adresem IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="d7215-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="d7215-114">Przykład 2. Dodawanie dodatku VirtualNetworkRule z virtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="d7215-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="d7215-115">To polecenie pozwala dodać pole VirtualNetworkRule z polem VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="d7215-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="d7215-116">Przykład 3. Dodawanie obiektów VirtualNetworkRules za pomocą funkcji VirtualNetworkRule Objects z innego konta</span><span class="sxs-lookup"><span data-stu-id="d7215-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="d7215-117">To polecenie pozwala dodać obiekty VirtualNetworkRules za pomocą funkcji VirtualNetworkRule Objects z innego konta.</span><span class="sxs-lookup"><span data-stu-id="d7215-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="d7215-118">Przykład 4. Dodawanie kilku adresów IpRule za pomocą obiektów IpRule, danych wejściowych za pomocą JSON</span><span class="sxs-lookup"><span data-stu-id="d7215-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="d7215-119">To polecenie pozwala dodać kilka poleceń IpRule z obiektami IpRule, dane wejściowe z wartością JSON.</span><span class="sxs-lookup"><span data-stu-id="d7215-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="d7215-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7215-120">PARAMETERS</span></span>

### <span data-ttu-id="d7215-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d7215-121">-AsJob</span></span>
<span data-ttu-id="d7215-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d7215-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7215-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7215-123">-DefaultProfile</span></span>
<span data-ttu-id="d7215-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7215-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7215-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d7215-125">-IPAddressOrRange</span></span>
<span data-ttu-id="d7215-126">Tablica IpAddressOrRange, dodaj wartości IpRules z wartością wejściową IpAddressOrRange i domyślną akcję Zezwalaj na właściwość NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d7215-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="d7215-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="d7215-127">-IPRule</span></span>
<span data-ttu-id="d7215-128">Tablica obiektów IpRule, które należy dodać do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d7215-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="d7215-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d7215-129">-Name</span></span>
<span data-ttu-id="d7215-130">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7215-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d7215-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7215-131">-ResourceGroupName</span></span>
<span data-ttu-id="d7215-132">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7215-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d7215-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d7215-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="d7215-134">Tablica virtualNetworkResourceId, doda wartość VirtualNetworkRule z wartością wejściową VirtualNetworkResourceId i domyślną akcję Zezwalaj na właściwość NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d7215-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="d7215-135">- VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d7215-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="d7215-136">Tablica obiektów VirtualNetworkRule, które należy dodać do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d7215-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="d7215-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7215-137">-Confirm</span></span>
<span data-ttu-id="d7215-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d7215-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7215-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7215-139">-WhatIf</span></span>
<span data-ttu-id="d7215-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7215-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7215-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d7215-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7215-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7215-142">CommonParameters</span></span>
<span data-ttu-id="d7215-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7215-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7215-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7215-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7215-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7215-145">INPUTS</span></span>

### <span data-ttu-id="d7215-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d7215-146">System.String</span></span>

### <span data-ttu-id="d7215-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="d7215-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="d7215-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="d7215-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="d7215-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7215-149">OUTPUTS</span></span>

### <span data-ttu-id="d7215-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d7215-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="d7215-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="d7215-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="d7215-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7215-152">NOTES</span></span>

## <span data-ttu-id="d7215-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7215-153">RELATED LINKS</span></span>
