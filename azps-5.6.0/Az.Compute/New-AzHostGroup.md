---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 69ab5a7ae89184a5d77344d45801da307e7840bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959674"
---
# <span data-ttu-id="217c4-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="217c4-101">New-AzHostGroup</span></span>

## <span data-ttu-id="217c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="217c4-102">SYNOPSIS</span></span>
<span data-ttu-id="217c4-103">Tworzy grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="217c4-103">Creates a host group.</span></span>

## <span data-ttu-id="217c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="217c4-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="217c4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="217c4-105">DESCRIPTION</span></span>
<span data-ttu-id="217c4-106">To polecenie cmdlet utworzy grupę hosta.</span><span class="sxs-lookup"><span data-stu-id="217c4-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="217c4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="217c4-107">EXAMPLES</span></span>

### <span data-ttu-id="217c4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="217c4-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="217c4-109">To polecenie umożliwia utworzenie grupy hostów w podanej lokalizacji i strefie.</span><span class="sxs-lookup"><span data-stu-id="217c4-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="217c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="217c4-110">PARAMETERS</span></span>

### <span data-ttu-id="217c4-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="217c4-111">-AsJob</span></span>
<span data-ttu-id="217c4-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="217c4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="217c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217c4-113">-DefaultProfile</span></span>
<span data-ttu-id="217c4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="217c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="217c4-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="217c4-115">-Location</span></span>
<span data-ttu-id="217c4-116">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="217c4-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217c4-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="217c4-117">-Name</span></span>
<span data-ttu-id="217c4-118">Określa nazwę grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="217c4-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="217c4-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="217c4-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="217c4-120">Określa liczbę domen błędów, które może obejmować grupa hosta.</span><span class="sxs-lookup"><span data-stu-id="217c4-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="217c4-121">Wartość minimalna wynosi 1, a maksymalna 3.</span><span class="sxs-lookup"><span data-stu-id="217c4-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="217c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="217c4-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="217c4-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="217c4-124">— Tag</span><span class="sxs-lookup"><span data-stu-id="217c4-124">-Tag</span></span>
<span data-ttu-id="217c4-125">Określa tagi</span><span class="sxs-lookup"><span data-stu-id="217c4-125">Specifies Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217c4-126">— Strefa</span><span class="sxs-lookup"><span data-stu-id="217c4-126">-Zone</span></span>
<span data-ttu-id="217c4-127">Określa strefy grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="217c4-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217c4-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="217c4-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="217c4-129">Określa, czy grupa HostGroup włączy automatyczne rozmieszczanie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="217c4-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="217c4-130">Automatyczne rozmieszczanie oznacza, że te maszyny wirtualne są umieszczane na dedykowanych hostach wybranych przez platformę Azure w ramach dedykowanej grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="217c4-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="217c4-131">Jeśli nie zostanie określona, wartość domyślna będzie fałszywa.</span><span class="sxs-lookup"><span data-stu-id="217c4-131">If not specified, default value will be false.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="217c4-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="217c4-132">-Confirm</span></span>
<span data-ttu-id="217c4-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="217c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="217c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="217c4-134">-WhatIf</span></span>
<span data-ttu-id="217c4-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="217c4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="217c4-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="217c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="217c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217c4-137">CommonParameters</span></span>
<span data-ttu-id="217c4-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="217c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217c4-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="217c4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217c4-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="217c4-140">INPUTS</span></span>

### <span data-ttu-id="217c4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="217c4-141">System.String</span></span>

## <span data-ttu-id="217c4-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="217c4-142">OUTPUTS</span></span>

### <span data-ttu-id="217c4-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="217c4-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="217c4-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="217c4-144">NOTES</span></span>

## <span data-ttu-id="217c4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="217c4-145">RELATED LINKS</span></span>
