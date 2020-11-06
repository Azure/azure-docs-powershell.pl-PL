---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552475"
---
# <span data-ttu-id="45e6d-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="45e6d-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="45e6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="45e6d-103">Dodaje nowe regiony wdrażania do wystąpienia PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="45e6d-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45e6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45e6d-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45e6d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="45e6d-106">Polecenie cmdlet **Add-AzureRmApiManagementRegion** dodaje nowe wystąpienie typu **PsApiManagementRegion** do kolekcji **AdditionalRegions** o podanym wystąpieniu typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="45e6d-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="45e6d-107">To polecenie cmdlet nie wdraża samych elementów, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="45e6d-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="45e6d-108">W celu zaktualizowania wdrożenia funkcji zarządzania interfejsem API przeszedł zmodyfikowane wystąpienie **PsApiManagement** , aby zaktualizować-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="45e6d-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="45e6d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45e6d-109">EXAMPLES</span></span>

### <span data-ttu-id="45e6d-110">Przykład 1: Dodawanie nowych regionów wdrożenia do wystąpienia PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="45e6d-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="45e6d-111">To polecenie dodaje dwie jednostki SKU Premium oraz region o nazwie wschód do **PsApiManagement** wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="45e6d-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="45e6d-112">Przykład 2: Dodawanie nowych regionów wdrażania do wystąpienia usługi PsApiManagement, a następnie aktualizowanie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="45e6d-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="45e6d-113">To polecenie pobiera obiekt **PsApiManagement** , dodaje dwie jednostki SKU Premium dla regionu o nazwie wschód USA, a następnie aktualizuje wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="45e6d-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="45e6d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45e6d-114">PARAMETERS</span></span>

### <span data-ttu-id="45e6d-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45e6d-115">-ApiManagement</span></span>
<span data-ttu-id="45e6d-116">Określa wystąpienie **PsApiManagement** , do którego są dodawane dodatkowe regiony wdrażania.</span><span class="sxs-lookup"><span data-stu-id="45e6d-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45e6d-117">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="45e6d-117">-Capacity</span></span>
<span data-ttu-id="45e6d-118">Określa pojemność jednostki składowania zapasu w obszarze wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="45e6d-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e6d-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="45e6d-119">-Location</span></span>
<span data-ttu-id="45e6d-120">Określa lokalizację nowego obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="45e6d-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="45e6d-121">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="45e6d-121">Valid values are:</span></span> 

- <span data-ttu-id="45e6d-122">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="45e6d-122">North Central US</span></span>
- <span data-ttu-id="45e6d-123">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="45e6d-123">South Central US</span></span>
- <span data-ttu-id="45e6d-124">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="45e6d-124">Central US</span></span>
- <span data-ttu-id="45e6d-125">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="45e6d-125">West Europe</span></span>
- <span data-ttu-id="45e6d-126">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="45e6d-126">North Europe</span></span>
- <span data-ttu-id="45e6d-127">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="45e6d-127">West US</span></span>
- <span data-ttu-id="45e6d-128">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="45e6d-128">East US</span></span>
- <span data-ttu-id="45e6d-129">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="45e6d-129">East US 2</span></span>
- <span data-ttu-id="45e6d-130">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="45e6d-130">Japan East</span></span>
- <span data-ttu-id="45e6d-131">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="45e6d-131">Japan West</span></span>
- <span data-ttu-id="45e6d-132">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="45e6d-132">Brazil South</span></span>
- <span data-ttu-id="45e6d-133">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="45e6d-133">Southeast Asia</span></span>
- <span data-ttu-id="45e6d-134">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="45e6d-134">East Asia</span></span>
- <span data-ttu-id="45e6d-135">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="45e6d-135">Australia East</span></span>
- <span data-ttu-id="45e6d-136">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="45e6d-136">Australia Southeast</span></span>

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

### <span data-ttu-id="45e6d-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="45e6d-137">-Sku</span></span>
<span data-ttu-id="45e6d-138">Określa poziom obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="45e6d-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="45e6d-139">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="45e6d-139">Valid values are:</span></span> 

- <span data-ttu-id="45e6d-140">Deweloper</span><span class="sxs-lookup"><span data-stu-id="45e6d-140">Developer</span></span>
- <span data-ttu-id="45e6d-141">Standard</span><span class="sxs-lookup"><span data-stu-id="45e6d-141">Standard</span></span>
- <span data-ttu-id="45e6d-142">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="45e6d-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e6d-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="45e6d-143">-VirtualNetwork</span></span>
<span data-ttu-id="45e6d-144">Określa konfigurację sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45e6d-144">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e6d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e6d-145">-DefaultProfile</span></span>
<span data-ttu-id="45e6d-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45e6d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45e6d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e6d-147">CommonParameters</span></span>
<span data-ttu-id="45e6d-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e6d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e6d-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45e6d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e6d-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45e6d-150">INPUTS</span></span>

### <span data-ttu-id="45e6d-151">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="45e6d-151">PsApiManagement</span></span>
<span data-ttu-id="45e6d-152">Parametr "ApiManagement" akceptuje wartość typu "PsApiManagement" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="45e6d-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="45e6d-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45e6d-153">OUTPUTS</span></span>

### <span data-ttu-id="45e6d-154">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="45e6d-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="45e6d-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45e6d-155">NOTES</span></span>
* <span data-ttu-id="45e6d-156">Polecenie cmdlet zapisuje zaktualizowaną instancję **PsApiManagement** w potoku.</span><span class="sxs-lookup"><span data-stu-id="45e6d-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="45e6d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45e6d-157">RELATED LINKS</span></span>

[<span data-ttu-id="45e6d-158">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="45e6d-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="45e6d-159">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="45e6d-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="45e6d-160">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="45e6d-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


