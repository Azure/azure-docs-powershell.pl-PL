---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185778"
---
# <span data-ttu-id="977b7-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="977b7-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="977b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="977b7-102">SYNOPSIS</span></span>
<span data-ttu-id="977b7-103">Tworzenie szablonu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="977b7-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="977b7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="977b7-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="977b7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="977b7-105">DESCRIPTION</span></span>
<span data-ttu-id="977b7-106">Tworzenie szablonu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="977b7-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="977b7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="977b7-107">EXAMPLES</span></span>

### <span data-ttu-id="977b7-108">Przykład 1. Tworzenie szablonu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="977b7-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="977b7-109">Te polecenia tworzą szablon obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="977b7-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="977b7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="977b7-110">PARAMETERS</span></span>

### <span data-ttu-id="977b7-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="977b7-111">-AsJob</span></span>
<span data-ttu-id="977b7-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="977b7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="977b7-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="977b7-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="977b7-114">Maksymalny czas oczekiwania podczas tworzenia szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="977b7-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="977b7-115">Pomiń lub określ wartość 0, aby użyć wartości domyślnej (4 godziny).</span><span class="sxs-lookup"><span data-stu-id="977b7-115">Omit or specify 0 to use the default (4 hours).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-116">— Dostosuj</span><span class="sxs-lookup"><span data-stu-id="977b7-116">-Customize</span></span>
<span data-ttu-id="977b7-117">Określa właściwości używane do opisywania kroków dostosowywania obrazu, takie jak źródło obrazów itp. Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje na temat dostosowywania właściwości i tworzenia tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="977b7-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977b7-118">-DefaultProfile</span></span>
<span data-ttu-id="977b7-119">region HideParameters Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="977b7-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-120">— Rozpowszechnij</span><span class="sxs-lookup"><span data-stu-id="977b7-120">-Distribute</span></span>
<span data-ttu-id="977b7-121">Cele rozkładu, do którego trzeba przejść do wyniku obrazu.</span><span class="sxs-lookup"><span data-stu-id="977b7-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="977b7-122">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach DISTRIBUTE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="977b7-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="977b7-123">-ImageTemplateName</span></span>
<span data-ttu-id="977b7-124">Nazwa szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="977b7-124">The name of the image Template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="977b7-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="977b7-126">Godzina zakończenia ostatniego uruchomienia (UTC).</span><span class="sxs-lookup"><span data-stu-id="977b7-126">End time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="977b7-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="977b7-128">Pełne informacje o stanie ostatniego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="977b7-128">Verbose information about the last run state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="977b7-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="977b7-130">Stan ostatniego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="977b7-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="977b7-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="977b7-132">Stan podrzędny ostatniego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="977b7-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="977b7-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="977b7-134">Godzina rozpoczęcia ostatniego uruchomienia (UTC).</span><span class="sxs-lookup"><span data-stu-id="977b7-134">Start time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="977b7-135">-Location</span></span>
<span data-ttu-id="977b7-136">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="977b7-136">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="977b7-137">-NoWait</span></span>
<span data-ttu-id="977b7-138">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="977b7-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="977b7-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="977b7-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="977b7-140">Kod błędu błędu inicjowania obsługi administracyjnej.</span><span class="sxs-lookup"><span data-stu-id="977b7-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="977b7-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="977b7-142">Pełny komunikat o błędzie dotyczący błędu inicjowania obsługi administracyjnej.</span><span class="sxs-lookup"><span data-stu-id="977b7-142">Verbose error message about the provisioning failure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="977b7-143">-ResourceGroupName</span></span>
<span data-ttu-id="977b7-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="977b7-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-145">— Źródło</span><span class="sxs-lookup"><span data-stu-id="977b7-145">-Source</span></span>
<span data-ttu-id="977b7-146">W tym artykule opisano źródło obrazów maszyn wirtualnych do tworzenia, dostosowywania i rozpowszechniania.</span><span class="sxs-lookup"><span data-stu-id="977b7-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="977b7-147">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach źródła i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="977b7-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-148">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="977b7-148">-SubscriptionId</span></span>
<span data-ttu-id="977b7-149">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="977b7-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-150">— Tag</span><span class="sxs-lookup"><span data-stu-id="977b7-150">-Tag</span></span>
<span data-ttu-id="977b7-151">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="977b7-151">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="977b7-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="977b7-153">Identyfikator przypisanej tożsamości użytkownika.</span><span class="sxs-lookup"><span data-stu-id="977b7-153">The id of user assigned identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-154">-VMProfileOssizeInGb</span><span class="sxs-lookup"><span data-stu-id="977b7-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="977b7-155">Rozmiar dysku systemu operacyjnego w GB.</span><span class="sxs-lookup"><span data-stu-id="977b7-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="977b7-156">Pomiń lub określ wartość 0, aby użyć domyślnego rozmiaru dysku systemu operacyjnego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="977b7-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="977b7-157">-VMProfileVmSize</span></span>
<span data-ttu-id="977b7-158">Rozmiar maszyny wirtualnej używanej do tworzenia, dostosowywania i przechwytywania obrazów.</span><span class="sxs-lookup"><span data-stu-id="977b7-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="977b7-159">Pomiń lub określ pusty ciąg, aby użyć domyślnego (Standard_D1_v2).</span><span class="sxs-lookup"><span data-stu-id="977b7-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="977b7-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="977b7-161">Identyfikator zasobu istniejącej podsieci.</span><span class="sxs-lookup"><span data-stu-id="977b7-161">Resource id of a pre-existing subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977b7-162">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="977b7-162">-Confirm</span></span>
<span data-ttu-id="977b7-163">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="977b7-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="977b7-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="977b7-164">-WhatIf</span></span>
<span data-ttu-id="977b7-165">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="977b7-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="977b7-166">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="977b7-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="977b7-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977b7-167">CommonParameters</span></span>
<span data-ttu-id="977b7-168">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="977b7-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977b7-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="977b7-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977b7-170">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="977b7-170">INPUTS</span></span>

