---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: e8a9c1f65c536abb3c7b3e7aa983292ccde925a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996318"
---
# <span data-ttu-id="cee04-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="cee04-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="cee04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cee04-102">SYNOPSIS</span></span>
<span data-ttu-id="cee04-103">Usuwa usługę Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="cee04-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="cee04-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cee04-104">SYNTAX</span></span>

### <span data-ttu-id="cee04-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cee04-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cee04-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cee04-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cee04-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cee04-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cee04-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cee04-108">DESCRIPTION</span></span>
<span data-ttu-id="cee04-109">Polecenie **cmdlet Remove-AzIpAllocation** usuwa usługę Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="cee04-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="cee04-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cee04-110">EXAMPLES</span></span>

### <span data-ttu-id="cee04-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cee04-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="cee04-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cee04-112">PARAMETERS</span></span>

### <span data-ttu-id="cee04-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cee04-113">-AsJob</span></span>
<span data-ttu-id="cee04-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cee04-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cee04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee04-115">-DefaultProfile</span></span>
<span data-ttu-id="cee04-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cee04-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cee04-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cee04-117">-Force</span></span>
<span data-ttu-id="cee04-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cee04-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cee04-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cee04-119">-InputObject</span></span>
<span data-ttu-id="cee04-120">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="cee04-120">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="cee04-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cee04-121">-Name</span></span>
<span data-ttu-id="cee04-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cee04-122">The resource name.</span></span>

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

### <span data-ttu-id="cee04-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cee04-123">-PassThru</span></span>
<span data-ttu-id="cee04-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="cee04-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cee04-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cee04-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cee04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee04-126">-ResourceGroupName</span></span>
<span data-ttu-id="cee04-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cee04-127">The resource group name.</span></span>

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

### <span data-ttu-id="cee04-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cee04-128">-ResourceId</span></span>
<span data-ttu-id="cee04-129">Identyfikator zasobu IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="cee04-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="cee04-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cee04-130">-Confirm</span></span>
<span data-ttu-id="cee04-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cee04-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cee04-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee04-132">-WhatIf</span></span>
<span data-ttu-id="cee04-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cee04-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cee04-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cee04-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cee04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee04-135">CommonParameters</span></span>
<span data-ttu-id="cee04-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee04-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cee04-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee04-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cee04-138">INPUTS</span></span>

### <span data-ttu-id="cee04-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cee04-139">System.String</span></span>

## <span data-ttu-id="cee04-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cee04-140">OUTPUTS</span></span>

### <span data-ttu-id="cee04-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cee04-141">System.Boolean</span></span>

## <span data-ttu-id="cee04-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cee04-142">NOTES</span></span>

## <span data-ttu-id="cee04-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cee04-143">RELATED LINKS</span></span>
