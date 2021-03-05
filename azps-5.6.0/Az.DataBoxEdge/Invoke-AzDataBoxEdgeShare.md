---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: a135a9bf994e2837351347a4cc741ed20b406a28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001626"
---
# <span data-ttu-id="fade6-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fade6-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="fade6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fade6-102">SYNOPSIS</span></span>
<span data-ttu-id="fade6-103">Wywołuje określone akcje dotyczące udziału.</span><span class="sxs-lookup"><span data-stu-id="fade6-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="fade6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fade6-104">SYNTAX</span></span>

### <span data-ttu-id="fade6-105">InvokeByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fade6-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fade6-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fade6-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fade6-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fade6-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fade6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fade6-108">DESCRIPTION</span></span>
<span data-ttu-id="fade6-109">Polecenie **cmdlet Invoke-AzDataBoxEdgeShare** wywoła akcję odświeżania danych w udostępnieniu na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="fade6-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="fade6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fade6-110">EXAMPLES</span></span>

### <span data-ttu-id="fade6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fade6-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="fade6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fade6-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="fade6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fade6-113">PARAMETERS</span></span>

### <span data-ttu-id="fade6-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fade6-114">-AsJob</span></span>
<span data-ttu-id="fade6-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fade6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fade6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fade6-116">-DefaultProfile</span></span>
<span data-ttu-id="fade6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fade6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fade6-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fade6-118">-DeviceName</span></span>
<span data-ttu-id="fade6-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="fade6-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fade6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fade6-120">-InputObject</span></span>
<span data-ttu-id="fade6-121">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="fade6-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fade6-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fade6-122">-Name</span></span>
<span data-ttu-id="fade6-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="fade6-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fade6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fade6-124">-PassThru</span></span>
<span data-ttu-id="fade6-125">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="fade6-125">returns true if successful</span></span>

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

### <span data-ttu-id="fade6-126">— RefreshData</span><span class="sxs-lookup"><span data-stu-id="fade6-126">-RefreshData</span></span>
<span data-ttu-id="fade6-127">Odświeżanie metadanych udostępniania danych z chmury</span><span class="sxs-lookup"><span data-stu-id="fade6-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="fade6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fade6-128">-ResourceGroupName</span></span>
<span data-ttu-id="fade6-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fade6-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fade6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fade6-130">-ResourceId</span></span>
<span data-ttu-id="fade6-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fade6-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fade6-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fade6-132">-Confirm</span></span>
<span data-ttu-id="fade6-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fade6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fade6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fade6-134">-WhatIf</span></span>
<span data-ttu-id="fade6-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fade6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fade6-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fade6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fade6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fade6-137">CommonParameters</span></span>
<span data-ttu-id="fade6-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fade6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fade6-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fade6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fade6-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fade6-140">INPUTS</span></span>

### <span data-ttu-id="fade6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fade6-141">System.String</span></span>

### <span data-ttu-id="fade6-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fade6-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="fade6-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fade6-143">OUTPUTS</span></span>

### <span data-ttu-id="fade6-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fade6-144">System.Boolean</span></span>

## <span data-ttu-id="fade6-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fade6-145">NOTES</span></span>

## <span data-ttu-id="fade6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fade6-146">RELATED LINKS</span></span>
