---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: bf0c995081e98f3c3e79af2aec8da5144c3e2e32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998544"
---
# <span data-ttu-id="ebe92-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ebe92-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="ebe92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebe92-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe92-103">Usuwa skojarzoną rolę IoT dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="ebe92-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="ebe92-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ebe92-104">SYNTAX</span></span>

### <span data-ttu-id="ebe92-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ebe92-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe92-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebe92-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe92-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebe92-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebe92-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ebe92-108">DESCRIPTION</span></span>
<span data-ttu-id="ebe92-109">Polecenie **cmdlet Remove-AzDataBoxEdgeRole** usuwa skojarzoną rolę IoT dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="ebe92-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="ebe92-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ebe92-110">EXAMPLES</span></span>

### <span data-ttu-id="ebe92-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ebe92-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="ebe92-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebe92-112">PARAMETERS</span></span>

### <span data-ttu-id="ebe92-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ebe92-113">-AsJob</span></span>
<span data-ttu-id="ebe92-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ebe92-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebe92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe92-115">-DefaultProfile</span></span>
<span data-ttu-id="ebe92-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe92-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebe92-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ebe92-117">-DeviceName</span></span>
<span data-ttu-id="ebe92-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="ebe92-118">Device Name</span></span>

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

### <span data-ttu-id="ebe92-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebe92-119">-InputObject</span></span>
<span data-ttu-id="ebe92-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="ebe92-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe92-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ebe92-121">-Name</span></span>
<span data-ttu-id="ebe92-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="ebe92-122">Resource Name</span></span>

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

### <span data-ttu-id="ebe92-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebe92-123">-PassThru</span></span>
<span data-ttu-id="ebe92-124">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="ebe92-124">returns true if successful</span></span>

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

### <span data-ttu-id="ebe92-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe92-125">-ResourceGroupName</span></span>
<span data-ttu-id="ebe92-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ebe92-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ebe92-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebe92-127">-ResourceId</span></span>
<span data-ttu-id="ebe92-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebe92-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="ebe92-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ebe92-129">-Confirm</span></span>
<span data-ttu-id="ebe92-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ebe92-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebe92-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebe92-131">-WhatIf</span></span>
<span data-ttu-id="ebe92-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebe92-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebe92-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ebe92-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebe92-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe92-134">CommonParameters</span></span>
<span data-ttu-id="ebe92-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebe92-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe92-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebe92-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe92-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebe92-137">INPUTS</span></span>

### <span data-ttu-id="ebe92-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ebe92-138">System.String</span></span>

### <span data-ttu-id="ebe92-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ebe92-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="ebe92-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebe92-140">OUTPUTS</span></span>

### <span data-ttu-id="ebe92-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ebe92-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="ebe92-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ebe92-142">NOTES</span></span>

## <span data-ttu-id="ebe92-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebe92-143">RELATED LINKS</span></span>
