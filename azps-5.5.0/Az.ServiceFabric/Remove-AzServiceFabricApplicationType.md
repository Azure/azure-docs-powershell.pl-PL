---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183474"
---
# <span data-ttu-id="a12e5-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a12e5-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="a12e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a12e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a12e5-103">Usuń sieć szkieletową usługi z klastrów.</span><span class="sxs-lookup"><span data-stu-id="a12e5-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="a12e5-104">Spowoduje to usunięcie wszystkich wersji tego typu w ramach tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="a12e5-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="a12e5-105">Obsługuje tylko ARM typów aplikacji wdrożonych.</span><span class="sxs-lookup"><span data-stu-id="a12e5-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="a12e5-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a12e5-106">SYNTAX</span></span>

### <span data-ttu-id="a12e5-107">ByResourceGroup (Default)</span><span class="sxs-lookup"><span data-stu-id="a12e5-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12e5-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a12e5-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12e5-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a12e5-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a12e5-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="a12e5-110">DESCRIPTION</span></span>
<span data-ttu-id="a12e5-111">To polecenie cmdlet powoduje usunięcie typu aplikacji z klastrem i usunięcie całej wersji typu w ramach tego zasobu, ale wszystkie aplikacje pod nim powinny zostać usunięte przed uruchomieniem tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="a12e5-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="a12e5-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a12e5-112">EXAMPLES</span></span>

### <span data-ttu-id="a12e5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a12e5-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="a12e5-114">W tym przykładzie usuniesz typ aplikacji "testAppType" i całą wersję pod nim.</span><span class="sxs-lookup"><span data-stu-id="a12e5-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="a12e5-115">Jeśli istnieją aplikacje utworzone za pomocą tego typu, polecenie zgłasza wyjątek.</span><span class="sxs-lookup"><span data-stu-id="a12e5-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="a12e5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a12e5-116">PARAMETERS</span></span>

### <span data-ttu-id="a12e5-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a12e5-117">-ClusterName</span></span>
<span data-ttu-id="a12e5-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="a12e5-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a12e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12e5-119">-DefaultProfile</span></span>
<span data-ttu-id="a12e5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a12e5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a12e5-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a12e5-121">-Force</span></span>
<span data-ttu-id="a12e5-122">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="a12e5-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="a12e5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a12e5-123">-InputObject</span></span>
<span data-ttu-id="a12e5-124">Zasób typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a12e5-124">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a12e5-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a12e5-125">-Name</span></span>
<span data-ttu-id="a12e5-126">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a12e5-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12e5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a12e5-127">-PassThru</span></span>
<span data-ttu-id="a12e5-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a12e5-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a12e5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a12e5-129">-ResourceGroupName</span></span>
<span data-ttu-id="a12e5-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a12e5-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a12e5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a12e5-131">-ResourceId</span></span>
<span data-ttu-id="a12e5-132">Arm ResourceId typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a12e5-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="a12e5-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a12e5-133">-Confirm</span></span>
<span data-ttu-id="a12e5-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a12e5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a12e5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a12e5-135">-WhatIf</span></span>
<span data-ttu-id="a12e5-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a12e5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a12e5-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a12e5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a12e5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12e5-138">CommonParameters</span></span>
<span data-ttu-id="a12e5-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a12e5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12e5-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a12e5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12e5-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a12e5-141">INPUTS</span></span>

### <span data-ttu-id="a12e5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a12e5-142">System.String</span></span>

### <span data-ttu-id="a12e5-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="a12e5-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="a12e5-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a12e5-144">OUTPUTS</span></span>

### <span data-ttu-id="a12e5-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a12e5-145">System.Boolean</span></span>

## <span data-ttu-id="a12e5-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a12e5-146">NOTES</span></span>

## <span data-ttu-id="a12e5-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a12e5-147">RELATED LINKS</span></span>
