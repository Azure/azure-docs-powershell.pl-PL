---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357884"
---
# <span data-ttu-id="5de81-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5de81-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="5de81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5de81-102">SYNOPSIS</span></span>
<span data-ttu-id="5de81-103">Usuwanie usługi z klastra.</span><span class="sxs-lookup"><span data-stu-id="5de81-103">Remove a service from the cluster.</span></span> <span data-ttu-id="5de81-104">Obsługuje tylko usługi wdrażania ARM.</span><span class="sxs-lookup"><span data-stu-id="5de81-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="5de81-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5de81-105">SYNTAX</span></span>

### <span data-ttu-id="5de81-106">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5de81-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5de81-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5de81-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5de81-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5de81-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5de81-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5de81-109">DESCRIPTION</span></span>
<span data-ttu-id="5de81-110">To polecenie cmdlet umożliwia usunięcie usługi z klastra.</span><span class="sxs-lookup"><span data-stu-id="5de81-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="5de81-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5de81-111">EXAMPLES</span></span>

### <span data-ttu-id="5de81-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5de81-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="5de81-113">W tym przykładzie zostanie usunięta usługa "testApp ~ testService1".</span><span class="sxs-lookup"><span data-stu-id="5de81-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="5de81-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5de81-114">PARAMETERS</span></span>

### <span data-ttu-id="5de81-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="5de81-115">-ApplicationName</span></span>
<span data-ttu-id="5de81-116">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5de81-116">Specify the name of the application.</span></span>

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

### <span data-ttu-id="5de81-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="5de81-117">-ClusterName</span></span>
<span data-ttu-id="5de81-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="5de81-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5de81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de81-119">-DefaultProfile</span></span>
<span data-ttu-id="5de81-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5de81-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5de81-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5de81-121">-Force</span></span>
<span data-ttu-id="5de81-122">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="5de81-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="5de81-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5de81-123">-InputObject</span></span>
<span data-ttu-id="5de81-124">Zasób usługi.</span><span class="sxs-lookup"><span data-stu-id="5de81-124">The service resource.</span></span>

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

### <span data-ttu-id="5de81-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5de81-125">-Name</span></span>
<span data-ttu-id="5de81-126">Określ nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="5de81-126">Specify the name of the service.</span></span>

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

### <span data-ttu-id="5de81-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5de81-127">-PassThru</span></span>
<span data-ttu-id="5de81-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5de81-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5de81-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5de81-129">-ResourceGroupName</span></span>
<span data-ttu-id="5de81-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5de81-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5de81-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5de81-131">-ResourceId</span></span>
<span data-ttu-id="5de81-132">Identyfikator zasobu ARM usługi.</span><span class="sxs-lookup"><span data-stu-id="5de81-132">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="5de81-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5de81-133">-Confirm</span></span>
<span data-ttu-id="5de81-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5de81-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5de81-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5de81-135">-WhatIf</span></span>
<span data-ttu-id="5de81-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5de81-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5de81-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5de81-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5de81-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de81-138">CommonParameters</span></span>
<span data-ttu-id="5de81-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5de81-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de81-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5de81-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de81-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5de81-141">INPUTS</span></span>

### <span data-ttu-id="5de81-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5de81-142">System.String</span></span>

### <span data-ttu-id="5de81-143">Microsoft. Azure. Commands. servicefabric. MODELES. PSService</span><span class="sxs-lookup"><span data-stu-id="5de81-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="5de81-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5de81-144">OUTPUTS</span></span>

### <span data-ttu-id="5de81-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5de81-145">System.Boolean</span></span>

## <span data-ttu-id="5de81-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5de81-146">NOTES</span></span>

## <span data-ttu-id="5de81-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5de81-147">RELATED LINKS</span></span>
