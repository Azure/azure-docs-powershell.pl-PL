---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 0e1011fb8e2aaec7a77f735c961fa6ec2ede9dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007658"
---
# <span data-ttu-id="c3581-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c3581-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="c3581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3581-102">SYNOPSIS</span></span>
<span data-ttu-id="c3581-103">Usuń usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="c3581-103">Remove an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c3581-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3581-104">SYNTAX</span></span>

### <span data-ttu-id="c3581-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c3581-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3581-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3581-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3581-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3581-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3581-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3581-108">DESCRIPTION</span></span>
<span data-ttu-id="c3581-109">Polecenie **cmdlet Remove-AzSearchService** usuwa usługę Azure Cognitive Search o określonych parametrach.</span><span class="sxs-lookup"><span data-stu-id="c3581-109">The **Remove-AzSearchService** cmdlet removes an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="c3581-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3581-110">EXAMPLES</span></span>

### <span data-ttu-id="c3581-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3581-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="c3581-112">W tym przykładzie usuniemy usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="c3581-112">The example removes an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c3581-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3581-113">PARAMETERS</span></span>

### <span data-ttu-id="c3581-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3581-114">-DefaultProfile</span></span>
<span data-ttu-id="c3581-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3581-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3581-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c3581-116">-Force</span></span>
<span data-ttu-id="c3581-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c3581-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c3581-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3581-118">-InputObject</span></span>
<span data-ttu-id="c3581-119">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="c3581-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3581-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c3581-120">-Name</span></span>
<span data-ttu-id="c3581-121">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="c3581-121">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3581-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3581-122">-PassThru</span></span>
<span data-ttu-id="c3581-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="c3581-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c3581-124">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="c3581-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c3581-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3581-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3581-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3581-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3581-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3581-127">-ResourceId</span></span>
<span data-ttu-id="c3581-128">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="c3581-128">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3581-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3581-129">-Confirm</span></span>
<span data-ttu-id="c3581-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c3581-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3581-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3581-131">-WhatIf</span></span>
<span data-ttu-id="c3581-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3581-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3581-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c3581-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3581-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3581-134">CommonParameters</span></span>
<span data-ttu-id="c3581-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3581-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3581-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3581-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3581-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3581-137">INPUTS</span></span>

### <span data-ttu-id="c3581-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c3581-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="c3581-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c3581-139">System.String</span></span>

## <span data-ttu-id="c3581-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3581-140">OUTPUTS</span></span>

### <span data-ttu-id="c3581-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3581-141">System.Boolean</span></span>

## <span data-ttu-id="c3581-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3581-142">NOTES</span></span>

## <span data-ttu-id="c3581-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3581-143">RELATED LINKS</span></span>

[<span data-ttu-id="c3581-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c3581-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="c3581-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c3581-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="c3581-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c3581-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)
