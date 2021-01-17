---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379108"
---
# <span data-ttu-id="fc364-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="fc364-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="fc364-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc364-102">SYNOPSIS</span></span>
<span data-ttu-id="fc364-103">Tworzy usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="fc364-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="fc364-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc364-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc364-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fc364-105">DESCRIPTION</span></span>
<span data-ttu-id="fc364-106">Polecenie cmdlet **New-AzIpAllocation** tworzy składnik Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="fc364-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="fc364-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc364-107">EXAMPLES</span></span>

### <span data-ttu-id="fc364-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc364-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="fc364-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fc364-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="fc364-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc364-110">PARAMETERS</span></span>

### <span data-ttu-id="fc364-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc364-111">-AsJob</span></span>
<span data-ttu-id="fc364-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fc364-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc364-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc364-113">-DefaultProfile</span></span>
<span data-ttu-id="fc364-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc364-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc364-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fc364-115">-Force</span></span>
<span data-ttu-id="fc364-116">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="fc364-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="fc364-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="fc364-117">-IpAllocationTag</span></span>
<span data-ttu-id="fc364-118">Znaczniki przydziału dla przydziału adresu IP</span><span class="sxs-lookup"><span data-stu-id="fc364-118">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="fc364-119">-IpAllocationType</span></span>
<span data-ttu-id="fc364-120">Typ przydziału adresu IP</span><span class="sxs-lookup"><span data-stu-id="fc364-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="fc364-121">-IpamAllocationId</span></span>
<span data-ttu-id="fc364-122">Identyfikator przydziału usługi IPAM przydziału adresów IP</span><span class="sxs-lookup"><span data-stu-id="fc364-122">The ipam allocation ID of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fc364-123">-Location</span></span>
<span data-ttu-id="fc364-124">pozycję.</span><span class="sxs-lookup"><span data-stu-id="fc364-124">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc364-125">-Name</span></span>
<span data-ttu-id="fc364-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="fc364-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="fc364-127">-Prefix</span></span>
<span data-ttu-id="fc364-128">Prefiks przydziału adresu IP</span><span class="sxs-lookup"><span data-stu-id="fc364-128">The prefix of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="fc364-129">-PrefixLength</span></span>
<span data-ttu-id="fc364-130">Długość prefiksu przydziału adresu IP</span><span class="sxs-lookup"><span data-stu-id="fc364-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-131">-Prefixtype</span><span class="sxs-lookup"><span data-stu-id="fc364-131">-PrefixType</span></span>
<span data-ttu-id="fc364-132">Typ prefiksu przydziału adresu IP</span><span class="sxs-lookup"><span data-stu-id="fc364-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc364-133">-ResourceGroupName</span></span>
<span data-ttu-id="fc364-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc364-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc364-135">-Tag</span></span>
<span data-ttu-id="fc364-136">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc364-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc364-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc364-137">-Confirm</span></span>
<span data-ttu-id="fc364-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc364-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc364-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc364-139">-WhatIf</span></span>
<span data-ttu-id="fc364-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc364-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc364-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc364-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc364-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc364-142">CommonParameters</span></span>
<span data-ttu-id="fc364-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc364-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc364-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc364-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc364-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc364-145">INPUTS</span></span>

### <span data-ttu-id="fc364-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fc364-146">System.String</span></span>

### <span data-ttu-id="fc364-147">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fc364-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="fc364-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fc364-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fc364-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc364-149">OUTPUTS</span></span>

### <span data-ttu-id="fc364-150">Microsoft. Azure. Commands. Network. models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="fc364-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="fc364-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc364-151">NOTES</span></span>

## <span data-ttu-id="fc364-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc364-152">RELATED LINKS</span></span>
