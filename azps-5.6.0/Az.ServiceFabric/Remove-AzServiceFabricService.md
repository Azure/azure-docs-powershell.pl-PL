---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 992cd2a381e9eda89b9388ec1ed37f74a76e9adf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005418"
---
# <span data-ttu-id="b26e2-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b26e2-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="b26e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b26e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b26e2-103">Usuń usługę z klastra.</span><span class="sxs-lookup"><span data-stu-id="b26e2-103">Remove a service from the cluster.</span></span> <span data-ttu-id="b26e2-104">Obsługuje tylko ARM usług.</span><span class="sxs-lookup"><span data-stu-id="b26e2-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="b26e2-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b26e2-105">SYNTAX</span></span>

### <span data-ttu-id="b26e2-106">ByResourceGroup (Default)</span><span class="sxs-lookup"><span data-stu-id="b26e2-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b26e2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b26e2-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b26e2-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b26e2-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b26e2-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b26e2-109">DESCRIPTION</span></span>
<span data-ttu-id="b26e2-110">To polecenie cmdlet usuwa formularz usługi z klastrem.</span><span class="sxs-lookup"><span data-stu-id="b26e2-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="b26e2-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b26e2-111">EXAMPLES</span></span>

### <span data-ttu-id="b26e2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b26e2-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="b26e2-113">W tym przykładzie usuniesz usługę "testApp~testService1".</span><span class="sxs-lookup"><span data-stu-id="b26e2-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="b26e2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b26e2-114">PARAMETERS</span></span>

### <span data-ttu-id="b26e2-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="b26e2-115">-ApplicationName</span></span>
<span data-ttu-id="b26e2-116">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b26e2-116">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26e2-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b26e2-117">-ClusterName</span></span>
<span data-ttu-id="b26e2-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="b26e2-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b26e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26e2-119">-DefaultProfile</span></span>
<span data-ttu-id="b26e2-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b26e2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b26e2-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b26e2-121">-Force</span></span>
<span data-ttu-id="b26e2-122">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="b26e2-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="b26e2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b26e2-123">-InputObject</span></span>
<span data-ttu-id="b26e2-124">Zasób usługi.</span><span class="sxs-lookup"><span data-stu-id="b26e2-124">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b26e2-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b26e2-125">-Name</span></span>
<span data-ttu-id="b26e2-126">Określ nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="b26e2-126">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26e2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b26e2-127">-PassThru</span></span>
<span data-ttu-id="b26e2-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b26e2-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b26e2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26e2-129">-ResourceGroupName</span></span>
<span data-ttu-id="b26e2-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b26e2-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b26e2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b26e2-131">-ResourceId</span></span>
<span data-ttu-id="b26e2-132">Arm ResourceId usługi.</span><span class="sxs-lookup"><span data-stu-id="b26e2-132">Arm ResourceId of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b26e2-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b26e2-133">-Confirm</span></span>
<span data-ttu-id="b26e2-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b26e2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b26e2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b26e2-135">-WhatIf</span></span>
<span data-ttu-id="b26e2-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b26e2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b26e2-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b26e2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b26e2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26e2-138">CommonParameters</span></span>
<span data-ttu-id="b26e2-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26e2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26e2-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b26e2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26e2-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b26e2-141">INPUTS</span></span>

### <span data-ttu-id="b26e2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b26e2-142">System.String</span></span>

### <span data-ttu-id="b26e2-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="b26e2-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="b26e2-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b26e2-144">OUTPUTS</span></span>

### <span data-ttu-id="b26e2-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b26e2-145">System.Boolean</span></span>

## <span data-ttu-id="b26e2-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b26e2-146">NOTES</span></span>

## <span data-ttu-id="b26e2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b26e2-147">RELATED LINKS</span></span>
