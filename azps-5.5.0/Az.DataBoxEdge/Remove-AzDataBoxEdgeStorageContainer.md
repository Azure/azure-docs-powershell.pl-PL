---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186306"
---
# <span data-ttu-id="16d21-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="16d21-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="16d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d21-102">SYNOPSIS</span></span>
<span data-ttu-id="16d21-103">Usuwa kontener magazynu dla konta magazynu dla usługi Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="16d21-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="16d21-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16d21-104">SYNTAX</span></span>

### <span data-ttu-id="16d21-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="16d21-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d21-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d21-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d21-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d21-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16d21-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="16d21-108">DESCRIPTION</span></span>
<span data-ttu-id="16d21-109">Polecenie **cmdlet Remove-AzDataBoxEdgeStorageContainer** usuwa skojarzony kontener magazynu dla konta magazynu edge na urządzeniu z programem Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="16d21-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="16d21-110">Możesz określić nazwę kontenera magazynu, który ma zostać usunięty jako parametr.</span><span class="sxs-lookup"><span data-stu-id="16d21-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="16d21-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16d21-111">EXAMPLES</span></span>

### <span data-ttu-id="16d21-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="16d21-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="16d21-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16d21-113">PARAMETERS</span></span>

### <span data-ttu-id="16d21-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="16d21-114">-AsJob</span></span>
<span data-ttu-id="16d21-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="16d21-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16d21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d21-116">-DefaultProfile</span></span>
<span data-ttu-id="16d21-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="16d21-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16d21-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="16d21-118">-DeviceName</span></span>
<span data-ttu-id="16d21-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="16d21-119">Device Name</span></span>

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

### <span data-ttu-id="16d21-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="16d21-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="16d21-121">Podaj nazwę istniejącego konta EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="16d21-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="16d21-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16d21-122">-InputObject</span></span>
<span data-ttu-id="16d21-123">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="16d21-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16d21-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="16d21-124">-Name</span></span>
<span data-ttu-id="16d21-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="16d21-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d21-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16d21-126">-PassThru</span></span>
<span data-ttu-id="16d21-127">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="16d21-127">returns true if successful</span></span>

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

### <span data-ttu-id="16d21-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d21-128">-ResourceGroupName</span></span>
<span data-ttu-id="16d21-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="16d21-129">Resource Group Name</span></span>

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

### <span data-ttu-id="16d21-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16d21-130">-ResourceId</span></span>
<span data-ttu-id="16d21-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="16d21-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="16d21-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16d21-132">-Confirm</span></span>
<span data-ttu-id="16d21-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="16d21-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16d21-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16d21-134">-WhatIf</span></span>
<span data-ttu-id="16d21-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16d21-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16d21-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="16d21-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16d21-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d21-137">CommonParameters</span></span>
<span data-ttu-id="16d21-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d21-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d21-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16d21-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d21-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16d21-140">INPUTS</span></span>

### <span data-ttu-id="16d21-141">System.String</span><span class="sxs-lookup"><span data-stu-id="16d21-141">System.String</span></span>

### <span data-ttu-id="16d21-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="16d21-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="16d21-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16d21-143">OUTPUTS</span></span>

### <span data-ttu-id="16d21-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16d21-144">System.Boolean</span></span>

## <span data-ttu-id="16d21-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16d21-145">NOTES</span></span>

## <span data-ttu-id="16d21-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16d21-146">RELATED LINKS</span></span>
