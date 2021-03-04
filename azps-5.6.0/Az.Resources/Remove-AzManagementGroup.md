---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 8ef763300d530c764aefc3fa18c6bbf2a781b4b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967697"
---
# <span data-ttu-id="b8534-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b8534-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="b8534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8534-102">SYNOPSIS</span></span>
<span data-ttu-id="b8534-103">Usuwa grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="b8534-103">Removes a Management Group</span></span>

## <span data-ttu-id="b8534-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8534-104">SYNTAX</span></span>

### <span data-ttu-id="b8534-105">GroupOperations (Default)</span><span class="sxs-lookup"><span data-stu-id="b8534-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8534-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="b8534-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8534-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8534-107">DESCRIPTION</span></span>
<span data-ttu-id="b8534-108">Polecenie **cmdlet Remove-AzManagementGroup** usuwa grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="b8534-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="b8534-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8534-109">EXAMPLES</span></span>

### <span data-ttu-id="b8534-110">Przykład 1. Usuwanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="b8534-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="b8534-111">Przykład 2. Usuwanie grupy zarządzania za pomocą rurowego obiektu PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b8534-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="b8534-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8534-112">PARAMETERS</span></span>

### <span data-ttu-id="b8534-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8534-113">-DefaultProfile</span></span>
<span data-ttu-id="b8534-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8534-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8534-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="b8534-115">-GroupName</span></span>
<span data-ttu-id="b8534-116">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="b8534-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8534-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8534-117">-InputObject</span></span>
<span data-ttu-id="b8534-118">Input Object from the Get call</span><span class="sxs-lookup"><span data-stu-id="b8534-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8534-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8534-119">-PassThru</span></span>
<span data-ttu-id="b8534-120">Powrót `true` do pomyślnego wykonania</span><span class="sxs-lookup"><span data-stu-id="b8534-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="b8534-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8534-121">-Confirm</span></span>
<span data-ttu-id="b8534-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8534-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8534-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8534-123">-WhatIf</span></span>
<span data-ttu-id="b8534-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8534-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8534-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b8534-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8534-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8534-126">CommonParameters</span></span>
<span data-ttu-id="b8534-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8534-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8534-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8534-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8534-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8534-129">INPUTS</span></span>

### <span data-ttu-id="b8534-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b8534-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="b8534-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8534-131">OUTPUTS</span></span>

### <span data-ttu-id="b8534-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b8534-132">System.Boolean</span></span>

## <span data-ttu-id="b8534-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8534-133">NOTES</span></span>

## <span data-ttu-id="b8534-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8534-134">RELATED LINKS</span></span>
