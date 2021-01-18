---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502803"
---
# <span data-ttu-id="239ab-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="239ab-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="239ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="239ab-102">SYNOPSIS</span></span>
<span data-ttu-id="239ab-103">Usuwanie usługi sieci szkieletowej w wersji typu aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="239ab-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="239ab-104">Obsługuje tylko wersje typu aplikacja ARM wdrożone.</span><span class="sxs-lookup"><span data-stu-id="239ab-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="239ab-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="239ab-105">SYNTAX</span></span>

### <span data-ttu-id="239ab-106">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="239ab-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="239ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="239ab-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="239ab-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="239ab-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="239ab-109">Opis</span><span class="sxs-lookup"><span data-stu-id="239ab-109">DESCRIPTION</span></span>
<span data-ttu-id="239ab-110">To polecenie cmdlet spowoduje usunięcie z klastra wersji typu aplikacji Fabric.</span><span class="sxs-lookup"><span data-stu-id="239ab-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="239ab-111">Wszystkie aplikacje w ramach tego zasobu muszą zostać usunięte przed uruchomieniem tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="239ab-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="239ab-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="239ab-112">EXAMPLES</span></span>

### <span data-ttu-id="239ab-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="239ab-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="239ab-114">W tym przykładzie zostanie usunięta wersja "v1" w obszarze typu "testAppType".</span><span class="sxs-lookup"><span data-stu-id="239ab-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="239ab-115">W obszarze tego zasobu są dostępne jakieś aplikacje. polecenie wygeneruje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="239ab-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="239ab-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="239ab-116">PARAMETERS</span></span>

### <span data-ttu-id="239ab-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="239ab-117">-ClusterName</span></span>
<span data-ttu-id="239ab-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="239ab-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="239ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="239ab-119">-DefaultProfile</span></span>
<span data-ttu-id="239ab-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="239ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="239ab-121">-Force</span><span class="sxs-lookup"><span data-stu-id="239ab-121">-Force</span></span>
<span data-ttu-id="239ab-122">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="239ab-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="239ab-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="239ab-123">-InputObject</span></span>
<span data-ttu-id="239ab-124">Zasób typ aplikacji.</span><span class="sxs-lookup"><span data-stu-id="239ab-124">The application type version resource.</span></span>

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

### <span data-ttu-id="239ab-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="239ab-125">-Name</span></span>
<span data-ttu-id="239ab-126">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="239ab-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="239ab-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="239ab-127">-PassThru</span></span>
<span data-ttu-id="239ab-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="239ab-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="239ab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="239ab-129">-ResourceGroupName</span></span>
<span data-ttu-id="239ab-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="239ab-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="239ab-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="239ab-131">-ResourceId</span></span>
<span data-ttu-id="239ab-132">Identyfikator zasobu ARM w wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="239ab-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="239ab-133">-Version</span><span class="sxs-lookup"><span data-stu-id="239ab-133">-Version</span></span>
<span data-ttu-id="239ab-134">Określ wersję typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="239ab-134">Specify the application type version.</span></span>

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

### <span data-ttu-id="239ab-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="239ab-135">-Confirm</span></span>
<span data-ttu-id="239ab-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="239ab-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="239ab-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="239ab-137">-WhatIf</span></span>
<span data-ttu-id="239ab-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="239ab-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="239ab-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="239ab-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="239ab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="239ab-140">CommonParameters</span></span>
<span data-ttu-id="239ab-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="239ab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="239ab-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="239ab-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="239ab-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="239ab-143">INPUTS</span></span>

### <span data-ttu-id="239ab-144">System. String</span><span class="sxs-lookup"><span data-stu-id="239ab-144">System.String</span></span>

### <span data-ttu-id="239ab-145">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="239ab-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="239ab-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="239ab-146">OUTPUTS</span></span>

### <span data-ttu-id="239ab-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="239ab-147">System.Boolean</span></span>

## <span data-ttu-id="239ab-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="239ab-148">NOTES</span></span>

## <span data-ttu-id="239ab-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="239ab-149">RELATED LINKS</span></span>
