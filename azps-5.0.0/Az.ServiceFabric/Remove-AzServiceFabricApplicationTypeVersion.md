---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 498dec77dfc2f4ede8ae81aa70b10acfe2ad2954
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308665"
---
# <span data-ttu-id="fd462-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fd462-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="fd462-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd462-102">SYNOPSIS</span></span>
<span data-ttu-id="fd462-103">Usuwanie usługi sieci szkieletowej w wersji typu aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="fd462-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="fd462-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd462-104">SYNTAX</span></span>

### <span data-ttu-id="fd462-105">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fd462-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd462-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd462-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd462-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd462-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd462-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fd462-108">DESCRIPTION</span></span>
<span data-ttu-id="fd462-109">To polecenie cmdlet spowoduje usunięcie z klastra wersji typu aplikacji Fabric.</span><span class="sxs-lookup"><span data-stu-id="fd462-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="fd462-110">Wszystkie aplikacje w ramach tego zasobu muszą zostać usunięte przed uruchomieniem tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="fd462-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="fd462-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd462-111">EXAMPLES</span></span>

### <span data-ttu-id="fd462-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd462-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="fd462-113">W tym przykładzie zostanie usunięta wersja "v1" w obszarze typu "testAppType".</span><span class="sxs-lookup"><span data-stu-id="fd462-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="fd462-114">W obszarze tego zasobu są dostępne jakieś aplikacje. polecenie wygeneruje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="fd462-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="fd462-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd462-115">PARAMETERS</span></span>

### <span data-ttu-id="fd462-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="fd462-116">-ClusterName</span></span>
<span data-ttu-id="fd462-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="fd462-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fd462-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd462-118">-DefaultProfile</span></span>
<span data-ttu-id="fd462-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd462-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd462-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fd462-120">-Force</span></span>
<span data-ttu-id="fd462-121">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="fd462-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="fd462-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fd462-122">-InputObject</span></span>
<span data-ttu-id="fd462-123">Zasób typ aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fd462-123">The application type version resource.</span></span>

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

### <span data-ttu-id="fd462-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd462-124">-Name</span></span>
<span data-ttu-id="fd462-125">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fd462-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="fd462-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd462-126">-PassThru</span></span>
<span data-ttu-id="fd462-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fd462-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fd462-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd462-128">-ResourceGroupName</span></span>
<span data-ttu-id="fd462-129">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd462-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fd462-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd462-130">-ResourceId</span></span>
<span data-ttu-id="fd462-131">Identyfikator zasobu ARM w wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fd462-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="fd462-132">-Version</span><span class="sxs-lookup"><span data-stu-id="fd462-132">-Version</span></span>
<span data-ttu-id="fd462-133">Określ wersję typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fd462-133">Specify the application type version.</span></span>

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

### <span data-ttu-id="fd462-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd462-134">-Confirm</span></span>
<span data-ttu-id="fd462-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd462-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd462-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd462-136">-WhatIf</span></span>
<span data-ttu-id="fd462-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd462-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd462-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd462-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd462-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd462-139">CommonParameters</span></span>
<span data-ttu-id="fd462-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd462-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd462-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd462-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd462-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd462-142">INPUTS</span></span>

### <span data-ttu-id="fd462-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fd462-143">System.String</span></span>

### <span data-ttu-id="fd462-144">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fd462-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="fd462-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd462-145">OUTPUTS</span></span>

### <span data-ttu-id="fd462-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd462-146">System.Boolean</span></span>

## <span data-ttu-id="fd462-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd462-147">NOTES</span></span>

## <span data-ttu-id="fd462-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd462-148">RELATED LINKS</span></span>
