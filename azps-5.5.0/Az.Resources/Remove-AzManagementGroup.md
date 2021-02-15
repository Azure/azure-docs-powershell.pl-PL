---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201874"
---
# <span data-ttu-id="d9278-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d9278-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="d9278-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9278-102">SYNOPSIS</span></span>
<span data-ttu-id="d9278-103">Usuwa grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="d9278-103">Removes a Management Group</span></span>

## <span data-ttu-id="d9278-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9278-104">SYNTAX</span></span>

### <span data-ttu-id="d9278-105">GroupOperations (Default)</span><span class="sxs-lookup"><span data-stu-id="d9278-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9278-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="d9278-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9278-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9278-107">DESCRIPTION</span></span>
<span data-ttu-id="d9278-108">Polecenie **cmdlet Remove-AzManagementGroup** usuwa grupę zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d9278-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="d9278-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9278-109">EXAMPLES</span></span>

### <span data-ttu-id="d9278-110">Przykład 1. Usuwanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="d9278-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="d9278-111">Przykład 2. Usuwanie grupy zarządzania za pomocą rurowego obiektu PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d9278-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="d9278-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9278-112">PARAMETERS</span></span>

### <span data-ttu-id="d9278-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9278-113">-DefaultProfile</span></span>
<span data-ttu-id="d9278-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9278-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9278-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="d9278-115">-GroupName</span></span>
<span data-ttu-id="d9278-116">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="d9278-116">Management Group Id</span></span>

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

### <span data-ttu-id="d9278-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9278-117">-InputObject</span></span>
<span data-ttu-id="d9278-118">Input Object from the Get call</span><span class="sxs-lookup"><span data-stu-id="d9278-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="d9278-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9278-119">-PassThru</span></span>
<span data-ttu-id="d9278-120">Powrót `true` do pomyślnego wykonania</span><span class="sxs-lookup"><span data-stu-id="d9278-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="d9278-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9278-121">-Confirm</span></span>
<span data-ttu-id="d9278-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9278-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9278-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9278-123">-WhatIf</span></span>
<span data-ttu-id="d9278-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9278-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9278-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9278-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9278-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9278-126">CommonParameters</span></span>
<span data-ttu-id="d9278-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9278-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9278-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9278-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9278-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9278-129">INPUTS</span></span>

### <span data-ttu-id="d9278-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d9278-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="d9278-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d9278-131">OUTPUTS</span></span>

### <span data-ttu-id="d9278-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d9278-132">System.Boolean</span></span>

## <span data-ttu-id="d9278-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9278-133">NOTES</span></span>

## <span data-ttu-id="d9278-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9278-134">RELATED LINKS</span></span>
