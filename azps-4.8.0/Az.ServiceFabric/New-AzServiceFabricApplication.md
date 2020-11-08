---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063195"
---
# <span data-ttu-id="15f43-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="15f43-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="15f43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15f43-102">SYNOPSIS</span></span>
<span data-ttu-id="15f43-103">Utwórz nową aplikację sieci szkieletowej usługi w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="15f43-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="15f43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15f43-104">SYNTAX</span></span>

### <span data-ttu-id="15f43-105">SkipAppTypeVersion (domyślny)</span><span class="sxs-lookup"><span data-stu-id="15f43-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15f43-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="15f43-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15f43-107">Opis</span><span class="sxs-lookup"><span data-stu-id="15f43-107">DESCRIPTION</span></span>
<span data-ttu-id="15f43-108">To polecenie cmdlet tworzy nową aplikację do obsługi sieci szkieletowej w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="15f43-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="15f43-109">Za pomocą parametru-PackageUrl można utworzyć wersję typu, jeśli wersja typu została zamknięta, ale jej stan w stanie niepowodzenia, w tym poleceniu cmdlet zostanie wyświetlony monit z pytaniem, czy użytkownik chce ponownie utworzyć wersję typu.</span><span class="sxs-lookup"><span data-stu-id="15f43-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="15f43-110">Jeśli ta operacja będzie kontynuowana w stanie niepowodzenia, polecenie zatrzyma proces i Zgłoś wyjątek.</span><span class="sxs-lookup"><span data-stu-id="15f43-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="15f43-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15f43-111">EXAMPLES</span></span>

### <span data-ttu-id="15f43-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15f43-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="15f43-113">W tym przykładzie zostanie utworzona aplikacja "testApp" w grupie zasobów "testRG" i klastrze "testCluster".</span><span class="sxs-lookup"><span data-stu-id="15f43-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="15f43-114">Typ aplikacji "TestAppType" w wersji "v1" powinien już istnieć w klastrze, a parametry aplikacji powinny być zdefiniowane w manifeście aplikacji w przeciwnym razie polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="15f43-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="15f43-115">Przykład 2: Określ-PackageUrl, aby utworzyć wersję typu aplikacji przed utworzeniem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="15f43-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="15f43-116">W tym przykładzie jest tworzony typ aplikacji "TestAppType" w wersji V1 przy użyciu podanego adresu URL pakietu.</span><span class="sxs-lookup"><span data-stu-id="15f43-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="15f43-117">Po wykonaniu tej czynności normalny proces tworzenia aplikacji będzie kontynuowany.</span><span class="sxs-lookup"><span data-stu-id="15f43-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="15f43-118">Jeśli wersja typu aplikacji jest już ZAMKNIĘTA, a stan inicjowania obsługi jest wyświetlany w stanie niepowodzenia, zostanie wyświetlony monit o określenie, czy użytkownik chce ponownie utworzyć wersję typu.</span><span class="sxs-lookup"><span data-stu-id="15f43-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="15f43-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15f43-119">PARAMETERS</span></span>

### <span data-ttu-id="15f43-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="15f43-120">-ApplicationParameter</span></span>
<span data-ttu-id="15f43-121">Określ parametry aplikacji jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="15f43-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="15f43-122">Te parametry muszą istnieć w manifeście aplikacji.</span><span class="sxs-lookup"><span data-stu-id="15f43-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="15f43-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="15f43-123">-ApplicationTypeName</span></span>
<span data-ttu-id="15f43-124">Określ nazwę typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="15f43-124">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f43-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="15f43-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="15f43-126">Określanie wersji typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="15f43-126">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f43-127">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="15f43-127">-ClusterName</span></span>
<span data-ttu-id="15f43-128">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="15f43-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="15f43-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f43-129">-DefaultProfile</span></span>
<span data-ttu-id="15f43-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15f43-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15f43-131">-Force</span><span class="sxs-lookup"><span data-stu-id="15f43-131">-Force</span></span>
<span data-ttu-id="15f43-132">Kontynuuj bez monitowania</span><span class="sxs-lookup"><span data-stu-id="15f43-132">Continue without prompts</span></span>

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

### <span data-ttu-id="15f43-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="15f43-133">-MaximumNodeCount</span></span>
<span data-ttu-id="15f43-134">Określa maksymalną liczbę węzłów, na których ma zostać umieszczona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="15f43-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f43-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="15f43-135">-MinimumNodeCount</span></span>
<span data-ttu-id="15f43-136">Określa minimalną liczbę węzłów, w których program Service Fabric rezerwuje wydajność dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="15f43-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f43-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="15f43-137">-Name</span></span>
<span data-ttu-id="15f43-138">Określanie nazwy aplikacji</span><span class="sxs-lookup"><span data-stu-id="15f43-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f43-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="15f43-139">-PackageUrl</span></span>
<span data-ttu-id="15f43-140">Określanie adresu URL pliku sfpkg pakietu aplikacji</span><span class="sxs-lookup"><span data-stu-id="15f43-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15f43-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15f43-141">-ResourceGroupName</span></span>
<span data-ttu-id="15f43-142">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="15f43-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="15f43-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15f43-143">-Confirm</span></span>
<span data-ttu-id="15f43-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15f43-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15f43-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15f43-145">-WhatIf</span></span>
<span data-ttu-id="15f43-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15f43-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15f43-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15f43-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15f43-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f43-148">CommonParameters</span></span>
<span data-ttu-id="15f43-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15f43-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f43-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15f43-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f43-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15f43-151">INPUTS</span></span>

### <span data-ttu-id="15f43-152">System. String</span><span class="sxs-lookup"><span data-stu-id="15f43-152">System.String</span></span>

### <span data-ttu-id="15f43-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="15f43-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="15f43-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15f43-154">OUTPUTS</span></span>

### <span data-ttu-id="15f43-155">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="15f43-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="15f43-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15f43-156">NOTES</span></span>

## <span data-ttu-id="15f43-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15f43-157">RELATED LINKS</span></span>
