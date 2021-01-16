---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343678"
---
# <span data-ttu-id="c54e7-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c54e7-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="c54e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c54e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c54e7-103">Usuwanie usługi Fabric typ aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="c54e7-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="c54e7-104">Spowoduje to usunięcie wszystkich wersji typów w obszarze ten zasób.</span><span class="sxs-lookup"><span data-stu-id="c54e7-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="c54e7-105">Obsługuje tylko typy aplikacji rozmieszczone w ARM.</span><span class="sxs-lookup"><span data-stu-id="c54e7-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="c54e7-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c54e7-106">SYNTAX</span></span>

### <span data-ttu-id="c54e7-107">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c54e7-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c54e7-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c54e7-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c54e7-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c54e7-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c54e7-110">Opis</span><span class="sxs-lookup"><span data-stu-id="c54e7-110">DESCRIPTION</span></span>
<span data-ttu-id="c54e7-111">To polecenie cmdlet umożliwia usunięcie typu aplikacji z klastra i usunięcie całej wersji tego typu w ramach tego zasobu, ale przed uruchomieniem tego polecenia wszystkie aplikacje w jego ramach powinny zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="c54e7-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="c54e7-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c54e7-112">EXAMPLES</span></span>

### <span data-ttu-id="c54e7-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c54e7-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="c54e7-114">W tym przykładzie zostanie usunięty typ aplikacji "testAppType" i cała jej wersja.</span><span class="sxs-lookup"><span data-stu-id="c54e7-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="c54e7-115">Jeśli istnieją jakieś aplikacje utworzone za pomocą tego typu, polecenie generuje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="c54e7-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="c54e7-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c54e7-116">PARAMETERS</span></span>

### <span data-ttu-id="c54e7-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="c54e7-117">-ClusterName</span></span>
<span data-ttu-id="c54e7-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="c54e7-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c54e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c54e7-119">-DefaultProfile</span></span>
<span data-ttu-id="c54e7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c54e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c54e7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c54e7-121">-Force</span></span>
<span data-ttu-id="c54e7-122">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="c54e7-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="c54e7-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c54e7-123">-InputObject</span></span>
<span data-ttu-id="c54e7-124">Zasób typ aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c54e7-124">The application type resource.</span></span>

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

### <span data-ttu-id="c54e7-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c54e7-125">-Name</span></span>
<span data-ttu-id="c54e7-126">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c54e7-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="c54e7-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c54e7-127">-PassThru</span></span>
<span data-ttu-id="c54e7-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c54e7-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c54e7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c54e7-129">-ResourceGroupName</span></span>
<span data-ttu-id="c54e7-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c54e7-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c54e7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c54e7-131">-ResourceId</span></span>
<span data-ttu-id="c54e7-132">Identyfikator zasobu ARM dla typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c54e7-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="c54e7-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c54e7-133">-Confirm</span></span>
<span data-ttu-id="c54e7-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c54e7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c54e7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c54e7-135">-WhatIf</span></span>
<span data-ttu-id="c54e7-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c54e7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c54e7-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c54e7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c54e7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c54e7-138">CommonParameters</span></span>
<span data-ttu-id="c54e7-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c54e7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c54e7-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c54e7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c54e7-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c54e7-141">INPUTS</span></span>

### <span data-ttu-id="c54e7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c54e7-142">System.String</span></span>

### <span data-ttu-id="c54e7-143">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="c54e7-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="c54e7-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c54e7-144">OUTPUTS</span></span>

### <span data-ttu-id="c54e7-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c54e7-145">System.Boolean</span></span>

## <span data-ttu-id="c54e7-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c54e7-146">NOTES</span></span>

## <span data-ttu-id="c54e7-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c54e7-147">RELATED LINKS</span></span>