## <span data-ttu-id="977b7-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="977b7-171">OUTPUTS</span></span>

### <span data-ttu-id="977b7-172">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="977b7-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="977b7-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="977b7-173">NOTES</span></span>

<span data-ttu-id="977b7-174">ALIASY</span><span class="sxs-lookup"><span data-stu-id="977b7-174">ALIASES</span></span>

<span data-ttu-id="977b7-175">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="977b7-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="977b7-176">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="977b7-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="977b7-177">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="977b7-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="977b7-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Określa właściwości używane do opisywania kroków dostosowywania obrazu, takie jak źródło obrazów itp.</span><span class="sxs-lookup"><span data-stu-id="977b7-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="977b7-179">`Type <String>`: typ narzędzia do dostosowywania, którego chcesz użyć na obrazie.</span><span class="sxs-lookup"><span data-stu-id="977b7-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="977b7-180">Na przykład "Shell" może być dostosowywanie powłoki</span><span class="sxs-lookup"><span data-stu-id="977b7-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="977b7-181">`[Name <String>]`: przyjazna nazwa w celu zapewnienia kontekstu na temat czynności w tym kroku dostosowywania</span><span class="sxs-lookup"><span data-stu-id="977b7-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="977b7-182">DISTRIBUTE <IImageTemplateDistributor[]>: miejsce docelowe rozkładu, do którego ma trafić dane wyjściowe obrazu.</span><span class="sxs-lookup"><span data-stu-id="977b7-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="977b7-183">`RunOutputName <String>`: Nazwa, która ma być używana dla skojarzonego RunOutput.</span><span class="sxs-lookup"><span data-stu-id="977b7-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="977b7-184">`Type <String>`: typ rozkładu.</span><span class="sxs-lookup"><span data-stu-id="977b7-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="977b7-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tagi, które zostaną zastosowane do artefaktu po jego utworzeniu/zaktualizowaniu przez dystrybutora.</span><span class="sxs-lookup"><span data-stu-id="977b7-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="977b7-186">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="977b7-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="977b7-187">ŹRÓDŁO: W tym artykule opisano źródło obrazów maszyn wirtualnych do <IImageTemplateSource> tworzenia, dostosowywania i rozpowszechniania.</span><span class="sxs-lookup"><span data-stu-id="977b7-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="977b7-188">`Type <String>`: określa typ obrazu źródłowego, od którego chcesz zacząć.</span><span class="sxs-lookup"><span data-stu-id="977b7-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="977b7-189">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="977b7-189">RELATED LINKS</span></span>

