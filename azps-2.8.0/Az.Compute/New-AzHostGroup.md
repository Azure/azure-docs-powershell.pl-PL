---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 9d6614204c8c6e8e95617ed989e3f75b88c9744e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706340"
---
# <span data-ttu-id="e6e47-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="e6e47-101">New-AzHostGroup</span></span>

## <span data-ttu-id="e6e47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6e47-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e47-103">Tworzy grupę hostów.</span><span class="sxs-lookup"><span data-stu-id="e6e47-103">Creates a host group.</span></span>

## <span data-ttu-id="e6e47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6e47-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e47-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6e47-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e47-106">To polecenie cmdlet utworzy grupę hostów.</span><span class="sxs-lookup"><span data-stu-id="e6e47-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="e6e47-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6e47-107">EXAMPLES</span></span>

### <span data-ttu-id="e6e47-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6e47-108">Example 1</span></span>
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

<span data-ttu-id="e6e47-109">To polecenie tworzy grupę hostów w podanej lokalizacji i strefie.</span><span class="sxs-lookup"><span data-stu-id="e6e47-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="e6e47-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6e47-110">PARAMETERS</span></span>

### <span data-ttu-id="e6e47-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6e47-111">-AsJob</span></span>
<span data-ttu-id="e6e47-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e6e47-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6e47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e47-113">-DefaultProfile</span></span>
<span data-ttu-id="e6e47-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e47-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6e47-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e6e47-115">-Location</span></span>
<span data-ttu-id="e6e47-116">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="e6e47-116">Specifies location.</span></span>

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

### <span data-ttu-id="e6e47-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6e47-117">-Name</span></span>
<span data-ttu-id="e6e47-118">Określa nazwę grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="e6e47-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="e6e47-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="e6e47-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="e6e47-120">Określa liczbę domen błędów, które może obejmować Grupa hostów.</span><span class="sxs-lookup"><span data-stu-id="e6e47-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="e6e47-121">Minimalna wartość wynosi 1, a wartość maksymalna to 3.</span><span class="sxs-lookup"><span data-stu-id="e6e47-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="e6e47-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e47-122">-ResourceGroupName</span></span>
<span data-ttu-id="e6e47-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6e47-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6e47-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6e47-124">-Tag</span></span>
<span data-ttu-id="e6e47-125">Określa Tagi</span><span class="sxs-lookup"><span data-stu-id="e6e47-125">Specifies Tags</span></span>

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

### <span data-ttu-id="e6e47-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="e6e47-126">-Zone</span></span>
<span data-ttu-id="e6e47-127">Określa strefy grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="e6e47-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="e6e47-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6e47-128">-Confirm</span></span>
<span data-ttu-id="e6e47-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e47-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e47-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e47-130">-WhatIf</span></span>
<span data-ttu-id="e6e47-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e47-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e47-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e6e47-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e47-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e47-133">CommonParameters</span></span>
<span data-ttu-id="e6e47-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e47-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e47-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6e47-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e47-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6e47-136">INPUTS</span></span>

### <span data-ttu-id="e6e47-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e6e47-137">System.String</span></span>

## <span data-ttu-id="e6e47-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6e47-138">OUTPUTS</span></span>

### <span data-ttu-id="e6e47-139">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="e6e47-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="e6e47-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6e47-140">NOTES</span></span>

## <span data-ttu-id="e6e47-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6e47-141">RELATED LINKS</span></span>