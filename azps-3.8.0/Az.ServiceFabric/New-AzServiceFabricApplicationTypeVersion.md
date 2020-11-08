---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 69bbcbbd508a5bf32163b91378aab62dbdcb3a64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050692"
---
# <span data-ttu-id="fd26c-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fd26c-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="fd26c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd26c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd26c-103">Tworzenie nowej wersji typu aplikacji w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="fd26c-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="fd26c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd26c-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd26c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd26c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd26c-106">To polecenie cmdlet powoduje utworzenie nowej wersji typu aplikacji przy użyciu pakietu określonego w parametrze-PackageUrl, który jest dostępny za pośrednictwem punktu końcowego usługi Azure Resource Manager w celu użycia podczas wdrażania i zawiera pakiet spakowane i spakowane z rozszerzeniem. sfpkg.</span><span class="sxs-lookup"><span data-stu-id="fd26c-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="fd26c-107">To polecenie utworzy typ aplikacji, jeśli jeszcze nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="fd26c-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="fd26c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd26c-108">EXAMPLES</span></span>

### <span data-ttu-id="fd26c-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd26c-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="fd26c-110">W tym przykładzie zostanie utworzona wersja typu aplikacji "v1" w obszarze typu "testAppType".</span><span class="sxs-lookup"><span data-stu-id="fd26c-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="fd26c-111">Wersja w manifeście aplikacji znajdująca się w pakiecie powinna być taka sama jak wersja określona w wersji.</span><span class="sxs-lookup"><span data-stu-id="fd26c-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="fd26c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd26c-112">PARAMETERS</span></span>

### <span data-ttu-id="fd26c-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="fd26c-113">-ClusterName</span></span>
<span data-ttu-id="fd26c-114">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="fd26c-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fd26c-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="fd26c-115">-DefaultParameter</span></span>
<span data-ttu-id="fd26c-116">Określ wartości domyślne parametrów aplikacji jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="fd26c-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="fd26c-117">Te parametry muszą istnieć w manifeście aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fd26c-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="fd26c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd26c-118">-DefaultProfile</span></span>
<span data-ttu-id="fd26c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd26c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd26c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fd26c-120">-Force</span></span>
<span data-ttu-id="fd26c-121">Kontynuuj bez monitowania</span><span class="sxs-lookup"><span data-stu-id="fd26c-121">Continue without prompts</span></span>

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

### <span data-ttu-id="fd26c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd26c-122">-Name</span></span>
<span data-ttu-id="fd26c-123">Określ nazwę typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="fd26c-123">Specify the name of the application type</span></span>

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

### <span data-ttu-id="fd26c-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="fd26c-124">-PackageUrl</span></span>
<span data-ttu-id="fd26c-125">Określanie adresu URL pliku sfpkg pakietu aplikacji</span><span class="sxs-lookup"><span data-stu-id="fd26c-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="fd26c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd26c-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd26c-127">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd26c-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fd26c-128">-Version</span><span class="sxs-lookup"><span data-stu-id="fd26c-128">-Version</span></span>
<span data-ttu-id="fd26c-129">Określanie wersji typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="fd26c-129">Specify the application type version</span></span>

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

### <span data-ttu-id="fd26c-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd26c-130">-Confirm</span></span>
<span data-ttu-id="fd26c-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd26c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd26c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd26c-132">-WhatIf</span></span>
<span data-ttu-id="fd26c-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd26c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd26c-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd26c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd26c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd26c-135">CommonParameters</span></span>
<span data-ttu-id="fd26c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd26c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd26c-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd26c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd26c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd26c-138">INPUTS</span></span>

### <span data-ttu-id="fd26c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fd26c-139">System.String</span></span>

### <span data-ttu-id="fd26c-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd26c-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fd26c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd26c-141">OUTPUTS</span></span>

### <span data-ttu-id="fd26c-142">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fd26c-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="fd26c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd26c-143">NOTES</span></span>

## <span data-ttu-id="fd26c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd26c-144">RELATED LINKS</span></span>
