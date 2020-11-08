---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 8dc06a9ce860dfb6e01c79674dd414eedb51df17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232639"
---
# <span data-ttu-id="cd162-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd162-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="cd162-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd162-102">SYNOPSIS</span></span>
<span data-ttu-id="cd162-103">Usuwanie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="cd162-103">Remove an application from the cluster.</span></span> <span data-ttu-id="cd162-104">Spowoduje to usunięcie wszystkich usług objętych aplikacją.</span><span class="sxs-lookup"><span data-stu-id="cd162-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="cd162-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd162-105">SYNTAX</span></span>

### <span data-ttu-id="cd162-106">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd162-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd162-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd162-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd162-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd162-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd162-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cd162-109">DESCRIPTION</span></span>
<span data-ttu-id="cd162-110">To polecenie cmdlet umożliwia usunięcie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="cd162-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="cd162-111">Spowoduje to usunięcie wszystkich usług, o ile istnieją, pod zasobem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd162-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="cd162-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd162-112">EXAMPLES</span></span>

### <span data-ttu-id="cd162-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd162-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="cd162-114">W tym przykładzie usunięto aplikację "testApp" w grupie zasobów "testRG" i klastrze "testCluster".</span><span class="sxs-lookup"><span data-stu-id="cd162-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="cd162-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd162-115">PARAMETERS</span></span>

### <span data-ttu-id="cd162-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="cd162-116">-ClusterName</span></span>
<span data-ttu-id="cd162-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="cd162-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cd162-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd162-118">-DefaultProfile</span></span>
<span data-ttu-id="cd162-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd162-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd162-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cd162-120">-Force</span></span>
<span data-ttu-id="cd162-121">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="cd162-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="cd162-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd162-122">-InputObject</span></span>
<span data-ttu-id="cd162-123">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd162-123">The application resource.</span></span>

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

### <span data-ttu-id="cd162-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd162-124">-Name</span></span>
<span data-ttu-id="cd162-125">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd162-125">Specify the name of the application.</span></span>

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

### <span data-ttu-id="cd162-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd162-126">-PassThru</span></span>
<span data-ttu-id="cd162-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cd162-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cd162-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd162-128">-ResourceGroupName</span></span>
<span data-ttu-id="cd162-129">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd162-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="cd162-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd162-130">-ResourceId</span></span>
<span data-ttu-id="cd162-131">Identyfikator zasobu ARM aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd162-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="cd162-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd162-132">-Confirm</span></span>
<span data-ttu-id="cd162-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd162-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd162-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd162-134">-WhatIf</span></span>
<span data-ttu-id="cd162-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd162-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd162-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd162-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd162-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd162-137">CommonParameters</span></span>
<span data-ttu-id="cd162-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd162-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd162-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd162-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd162-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd162-140">INPUTS</span></span>

### <span data-ttu-id="cd162-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cd162-141">System.String</span></span>

### <span data-ttu-id="cd162-142">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="cd162-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="cd162-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd162-143">OUTPUTS</span></span>

### <span data-ttu-id="cd162-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd162-144">System.Boolean</span></span>

## <span data-ttu-id="cd162-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd162-145">NOTES</span></span>

## <span data-ttu-id="cd162-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd162-146">RELATED LINKS</span></span>
