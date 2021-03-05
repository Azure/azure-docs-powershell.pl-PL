---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 8fe4787ca14d26b7e734a0ac081cdbaef8eddbd9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012241"
---
# <span data-ttu-id="9c9b5-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9c9b5-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="9c9b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c9b5-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9b5-103">Usuwa zamówienie na urządzenie.</span><span class="sxs-lookup"><span data-stu-id="9c9b5-103">Removes the order for a device.</span></span>

## <span data-ttu-id="9c9b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9c9b5-104">SYNTAX</span></span>

### <span data-ttu-id="9c9b5-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9c9b5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c9b5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c9b5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c9b5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c9b5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c9b5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9c9b5-108">DESCRIPTION</span></span>
<span data-ttu-id="9c9b5-109">Polecenie **cmdlet Remove-AzDataBoxEdgeOrder** usuwa istniejącą kolejność dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="9c9b5-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="9c9b5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9c9b5-110">EXAMPLES</span></span>

### <span data-ttu-id="9c9b5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c9b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="9c9b5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c9b5-112">PARAMETERS</span></span>

### <span data-ttu-id="9c9b5-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9c9b5-113">-AsJob</span></span>
<span data-ttu-id="9c9b5-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9c9b5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c9b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c9b5-115">-DefaultProfile</span></span>
<span data-ttu-id="9c9b5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c9b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c9b5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9c9b5-117">-DeviceName</span></span>
<span data-ttu-id="9c9b5-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="9c9b5-118">Device Name</span></span>

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

### <span data-ttu-id="9c9b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c9b5-119">-InputObject</span></span>
<span data-ttu-id="9c9b5-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="9c9b5-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c9b5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c9b5-121">-PassThru</span></span>
<span data-ttu-id="9c9b5-122">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="9c9b5-122">returns true if successful</span></span>

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

### <span data-ttu-id="9c9b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c9b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="9c9b5-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9c9b5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="9c9b5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c9b5-125">-ResourceId</span></span>
<span data-ttu-id="9c9b5-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c9b5-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="9c9b5-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c9b5-127">-Confirm</span></span>
<span data-ttu-id="9c9b5-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9c9b5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c9b5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c9b5-129">-WhatIf</span></span>
<span data-ttu-id="9c9b5-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c9b5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c9b5-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9c9b5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c9b5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9b5-132">CommonParameters</span></span>
<span data-ttu-id="9c9b5-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c9b5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9b5-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c9b5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9b5-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c9b5-135">INPUTS</span></span>

### <span data-ttu-id="9c9b5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9c9b5-136">System.String</span></span>

### <span data-ttu-id="9c9b5-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9c9b5-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="9c9b5-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c9b5-138">OUTPUTS</span></span>

### <span data-ttu-id="9c9b5-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9c9b5-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="9c9b5-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9c9b5-140">NOTES</span></span>

## <span data-ttu-id="9c9b5-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c9b5-141">RELATED LINKS</span></span>
