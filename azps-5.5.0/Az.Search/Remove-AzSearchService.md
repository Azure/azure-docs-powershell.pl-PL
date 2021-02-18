---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: eb5c139aea0520df77bf86af01bc3c02f8118263
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239995"
---
# <span data-ttu-id="f0847-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f0847-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="f0847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0847-102">SYNOPSIS</span></span>
<span data-ttu-id="f0847-103">Usuń usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f0847-103">Remove an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f0847-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f0847-104">SYNTAX</span></span>

### <span data-ttu-id="f0847-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f0847-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0847-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0847-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0847-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0847-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0847-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f0847-108">DESCRIPTION</span></span>
<span data-ttu-id="f0847-109">Polecenie **cmdlet Remove-AzSearchService** usuwa usługę Azure Cognitive Search o określonych parametrach.</span><span class="sxs-lookup"><span data-stu-id="f0847-109">The **Remove-AzSearchService** cmdlet removes an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="f0847-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f0847-110">EXAMPLES</span></span>

### <span data-ttu-id="f0847-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f0847-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="f0847-112">W tym przykładzie usuniemy usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f0847-112">The example removes an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f0847-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0847-113">PARAMETERS</span></span>

### <span data-ttu-id="f0847-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0847-114">-DefaultProfile</span></span>
<span data-ttu-id="f0847-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0847-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0847-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f0847-116">-Force</span></span>
<span data-ttu-id="f0847-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0847-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f0847-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0847-118">-InputObject</span></span>
<span data-ttu-id="f0847-119">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f0847-119">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="f0847-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f0847-120">-Name</span></span>
<span data-ttu-id="f0847-121">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f0847-121">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="f0847-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0847-122">-PassThru</span></span>
<span data-ttu-id="f0847-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f0847-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="f0847-124">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="f0847-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f0847-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0847-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0847-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f0847-126">Resource Group name.</span></span>

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

### <span data-ttu-id="f0847-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0847-127">-ResourceId</span></span>
<span data-ttu-id="f0847-128">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f0847-128">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="f0847-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0847-129">-Confirm</span></span>
<span data-ttu-id="f0847-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0847-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0847-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0847-131">-WhatIf</span></span>
<span data-ttu-id="f0847-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0847-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0847-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f0847-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0847-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0847-134">CommonParameters</span></span>
<span data-ttu-id="f0847-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0847-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0847-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0847-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0847-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0847-137">INPUTS</span></span>

### <span data-ttu-id="f0847-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="f0847-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="f0847-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f0847-139">System.String</span></span>

## <span data-ttu-id="f0847-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0847-140">OUTPUTS</span></span>

### <span data-ttu-id="f0847-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0847-141">System.Boolean</span></span>

## <span data-ttu-id="f0847-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f0847-142">NOTES</span></span>

## <span data-ttu-id="f0847-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0847-143">RELATED LINKS</span></span>

[<span data-ttu-id="f0847-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f0847-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="f0847-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f0847-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="f0847-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f0847-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)
