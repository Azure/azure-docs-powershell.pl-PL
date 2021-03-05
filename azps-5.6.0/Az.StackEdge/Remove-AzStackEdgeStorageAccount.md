---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 0a573f8fa293d2c3e4c84eced54c88eb77032970
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005121"
---
# <span data-ttu-id="ee2ea-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee2ea-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="ee2ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2ea-103">Usuwa konto magazynu dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="ee2ea-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ee2ea-104">SYNTAX</span></span>

### <span data-ttu-id="ee2ea-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ee2ea-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2ea-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2ea-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee2ea-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee2ea-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee2ea-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ee2ea-108">DESCRIPTION</span></span>
<span data-ttu-id="ee2ea-109">Polecenie **cmdlet Remove-AzStackEdgeStorageAccount** usuwa skojarzone konto magazynu edge dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="ee2ea-110">Możesz określić nazwę konta magazynu dla usługi Edge, które ma zostać usunięte jako parametr w poleceniach cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="ee2ea-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ee2ea-111">EXAMPLES</span></span>

### <span data-ttu-id="ee2ea-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee2ea-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="ee2ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee2ea-113">PARAMETERS</span></span>

### <span data-ttu-id="ee2ea-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ee2ea-114">-AsJob</span></span>
<span data-ttu-id="ee2ea-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ee2ea-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee2ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2ea-116">-DefaultProfile</span></span>
<span data-ttu-id="ee2ea-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee2ea-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ee2ea-118">-DeviceName</span></span>
<span data-ttu-id="ee2ea-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="ee2ea-119">Device Name</span></span>

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

### <span data-ttu-id="ee2ea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee2ea-120">-InputObject</span></span>
<span data-ttu-id="ee2ea-121">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="ee2ea-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee2ea-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ee2ea-122">-Name</span></span>
<span data-ttu-id="ee2ea-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="ee2ea-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee2ea-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee2ea-124">-PassThru</span></span>
<span data-ttu-id="ee2ea-125">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="ee2ea-125">returns true if successful</span></span>

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

### <span data-ttu-id="ee2ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee2ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee2ea-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ee2ea-127">Resource Group Name</span></span>

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

### <span data-ttu-id="ee2ea-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee2ea-128">-ResourceId</span></span>
<span data-ttu-id="ee2ea-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee2ea-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="ee2ea-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee2ea-130">-Confirm</span></span>
<span data-ttu-id="ee2ea-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee2ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2ea-132">-WhatIf</span></span>
<span data-ttu-id="ee2ea-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee2ea-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee2ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2ea-135">CommonParameters</span></span>
<span data-ttu-id="ee2ea-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee2ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2ea-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee2ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2ea-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee2ea-138">INPUTS</span></span>

### <span data-ttu-id="ee2ea-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ee2ea-139">System.String</span></span>

### <span data-ttu-id="ee2ea-140">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee2ea-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="ee2ea-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee2ea-141">OUTPUTS</span></span>

### <span data-ttu-id="ee2ea-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee2ea-142">System.Boolean</span></span>

## <span data-ttu-id="ee2ea-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ee2ea-143">NOTES</span></span>

## <span data-ttu-id="ee2ea-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee2ea-144">RELATED LINKS</span></span>
