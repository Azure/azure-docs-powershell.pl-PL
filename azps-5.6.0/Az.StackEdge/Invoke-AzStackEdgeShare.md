---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: fc920e04ce3e031e25b0c27ec0998266f077840c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002945"
---
# <span data-ttu-id="6c508-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="6c508-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="6c508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c508-102">SYNOPSIS</span></span>
<span data-ttu-id="6c508-103">Wywołuje określone akcje dotyczące udziału.</span><span class="sxs-lookup"><span data-stu-id="6c508-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="6c508-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c508-104">SYNTAX</span></span>

### <span data-ttu-id="6c508-105">InvokeByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6c508-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c508-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c508-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c508-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c508-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c508-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c508-108">DESCRIPTION</span></span>
<span data-ttu-id="6c508-109">Polecenie cmdlet **Invoke-AzStackEdgeShare** wywoła akcję odświeżania danych w udostępnieniu na urządzeniu Ze stosem Edge.</span><span class="sxs-lookup"><span data-stu-id="6c508-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="6c508-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c508-110">EXAMPLES</span></span>

### <span data-ttu-id="6c508-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c508-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="6c508-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6c508-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="6c508-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c508-113">PARAMETERS</span></span>

### <span data-ttu-id="6c508-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6c508-114">-AsJob</span></span>
<span data-ttu-id="6c508-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6c508-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c508-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c508-116">-DefaultProfile</span></span>
<span data-ttu-id="6c508-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c508-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c508-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6c508-118">-DeviceName</span></span>
<span data-ttu-id="6c508-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="6c508-119">Device Name</span></span>

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

### <span data-ttu-id="6c508-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c508-120">-InputObject</span></span>
<span data-ttu-id="6c508-121">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="6c508-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c508-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6c508-122">-Name</span></span>
<span data-ttu-id="6c508-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="6c508-123">Resource Name</span></span>

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

### <span data-ttu-id="6c508-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c508-124">-PassThru</span></span>
<span data-ttu-id="6c508-125">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="6c508-125">returns true if successful</span></span>

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

### <span data-ttu-id="6c508-126">— RefreshData</span><span class="sxs-lookup"><span data-stu-id="6c508-126">-RefreshData</span></span>
<span data-ttu-id="6c508-127">Odświeżanie metadanych udostępniania danych z chmury</span><span class="sxs-lookup"><span data-stu-id="6c508-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="6c508-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c508-128">-ResourceGroupName</span></span>
<span data-ttu-id="6c508-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6c508-129">Resource Group Name</span></span>

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

### <span data-ttu-id="6c508-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c508-130">-ResourceId</span></span>
<span data-ttu-id="6c508-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c508-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="6c508-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c508-132">-Confirm</span></span>
<span data-ttu-id="6c508-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6c508-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c508-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c508-134">-WhatIf</span></span>
<span data-ttu-id="6c508-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c508-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c508-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6c508-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c508-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c508-137">CommonParameters</span></span>
<span data-ttu-id="6c508-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c508-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c508-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c508-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c508-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c508-140">INPUTS</span></span>

### <span data-ttu-id="6c508-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6c508-141">System.String</span></span>

### <span data-ttu-id="6c508-142">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="6c508-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="6c508-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c508-143">OUTPUTS</span></span>

### <span data-ttu-id="6c508-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c508-144">System.Boolean</span></span>

## <span data-ttu-id="6c508-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c508-145">NOTES</span></span>

## <span data-ttu-id="6c508-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c508-146">RELATED LINKS</span></span>
