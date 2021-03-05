---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: e1e6efbdeaed90fe7591ed2dd5a645955dd5a314
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982161"
---
# <span data-ttu-id="ff416-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ff416-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="ff416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff416-102">SYNOPSIS</span></span>
<span data-ttu-id="ff416-103">Utwórz nową aplikację szkieletową usług w ramach określonej grupy zasobów i klastrów.</span><span class="sxs-lookup"><span data-stu-id="ff416-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="ff416-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff416-104">SYNTAX</span></span>

### <span data-ttu-id="ff416-105">SkipAppTypeVersion (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ff416-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff416-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff416-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff416-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff416-107">DESCRIPTION</span></span>
<span data-ttu-id="ff416-108">To polecenie cmdlet tworzy nową aplikację szkieletową usługi w ramach określonej grupy zasobów i klastru.</span><span class="sxs-lookup"><span data-stu-id="ff416-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="ff416-109">Parametr -PackageUrl może zostać użyty do utworzenia wersji typu. Jeśli wersja typu już zakończy działanie, ale jest w stanie "Niepowodzenie", polecenie cmdlet zapyta, czy użytkownik chce ponownie utworzyć wersję typu.</span><span class="sxs-lookup"><span data-stu-id="ff416-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="ff416-110">Jeśli proces będzie kontynuowany w stanie "Niepowodzenie", polecenie zatrzyma proces i zgłasza wyjątek.</span><span class="sxs-lookup"><span data-stu-id="ff416-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="ff416-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff416-111">EXAMPLES</span></span>

### <span data-ttu-id="ff416-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ff416-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="ff416-113">W tym przykładzie aplikacja "testApp" jest skojrzana z grupą zasobów "testRG" i klaster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="ff416-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="ff416-114">Typ aplikacji "TestAppType" wersja "v1" powinien już istnieć w klastrze, a parametry aplikacji powinny być zdefiniowane w manifestie aplikacji w przeciwnym razie polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ff416-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="ff416-115">Przykład 2. Określanie wartości -PackageUrl w celu utworzenia wersji typu aplikacji przed utworzeniem aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff416-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="ff416-116">W tym przykładzie jest tworzenie typu aplikacji "TestAppType" w wersji "v1" przy użyciu podanego adresu URL pakietu.</span><span class="sxs-lookup"><span data-stu-id="ff416-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="ff416-117">Następnie będzie kontynuowany normalny proces tworzenia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff416-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="ff416-118">Jeśli wersja typu aplikacji zakończy się już i stan inicjowania obsługi administracyjnej w stanie "Nie powiodło się", zostanie wyświetlony monit o podjęcie decyzji, czy użytkownik chce ponownie utworzyć wersję typu.</span><span class="sxs-lookup"><span data-stu-id="ff416-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="ff416-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff416-119">PARAMETERS</span></span>

### <span data-ttu-id="ff416-120">-ApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="ff416-120">-ApplicationParameter</span></span>
<span data-ttu-id="ff416-121">Określ parametry aplikacji jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="ff416-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="ff416-122">Te parametry muszą istnieć w pliku manifestu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff416-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="ff416-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="ff416-123">-ApplicationTypeName</span></span>
<span data-ttu-id="ff416-124">Określanie nazwy typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="ff416-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="ff416-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff416-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="ff416-126">Określanie wersji typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="ff416-126">Specify the application type version</span></span>

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

### <span data-ttu-id="ff416-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ff416-127">-ClusterName</span></span>
<span data-ttu-id="ff416-128">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="ff416-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ff416-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff416-129">-DefaultProfile</span></span>
<span data-ttu-id="ff416-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff416-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff416-131">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ff416-131">-Force</span></span>
<span data-ttu-id="ff416-132">Kontynuuj bez monitów</span><span class="sxs-lookup"><span data-stu-id="ff416-132">Continue without prompts</span></span>

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

### <span data-ttu-id="ff416-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="ff416-133">-MaximumNodeCount</span></span>
<span data-ttu-id="ff416-134">Określa maksymalną liczbę węzłów, w których ma być umieszczana aplikacja.</span><span class="sxs-lookup"><span data-stu-id="ff416-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="ff416-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="ff416-135">-MinimumNodeCount</span></span>
<span data-ttu-id="ff416-136">Określa minimalną liczbę węzłów, w których usługa Service Fabric będzie rezerwować pojemność dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff416-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="ff416-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ff416-137">-Name</span></span>
<span data-ttu-id="ff416-138">Określanie nazwy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ff416-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="ff416-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="ff416-139">-PackageUrl</span></span>
<span data-ttu-id="ff416-140">Określanie adresu URL pliku sfpkg pakietu aplikacji</span><span class="sxs-lookup"><span data-stu-id="ff416-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="ff416-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff416-141">-ResourceGroupName</span></span>
<span data-ttu-id="ff416-142">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff416-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ff416-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff416-143">-Confirm</span></span>
<span data-ttu-id="ff416-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ff416-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff416-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff416-145">-WhatIf</span></span>
<span data-ttu-id="ff416-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff416-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff416-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ff416-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff416-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff416-148">CommonParameters</span></span>
<span data-ttu-id="ff416-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff416-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff416-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff416-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff416-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff416-151">INPUTS</span></span>

### <span data-ttu-id="ff416-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ff416-152">System.String</span></span>

### <span data-ttu-id="ff416-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff416-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ff416-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff416-154">OUTPUTS</span></span>

### <span data-ttu-id="ff416-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="ff416-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ff416-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff416-156">NOTES</span></span>

## <span data-ttu-id="ff416-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff416-157">RELATED LINKS</span></span>
