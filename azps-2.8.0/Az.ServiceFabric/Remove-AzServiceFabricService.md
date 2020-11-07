---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1314eb4d6bf4cfa802e0c6f40cc5ae7646209572
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871504"
---
# <span data-ttu-id="6ccf9-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6ccf9-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="6ccf9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ccf9-102">SYNOPSIS</span></span>
<span data-ttu-id="6ccf9-103">Usuwanie usługi z klastra.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="6ccf9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ccf9-104">SYNTAX</span></span>

### <span data-ttu-id="6ccf9-105">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ccf9-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ccf9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ccf9-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ccf9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6ccf9-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ccf9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ccf9-108">DESCRIPTION</span></span>
<span data-ttu-id="6ccf9-109">To polecenie cmdlet umożliwia usunięcie usługi z klastra.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="6ccf9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ccf9-110">EXAMPLES</span></span>

### <span data-ttu-id="6ccf9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ccf9-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="6ccf9-112">W tym przykładzie zostanie usunięta usługa "testApp ~ testService1".</span><span class="sxs-lookup"><span data-stu-id="6ccf9-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="6ccf9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ccf9-113">PARAMETERS</span></span>

### <span data-ttu-id="6ccf9-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6ccf9-114">-ApplicationName</span></span>
<span data-ttu-id="6ccf9-115">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-115">Specify the name of the application.</span></span>

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

### <span data-ttu-id="6ccf9-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="6ccf9-116">-ClusterName</span></span>
<span data-ttu-id="6ccf9-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6ccf9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ccf9-118">-DefaultProfile</span></span>
<span data-ttu-id="6ccf9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ccf9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6ccf9-120">-Force</span></span>
<span data-ttu-id="6ccf9-121">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="6ccf9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6ccf9-122">-InputObject</span></span>
<span data-ttu-id="6ccf9-123">Zasób usługi.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-123">The service resource.</span></span>

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

### <span data-ttu-id="6ccf9-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ccf9-124">-Name</span></span>
<span data-ttu-id="6ccf9-125">Określ nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-125">Specify the name of the service.</span></span>

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

### <span data-ttu-id="6ccf9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ccf9-126">-PassThru</span></span>
<span data-ttu-id="6ccf9-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6ccf9-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6ccf9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ccf9-128">-ResourceGroupName</span></span>
<span data-ttu-id="6ccf9-129">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6ccf9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ccf9-130">-ResourceId</span></span>
<span data-ttu-id="6ccf9-131">Identyfikator zasobu ARM usługi.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="6ccf9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ccf9-132">-Confirm</span></span>
<span data-ttu-id="6ccf9-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ccf9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ccf9-134">-WhatIf</span></span>
<span data-ttu-id="6ccf9-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ccf9-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ccf9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ccf9-137">CommonParameters</span></span>
<span data-ttu-id="6ccf9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ccf9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ccf9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ccf9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ccf9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ccf9-140">INPUTS</span></span>

### <span data-ttu-id="6ccf9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6ccf9-141">System.String</span></span>

### <span data-ttu-id="6ccf9-142">Microsoft. Azure. Commands. servicefabric. MODELES. PSService</span><span class="sxs-lookup"><span data-stu-id="6ccf9-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="6ccf9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ccf9-143">OUTPUTS</span></span>

### <span data-ttu-id="6ccf9-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ccf9-144">System.Boolean</span></span>

## <span data-ttu-id="6ccf9-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ccf9-145">NOTES</span></span>

## <span data-ttu-id="6ccf9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ccf9-146">RELATED LINKS</span></span>
