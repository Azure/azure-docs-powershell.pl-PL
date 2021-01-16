---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357931"
---
# <span data-ttu-id="24c7d-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="24c7d-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="24c7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="24c7d-103">Usuń rozszerzenie maszyny wirtualnej z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="24c7d-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="24c7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24c7d-104">SYNTAX</span></span>

### <span data-ttu-id="24c7d-105">ByObj (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24c7d-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24c7d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="24c7d-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c7d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="24c7d-107">DESCRIPTION</span></span>
<span data-ttu-id="24c7d-108">Usuń rozszerzenie maszyny wirtualnej z typu węzła według nazwy.</span><span class="sxs-lookup"><span data-stu-id="24c7d-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="24c7d-109">W celu wyświetlenia bieżącego rozszerzenia typu węzła użyj [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) i sprawdź, czy właściwość VmExtensions jest obecne.</span><span class="sxs-lookup"><span data-stu-id="24c7d-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="24c7d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24c7d-110">EXAMPLES</span></span>

### <span data-ttu-id="24c7d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24c7d-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="24c7d-112">Usuwanie rozszerzenia z typu węzła według nazwy.</span><span class="sxs-lookup"><span data-stu-id="24c7d-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="24c7d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="24c7d-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="24c7d-114">Usuwanie rozszerzenia z typu węzła według nazwy z potokiem.</span><span class="sxs-lookup"><span data-stu-id="24c7d-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="24c7d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24c7d-115">PARAMETERS</span></span>

### <span data-ttu-id="24c7d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24c7d-116">-AsJob</span></span>
<span data-ttu-id="24c7d-117">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="24c7d-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="24c7d-118">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="24c7d-118">-ClusterName</span></span>
<span data-ttu-id="24c7d-119">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="24c7d-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="24c7d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c7d-120">-DefaultProfile</span></span>
<span data-ttu-id="24c7d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24c7d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24c7d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="24c7d-122">-InputObject</span></span>
<span data-ttu-id="24c7d-123">Zasób typu węzła</span><span class="sxs-lookup"><span data-stu-id="24c7d-123">Node type resource</span></span>

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

### <span data-ttu-id="24c7d-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24c7d-124">-Name</span></span>
<span data-ttu-id="24c7d-125">Nazwa rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="24c7d-125">extension name.</span></span>

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

### <span data-ttu-id="24c7d-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="24c7d-126">-NodeTypeName</span></span>
<span data-ttu-id="24c7d-127">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="24c7d-127">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="24c7d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24c7d-128">-PassThru</span></span>
<span data-ttu-id="24c7d-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="24c7d-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="24c7d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c7d-130">-ResourceGroupName</span></span>
<span data-ttu-id="24c7d-131">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24c7d-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="24c7d-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24c7d-132">-Confirm</span></span>
<span data-ttu-id="24c7d-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24c7d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c7d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c7d-134">-WhatIf</span></span>
<span data-ttu-id="24c7d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24c7d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24c7d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24c7d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c7d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c7d-137">CommonParameters</span></span>
<span data-ttu-id="24c7d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c7d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c7d-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24c7d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c7d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24c7d-140">INPUTS</span></span>

### <span data-ttu-id="24c7d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="24c7d-141">System.String</span></span>

## <span data-ttu-id="24c7d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24c7d-142">OUTPUTS</span></span>

### <span data-ttu-id="24c7d-143">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="24c7d-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="24c7d-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24c7d-144">NOTES</span></span>

## <span data-ttu-id="24c7d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24c7d-145">RELATED LINKS</span></span>
