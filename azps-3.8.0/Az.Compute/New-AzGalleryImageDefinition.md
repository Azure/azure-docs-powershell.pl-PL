---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049530"
---
# <span data-ttu-id="8ae7c-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="8ae7c-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="8ae7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ae7c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae7c-103">Tworzenie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="8ae7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ae7c-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ae7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8ae7c-105">DESCRIPTION</span></span>
<span data-ttu-id="8ae7c-106">Tworzenie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="8ae7c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ae7c-107">EXAMPLES</span></span>

### <span data-ttu-id="8ae7c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ae7c-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="8ae7c-109">Tworzenie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="8ae7c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ae7c-110">PARAMETERS</span></span>

### <span data-ttu-id="8ae7c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ae7c-111">-AsJob</span></span>
<span data-ttu-id="8ae7c-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8ae7c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ae7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae7c-113">-DefaultProfile</span></span>
<span data-ttu-id="8ae7c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ae7c-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="8ae7c-115">-Description</span></span>
<span data-ttu-id="8ae7c-116">Opis zasobu definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-116">The description of the gallery image Definition resource.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="8ae7c-117">-DisallowedDiskType</span></span>
<span data-ttu-id="8ae7c-118">Niedozwolone typy dysków.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-118">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="8ae7c-119">-EndOfLifeDate</span></span>
<span data-ttu-id="8ae7c-120">Data zakończenia okresu użytkowania definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="8ae7c-120">The end of life date of the gallery Image Definition</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-121">— Umowa licencyjna użytkownika</span><span class="sxs-lookup"><span data-stu-id="8ae7c-121">-Eula</span></span>
<span data-ttu-id="8ae7c-122">Umowa licencyjna dotycząca definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-122">The Eula agreement for the gallery Image Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-123">-Gallery</span><span class="sxs-lookup"><span data-stu-id="8ae7c-123">-GalleryName</span></span>
<span data-ttu-id="8ae7c-124">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="8ae7c-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="8ae7c-125">-HyperVGeneration</span></span>
<span data-ttu-id="8ae7c-126">Generowanie funkcji hypervisor maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="8ae7c-127">Dotyczy tylko dysków z systemem operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="8ae7c-128">Dozwolone wartości to V1 i v2.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-128">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8ae7c-129">-Location</span></span>
<span data-ttu-id="8ae7c-130">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="8ae7c-130">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="8ae7c-131">-MaximumMemory</span></span>
<span data-ttu-id="8ae7c-132">Maksymalnie zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="8ae7c-132">The maximum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="8ae7c-133">-MaximumVCPU</span></span>
<span data-ttu-id="8ae7c-134">Maksymalna liczba zalecanych rdzeni procesora</span><span class="sxs-lookup"><span data-stu-id="8ae7c-134">The maximum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="8ae7c-135">-MinimumMemory</span></span>
<span data-ttu-id="8ae7c-136">Minimalna zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="8ae7c-136">The minimum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="8ae7c-137">-MinimumVCPU</span></span>
<span data-ttu-id="8ae7c-138">Minimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="8ae7c-138">The minimum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ae7c-139">-Name</span></span>
<span data-ttu-id="8ae7c-140">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-140">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-141">-Offer</span><span class="sxs-lookup"><span data-stu-id="8ae7c-141">-Offer</span></span>
<span data-ttu-id="8ae7c-142">Nazwa oferty definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="8ae7c-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="8ae7c-143">-OsState</span></span>
<span data-ttu-id="8ae7c-144">Stan systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="8ae7c-144">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="8ae7c-145">-OsType</span></span>
<span data-ttu-id="8ae7c-146">Typ systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="8ae7c-146">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="8ae7c-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="8ae7c-148">Identyfikator URI oświadczenia o ochronie prywatności.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-148">The privacy statement uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-149">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="8ae7c-149">-Publisher</span></span>
<span data-ttu-id="8ae7c-150">Nazwa wydawcy definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="8ae7c-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="8ae7c-151">-PurchasePlanName</span></span>
<span data-ttu-id="8ae7c-152">Identyfikator planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-152">The ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="8ae7c-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="8ae7c-154">Identyfikator produktu dla planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-154">The product ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="8ae7c-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="8ae7c-156">IDENTYFIKATOR wydawcy planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-156">The publisher ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="8ae7c-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="8ae7c-158">Identyfikator URI notatki o wersji.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-158">The release note uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7c-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae7c-159">-ResourceGroupName</span></span>
<span data-ttu-id="8ae7c-160">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="8ae7c-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="8ae7c-161">-Sku</span></span>
<span data-ttu-id="8ae7c-162">Nazwa SKU definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="8ae7c-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="8ae7c-163">-Tag</span></span>
<span data-ttu-id="8ae7c-164">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="8ae7c-164">Resource tags</span></span>

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

### <span data-ttu-id="8ae7c-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ae7c-165">-Confirm</span></span>
<span data-ttu-id="8ae7c-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae7c-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae7c-167">-WhatIf</span></span>
<span data-ttu-id="8ae7c-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ae7c-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae7c-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae7c-170">CommonParameters</span></span>
<span data-ttu-id="8ae7c-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ae7c-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae7c-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ae7c-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae7c-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ae7c-173">INPUTS</span></span>

### <span data-ttu-id="8ae7c-174">System. String</span><span class="sxs-lookup"><span data-stu-id="8ae7c-174">System.String</span></span>

### <span data-ttu-id="8ae7c-175">Microsoft. Azure. Management. COMPUTE. MODELES. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="8ae7c-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="8ae7c-176">Microsoft. Azure. Management. COMPUTE. MODELES. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="8ae7c-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="8ae7c-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="8ae7c-177">System.DateTime</span></span>

### <span data-ttu-id="8ae7c-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8ae7c-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8ae7c-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8ae7c-179">System.Int32</span></span>

### <span data-ttu-id="8ae7c-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="8ae7c-180">System.String[]</span></span>

## <span data-ttu-id="8ae7c-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ae7c-181">OUTPUTS</span></span>

### <span data-ttu-id="8ae7c-182">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="8ae7c-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="8ae7c-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ae7c-183">NOTES</span></span>

## <span data-ttu-id="8ae7c-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ae7c-184">RELATED LINKS</span></span>
