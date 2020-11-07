---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: fb8df6e3444a650cc5f3c249545a43b4033689bd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892293"
---
# <span data-ttu-id="f601c-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f601c-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="f601c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f601c-102">SYNOPSIS</span></span>
 <span data-ttu-id="f601c-103">Dodawanie IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f601c-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f601c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f601c-104">SYNTAX</span></span>

### <span data-ttu-id="f601c-105">NetWorkRuleString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f601c-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f601c-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="f601c-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f601c-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="f601c-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f601c-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="f601c-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f601c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f601c-109">DESCRIPTION</span></span>
<span data-ttu-id="f601c-110">Polecenie cmdlet **Add-AzStorageAccountNetworkRule** dodaje IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f601c-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f601c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f601c-111">EXAMPLES</span></span>

### <span data-ttu-id="f601c-112">Przykład 1. Dodaj kilka IpRules za pomocą IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f601c-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="f601c-113">To polecenie umożliwia dodanie kilku IpRules z IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="f601c-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="f601c-114">Przykład 2: Dodawanie VirtualNetworkRule za pomocą VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="f601c-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="f601c-115">To polecenie umożliwia dodanie VirtualNetworkRule z VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="f601c-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="f601c-116">Przykład 3: Dodawanie VirtualNetworkRules za pomocą obiektów VirtualNetworkRule z innego konta</span><span class="sxs-lookup"><span data-stu-id="f601c-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="f601c-117">To polecenie umożliwia dodanie VirtualNetworkRules z obiektami VirtualNetworkRule z innego konta.</span><span class="sxs-lookup"><span data-stu-id="f601c-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="f601c-118">Przykład 4: Dodawanie kilku IpRule za pomocą obiektów IpRule, wprowadzanie za pomocą notacji JSON</span><span class="sxs-lookup"><span data-stu-id="f601c-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="f601c-119">To polecenie umożliwia dodanie kilku IpRule z obiektami IpRule, które są wprowadzane za pomocą notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="f601c-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="f601c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f601c-120">PARAMETERS</span></span>

### <span data-ttu-id="f601c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f601c-121">-AsJob</span></span>
<span data-ttu-id="f601c-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f601c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f601c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f601c-123">-DefaultProfile</span></span>
<span data-ttu-id="f601c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f601c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f601c-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f601c-125">-IPAddressOrRange</span></span>
<span data-ttu-id="f601c-126">Tablica IpAddressOrRange, Dodawanie IpRules z IpAddressOrRange wejściowym i akcją domyślną Zezwól na NetworkRule właściwości.</span><span class="sxs-lookup"><span data-stu-id="f601c-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="f601c-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="f601c-127">-IPRule</span></span>
<span data-ttu-id="f601c-128">Tablica obiektów IpRule, które mają zostać dodane do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="f601c-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="f601c-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f601c-129">-Name</span></span>
<span data-ttu-id="f601c-130">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f601c-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="f601c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f601c-131">-ResourceGroupName</span></span>
<span data-ttu-id="f601c-132">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="f601c-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="f601c-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f601c-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="f601c-134">W tablicy VirtualNetworkResourceId zostaną dodane VirtualNetworkRule z VirtualNetworkResourceId wejściowym i akcją domyślną NetworkRule właściwości.</span><span class="sxs-lookup"><span data-stu-id="f601c-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="f601c-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f601c-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="f601c-136">Tablica obiektów VirtualNetworkRule, które mają zostać dodane do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="f601c-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="f601c-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f601c-137">-Confirm</span></span>
<span data-ttu-id="f601c-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f601c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f601c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f601c-139">-WhatIf</span></span>
<span data-ttu-id="f601c-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f601c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f601c-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f601c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f601c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f601c-142">CommonParameters</span></span>
<span data-ttu-id="f601c-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f601c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f601c-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f601c-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f601c-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f601c-145">INPUTS</span></span>

### <span data-ttu-id="f601c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f601c-146">System.String</span></span>

### <span data-ttu-id="f601c-147">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="f601c-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="f601c-148">Parametry: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f601c-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="f601c-149">Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="f601c-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="f601c-150">Parametry: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f601c-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="f601c-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f601c-151">OUTPUTS</span></span>

### <span data-ttu-id="f601c-152">Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f601c-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="f601c-153">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="f601c-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="f601c-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f601c-154">NOTES</span></span>

## <span data-ttu-id="f601c-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f601c-155">RELATED LINKS</span></span>
