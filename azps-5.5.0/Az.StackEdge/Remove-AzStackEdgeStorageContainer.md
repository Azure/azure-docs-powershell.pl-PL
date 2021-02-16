---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178274"
---
# <span data-ttu-id="a7ed6-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7ed6-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="a7ed6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ed6-103">Usuwa kontener magazynu dla konta magazynu dla usługi Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="a7ed6-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="a7ed6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7ed6-104">SYNTAX</span></span>

### <span data-ttu-id="a7ed6-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a7ed6-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7ed6-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7ed6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7ed6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7ed6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7ed6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7ed6-108">DESCRIPTION</span></span>
<span data-ttu-id="a7ed6-109">Polecenie **cmdlet Remove-AzStackEdgeStorageContainer** usuwa skojarzony kontener magazynu dla konta magazynu edge na urządzeniu Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="a7ed6-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="a7ed6-110">Możesz określić nazwę kontenera magazynu, który ma zostać usunięty jako parametr.</span><span class="sxs-lookup"><span data-stu-id="a7ed6-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="a7ed6-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7ed6-111">EXAMPLES</span></span>

### <span data-ttu-id="a7ed6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7ed6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="a7ed6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7ed6-113">PARAMETERS</span></span>

### <span data-ttu-id="a7ed6-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a7ed6-114">-AsJob</span></span>
<span data-ttu-id="a7ed6-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a7ed6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7ed6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ed6-116">-DefaultProfile</span></span>
<span data-ttu-id="a7ed6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7ed6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7ed6-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a7ed6-118">-DeviceName</span></span>
<span data-ttu-id="a7ed6-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="a7ed6-119">Device Name</span></span>

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

### <span data-ttu-id="a7ed6-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a7ed6-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="a7ed6-121">Podaj nazwę istniejącego konta EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7ed6-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ed6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7ed6-122">-InputObject</span></span>
<span data-ttu-id="a7ed6-123">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="a7ed6-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ed6-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a7ed6-124">-Name</span></span>
<span data-ttu-id="a7ed6-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="a7ed6-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ed6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7ed6-126">-PassThru</span></span>
<span data-ttu-id="a7ed6-127">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="a7ed6-127">returns true if successful</span></span>

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

### <span data-ttu-id="a7ed6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7ed6-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7ed6-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a7ed6-129">Resource Group Name</span></span>

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

### <span data-ttu-id="a7ed6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7ed6-130">-ResourceId</span></span>
<span data-ttu-id="a7ed6-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7ed6-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="a7ed6-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7ed6-132">-Confirm</span></span>
<span data-ttu-id="a7ed6-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a7ed6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7ed6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7ed6-134">-WhatIf</span></span>
<span data-ttu-id="a7ed6-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7ed6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7ed6-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a7ed6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7ed6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ed6-137">CommonParameters</span></span>
<span data-ttu-id="a7ed6-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ed6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ed6-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7ed6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ed6-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7ed6-140">INPUTS</span></span>

### <span data-ttu-id="a7ed6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a7ed6-141">System.String</span></span>

### <span data-ttu-id="a7ed6-142">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7ed6-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="a7ed6-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7ed6-143">OUTPUTS</span></span>

### <span data-ttu-id="a7ed6-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7ed6-144">System.Boolean</span></span>

## <span data-ttu-id="a7ed6-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7ed6-145">NOTES</span></span>

## <span data-ttu-id="a7ed6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7ed6-146">RELATED LINKS</span></span>
