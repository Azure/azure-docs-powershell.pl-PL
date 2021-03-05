---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 6a07031c376e406be1d957a33475af799b229b8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005098"
---
# <span data-ttu-id="86f8b-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="86f8b-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="86f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="86f8b-103">Usuwa kontener magazynu dla konta magazynu dla usługi Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="86f8b-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="86f8b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="86f8b-104">SYNTAX</span></span>

### <span data-ttu-id="86f8b-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="86f8b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86f8b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86f8b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86f8b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86f8b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86f8b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="86f8b-108">DESCRIPTION</span></span>
<span data-ttu-id="86f8b-109">Polecenie **cmdlet Remove-AzStackEdgeStorageContainer** usuwa skojarzony kontener magazynu dla konta magazynu edge na urządzeniu Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="86f8b-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="86f8b-110">Możesz określić nazwę kontenera magazynu, który ma zostać usunięty jako parametr.</span><span class="sxs-lookup"><span data-stu-id="86f8b-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="86f8b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="86f8b-111">EXAMPLES</span></span>

### <span data-ttu-id="86f8b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86f8b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="86f8b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86f8b-113">PARAMETERS</span></span>

### <span data-ttu-id="86f8b-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="86f8b-114">-AsJob</span></span>
<span data-ttu-id="86f8b-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="86f8b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86f8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f8b-116">-DefaultProfile</span></span>
<span data-ttu-id="86f8b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="86f8b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86f8b-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="86f8b-118">-DeviceName</span></span>
<span data-ttu-id="86f8b-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="86f8b-119">Device Name</span></span>

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

### <span data-ttu-id="86f8b-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="86f8b-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="86f8b-121">Podaj nazwę istniejącego konta EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="86f8b-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="86f8b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86f8b-122">-InputObject</span></span>
<span data-ttu-id="86f8b-123">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="86f8b-123">Input Object</span></span>

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

### <span data-ttu-id="86f8b-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="86f8b-124">-Name</span></span>
<span data-ttu-id="86f8b-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="86f8b-125">Resource Name</span></span>

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

### <span data-ttu-id="86f8b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86f8b-126">-PassThru</span></span>
<span data-ttu-id="86f8b-127">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="86f8b-127">returns true if successful</span></span>

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

### <span data-ttu-id="86f8b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f8b-128">-ResourceGroupName</span></span>
<span data-ttu-id="86f8b-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="86f8b-129">Resource Group Name</span></span>

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

### <span data-ttu-id="86f8b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86f8b-130">-ResourceId</span></span>
<span data-ttu-id="86f8b-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="86f8b-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="86f8b-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86f8b-132">-Confirm</span></span>
<span data-ttu-id="86f8b-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="86f8b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86f8b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86f8b-134">-WhatIf</span></span>
<span data-ttu-id="86f8b-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86f8b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86f8b-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="86f8b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86f8b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f8b-137">CommonParameters</span></span>
<span data-ttu-id="86f8b-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f8b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f8b-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86f8b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f8b-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86f8b-140">INPUTS</span></span>

### <span data-ttu-id="86f8b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="86f8b-141">System.String</span></span>

### <span data-ttu-id="86f8b-142">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="86f8b-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="86f8b-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86f8b-143">OUTPUTS</span></span>

### <span data-ttu-id="86f8b-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="86f8b-144">System.Boolean</span></span>

## <span data-ttu-id="86f8b-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="86f8b-145">NOTES</span></span>

## <span data-ttu-id="86f8b-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86f8b-146">RELATED LINKS</span></span>
