---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: 9f8d098cb27532980b01cf46da6c83d4da30ed48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717560"
---
# <span data-ttu-id="2c5a6-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2c5a6-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="2c5a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c5a6-102">SYNOPSIS</span></span>
 <span data-ttu-id="2c5a6-103">Dodawanie IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="2c5a6-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c5a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c5a6-104">SYNTAX</span></span>

### <span data-ttu-id="2c5a6-105">NetWorkRuleString (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2c5a6-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c5a6-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="2c5a6-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c5a6-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="2c5a6-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c5a6-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="2c5a6-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c5a6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2c5a6-109">DESCRIPTION</span></span>
<span data-ttu-id="2c5a6-110">Polecenie cmdlet **Add-AzureRmStorageAccountNetworkRule** dodaje IpRules lub VirtualNetworkRules do właściwości NetworkRule konta magazynu</span><span class="sxs-lookup"><span data-stu-id="2c5a6-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="2c5a6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c5a6-111">EXAMPLES</span></span>

### <span data-ttu-id="2c5a6-112">Przykład 1. Dodaj kilka IpRules za pomocą IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2c5a6-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="2c5a6-113">To polecenie umożliwia dodanie kilku IpRules z IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="2c5a6-114">Przykład 2: Dodawanie VirtualNetworkRule za pomocą VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="2c5a6-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="2c5a6-115">To polecenie umożliwia dodanie VirtualNetworkRule z VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="2c5a6-116">Przykład 3: Dodawanie VirtualNetworkRules za pomocą obiektów VirtualNetworkRule z innego konta</span><span class="sxs-lookup"><span data-stu-id="2c5a6-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="2c5a6-117">To polecenie umożliwia dodanie VirtualNetworkRules z obiektami VirtualNetworkRule z innego konta.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="2c5a6-118">Przykład 4: Dodawanie kilku IpRule za pomocą obiektów IpRule, wprowadzanie za pomocą notacji JSON</span><span class="sxs-lookup"><span data-stu-id="2c5a6-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="2c5a6-119">To polecenie umożliwia dodanie kilku IpRule z obiektami IpRule, które są wprowadzane za pomocą notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="2c5a6-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c5a6-120">PARAMETERS</span></span>

### <span data-ttu-id="2c5a6-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2c5a6-121">-IPAddressOrRange</span></span>
<span data-ttu-id="2c5a6-122">Tablica IpAddressOrRange, Dodawanie IpRules z IpAddressOrRange wejściowym i akcją domyślną Zezwól na NetworkRule właściwości.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-122">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="2c5a6-123">-IPRule</span><span class="sxs-lookup"><span data-stu-id="2c5a6-123">-IPRule</span></span>
<span data-ttu-id="2c5a6-124">Tablica obiektów IpRule, które mają zostać dodane do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-124">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="2c5a6-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c5a6-125">-Name</span></span>
<span data-ttu-id="2c5a6-126">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-126">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="2c5a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c5a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c5a6-128">Określa nazwę grupy zasobów zawierającą konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-128">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="2c5a6-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="2c5a6-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="2c5a6-130">W tablicy VirtualNetworkResourceId zostaną dodane VirtualNetworkRule z VirtualNetworkResourceId wejściowym i akcją domyślną NetworkRule właściwości.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-130">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="2c5a6-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2c5a6-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="2c5a6-132">Tablica obiektów VirtualNetworkRule, które mają zostać dodane do właściwości NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-132">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="2c5a6-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c5a6-133">-Confirm</span></span>
<span data-ttu-id="2c5a6-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c5a6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c5a6-135">-WhatIf</span></span>
<span data-ttu-id="2c5a6-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c5a6-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c5a6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c5a6-138">-DefaultProfile</span></span>
<span data-ttu-id="2c5a6-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c5a6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5a6-140">CommonParameters</span></span>
<span data-ttu-id="2c5a6-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c5a6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5a6-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c5a6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5a6-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c5a6-143">INPUTS</span></span>

### <span data-ttu-id="2c5a6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2c5a6-144">System.String</span></span>
<span data-ttu-id="2c5a6-145">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="2c5a6-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="2c5a6-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c5a6-146">OUTPUTS</span></span>

### <span data-ttu-id="2c5a6-147">Microsoft. Azure. Commands. Management. Storage. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2c5a6-147">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="2c5a6-148">Microsoft. Azure. Commands. Management. Storage. models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="2c5a6-148">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="2c5a6-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c5a6-149">NOTES</span></span>

## <span data-ttu-id="2c5a6-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c5a6-150">RELATED LINKS</span></span>

