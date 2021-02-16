---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183475"
---
# <span data-ttu-id="9aaa0-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="9aaa0-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="9aaa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aaa0-102">SYNOPSIS</span></span>
<span data-ttu-id="9aaa0-103">Usuń aplikację z klastra.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-103">Remove an application from the cluster.</span></span> <span data-ttu-id="9aaa0-104">Spowoduje to usunięcie wszystkich usług w ramach aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-104">This will remove all the services under the application.</span></span> <span data-ttu-id="9aaa0-105">Obsługuje tylko ARM wdrożonych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="9aaa0-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9aaa0-106">SYNTAX</span></span>

### <span data-ttu-id="9aaa0-107">ByResourceGroup (Default)</span><span class="sxs-lookup"><span data-stu-id="9aaa0-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aaa0-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9aaa0-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aaa0-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9aaa0-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aaa0-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="9aaa0-110">DESCRIPTION</span></span>
<span data-ttu-id="9aaa0-111">To polecenie cmdlet usuwa formularz aplikacji z klastrem.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="9aaa0-112">Spowoduje to usunięcie wszystkich usług, jeśli w ogóle, w obszarze zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="9aaa0-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9aaa0-113">EXAMPLES</span></span>

### <span data-ttu-id="9aaa0-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9aaa0-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="9aaa0-115">W tym przykładzie usuniemy aplikację "testApp" w grupie zasobów "testRG" i klaster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="9aaa0-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="9aaa0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9aaa0-116">PARAMETERS</span></span>

### <span data-ttu-id="9aaa0-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9aaa0-117">-ClusterName</span></span>
<span data-ttu-id="9aaa0-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9aaa0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aaa0-119">-DefaultProfile</span></span>
<span data-ttu-id="9aaa0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aaa0-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9aaa0-121">-Force</span></span>
<span data-ttu-id="9aaa0-122">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="9aaa0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9aaa0-123">-InputObject</span></span>
<span data-ttu-id="9aaa0-124">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-124">The application resource.</span></span>

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

### <span data-ttu-id="9aaa0-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9aaa0-125">-Name</span></span>
<span data-ttu-id="9aaa0-126">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-126">Specify the name of the application.</span></span>

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

### <span data-ttu-id="9aaa0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9aaa0-127">-PassThru</span></span>
<span data-ttu-id="9aaa0-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9aaa0-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9aaa0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aaa0-129">-ResourceGroupName</span></span>
<span data-ttu-id="9aaa0-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9aaa0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9aaa0-131">-ResourceId</span></span>
<span data-ttu-id="9aaa0-132">Arm ResourceId aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="9aaa0-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9aaa0-133">-Confirm</span></span>
<span data-ttu-id="9aaa0-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aaa0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aaa0-135">-WhatIf</span></span>
<span data-ttu-id="9aaa0-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aaa0-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aaa0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aaa0-138">CommonParameters</span></span>
<span data-ttu-id="9aaa0-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aaa0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aaa0-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9aaa0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aaa0-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9aaa0-141">INPUTS</span></span>

### <span data-ttu-id="9aaa0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9aaa0-142">System.String</span></span>

### <span data-ttu-id="9aaa0-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="9aaa0-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="9aaa0-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9aaa0-144">OUTPUTS</span></span>

### <span data-ttu-id="9aaa0-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9aaa0-145">System.Boolean</span></span>

## <span data-ttu-id="9aaa0-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9aaa0-146">NOTES</span></span>

## <span data-ttu-id="9aaa0-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9aaa0-147">RELATED LINKS</span></span>
