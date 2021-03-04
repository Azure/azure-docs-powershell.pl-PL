---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: d13e2e4473c390a27be4741de703818bda769efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959370"
---
# <span data-ttu-id="d164a-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d164a-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="d164a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d164a-102">SYNOPSIS</span></span>
<span data-ttu-id="d164a-103">Utwórz nową wersję typu aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="d164a-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="d164a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d164a-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d164a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d164a-105">DESCRIPTION</span></span>
<span data-ttu-id="d164a-106">To polecenie cmdlet tworzy nową wersję typu aplikacji przy użyciu pakietu określonego w pliku -PackageUrl. To powinno być dostępne za pośrednictwem punktu końcowego REST dla usługi Azure Resource Manager do użycia podczas wdrażania i zawierało aplikację spakowana i spakowana wraz z rozszerzeniem sfpkg.</span><span class="sxs-lookup"><span data-stu-id="d164a-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="d164a-107">To polecenie spowoduje utworzenie typu aplikacji, jeśli jeszcze nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="d164a-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="d164a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d164a-108">EXAMPLES</span></span>

### <span data-ttu-id="d164a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d164a-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="d164a-110">W tym przykładzie utworzysz wersję typu aplikacji "v1" pod typem "testAppType".</span><span class="sxs-lookup"><span data-stu-id="d164a-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="d164a-111">Wersja w pliku manifestu aplikacji zawarta w pakiecie powinna mieć tę samą wersję, co wersja określona w pliku -Version.</span><span class="sxs-lookup"><span data-stu-id="d164a-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="d164a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d164a-112">PARAMETERS</span></span>

### <span data-ttu-id="d164a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d164a-113">-ClusterName</span></span>
<span data-ttu-id="d164a-114">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d164a-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d164a-115">-DefaultParameters</span><span class="sxs-lookup"><span data-stu-id="d164a-115">-DefaultParameter</span></span>
<span data-ttu-id="d164a-116">Określ wartości domyślne parametrów aplikacji jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="d164a-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="d164a-117">Te parametry muszą istnieć w pliku manifestu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d164a-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="d164a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d164a-118">-DefaultProfile</span></span>
<span data-ttu-id="d164a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d164a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d164a-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d164a-120">-Force</span></span>
<span data-ttu-id="d164a-121">Kontynuuj bez monitów</span><span class="sxs-lookup"><span data-stu-id="d164a-121">Continue without prompts</span></span>

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

### <span data-ttu-id="d164a-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d164a-122">-Name</span></span>
<span data-ttu-id="d164a-123">Określanie nazwy typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="d164a-123">Specify the name of the application type</span></span>

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

### <span data-ttu-id="d164a-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="d164a-124">-PackageUrl</span></span>
<span data-ttu-id="d164a-125">Określanie adresu URL pliku sfpkg pakietu aplikacji</span><span class="sxs-lookup"><span data-stu-id="d164a-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="d164a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d164a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d164a-127">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d164a-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d164a-128">— Wersja</span><span class="sxs-lookup"><span data-stu-id="d164a-128">-Version</span></span>
<span data-ttu-id="d164a-129">Określanie wersji typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="d164a-129">Specify the application type version</span></span>

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

### <span data-ttu-id="d164a-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d164a-130">-Confirm</span></span>
<span data-ttu-id="d164a-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d164a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d164a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d164a-132">-WhatIf</span></span>
<span data-ttu-id="d164a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d164a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d164a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d164a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d164a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d164a-135">CommonParameters</span></span>
<span data-ttu-id="d164a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d164a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d164a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d164a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d164a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d164a-138">INPUTS</span></span>

### <span data-ttu-id="d164a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d164a-139">System.String</span></span>

### <span data-ttu-id="d164a-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d164a-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d164a-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d164a-141">OUTPUTS</span></span>

### <span data-ttu-id="d164a-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d164a-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="d164a-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d164a-143">NOTES</span></span>

## <span data-ttu-id="d164a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d164a-144">RELATED LINKS</span></span>
