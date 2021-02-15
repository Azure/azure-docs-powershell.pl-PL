---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 3f9c88177d3f791acdd0be5c81eec2fb5bc6911c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400709"
---
# <span data-ttu-id="dcaa0-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="dcaa0-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="dcaa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcaa0-102">SYNOPSIS</span></span>
<span data-ttu-id="dcaa0-103">Aktualizuje istniejący region wdrażania w wystąpieniu programu PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="dcaa0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dcaa0-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcaa0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dcaa0-105">DESCRIPTION</span></span>
<span data-ttu-id="dcaa0-106">Polecenie cmdlet **Update-AzApiManagementRegion** aktualizuje istniejące wystąpienie typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** w zbiorze **obiektów AdditionalRegions** o dostarczonym wystąpieniu typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="dcaa0-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="dcaa0-107">To polecenie cmdlet nie wdraża niczego, ale aktualizuje wystąpienie programu **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="dcaa0-108">Aby zaktualizować wdrożenie zarządzania interfejsem API, użyj zmodyfikowanego polecenia **cmdlet PsApiManagementInstance** Set-AzApiManagement cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="dcaa0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dcaa0-109">EXAMPLES</span></span>

### <span data-ttu-id="dcaa0-110">Przykład 1. Zwiększenie pojemności dodatkowego regionu w wystąpieniu programu PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcaa0-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="dcaa0-111">To polecenie otrzymuje usługę SKU API Management Premium z regionami w południowo-środkowych Stanów Zjednoczonych i Północno-Środkowych Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="dcaa0-112">Następnie zwiększa wydajność regionu Północno-Środkowych Stanów Zjednoczonych do 2 przy użyciu **update-azApiManagementRegion.**</span><span class="sxs-lookup"><span data-stu-id="dcaa0-112">It then increases the Capacity of the North Central US region to 2 using the **Update-AzApiManagementRegion**.</span></span> <span data-ttu-id="dcaa0-113">Następne polecenie cmdlet Set-AzApiManagement zmiany konfiguracji do usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-113">The next cmdlet Set-AzApiManagement applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="dcaa0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcaa0-114">PARAMETERS</span></span>

### <span data-ttu-id="dcaa0-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcaa0-115">-ApiManagement</span></span>
<span data-ttu-id="dcaa0-116">Określa wystąpienie **PsApiManagement,** w przypadku których ma być aktualizowane istniejący region wdrażania.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="dcaa0-117">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="dcaa0-117">-Capacity</span></span>
<span data-ttu-id="dcaa0-118">Określa nową wartość pojemności SKU dla regionu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="dcaa0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcaa0-119">-DefaultProfile</span></span>
<span data-ttu-id="dcaa0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcaa0-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dcaa0-121">-Location</span></span>
<span data-ttu-id="dcaa0-122">Określa lokalizację regionu wdrażania do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="dcaa0-123">Określa lokalizację nowego regionu wdrażania pośród obsługiwanego regionu usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="dcaa0-124">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | gdzie {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object lokalizacji</span><span class="sxs-lookup"><span data-stu-id="dcaa0-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="dcaa0-125">- SKU</span><span class="sxs-lookup"><span data-stu-id="dcaa0-125">-Sku</span></span>
<span data-ttu-id="dcaa0-126">Określa nową wartość warstwy dla regionu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="dcaa0-127">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="dcaa0-127">Valid values are:</span></span>
- <span data-ttu-id="dcaa0-128">Deweloper</span><span class="sxs-lookup"><span data-stu-id="dcaa0-128">Developer</span></span>
- <span data-ttu-id="dcaa0-129">Standardowe</span><span class="sxs-lookup"><span data-stu-id="dcaa0-129">Standard</span></span>
- <span data-ttu-id="dcaa0-130">Premium</span><span class="sxs-lookup"><span data-stu-id="dcaa0-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcaa0-131">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dcaa0-131">-VirtualNetwork</span></span>
<span data-ttu-id="dcaa0-132">Określa konfigurację sieci wirtualnej dla regionu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="dcaa0-133">Przekazanie $null spowoduje usunięcie konfiguracji sieci wirtualnej dla tego regionu.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="dcaa0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcaa0-134">CommonParameters</span></span>
<span data-ttu-id="dcaa0-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcaa0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcaa0-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcaa0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcaa0-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcaa0-137">INPUTS</span></span>

### <span data-ttu-id="dcaa0-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcaa0-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="dcaa0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dcaa0-139">System.String</span></span>

### <span data-ttu-id="dcaa0-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="dcaa0-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="dcaa0-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="dcaa0-141">System.Int32</span></span>

### <span data-ttu-id="dcaa0-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dcaa0-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="dcaa0-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dcaa0-143">OUTPUTS</span></span>

### <span data-ttu-id="dcaa0-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcaa0-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="dcaa0-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dcaa0-145">NOTES</span></span>

## <span data-ttu-id="dcaa0-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcaa0-146">RELATED LINKS</span></span>

[<span data-ttu-id="dcaa0-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="dcaa0-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="dcaa0-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="dcaa0-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="dcaa0-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcaa0-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
