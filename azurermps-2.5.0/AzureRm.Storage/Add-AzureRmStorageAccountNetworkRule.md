---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstorageaccountnetworkrule
schema: 2.0.0
ms.openlocfilehash: 0b1d497bbd7e976d942bdc3f99c6bea2d4c2c1cb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898165"
---
# <span data-ttu-id="d4a81-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d4a81-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="d4a81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4a81-102">SYNOPSIS</span></span>
 <span data-ttu-id="d4a81-103">Dodawanie IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d4a81-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4a81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4a81-104">SYNTAX</span></span>

### <span data-ttu-id="d4a81-105">NetWorkRuleString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d4a81-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4a81-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="d4a81-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a81-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="d4a81-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a81-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="d4a81-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a81-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d4a81-109">DESCRIPTION</span></span>
<span data-ttu-id="d4a81-110">Polecenie cmdlet **Add-AzureRmStorageAccountNetworkRule** dodaje IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d4a81-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d4a81-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4a81-111">EXAMPLES</span></span>

### <span data-ttu-id="d4a81-112">Przykład 1. Dodaj kilka IpRules za pomocą IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d4a81-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="d4a81-113">To polecenie umożliwia dodanie kilku IpRules z IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="d4a81-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="d4a81-114">Przykład 2: Dodawanie VirtualNetworkRule za pomocą VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="d4a81-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="d4a81-115">To polecenie umożliwia dodanie VirtualNetworkRule z VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="d4a81-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="d4a81-116">Przykład 3: Dodawanie VirtualNetworkRules za pomocą obiektów VirtualNetworkRule z innego konta</span><span class="sxs-lookup"><span data-stu-id="d4a81-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="d4a81-117">To polecenie umożliwia dodanie VirtualNetworkRules z obiektami VirtualNetworkRule z innego konta.</span><span class="sxs-lookup"><span data-stu-id="d4a81-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="d4a81-118">Przykład 4: Dodawanie kilku IpRule za pomocą obiektów IpRule, wprowadzanie za pomocą notacji JSON</span><span class="sxs-lookup"><span data-stu-id="d4a81-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="d4a81-119">To polecenie umożliwia dodanie kilku IpRule z obiektami IpRule, które są wprowadzane za pomocą notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="d4a81-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="d4a81-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4a81-120">PARAMETERS</span></span>

### <span data-ttu-id="d4a81-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4a81-121">-AsJob</span></span>
<span data-ttu-id="d4a81-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d4a81-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4a81-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a81-123">-DefaultProfile</span></span>
<span data-ttu-id="d4a81-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a81-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a81-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d4a81-125">-IPAddressOrRange</span></span>
<span data-ttu-id="d4a81-126">Tablica IpAddressOrRange, Dodawanie IpRules z IpAddressOrRange wejściowym i akcją domyślną Zezwól na NetworkRule właściwości.</span><span class="sxs-lookup"><span data-stu-id="d4a81-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="d4a81-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="d4a81-127">-IPRule</span></span>
<span data-ttu-id="d4a81-128">Tablica obiektów IpRule, które mają zostać dodane do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d4a81-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="d4a81-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4a81-129">-Name</span></span>
<span data-ttu-id="d4a81-130">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d4a81-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d4a81-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a81-131">-ResourceGroupName</span></span>
<span data-ttu-id="d4a81-132">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d4a81-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d4a81-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d4a81-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="d4a81-134">W tablicy VirtualNetworkResourceId zostaną dodane VirtualNetworkRule z VirtualNetworkResourceId wejściowym i akcją domyślną NetworkRule właściwości.</span><span class="sxs-lookup"><span data-stu-id="d4a81-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="d4a81-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d4a81-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="d4a81-136">Tablica obiektów VirtualNetworkRule, które mają zostać dodane do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d4a81-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="d4a81-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4a81-137">-Confirm</span></span>
<span data-ttu-id="d4a81-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a81-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a81-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a81-139">-WhatIf</span></span>
<span data-ttu-id="d4a81-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a81-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a81-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4a81-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a81-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a81-142">CommonParameters</span></span>
<span data-ttu-id="d4a81-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a81-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a81-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a81-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a81-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4a81-145">INPUTS</span></span>

### <span data-ttu-id="d4a81-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d4a81-146">System.String</span></span>

### <span data-ttu-id="d4a81-147">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="d4a81-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="d4a81-148">Parametry: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4a81-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="d4a81-149">Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="d4a81-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="d4a81-150">Parametry: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4a81-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="d4a81-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4a81-151">OUTPUTS</span></span>

### <span data-ttu-id="d4a81-152">Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d4a81-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="d4a81-153">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="d4a81-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="d4a81-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4a81-154">NOTES</span></span>

## <span data-ttu-id="d4a81-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4a81-155">RELATED LINKS</span></span>
