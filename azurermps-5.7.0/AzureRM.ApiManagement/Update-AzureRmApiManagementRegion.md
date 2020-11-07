---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: d6c97ac0fc948ba3ee4f86a2e657a1386c693f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718511"
---
# <span data-ttu-id="ccbf3-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ccbf3-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="ccbf3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccbf3-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbf3-103">Aktualizuje istniejący region wdrożenia w wystąpieniu PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccbf3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccbf3-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccbf3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ccbf3-105">DESCRIPTION</span></span>
<span data-ttu-id="ccbf3-106">Polecenie cmdlet **Update-AzureRmApiManagementRegion** aktualizuje istniejące wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** w kolekcji obiektów **AdditionalRegions** udostępnionego wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="ccbf3-107">To polecenie cmdlet nie rozmieszcza żadnych elementów, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="ccbf3-108">Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, użyj zmodyfikowanego **PsApiManagementInstance** do polecenia cmdlet Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="ccbf3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccbf3-109">EXAMPLES</span></span>

## <span data-ttu-id="ccbf3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccbf3-110">PARAMETERS</span></span>

### <span data-ttu-id="ccbf3-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ccbf3-111">-ApiManagement</span></span>
<span data-ttu-id="ccbf3-112">Umożliwia określenie wystąpienia **PsApiManagement** , w którym ma zostać zaktualizowany istniejący region wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf3-113">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="ccbf3-113">-Capacity</span></span>
<span data-ttu-id="ccbf3-114">Określa nową wartość pojemności jednostki SKU dla obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbf3-115">-DefaultProfile</span></span>
<span data-ttu-id="ccbf3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf3-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ccbf3-117">-Location</span></span>
<span data-ttu-id="ccbf3-118">Określa lokalizację obszaru wdrożenia, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-118">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="ccbf3-119">Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="ccbf3-120">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="ccbf3-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf3-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="ccbf3-121">-Sku</span></span>
<span data-ttu-id="ccbf3-122">Określa nową wartość warstwy obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-122">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="ccbf3-123">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ccbf3-123">Valid values are:</span></span>

- <span data-ttu-id="ccbf3-124">Deweloper</span><span class="sxs-lookup"><span data-stu-id="ccbf3-124">Developer</span></span>
- <span data-ttu-id="ccbf3-125">Standard</span><span class="sxs-lookup"><span data-stu-id="ccbf3-125">Standard</span></span>
- <span data-ttu-id="ccbf3-126">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="ccbf3-126">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf3-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ccbf3-127">-VirtualNetwork</span></span>
<span data-ttu-id="ccbf3-128">Określa konfigurację sieci wirtualnej dla obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="ccbf3-129">Przekazanie $null spowoduje usunięcie konfiguracji sieci wirtualnej dla tego regionu.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-129">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccbf3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbf3-130">CommonParameters</span></span>
<span data-ttu-id="ccbf3-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbf3-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbf3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbf3-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccbf3-133">INPUTS</span></span>

### <span data-ttu-id="ccbf3-134">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ccbf3-134">PsApiManagement</span></span>
<span data-ttu-id="ccbf3-135">Parametr "ApiManagement" akceptuje wartość typu "PsApiManagement" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ccbf3-135">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="ccbf3-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccbf3-136">OUTPUTS</span></span>

### <span data-ttu-id="ccbf3-137">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ccbf3-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ccbf3-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccbf3-138">NOTES</span></span>

## <span data-ttu-id="ccbf3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccbf3-139">RELATED LINKS</span></span>

[<span data-ttu-id="ccbf3-140">Dodaj-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ccbf3-140">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="ccbf3-141">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ccbf3-141">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="ccbf3-142">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ccbf3-142">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
