---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 8dcfe4adedd7da375e888dade108125d7899d7d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553641"
---
# <span data-ttu-id="81663-101">New-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="81663-101">New-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="81663-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81663-102">SYNOPSIS</span></span>
<span data-ttu-id="81663-103">Tworzenie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-103">Create a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81663-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81663-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Location] <String> -Publisher <String> -Offer <String> -Sku <String>
 -OsState <OperatingSystemStateTypes> -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81663-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81663-105">DESCRIPTION</span></span>
<span data-ttu-id="81663-106">Tworzenie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="81663-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81663-107">EXAMPLES</span></span>

### <span data-ttu-id="81663-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81663-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="81663-109">Tworzenie definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="81663-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81663-110">PARAMETERS</span></span>

### <span data-ttu-id="81663-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81663-111">-AsJob</span></span>
<span data-ttu-id="81663-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="81663-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81663-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81663-113">-DefaultProfile</span></span>
<span data-ttu-id="81663-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81663-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81663-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="81663-115">-Description</span></span>
<span data-ttu-id="81663-116">Opis zasobu definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="81663-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="81663-117">-DisallowedDiskType</span></span>
<span data-ttu-id="81663-118">Niedozwolone typy dysków.</span><span class="sxs-lookup"><span data-stu-id="81663-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="81663-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="81663-119">-EndOfLifeDate</span></span>
<span data-ttu-id="81663-120">Data zakończenia okresu użytkowania definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="81663-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="81663-121">— Umowa licencyjna użytkownika</span><span class="sxs-lookup"><span data-stu-id="81663-121">-Eula</span></span>
<span data-ttu-id="81663-122">Umowa licencyjna dotycząca definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="81663-123">-Gallery</span><span class="sxs-lookup"><span data-stu-id="81663-123">-GalleryName</span></span>
<span data-ttu-id="81663-124">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="81663-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="81663-125">-Location</span></span>
<span data-ttu-id="81663-126">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="81663-126">Resource location</span></span>

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

### <span data-ttu-id="81663-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="81663-127">-MaximumMemory</span></span>
<span data-ttu-id="81663-128">Maksymalnie zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="81663-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="81663-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="81663-129">-MaximumVCPU</span></span>
<span data-ttu-id="81663-130">Maksymalna liczba zalecanych rdzeni procesora</span><span class="sxs-lookup"><span data-stu-id="81663-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="81663-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="81663-131">-MinimumMemory</span></span>
<span data-ttu-id="81663-132">Minimalna zalecana pamięć</span><span class="sxs-lookup"><span data-stu-id="81663-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="81663-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="81663-133">-MinimumVCPU</span></span>
<span data-ttu-id="81663-134">Minimum zalecanego rdzenia procesora</span><span class="sxs-lookup"><span data-stu-id="81663-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="81663-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81663-135">-Name</span></span>
<span data-ttu-id="81663-136">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-136">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="81663-137">-Offer</span><span class="sxs-lookup"><span data-stu-id="81663-137">-Offer</span></span>
<span data-ttu-id="81663-138">Nazwa oferty definicji obrazu galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="81663-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="81663-139">-OsState</span></span>
<span data-ttu-id="81663-140">Stan systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="81663-140">The state of OS</span></span>

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

### <span data-ttu-id="81663-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="81663-141">-OsType</span></span>
<span data-ttu-id="81663-142">Typ systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="81663-142">The type of OS</span></span>

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

### <span data-ttu-id="81663-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="81663-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="81663-144">Identyfikator URI oświadczenia o ochronie prywatności.</span><span class="sxs-lookup"><span data-stu-id="81663-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="81663-145">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="81663-145">-Publisher</span></span>
<span data-ttu-id="81663-146">Nazwa wydawcy definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="81663-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="81663-147">-PurchasePlanName</span></span>
<span data-ttu-id="81663-148">Identyfikator planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="81663-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="81663-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="81663-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="81663-150">Identyfikator produktu dla planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="81663-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="81663-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="81663-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="81663-152">IDENTYFIKATOR wydawcy planu zakupów.</span><span class="sxs-lookup"><span data-stu-id="81663-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="81663-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="81663-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="81663-154">Identyfikator URI notatki o wersji.</span><span class="sxs-lookup"><span data-stu-id="81663-154">The release note uri.</span></span>

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

### <span data-ttu-id="81663-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81663-155">-ResourceGroupName</span></span>
<span data-ttu-id="81663-156">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="81663-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="81663-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="81663-157">-Sku</span></span>
<span data-ttu-id="81663-158">Nazwa SKU definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="81663-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="81663-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="81663-159">-Tag</span></span>
<span data-ttu-id="81663-160">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="81663-160">Resource tags</span></span>

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

### <span data-ttu-id="81663-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81663-161">-Confirm</span></span>
<span data-ttu-id="81663-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81663-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81663-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81663-163">-WhatIf</span></span>
<span data-ttu-id="81663-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81663-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81663-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81663-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81663-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81663-166">CommonParameters</span></span>
<span data-ttu-id="81663-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81663-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81663-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81663-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81663-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81663-169">INPUTS</span></span>

### <span data-ttu-id="81663-170">System. String</span><span class="sxs-lookup"><span data-stu-id="81663-170">System.String</span></span>

### <span data-ttu-id="81663-171">Microsoft. Azure. Management. COMPUTE. MODELES. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="81663-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="81663-172">Microsoft. Azure. Management. COMPUTE. MODELES. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="81663-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="81663-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="81663-173">System.DateTime</span></span>

### <span data-ttu-id="81663-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="81663-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="81663-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="81663-175">System.Int32</span></span>

### <span data-ttu-id="81663-176">System. String []</span><span class="sxs-lookup"><span data-stu-id="81663-176">System.String[]</span></span>

## <span data-ttu-id="81663-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81663-177">OUTPUTS</span></span>

### <span data-ttu-id="81663-178">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="81663-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="81663-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81663-179">NOTES</span></span>

## <span data-ttu-id="81663-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81663-180">RELATED LINKS</span></span>
