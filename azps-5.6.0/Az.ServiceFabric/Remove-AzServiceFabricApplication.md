---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 5004b6b9528eb91a1883805405dba6147d5161a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005585"
---
# <span data-ttu-id="5ea69-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5ea69-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="5ea69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ea69-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea69-103">Usuń aplikację z klastra.</span><span class="sxs-lookup"><span data-stu-id="5ea69-103">Remove an application from the cluster.</span></span> <span data-ttu-id="5ea69-104">Spowoduje to usunięcie wszystkich usług w ramach aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5ea69-104">This will remove all the services under the application.</span></span> <span data-ttu-id="5ea69-105">Obsługuje tylko ARM wdrożonych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5ea69-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="5ea69-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ea69-106">SYNTAX</span></span>

### <span data-ttu-id="5ea69-107">ByResourceGroup (Default)</span><span class="sxs-lookup"><span data-stu-id="5ea69-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ea69-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ea69-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ea69-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5ea69-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ea69-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ea69-110">DESCRIPTION</span></span>
<span data-ttu-id="5ea69-111">To polecenie cmdlet usuwa formularz aplikacji z klastrem.</span><span class="sxs-lookup"><span data-stu-id="5ea69-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="5ea69-112">Spowoduje to usunięcie wszystkich usług, jeśli w ogóle, w obszarze zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5ea69-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="5ea69-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ea69-113">EXAMPLES</span></span>

### <span data-ttu-id="5ea69-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ea69-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="5ea69-115">W tym przykładzie usuniemy aplikację "testApp" w grupie zasobów "testRG" i klaster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="5ea69-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="5ea69-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ea69-116">PARAMETERS</span></span>

### <span data-ttu-id="5ea69-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5ea69-117">-ClusterName</span></span>
<span data-ttu-id="5ea69-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="5ea69-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5ea69-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea69-119">-DefaultProfile</span></span>
<span data-ttu-id="5ea69-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea69-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ea69-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5ea69-121">-Force</span></span>
<span data-ttu-id="5ea69-122">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="5ea69-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="5ea69-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ea69-123">-InputObject</span></span>
<span data-ttu-id="5ea69-124">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5ea69-124">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ea69-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5ea69-125">-Name</span></span>
<span data-ttu-id="5ea69-126">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5ea69-126">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ea69-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ea69-127">-PassThru</span></span>
<span data-ttu-id="5ea69-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5ea69-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5ea69-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea69-129">-ResourceGroupName</span></span>
<span data-ttu-id="5ea69-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ea69-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5ea69-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ea69-131">-ResourceId</span></span>
<span data-ttu-id="5ea69-132">Arm ResourceId aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5ea69-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="5ea69-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ea69-133">-Confirm</span></span>
<span data-ttu-id="5ea69-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ea69-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ea69-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ea69-135">-WhatIf</span></span>
<span data-ttu-id="5ea69-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ea69-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ea69-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5ea69-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ea69-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea69-138">CommonParameters</span></span>
<span data-ttu-id="5ea69-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea69-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea69-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ea69-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea69-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ea69-141">INPUTS</span></span>

### <span data-ttu-id="5ea69-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5ea69-142">System.String</span></span>

### <span data-ttu-id="5ea69-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="5ea69-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="5ea69-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ea69-144">OUTPUTS</span></span>

### <span data-ttu-id="5ea69-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ea69-145">System.Boolean</span></span>

## <span data-ttu-id="5ea69-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ea69-146">NOTES</span></span>

## <span data-ttu-id="5ea69-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ea69-147">RELATED LINKS</span></span>
