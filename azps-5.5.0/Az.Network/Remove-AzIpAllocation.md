---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189611"
---
# <span data-ttu-id="0b2f0-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="0b2f0-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="0b2f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2f0-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2f0-103">Usuwa usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="0b2f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b2f0-104">SYNTAX</span></span>

### <span data-ttu-id="0b2f0-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b2f0-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2f0-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b2f0-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2f0-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b2f0-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b2f0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b2f0-108">DESCRIPTION</span></span>
<span data-ttu-id="0b2f0-109">Polecenie **cmdlet Remove-AzIpAllocation** usuwa usługę Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="0b2f0-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="0b2f0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b2f0-110">EXAMPLES</span></span>

### <span data-ttu-id="0b2f0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0b2f0-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="0b2f0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b2f0-112">PARAMETERS</span></span>

### <span data-ttu-id="0b2f0-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0b2f0-113">-AsJob</span></span>
<span data-ttu-id="0b2f0-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0b2f0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b2f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2f0-115">-DefaultProfile</span></span>
<span data-ttu-id="0b2f0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2f0-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0b2f0-117">-Force</span></span>
<span data-ttu-id="0b2f0-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0b2f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b2f0-119">-InputObject</span></span>
<span data-ttu-id="0b2f0-120">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="0b2f0-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0b2f0-121">-Name</span></span>
<span data-ttu-id="0b2f0-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b2f0-123">-PassThru</span></span>
<span data-ttu-id="0b2f0-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0b2f0-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b2f0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2f0-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b2f0-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b2f0-128">-ResourceId</span></span>
<span data-ttu-id="0b2f0-129">Identyfikator zasobu IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2f0-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b2f0-130">-Confirm</span></span>
<span data-ttu-id="0b2f0-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2f0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2f0-132">-WhatIf</span></span>
<span data-ttu-id="0b2f0-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2f0-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2f0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2f0-135">CommonParameters</span></span>
<span data-ttu-id="0b2f0-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2f0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2f0-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b2f0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2f0-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b2f0-138">INPUTS</span></span>

### <span data-ttu-id="0b2f0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0b2f0-139">System.String</span></span>

## <span data-ttu-id="0b2f0-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0b2f0-140">OUTPUTS</span></span>

### <span data-ttu-id="0b2f0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b2f0-141">System.Boolean</span></span>

## <span data-ttu-id="0b2f0-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b2f0-142">NOTES</span></span>

## <span data-ttu-id="0b2f0-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b2f0-143">RELATED LINKS</span></span>
