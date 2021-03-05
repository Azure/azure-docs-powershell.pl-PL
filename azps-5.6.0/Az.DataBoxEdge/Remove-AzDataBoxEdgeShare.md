---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8e8b26ac8bdb097ac87135f764e1dfc4f4450f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972865"
---
# <span data-ttu-id="16e55-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="16e55-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="16e55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16e55-102">SYNOPSIS</span></span>
<span data-ttu-id="16e55-103">Usuwa udział z urządzenia.</span><span class="sxs-lookup"><span data-stu-id="16e55-103">Removes a share from the device.</span></span>

## <span data-ttu-id="16e55-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16e55-104">SYNTAX</span></span>

### <span data-ttu-id="16e55-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="16e55-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16e55-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16e55-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16e55-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16e55-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e55-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="16e55-108">DESCRIPTION</span></span>
<span data-ttu-id="16e55-109">Polecenie **cmdlet Remove-AzDataBoxEdgeShare** usuwa skojarzone udziały brzegowe dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="16e55-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="16e55-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16e55-110">EXAMPLES</span></span>

### <span data-ttu-id="16e55-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="16e55-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="16e55-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16e55-112">PARAMETERS</span></span>

### <span data-ttu-id="16e55-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="16e55-113">-AsJob</span></span>
<span data-ttu-id="16e55-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="16e55-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16e55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e55-115">-DefaultProfile</span></span>
<span data-ttu-id="16e55-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="16e55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16e55-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="16e55-117">-DeviceName</span></span>
<span data-ttu-id="16e55-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="16e55-118">Device Name</span></span>

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

### <span data-ttu-id="16e55-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16e55-119">-InputObject</span></span>
<span data-ttu-id="16e55-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="16e55-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16e55-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="16e55-121">-Name</span></span>
<span data-ttu-id="16e55-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="16e55-122">Resource Name</span></span>

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

### <span data-ttu-id="16e55-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16e55-123">-PassThru</span></span>
<span data-ttu-id="16e55-124">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="16e55-124">returns true if successful</span></span>

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

### <span data-ttu-id="16e55-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e55-125">-ResourceGroupName</span></span>
<span data-ttu-id="16e55-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="16e55-126">Resource Group Name</span></span>

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

### <span data-ttu-id="16e55-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16e55-127">-ResourceId</span></span>
<span data-ttu-id="16e55-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="16e55-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="16e55-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16e55-129">-Confirm</span></span>
<span data-ttu-id="16e55-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="16e55-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e55-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e55-131">-WhatIf</span></span>
<span data-ttu-id="16e55-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16e55-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16e55-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="16e55-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e55-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e55-134">CommonParameters</span></span>
<span data-ttu-id="16e55-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e55-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e55-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16e55-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e55-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16e55-137">INPUTS</span></span>

### <span data-ttu-id="16e55-138">System.String</span><span class="sxs-lookup"><span data-stu-id="16e55-138">System.String</span></span>

### <span data-ttu-id="16e55-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="16e55-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="16e55-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16e55-140">OUTPUTS</span></span>

### <span data-ttu-id="16e55-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16e55-141">System.Boolean</span></span>

## <span data-ttu-id="16e55-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16e55-142">NOTES</span></span>

## <span data-ttu-id="16e55-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16e55-143">RELATED LINKS</span></span>
