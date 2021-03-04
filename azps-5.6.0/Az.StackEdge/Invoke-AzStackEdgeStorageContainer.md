---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: ce4c80146524f57e48570b9739f78635e3e21b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982010"
---
# <span data-ttu-id="55007-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="55007-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="55007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55007-102">SYNOPSIS</span></span>
<span data-ttu-id="55007-103">Wywołuje określone akcje w kontenerze magazynu.</span><span class="sxs-lookup"><span data-stu-id="55007-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="55007-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="55007-104">SYNTAX</span></span>

### <span data-ttu-id="55007-105">InvokeByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="55007-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55007-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55007-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55007-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55007-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55007-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="55007-108">DESCRIPTION</span></span>
<span data-ttu-id="55007-109">Polecenie cmdlet **Invoke-AzStackEdgeStorageContainer** wywoła akcje w celu odświeżenia danych w kontenerze magazynu na urządzeniu ze stosem Edge.</span><span class="sxs-lookup"><span data-stu-id="55007-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="55007-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="55007-110">EXAMPLES</span></span>

### <span data-ttu-id="55007-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="55007-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="55007-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="55007-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="55007-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55007-113">PARAMETERS</span></span>

### <span data-ttu-id="55007-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="55007-114">-AsJob</span></span>
<span data-ttu-id="55007-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="55007-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55007-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55007-116">-DefaultProfile</span></span>
<span data-ttu-id="55007-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="55007-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55007-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="55007-118">-DeviceName</span></span>
<span data-ttu-id="55007-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="55007-119">Device Name</span></span>

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

### <span data-ttu-id="55007-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="55007-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="55007-121">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="55007-121">Resource Name</span></span>

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

### <span data-ttu-id="55007-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55007-122">-InputObject</span></span>
<span data-ttu-id="55007-123">Podaj istniejący obiekt EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="55007-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55007-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="55007-124">-Name</span></span>
<span data-ttu-id="55007-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="55007-125">Resource Name</span></span>

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

### <span data-ttu-id="55007-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55007-126">-PassThru</span></span>
<span data-ttu-id="55007-127">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="55007-127">returns true if successful</span></span>

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

### <span data-ttu-id="55007-128">— RefreshData</span><span class="sxs-lookup"><span data-stu-id="55007-128">-RefreshData</span></span>
<span data-ttu-id="55007-129">Odświeżanie metadanych kontenera przy użyciu danych z chmury</span><span class="sxs-lookup"><span data-stu-id="55007-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="55007-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55007-130">-ResourceGroupName</span></span>
<span data-ttu-id="55007-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="55007-131">Resource Group Name</span></span>

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

### <span data-ttu-id="55007-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55007-132">-ResourceId</span></span>
<span data-ttu-id="55007-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="55007-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="55007-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55007-134">-Confirm</span></span>
<span data-ttu-id="55007-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="55007-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55007-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55007-136">-WhatIf</span></span>
<span data-ttu-id="55007-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55007-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55007-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="55007-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55007-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55007-139">CommonParameters</span></span>
<span data-ttu-id="55007-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55007-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55007-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55007-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55007-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55007-142">INPUTS</span></span>

### <span data-ttu-id="55007-143">System.String</span><span class="sxs-lookup"><span data-stu-id="55007-143">System.String</span></span>

### <span data-ttu-id="55007-144">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="55007-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="55007-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55007-145">OUTPUTS</span></span>

### <span data-ttu-id="55007-146">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="55007-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="55007-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="55007-147">NOTES</span></span>

## <span data-ttu-id="55007-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55007-148">RELATED LINKS</span></span>
