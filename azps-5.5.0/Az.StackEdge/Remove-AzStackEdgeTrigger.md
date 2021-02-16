---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: ad2761e4e0fba3ef7dbb7a28b15477a649891042
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176682"
---
# <span data-ttu-id="848f8-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="848f8-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="848f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="848f8-102">SYNOPSIS</span></span>
<span data-ttu-id="848f8-103">Usuwa istniejący wyzwalacz na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="848f8-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="848f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="848f8-104">SYNTAX</span></span>

### <span data-ttu-id="848f8-105">DeleteByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="848f8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848f8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="848f8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848f8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="848f8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="848f8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="848f8-108">DESCRIPTION</span></span>
<span data-ttu-id="848f8-109">Polecenie **cmdlet Remove-AzStackEdgeTrigger** usuwa istniejący wyzwalacz na urządzeniu Ze stosem Edge.</span><span class="sxs-lookup"><span data-stu-id="848f8-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="848f8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="848f8-110">EXAMPLES</span></span>

### <span data-ttu-id="848f8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="848f8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="848f8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="848f8-112">PARAMETERS</span></span>

### <span data-ttu-id="848f8-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="848f8-113">-AsJob</span></span>
<span data-ttu-id="848f8-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="848f8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="848f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848f8-115">-DefaultProfile</span></span>
<span data-ttu-id="848f8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="848f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="848f8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="848f8-117">-DeviceName</span></span>
<span data-ttu-id="848f8-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="848f8-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848f8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="848f8-119">-InputObject</span></span>
<span data-ttu-id="848f8-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="848f8-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="848f8-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="848f8-121">-Name</span></span>
<span data-ttu-id="848f8-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="848f8-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848f8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="848f8-123">-PassThru</span></span>
<span data-ttu-id="848f8-124">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="848f8-124">returns true if successful</span></span>

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

### <span data-ttu-id="848f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="848f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="848f8-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="848f8-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848f8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="848f8-127">-ResourceId</span></span>
<span data-ttu-id="848f8-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="848f8-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848f8-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="848f8-129">-Confirm</span></span>
<span data-ttu-id="848f8-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="848f8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="848f8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="848f8-131">-WhatIf</span></span>
<span data-ttu-id="848f8-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="848f8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="848f8-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="848f8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="848f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848f8-134">CommonParameters</span></span>
<span data-ttu-id="848f8-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="848f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848f8-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="848f8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848f8-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="848f8-137">INPUTS</span></span>

### <span data-ttu-id="848f8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="848f8-138">System.String</span></span>

### <span data-ttu-id="848f8-139">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="848f8-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="848f8-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="848f8-140">OUTPUTS</span></span>

### <span data-ttu-id="848f8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="848f8-141">System.Boolean</span></span>

## <span data-ttu-id="848f8-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="848f8-142">NOTES</span></span>

## <span data-ttu-id="848f8-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="848f8-143">RELATED LINKS</span></span>
