---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: 410509f59cc34dd139761a3e4ddb5de9907ef720
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005457"
---
# <span data-ttu-id="7e2a7-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="7e2a7-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="7e2a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e2a7-103">Usuń rozszerzenie maszyny wirtualnej z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="7e2a7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7e2a7-104">SYNTAX</span></span>

### <span data-ttu-id="7e2a7-105">ByObj (Domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7e2a7-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e2a7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7e2a7-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e2a7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7e2a7-107">DESCRIPTION</span></span>
<span data-ttu-id="7e2a7-108">Usuń rozszerzenie maszyny wirtualnej z typu węzła według nazwy.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="7e2a7-109">Użyj [właściwości Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) i sprawdź właściwość VmExtensions, aby zobaczyć bieżące rozszerzenie typu węzła.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="7e2a7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7e2a7-110">EXAMPLES</span></span>

### <span data-ttu-id="7e2a7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e2a7-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="7e2a7-112">Usuń rozszerzenie z typu węzła według nazwy.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="7e2a7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7e2a7-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="7e2a7-114">Usuń rozszerzenie z typu węzła według nazwy za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="7e2a7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e2a7-115">PARAMETERS</span></span>

### <span data-ttu-id="7e2a7-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7e2a7-116">-AsJob</span></span>
<span data-ttu-id="7e2a7-117">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7e2a7-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7e2a7-118">-ClusterName</span></span>
<span data-ttu-id="7e2a7-119">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-119">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e2a7-120">-DefaultProfile</span></span>
<span data-ttu-id="7e2a7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e2a7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e2a7-122">-InputObject</span></span>
<span data-ttu-id="7e2a7-123">Zasób typu węzła</span><span class="sxs-lookup"><span data-stu-id="7e2a7-123">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a7-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7e2a7-124">-Name</span></span>
<span data-ttu-id="7e2a7-125">nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a7-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="7e2a7-126">-NodeTypeName</span></span>
<span data-ttu-id="7e2a7-127">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e2a7-128">-PassThru</span></span>
<span data-ttu-id="7e2a7-129">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="7e2a7-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7e2a7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e2a7-130">-ResourceGroupName</span></span>
<span data-ttu-id="7e2a7-131">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-131">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a7-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e2a7-132">-Confirm</span></span>
<span data-ttu-id="7e2a7-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e2a7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e2a7-134">-WhatIf</span></span>
<span data-ttu-id="7e2a7-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e2a7-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e2a7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e2a7-137">CommonParameters</span></span>
<span data-ttu-id="7e2a7-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e2a7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e2a7-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e2a7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e2a7-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e2a7-140">INPUTS</span></span>

### <span data-ttu-id="7e2a7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7e2a7-141">System.String</span></span>

## <span data-ttu-id="7e2a7-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e2a7-142">OUTPUTS</span></span>

### <span data-ttu-id="7e2a7-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="7e2a7-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="7e2a7-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7e2a7-144">NOTES</span></span>

## <span data-ttu-id="7e2a7-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e2a7-145">RELATED LINKS</span></span>
