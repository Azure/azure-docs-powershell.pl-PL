---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 87557a67c8cb087b8a22ecc9cdfa59a3690057dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304506"
---
# <span data-ttu-id="d4662-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4662-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="d4662-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4662-102">SYNOPSIS</span></span>
<span data-ttu-id="d4662-103">Usuwanie usługi Fabric typ aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="d4662-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="d4662-104">Spowoduje to usunięcie wszystkich wersji typów w obszarze ten zasób.</span><span class="sxs-lookup"><span data-stu-id="d4662-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="d4662-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4662-105">SYNTAX</span></span>

### <span data-ttu-id="d4662-106">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d4662-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4662-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d4662-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4662-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d4662-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4662-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d4662-109">DESCRIPTION</span></span>
<span data-ttu-id="d4662-110">To polecenie cmdlet umożliwia usunięcie typu aplikacji z klastra i usunięcie całej wersji tego typu w ramach tego zasobu, ale przed uruchomieniem tego polecenia wszystkie aplikacje w jego ramach powinny zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="d4662-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="d4662-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4662-111">EXAMPLES</span></span>

### <span data-ttu-id="d4662-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4662-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="d4662-113">W tym przykładzie zostanie usunięty typ aplikacji "testAppType" i cała jej wersja.</span><span class="sxs-lookup"><span data-stu-id="d4662-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="d4662-114">Jeśli istnieją jakieś aplikacje utworzone za pomocą tego typu, polecenie generuje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="d4662-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="d4662-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4662-115">PARAMETERS</span></span>

### <span data-ttu-id="d4662-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d4662-116">-ClusterName</span></span>
<span data-ttu-id="d4662-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d4662-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d4662-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4662-118">-DefaultProfile</span></span>
<span data-ttu-id="d4662-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4662-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4662-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d4662-120">-Force</span></span>
<span data-ttu-id="d4662-121">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="d4662-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="d4662-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4662-122">-InputObject</span></span>
<span data-ttu-id="d4662-123">Zasób typ aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d4662-123">The application type resource.</span></span>

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

### <span data-ttu-id="d4662-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4662-124">-Name</span></span>
<span data-ttu-id="d4662-125">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d4662-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="d4662-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4662-126">-PassThru</span></span>
<span data-ttu-id="d4662-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d4662-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d4662-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4662-128">-ResourceGroupName</span></span>
<span data-ttu-id="d4662-129">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4662-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d4662-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4662-130">-ResourceId</span></span>
<span data-ttu-id="d4662-131">Identyfikator zasobu ARM dla typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d4662-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="d4662-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4662-132">-Confirm</span></span>
<span data-ttu-id="d4662-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4662-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4662-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4662-134">-WhatIf</span></span>
<span data-ttu-id="d4662-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4662-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4662-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4662-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4662-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4662-137">CommonParameters</span></span>
<span data-ttu-id="d4662-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4662-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4662-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4662-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4662-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4662-140">INPUTS</span></span>

### <span data-ttu-id="d4662-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d4662-141">System.String</span></span>

### <span data-ttu-id="d4662-142">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="d4662-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="d4662-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4662-143">OUTPUTS</span></span>

### <span data-ttu-id="d4662-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4662-144">System.Boolean</span></span>

## <span data-ttu-id="d4662-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4662-145">NOTES</span></span>

## <span data-ttu-id="d4662-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4662-146">RELATED LINKS</span></span>
