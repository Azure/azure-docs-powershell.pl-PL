---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063591"
---
# <span data-ttu-id="6f45e-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="6f45e-101">New-AzHostGroup</span></span>

## <span data-ttu-id="6f45e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f45e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f45e-103">Tworzy grupę hostów.</span><span class="sxs-lookup"><span data-stu-id="6f45e-103">Creates a host group.</span></span>

## <span data-ttu-id="6f45e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f45e-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f45e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6f45e-105">DESCRIPTION</span></span>
<span data-ttu-id="6f45e-106">To polecenie cmdlet utworzy grupę hostów.</span><span class="sxs-lookup"><span data-stu-id="6f45e-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="6f45e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f45e-107">EXAMPLES</span></span>

### <span data-ttu-id="6f45e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6f45e-108">Example 1</span></span>
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

<span data-ttu-id="6f45e-109">To polecenie tworzy grupę hostów w podanej lokalizacji i strefie.</span><span class="sxs-lookup"><span data-stu-id="6f45e-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="6f45e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f45e-110">PARAMETERS</span></span>

### <span data-ttu-id="6f45e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f45e-111">-AsJob</span></span>
<span data-ttu-id="6f45e-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6f45e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f45e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f45e-113">-DefaultProfile</span></span>
<span data-ttu-id="6f45e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f45e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f45e-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6f45e-115">-Location</span></span>
<span data-ttu-id="6f45e-116">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="6f45e-116">Specifies location.</span></span>

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

### <span data-ttu-id="6f45e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f45e-117">-Name</span></span>
<span data-ttu-id="6f45e-118">Określa nazwę grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="6f45e-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="6f45e-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="6f45e-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="6f45e-120">Określa liczbę domen błędów, które może obejmować Grupa hostów.</span><span class="sxs-lookup"><span data-stu-id="6f45e-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="6f45e-121">Minimalna wartość wynosi 1, a wartość maksymalna to 3.</span><span class="sxs-lookup"><span data-stu-id="6f45e-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="6f45e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f45e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f45e-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6f45e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6f45e-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="6f45e-124">-Tag</span></span>
<span data-ttu-id="6f45e-125">Określa Tagi</span><span class="sxs-lookup"><span data-stu-id="6f45e-125">Specifies Tags</span></span>

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

### <span data-ttu-id="6f45e-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="6f45e-126">-Zone</span></span>
<span data-ttu-id="6f45e-127">Określa strefy grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="6f45e-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="6f45e-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="6f45e-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="6f45e-129">Określa, czy element Host umożliwia automatyczne umieszczanie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f45e-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="6f45e-130">Automatyczne umieszczanie oznacza, że te maszyny wirtualne są umieszczane na dedykowanych hostach, wybranych przez usługę Azure w ramach dedykowanej grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="6f45e-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="6f45e-131">Jeśli nie określono, wartość domyślna będzie równa prawda.</span><span class="sxs-lookup"><span data-stu-id="6f45e-131">If not specified, default value will be true.</span></span>

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


### <span data-ttu-id="6f45e-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f45e-132">-Confirm</span></span>
<span data-ttu-id="6f45e-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f45e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f45e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f45e-134">-WhatIf</span></span>
<span data-ttu-id="6f45e-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f45e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f45e-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6f45e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f45e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f45e-137">CommonParameters</span></span>
<span data-ttu-id="6f45e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f45e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f45e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f45e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f45e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f45e-140">INPUTS</span></span>

### <span data-ttu-id="6f45e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6f45e-141">System.String</span></span>

## <span data-ttu-id="6f45e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f45e-142">OUTPUTS</span></span>

### <span data-ttu-id="6f45e-143">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="6f45e-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="6f45e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f45e-144">NOTES</span></span>

## <span data-ttu-id="6f45e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f45e-145">RELATED LINKS</span></span>
