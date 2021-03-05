---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 2e1b3e3db319f724e22673e4139b4cb290879d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004289"
---
# <span data-ttu-id="719ee-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="719ee-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="719ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="719ee-102">SYNOPSIS</span></span>
<span data-ttu-id="719ee-103">Usuwa istniejący wyzwalacz na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="719ee-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="719ee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="719ee-104">SYNTAX</span></span>

### <span data-ttu-id="719ee-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="719ee-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="719ee-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="719ee-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="719ee-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="719ee-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="719ee-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="719ee-108">DESCRIPTION</span></span>
<span data-ttu-id="719ee-109">Polecenie **cmdlet Remove-AzDataBoxEdgeTrigger** usuwa istniejący wyzwalacz na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="719ee-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="719ee-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="719ee-110">EXAMPLES</span></span>

### <span data-ttu-id="719ee-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="719ee-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="719ee-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="719ee-112">PARAMETERS</span></span>

### <span data-ttu-id="719ee-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="719ee-113">-AsJob</span></span>
<span data-ttu-id="719ee-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="719ee-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="719ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="719ee-115">-DefaultProfile</span></span>
<span data-ttu-id="719ee-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="719ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="719ee-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="719ee-117">-DeviceName</span></span>
<span data-ttu-id="719ee-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="719ee-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719ee-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="719ee-119">-InputObject</span></span>
<span data-ttu-id="719ee-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="719ee-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="719ee-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="719ee-121">-Name</span></span>
<span data-ttu-id="719ee-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="719ee-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719ee-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="719ee-123">-PassThru</span></span>
<span data-ttu-id="719ee-124">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="719ee-124">returns true if successful</span></span>

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

### <span data-ttu-id="719ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="719ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="719ee-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="719ee-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="719ee-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="719ee-127">-ResourceId</span></span>
<span data-ttu-id="719ee-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="719ee-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="719ee-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="719ee-129">-Confirm</span></span>
<span data-ttu-id="719ee-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="719ee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="719ee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="719ee-131">-WhatIf</span></span>
<span data-ttu-id="719ee-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="719ee-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="719ee-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="719ee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="719ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="719ee-134">CommonParameters</span></span>
<span data-ttu-id="719ee-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="719ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="719ee-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="719ee-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="719ee-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="719ee-137">INPUTS</span></span>

### <span data-ttu-id="719ee-138">System.String</span><span class="sxs-lookup"><span data-stu-id="719ee-138">System.String</span></span>

### <span data-ttu-id="719ee-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="719ee-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="719ee-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="719ee-140">OUTPUTS</span></span>

### <span data-ttu-id="719ee-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="719ee-141">System.Boolean</span></span>

## <span data-ttu-id="719ee-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="719ee-142">NOTES</span></span>

## <span data-ttu-id="719ee-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="719ee-143">RELATED LINKS</span></span>
