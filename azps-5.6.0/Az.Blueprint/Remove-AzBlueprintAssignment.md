---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: f8a50a7e9686a3e40f517992e6c4de9912e8671b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965105"
---
# <span data-ttu-id="e52c0-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e52c0-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e52c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e52c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e52c0-103">Usuń przypisanie planu z subskrypcji lub grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e52c0-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="e52c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e52c0-104">SYNTAX</span></span>

### <span data-ttu-id="e52c0-105">BySubscriptionAndName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e52c0-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e52c0-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="e52c0-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e52c0-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="e52c0-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e52c0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e52c0-108">DESCRIPTION</span></span>
<span data-ttu-id="e52c0-109">Usuń plan, który został przypisany do subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e52c0-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="e52c0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e52c0-110">EXAMPLES</span></span>

### <span data-ttu-id="e52c0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e52c0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="e52c0-112">Usuń przypisanie planu określonego za pomocą nazwy z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e52c0-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="e52c0-113">Polecenie cmdlet wyświetli monit o potwierdzenie przed wykonaniem polecenia.</span><span class="sxs-lookup"><span data-stu-id="e52c0-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="e52c0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e52c0-114">PARAMETERS</span></span>

### <span data-ttu-id="e52c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e52c0-115">-DefaultProfile</span></span>
<span data-ttu-id="e52c0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e52c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e52c0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e52c0-117">-InputObject</span></span>
<span data-ttu-id="e52c0-118">Obiekt przydziału planu.</span><span class="sxs-lookup"><span data-stu-id="e52c0-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e52c0-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e52c0-119">-ManagementGroupId</span></span>
<span data-ttu-id="e52c0-120">Identyfikator grupy zarządzania, w której jest zapisywany przydział Plan.</span><span class="sxs-lookup"><span data-stu-id="e52c0-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e52c0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e52c0-121">-Name</span></span>
<span data-ttu-id="e52c0-122">Nazwa zadania planu.</span><span class="sxs-lookup"><span data-stu-id="e52c0-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e52c0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e52c0-123">-PassThru</span></span>
<span data-ttu-id="e52c0-124">Po jego skonfigurowaniu polecenie cmdlet zwróci obiekt reprezentujący usunięte przypisanie Plan.</span><span class="sxs-lookup"><span data-stu-id="e52c0-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="e52c0-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e52c0-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e52c0-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e52c0-126">-SubscriptionId</span></span>
<span data-ttu-id="e52c0-127">Identyfikator subskrypcji, w ramach których wdrożono przypisanie planu.</span><span class="sxs-lookup"><span data-stu-id="e52c0-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e52c0-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e52c0-128">-Confirm</span></span>
<span data-ttu-id="e52c0-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e52c0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e52c0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e52c0-130">-WhatIf</span></span>
<span data-ttu-id="e52c0-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e52c0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e52c0-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e52c0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e52c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e52c0-133">CommonParameters</span></span>
<span data-ttu-id="e52c0-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e52c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e52c0-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e52c0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e52c0-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e52c0-136">INPUTS</span></span>

### <span data-ttu-id="e52c0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e52c0-137">System.String</span></span>

### <span data-ttu-id="e52c0-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="e52c0-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="e52c0-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e52c0-139">OUTPUTS</span></span>

### <span data-ttu-id="e52c0-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="e52c0-140">System.Object</span></span>
## <span data-ttu-id="e52c0-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e52c0-141">NOTES</span></span>

## <span data-ttu-id="e52c0-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e52c0-142">RELATED LINKS</span></span>
