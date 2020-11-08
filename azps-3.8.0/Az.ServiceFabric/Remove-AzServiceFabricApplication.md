---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: e9f248575d0f5193a11c729384e674870b3de29c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050658"
---
# <span data-ttu-id="de5f0-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="de5f0-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="de5f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="de5f0-103">Usuwanie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="de5f0-103">Remove an application from the cluster.</span></span> <span data-ttu-id="de5f0-104">Spowoduje to usunięcie wszystkich usług objętych aplikacją.</span><span class="sxs-lookup"><span data-stu-id="de5f0-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="de5f0-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de5f0-105">SYNTAX</span></span>

### <span data-ttu-id="de5f0-106">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de5f0-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de5f0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="de5f0-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de5f0-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="de5f0-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de5f0-109">Opis</span><span class="sxs-lookup"><span data-stu-id="de5f0-109">DESCRIPTION</span></span>
<span data-ttu-id="de5f0-110">To polecenie cmdlet umożliwia usunięcie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="de5f0-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="de5f0-111">Spowoduje to usunięcie wszystkich usług, o ile istnieją, pod zasobem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="de5f0-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="de5f0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de5f0-112">EXAMPLES</span></span>

### <span data-ttu-id="de5f0-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de5f0-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="de5f0-114">W tym przykładzie usunięto aplikację "testApp" w grupie zasobów "testRG" i klastrze "testCluster".</span><span class="sxs-lookup"><span data-stu-id="de5f0-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="de5f0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de5f0-115">PARAMETERS</span></span>

### <span data-ttu-id="de5f0-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="de5f0-116">-ClusterName</span></span>
<span data-ttu-id="de5f0-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="de5f0-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="de5f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5f0-118">-DefaultProfile</span></span>
<span data-ttu-id="de5f0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de5f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de5f0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="de5f0-120">-Force</span></span>
<span data-ttu-id="de5f0-121">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="de5f0-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="de5f0-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="de5f0-122">-InputObject</span></span>
<span data-ttu-id="de5f0-123">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="de5f0-123">The application resource.</span></span>

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

### <span data-ttu-id="de5f0-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de5f0-124">-Name</span></span>
<span data-ttu-id="de5f0-125">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="de5f0-125">Specify the name of the application.</span></span>

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

### <span data-ttu-id="de5f0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de5f0-126">-PassThru</span></span>
<span data-ttu-id="de5f0-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="de5f0-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="de5f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de5f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="de5f0-129">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de5f0-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="de5f0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de5f0-130">-ResourceId</span></span>
<span data-ttu-id="de5f0-131">Identyfikator zasobu ARM aplikacji.</span><span class="sxs-lookup"><span data-stu-id="de5f0-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="de5f0-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de5f0-132">-Confirm</span></span>
<span data-ttu-id="de5f0-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de5f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de5f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5f0-134">-WhatIf</span></span>
<span data-ttu-id="de5f0-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de5f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de5f0-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de5f0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de5f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5f0-137">CommonParameters</span></span>
<span data-ttu-id="de5f0-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de5f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5f0-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5f0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5f0-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de5f0-140">INPUTS</span></span>

### <span data-ttu-id="de5f0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="de5f0-141">System.String</span></span>

### <span data-ttu-id="de5f0-142">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="de5f0-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="de5f0-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de5f0-143">OUTPUTS</span></span>

### <span data-ttu-id="de5f0-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de5f0-144">System.Boolean</span></span>

## <span data-ttu-id="de5f0-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de5f0-145">NOTES</span></span>

## <span data-ttu-id="de5f0-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de5f0-146">RELATED LINKS</span></span>
