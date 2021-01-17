---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348601"
---
# <span data-ttu-id="eeb7e-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="eeb7e-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="eeb7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eeb7e-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb7e-103">Usuwanie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-103">Remove an application from the cluster.</span></span> <span data-ttu-id="eeb7e-104">Spowoduje to usunięcie wszystkich usług objętych aplikacją.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-104">This will remove all the services under the application.</span></span> <span data-ttu-id="eeb7e-105">Obsługuje tylko aplikacje rozmieszczone w ARM.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="eeb7e-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eeb7e-106">SYNTAX</span></span>

### <span data-ttu-id="eeb7e-107">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eeb7e-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb7e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eeb7e-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb7e-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eeb7e-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb7e-110">Opis</span><span class="sxs-lookup"><span data-stu-id="eeb7e-110">DESCRIPTION</span></span>
<span data-ttu-id="eeb7e-111">To polecenie cmdlet umożliwia usunięcie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="eeb7e-112">Spowoduje to usunięcie wszystkich usług, o ile istnieją, pod zasobem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="eeb7e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eeb7e-113">EXAMPLES</span></span>

### <span data-ttu-id="eeb7e-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eeb7e-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="eeb7e-115">W tym przykładzie usunięto aplikację "testApp" w grupie zasobów "testRG" i klastrze "testCluster".</span><span class="sxs-lookup"><span data-stu-id="eeb7e-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="eeb7e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eeb7e-116">PARAMETERS</span></span>

### <span data-ttu-id="eeb7e-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="eeb7e-117">-ClusterName</span></span>
<span data-ttu-id="eeb7e-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="eeb7e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb7e-119">-DefaultProfile</span></span>
<span data-ttu-id="eeb7e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeb7e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="eeb7e-121">-Force</span></span>
<span data-ttu-id="eeb7e-122">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="eeb7e-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eeb7e-123">-InputObject</span></span>
<span data-ttu-id="eeb7e-124">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-124">The application resource.</span></span>

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

### <span data-ttu-id="eeb7e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eeb7e-125">-Name</span></span>
<span data-ttu-id="eeb7e-126">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-126">Specify the name of the application.</span></span>

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

### <span data-ttu-id="eeb7e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eeb7e-127">-PassThru</span></span>
<span data-ttu-id="eeb7e-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="eeb7e-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="eeb7e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb7e-129">-ResourceGroupName</span></span>
<span data-ttu-id="eeb7e-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="eeb7e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeb7e-131">-ResourceId</span></span>
<span data-ttu-id="eeb7e-132">Identyfikator zasobu ARM aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="eeb7e-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eeb7e-133">-Confirm</span></span>
<span data-ttu-id="eeb7e-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb7e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb7e-135">-WhatIf</span></span>
<span data-ttu-id="eeb7e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb7e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb7e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb7e-138">CommonParameters</span></span>
<span data-ttu-id="eeb7e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb7e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb7e-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeb7e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb7e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eeb7e-141">INPUTS</span></span>

### <span data-ttu-id="eeb7e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="eeb7e-142">System.String</span></span>

### <span data-ttu-id="eeb7e-143">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="eeb7e-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="eeb7e-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eeb7e-144">OUTPUTS</span></span>

### <span data-ttu-id="eeb7e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eeb7e-145">System.Boolean</span></span>

## <span data-ttu-id="eeb7e-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eeb7e-146">NOTES</span></span>

## <span data-ttu-id="eeb7e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eeb7e-147">RELATED LINKS</span></span>
