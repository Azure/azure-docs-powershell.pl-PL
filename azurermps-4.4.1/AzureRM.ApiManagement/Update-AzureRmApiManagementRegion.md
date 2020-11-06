---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525734"
---
# <span data-ttu-id="3f098-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3f098-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="3f098-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f098-102">SYNOPSIS</span></span>
<span data-ttu-id="3f098-103">Aktualizuje istniejący region wdrożenia w wystąpieniu PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3f098-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f098-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f098-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f098-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f098-105">DESCRIPTION</span></span>
<span data-ttu-id="3f098-106">Polecenie cmdlet **Update-AzureRmApiManagementRegion** aktualizuje istniejące wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** w kolekcji obiektów **AdditionalRegions** udostępnionego wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="3f098-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="3f098-107">To polecenie cmdlet nie rozmieszcza żadnych elementów, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="3f098-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="3f098-108">Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, użyj zmodyfikowanego **PsApiManagementInstance** do polecenia cmdlet Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="3f098-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="3f098-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f098-109">EXAMPLES</span></span>

## <span data-ttu-id="3f098-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f098-110">PARAMETERS</span></span>

### <span data-ttu-id="3f098-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f098-111">-ApiManagement</span></span>
<span data-ttu-id="3f098-112">Umożliwia określenie wystąpienia **PsApiManagement** , w którym ma zostać zaktualizowany istniejący region wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3f098-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="3f098-113">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="3f098-113">-Capacity</span></span>
<span data-ttu-id="3f098-114">Określa nową wartość pojemności jednostki SKU dla obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3f098-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f098-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3f098-115">-Location</span></span>
<span data-ttu-id="3f098-116">Określa lokalizację obszaru wdrożenia, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="3f098-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="3f098-117">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3f098-117">Valid values are:</span></span>

- <span data-ttu-id="3f098-118">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="3f098-118">North Central US</span></span>
- <span data-ttu-id="3f098-119">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="3f098-119">South Central US</span></span>
- <span data-ttu-id="3f098-120">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="3f098-120">Central US</span></span>
- <span data-ttu-id="3f098-121">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="3f098-121">West Europe</span></span>
- <span data-ttu-id="3f098-122">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="3f098-122">North Europe</span></span>
- <span data-ttu-id="3f098-123">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="3f098-123">West US</span></span>
- <span data-ttu-id="3f098-124">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="3f098-124">East US</span></span>
- <span data-ttu-id="3f098-125">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="3f098-125">East US 2</span></span>
- <span data-ttu-id="3f098-126">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="3f098-126">Japan East</span></span>
- <span data-ttu-id="3f098-127">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="3f098-127">Japan West</span></span>
- <span data-ttu-id="3f098-128">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="3f098-128">Brazil South</span></span>
- <span data-ttu-id="3f098-129">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="3f098-129">Southeast Asia</span></span>
- <span data-ttu-id="3f098-130">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="3f098-130">East Asia</span></span>
- <span data-ttu-id="3f098-131">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="3f098-131">Australia East</span></span>
- <span data-ttu-id="3f098-132">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="3f098-132">Australia Southeast</span></span>

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

### <span data-ttu-id="3f098-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="3f098-133">-Sku</span></span>
<span data-ttu-id="3f098-134">Określa nową wartość warstwy obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3f098-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="3f098-135">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3f098-135">Valid values are:</span></span>

- <span data-ttu-id="3f098-136">Deweloper</span><span class="sxs-lookup"><span data-stu-id="3f098-136">Developer</span></span>
- <span data-ttu-id="3f098-137">Standard</span><span class="sxs-lookup"><span data-stu-id="3f098-137">Standard</span></span>
- <span data-ttu-id="3f098-138">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="3f098-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f098-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3f098-139">-VirtualNetwork</span></span>
<span data-ttu-id="3f098-140">Określa konfigurację sieci wirtualnej dla obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3f098-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="3f098-141">Przekazanie $null spowoduje usunięcie konfiguracji sieci wirtualnej dla tego regionu.</span><span class="sxs-lookup"><span data-stu-id="3f098-141">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f098-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f098-142">-DefaultProfile</span></span>
<span data-ttu-id="3f098-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f098-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f098-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f098-144">CommonParameters</span></span>
<span data-ttu-id="3f098-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f098-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f098-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f098-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f098-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f098-147">INPUTS</span></span>

### <span data-ttu-id="3f098-148">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f098-148">PsApiManagement</span></span>
<span data-ttu-id="3f098-149">Parametr "ApiManagement" akceptuje wartość typu "PsApiManagement" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3f098-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="3f098-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f098-150">OUTPUTS</span></span>

### <span data-ttu-id="3f098-151">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f098-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3f098-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f098-152">NOTES</span></span>

## <span data-ttu-id="3f098-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f098-153">RELATED LINKS</span></span>

[<span data-ttu-id="3f098-154">Dodaj-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3f098-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="3f098-155">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3f098-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="3f098-156">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="3f098-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
