---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189098"
---
# <span data-ttu-id="26a52-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="26a52-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="26a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26a52-102">SYNOPSIS</span></span>
<span data-ttu-id="26a52-103">Usuń sieć szkieletową usługi z wersji aplikacji o typie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="26a52-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="26a52-104">Obsługuje tylko ARM wersji typów aplikacji wdrożonych.</span><span class="sxs-lookup"><span data-stu-id="26a52-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="26a52-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="26a52-105">SYNTAX</span></span>

### <span data-ttu-id="26a52-106">ByResourceGroup (Default)</span><span class="sxs-lookup"><span data-stu-id="26a52-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a52-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="26a52-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a52-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="26a52-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26a52-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="26a52-109">DESCRIPTION</span></span>
<span data-ttu-id="26a52-110">To polecenie cmdlet spowoduje usunięcie z klastrów struktury usługi wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="26a52-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="26a52-111">Wszystkie aplikacje w ramach tego zasobu muszą zostać usunięte przed uruchomieniem tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="26a52-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="26a52-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="26a52-112">EXAMPLES</span></span>

### <span data-ttu-id="26a52-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26a52-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="26a52-114">W tym przykładzie usuniesz wersję "v1" pod typem "testAppType".</span><span class="sxs-lookup"><span data-stu-id="26a52-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="26a52-115">W obszarze tego zasobu istnieją aplikacje, dla których polecenie zgłasza wyjątek.</span><span class="sxs-lookup"><span data-stu-id="26a52-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="26a52-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26a52-116">PARAMETERS</span></span>

### <span data-ttu-id="26a52-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="26a52-117">-ClusterName</span></span>
<span data-ttu-id="26a52-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="26a52-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="26a52-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a52-119">-DefaultProfile</span></span>
<span data-ttu-id="26a52-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="26a52-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26a52-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="26a52-121">-Force</span></span>
<span data-ttu-id="26a52-122">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="26a52-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="26a52-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26a52-123">-InputObject</span></span>
<span data-ttu-id="26a52-124">Zasób wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="26a52-124">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26a52-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="26a52-125">-Name</span></span>
<span data-ttu-id="26a52-126">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="26a52-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a52-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26a52-127">-PassThru</span></span>
<span data-ttu-id="26a52-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="26a52-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="26a52-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26a52-129">-ResourceGroupName</span></span>
<span data-ttu-id="26a52-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26a52-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="26a52-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26a52-131">-ResourceId</span></span>
<span data-ttu-id="26a52-132">Arm ResourceId wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="26a52-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="26a52-133">— Wersja</span><span class="sxs-lookup"><span data-stu-id="26a52-133">-Version</span></span>
<span data-ttu-id="26a52-134">Określ wersję typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="26a52-134">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26a52-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26a52-135">-Confirm</span></span>
<span data-ttu-id="26a52-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26a52-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26a52-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26a52-137">-WhatIf</span></span>
<span data-ttu-id="26a52-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26a52-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26a52-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="26a52-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26a52-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a52-140">CommonParameters</span></span>
<span data-ttu-id="26a52-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a52-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a52-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26a52-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a52-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26a52-143">INPUTS</span></span>

### <span data-ttu-id="26a52-144">System.String</span><span class="sxs-lookup"><span data-stu-id="26a52-144">System.String</span></span>

### <span data-ttu-id="26a52-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="26a52-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="26a52-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26a52-146">OUTPUTS</span></span>

### <span data-ttu-id="26a52-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26a52-147">System.Boolean</span></span>

## <span data-ttu-id="26a52-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="26a52-148">NOTES</span></span>

## <span data-ttu-id="26a52-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26a52-149">RELATED LINKS</span></span>
