---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f6607f59e2cc29557c41bf07014c3604fdb1bf47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998068"
---
# <span data-ttu-id="489f3-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="489f3-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="489f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="489f3-102">SYNOPSIS</span></span>
<span data-ttu-id="489f3-103">Wywołuje określone akcje w kontenerze magazynu.</span><span class="sxs-lookup"><span data-stu-id="489f3-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="489f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="489f3-104">SYNTAX</span></span>

### <span data-ttu-id="489f3-105">InvokeByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="489f3-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="489f3-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="489f3-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="489f3-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="489f3-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="489f3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="489f3-108">DESCRIPTION</span></span>
<span data-ttu-id="489f3-109">Polecenie cmdlet **Invoke-AzDataBoxEdgeStorageContainer** wywoła akcje w celu odświeżenia danych w kontenerze magazynu na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="489f3-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="489f3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="489f3-110">EXAMPLES</span></span>

### <span data-ttu-id="489f3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="489f3-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="489f3-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="489f3-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="489f3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="489f3-113">PARAMETERS</span></span>

### <span data-ttu-id="489f3-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="489f3-114">-AsJob</span></span>
<span data-ttu-id="489f3-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="489f3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="489f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="489f3-116">-DefaultProfile</span></span>
<span data-ttu-id="489f3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="489f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="489f3-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="489f3-118">-DeviceName</span></span>
<span data-ttu-id="489f3-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="489f3-119">Device Name</span></span>

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

### <span data-ttu-id="489f3-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="489f3-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="489f3-121">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="489f3-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="489f3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="489f3-122">-InputObject</span></span>
<span data-ttu-id="489f3-123">Podaj istniejący obiekt EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="489f3-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="489f3-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="489f3-124">-Name</span></span>
<span data-ttu-id="489f3-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="489f3-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="489f3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="489f3-126">-PassThru</span></span>
<span data-ttu-id="489f3-127">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="489f3-127">returns true if successful</span></span>

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

### <span data-ttu-id="489f3-128">— RefreshData</span><span class="sxs-lookup"><span data-stu-id="489f3-128">-RefreshData</span></span>
<span data-ttu-id="489f3-129">Odświeżanie metadanych kontenera przy użyciu danych z chmury</span><span class="sxs-lookup"><span data-stu-id="489f3-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="489f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="489f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="489f3-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="489f3-131">Resource Group Name</span></span>

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

### <span data-ttu-id="489f3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="489f3-132">-ResourceId</span></span>
<span data-ttu-id="489f3-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="489f3-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="489f3-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="489f3-134">-Confirm</span></span>
<span data-ttu-id="489f3-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="489f3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="489f3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="489f3-136">-WhatIf</span></span>
<span data-ttu-id="489f3-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="489f3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="489f3-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="489f3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="489f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="489f3-139">CommonParameters</span></span>
<span data-ttu-id="489f3-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="489f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="489f3-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="489f3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="489f3-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="489f3-142">INPUTS</span></span>

### <span data-ttu-id="489f3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="489f3-143">System.String</span></span>

### <span data-ttu-id="489f3-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="489f3-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="489f3-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="489f3-145">OUTPUTS</span></span>

### <span data-ttu-id="489f3-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="489f3-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="489f3-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="489f3-147">NOTES</span></span>

## <span data-ttu-id="489f3-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="489f3-148">RELATED LINKS</span></span>
