---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184451"
---
# <span data-ttu-id="90069-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="90069-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="90069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90069-102">SYNOPSIS</span></span>
<span data-ttu-id="90069-103">Tworzy usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="90069-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="90069-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="90069-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90069-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="90069-105">DESCRIPTION</span></span>
<span data-ttu-id="90069-106">Polecenie **cmdlet New-AzIpAllocation** tworzy usługę Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="90069-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="90069-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="90069-107">EXAMPLES</span></span>

### <span data-ttu-id="90069-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90069-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="90069-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="90069-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="90069-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90069-110">PARAMETERS</span></span>

### <span data-ttu-id="90069-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="90069-111">-AsJob</span></span>
<span data-ttu-id="90069-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="90069-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90069-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90069-113">-DefaultProfile</span></span>
<span data-ttu-id="90069-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="90069-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90069-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="90069-115">-Force</span></span>
<span data-ttu-id="90069-116">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="90069-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="90069-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="90069-117">-IpAllocationTag</span></span>
<span data-ttu-id="90069-118">Tagi alokacji w przydziałach adresów IP</span><span class="sxs-lookup"><span data-stu-id="90069-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="90069-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="90069-119">-IpAllocationType</span></span>
<span data-ttu-id="90069-120">Typ alokacji adresów IP</span><span class="sxs-lookup"><span data-stu-id="90069-120">The type of the IP allocation</span></span>

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

### <span data-ttu-id="90069-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="90069-121">-IpamAllocationId</span></span>
<span data-ttu-id="90069-122">Identyfikator alokacji ipam w alokacji ipam</span><span class="sxs-lookup"><span data-stu-id="90069-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="90069-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="90069-123">-Location</span></span>
<span data-ttu-id="90069-124">.</span><span class="sxs-lookup"><span data-stu-id="90069-124">location.</span></span>

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

### <span data-ttu-id="90069-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="90069-125">-Name</span></span>
<span data-ttu-id="90069-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="90069-126">The resource name.</span></span>

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

### <span data-ttu-id="90069-127">—Prefiks</span><span class="sxs-lookup"><span data-stu-id="90069-127">-Prefix</span></span>
<span data-ttu-id="90069-128">Prefiks alokacji IP</span><span class="sxs-lookup"><span data-stu-id="90069-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="90069-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="90069-129">-PrefixLength</span></span>
<span data-ttu-id="90069-130">Długość prefiksu w alokacji adresów IP</span><span class="sxs-lookup"><span data-stu-id="90069-130">The prefix length of the IP allocation</span></span>

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

### <span data-ttu-id="90069-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="90069-131">-PrefixType</span></span>
<span data-ttu-id="90069-132">Typ prefiksu alokacji IP</span><span class="sxs-lookup"><span data-stu-id="90069-132">The prefix type of the IP allocation</span></span>

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

### <span data-ttu-id="90069-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90069-133">-ResourceGroupName</span></span>
<span data-ttu-id="90069-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="90069-134">The resource group name.</span></span>

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

### <span data-ttu-id="90069-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="90069-135">-Tag</span></span>
<span data-ttu-id="90069-136">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="90069-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="90069-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90069-137">-Confirm</span></span>
<span data-ttu-id="90069-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="90069-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90069-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90069-139">-WhatIf</span></span>
<span data-ttu-id="90069-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90069-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90069-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="90069-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90069-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90069-142">CommonParameters</span></span>
<span data-ttu-id="90069-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90069-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90069-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90069-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90069-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90069-145">INPUTS</span></span>

### <span data-ttu-id="90069-146">System.String</span><span class="sxs-lookup"><span data-stu-id="90069-146">System.String</span></span>

### <span data-ttu-id="90069-147">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="90069-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="90069-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="90069-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="90069-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90069-149">OUTPUTS</span></span>

### <span data-ttu-id="90069-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="90069-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="90069-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="90069-151">NOTES</span></span>

## <span data-ttu-id="90069-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90069-152">RELATED LINKS</span></span>
