---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 1ad1e8220ed77a9206503adaf4f9924f95fe4f44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873051"
---
# <span data-ttu-id="9529b-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="9529b-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="9529b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9529b-102">SYNOPSIS</span></span>
<span data-ttu-id="9529b-103">Usuwanie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="9529b-103">Remove an application from the cluster.</span></span> <span data-ttu-id="9529b-104">Spowoduje to usunięcie wszystkich usług objętych aplikacją.</span><span class="sxs-lookup"><span data-stu-id="9529b-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="9529b-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9529b-105">SYNTAX</span></span>

### <span data-ttu-id="9529b-106">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9529b-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9529b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9529b-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9529b-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9529b-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9529b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9529b-109">DESCRIPTION</span></span>
<span data-ttu-id="9529b-110">To polecenie cmdlet umożliwia usunięcie aplikacji z klastra.</span><span class="sxs-lookup"><span data-stu-id="9529b-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="9529b-111">Spowoduje to usunięcie wszystkich usług, o ile istnieją, pod zasobem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9529b-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="9529b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9529b-112">EXAMPLES</span></span>

### <span data-ttu-id="9529b-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9529b-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="9529b-114">W tym przykładzie usunięto aplikację "testApp" w grupie zasobów "testRG" i klastrze "testCluster".</span><span class="sxs-lookup"><span data-stu-id="9529b-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="9529b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9529b-115">PARAMETERS</span></span>

### <span data-ttu-id="9529b-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="9529b-116">-ClusterName</span></span>
<span data-ttu-id="9529b-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="9529b-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9529b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9529b-118">-DefaultProfile</span></span>
<span data-ttu-id="9529b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9529b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9529b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9529b-120">-Force</span></span>
<span data-ttu-id="9529b-121">Usuń bez monitu.</span><span class="sxs-lookup"><span data-stu-id="9529b-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="9529b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9529b-122">-InputObject</span></span>
<span data-ttu-id="9529b-123">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9529b-123">The application resource.</span></span>

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

### <span data-ttu-id="9529b-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9529b-124">-Name</span></span>
<span data-ttu-id="9529b-125">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9529b-125">Specify the name of the application.</span></span>

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

### <span data-ttu-id="9529b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9529b-126">-PassThru</span></span>
<span data-ttu-id="9529b-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9529b-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9529b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9529b-128">-ResourceGroupName</span></span>
<span data-ttu-id="9529b-129">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9529b-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9529b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9529b-130">-ResourceId</span></span>
<span data-ttu-id="9529b-131">Identyfikator zasobu ARM aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9529b-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="9529b-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9529b-132">-Confirm</span></span>
<span data-ttu-id="9529b-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9529b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9529b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9529b-134">-WhatIf</span></span>
<span data-ttu-id="9529b-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9529b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9529b-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9529b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9529b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9529b-137">CommonParameters</span></span>
<span data-ttu-id="9529b-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9529b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9529b-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9529b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9529b-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9529b-140">INPUTS</span></span>

### <span data-ttu-id="9529b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9529b-141">System.String</span></span>

### <span data-ttu-id="9529b-142">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="9529b-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="9529b-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9529b-143">OUTPUTS</span></span>

### <span data-ttu-id="9529b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9529b-144">System.Boolean</span></span>

## <span data-ttu-id="9529b-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9529b-145">NOTES</span></span>

## <span data-ttu-id="9529b-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9529b-146">RELATED LINKS</span></span>
