---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 716beafc05c4746d0cfe76dce70109226b1f8f26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005162"
---
# <span data-ttu-id="0dbf8-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="0dbf8-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="0dbf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dbf8-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbf8-103">Usuwa zamówienie na urządzenie.</span><span class="sxs-lookup"><span data-stu-id="0dbf8-103">Removes the order for a device.</span></span>

## <span data-ttu-id="0dbf8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0dbf8-104">SYNTAX</span></span>

### <span data-ttu-id="0dbf8-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0dbf8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dbf8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dbf8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dbf8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dbf8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dbf8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0dbf8-108">DESCRIPTION</span></span>
<span data-ttu-id="0dbf8-109">Polecenie **cmdlet Remove-AzStackEdgeOrder** usuwa istniejącą kolejność dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="0dbf8-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="0dbf8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0dbf8-110">EXAMPLES</span></span>

### <span data-ttu-id="0dbf8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0dbf8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="0dbf8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dbf8-112">PARAMETERS</span></span>

### <span data-ttu-id="0dbf8-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0dbf8-113">-AsJob</span></span>
<span data-ttu-id="0dbf8-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0dbf8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0dbf8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbf8-115">-DefaultProfile</span></span>
<span data-ttu-id="0dbf8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0dbf8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dbf8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0dbf8-117">-DeviceName</span></span>
<span data-ttu-id="0dbf8-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="0dbf8-118">Device Name</span></span>

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

### <span data-ttu-id="0dbf8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dbf8-119">-InputObject</span></span>
<span data-ttu-id="0dbf8-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="0dbf8-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dbf8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dbf8-121">-PassThru</span></span>
<span data-ttu-id="0dbf8-122">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="0dbf8-122">returns true if successful</span></span>

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

### <span data-ttu-id="0dbf8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dbf8-123">-ResourceGroupName</span></span>
<span data-ttu-id="0dbf8-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0dbf8-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0dbf8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0dbf8-125">-ResourceId</span></span>
<span data-ttu-id="0dbf8-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0dbf8-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="0dbf8-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0dbf8-127">-Confirm</span></span>
<span data-ttu-id="0dbf8-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0dbf8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dbf8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dbf8-129">-WhatIf</span></span>
<span data-ttu-id="0dbf8-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dbf8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dbf8-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0dbf8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dbf8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbf8-132">CommonParameters</span></span>
<span data-ttu-id="0dbf8-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dbf8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbf8-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dbf8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbf8-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dbf8-135">INPUTS</span></span>

### <span data-ttu-id="0dbf8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0dbf8-136">System.String</span></span>

### <span data-ttu-id="0dbf8-137">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="0dbf8-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="0dbf8-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dbf8-138">OUTPUTS</span></span>

### <span data-ttu-id="0dbf8-139">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="0dbf8-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="0dbf8-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0dbf8-140">NOTES</span></span>

## <span data-ttu-id="0dbf8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0dbf8-141">RELATED LINKS</span></span>
