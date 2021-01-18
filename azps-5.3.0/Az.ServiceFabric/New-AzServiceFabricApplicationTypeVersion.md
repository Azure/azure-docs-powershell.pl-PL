---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 60065541ecdd8439b67f4370bc1ef8bdc24119bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502814"
---
# <span data-ttu-id="859c4-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="859c4-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="859c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="859c4-102">SYNOPSIS</span></span>
<span data-ttu-id="859c4-103">Tworzenie nowej wersji typu aplikacji w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="859c4-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="859c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="859c4-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="859c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="859c4-105">DESCRIPTION</span></span>
<span data-ttu-id="859c4-106">To polecenie cmdlet powoduje utworzenie nowej wersji typu aplikacji przy użyciu pakietu określonego w parametrze-PackageUrl, który jest dostępny za pośrednictwem punktu końcowego usługi Azure Resource Manager w celu użycia podczas wdrażania i zawiera pakiet spakowane i spakowane z rozszerzeniem. sfpkg.</span><span class="sxs-lookup"><span data-stu-id="859c4-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="859c4-107">To polecenie utworzy typ aplikacji, jeśli jeszcze nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="859c4-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="859c4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="859c4-108">EXAMPLES</span></span>

### <span data-ttu-id="859c4-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="859c4-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="859c4-110">W tym przykładzie zostanie utworzona wersja typu aplikacji "v1" w obszarze typu "testAppType".</span><span class="sxs-lookup"><span data-stu-id="859c4-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="859c4-111">Wersja w manifeście aplikacji znajdująca się w pakiecie powinna być taka sama jak wersja określona w wersji.</span><span class="sxs-lookup"><span data-stu-id="859c4-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="859c4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="859c4-112">PARAMETERS</span></span>

### <span data-ttu-id="859c4-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="859c4-113">-ClusterName</span></span>
<span data-ttu-id="859c4-114">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="859c4-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859c4-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="859c4-115">-DefaultParameter</span></span>
<span data-ttu-id="859c4-116">Określ wartości domyślne parametrów aplikacji jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="859c4-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="859c4-117">Te parametry muszą istnieć w manifeście aplikacji.</span><span class="sxs-lookup"><span data-stu-id="859c4-117">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859c4-118">-DefaultProfile</span></span>
<span data-ttu-id="859c4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="859c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="859c4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="859c4-120">-Force</span></span>
<span data-ttu-id="859c4-121">Kontynuuj bez monitowania</span><span class="sxs-lookup"><span data-stu-id="859c4-121">Continue without prompts</span></span>

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

### <span data-ttu-id="859c4-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="859c4-122">-Name</span></span>
<span data-ttu-id="859c4-123">Określ nazwę typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="859c4-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859c4-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="859c4-124">-PackageUrl</span></span>
<span data-ttu-id="859c4-125">Określanie adresu URL pliku sfpkg pakietu aplikacji</span><span class="sxs-lookup"><span data-stu-id="859c4-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="859c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="859c4-127">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="859c4-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859c4-128">-Version</span><span class="sxs-lookup"><span data-stu-id="859c4-128">-Version</span></span>
<span data-ttu-id="859c4-129">Określanie wersji typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="859c4-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859c4-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="859c4-130">-Confirm</span></span>
<span data-ttu-id="859c4-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="859c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="859c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859c4-132">-WhatIf</span></span>
<span data-ttu-id="859c4-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="859c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="859c4-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="859c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="859c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859c4-135">CommonParameters</span></span>
<span data-ttu-id="859c4-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="859c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859c4-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="859c4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859c4-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="859c4-138">INPUTS</span></span>

### <span data-ttu-id="859c4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="859c4-139">System.String</span></span>

### <span data-ttu-id="859c4-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="859c4-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="859c4-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="859c4-141">OUTPUTS</span></span>

### <span data-ttu-id="859c4-142">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="859c4-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="859c4-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="859c4-143">NOTES</span></span>

## <span data-ttu-id="859c4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="859c4-144">RELATED LINKS</span></span>
