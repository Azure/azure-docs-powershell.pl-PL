---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: fff6145adaa909bcadde90f36802072b812ba0ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053124"
---
# <span data-ttu-id="70624-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="70624-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="70624-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70624-102">SYNOPSIS</span></span>
<span data-ttu-id="70624-103">Aktualizuje istniejący region wdrożenia w wystąpieniu PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="70624-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="70624-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70624-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70624-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70624-105">DESCRIPTION</span></span>
<span data-ttu-id="70624-106">Polecenie cmdlet **Update-AzApiManagementRegion** aktualizuje istniejące wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** w kolekcji obiektów **AdditionalRegions** udostępnionego wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="70624-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="70624-107">To polecenie cmdlet nie rozmieszcza żadnych elementów, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="70624-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="70624-108">Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, użyj zmodyfikowanego **PsApiManagementInstance** do polecenia cmdlet Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="70624-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="70624-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70624-109">EXAMPLES</span></span>

### <span data-ttu-id="70624-110">Przykład 1: zwiększanie pojemności dodatkowego regionu w wystąpieniu PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="70624-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="70624-111">To polecenie pobiera usługę SKU zarządzania interfejsem API, posiadającą regiony w Ameryce Południowej centralach w STANach Zjednoczonych i Północno-środkowe.</span><span class="sxs-lookup"><span data-stu-id="70624-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="70624-112">Następnie zwiększa się zdolność centralnego regionu północno-USA do 2 przy użyciu **zestawu-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="70624-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="70624-113">Następny zestaw poleceń cmdlet **-AzApiManagement** stosuje zmianę konfiguracji do usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="70624-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="70624-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70624-114">PARAMETERS</span></span>

### <span data-ttu-id="70624-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="70624-115">-ApiManagement</span></span>
<span data-ttu-id="70624-116">Umożliwia określenie wystąpienia **PsApiManagement** , w którym ma zostać zaktualizowany istniejący region wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="70624-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="70624-117">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="70624-117">-Capacity</span></span>
<span data-ttu-id="70624-118">Określa nową wartość pojemności jednostki SKU dla obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="70624-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="70624-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70624-119">-DefaultProfile</span></span>
<span data-ttu-id="70624-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70624-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70624-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="70624-121">-Location</span></span>
<span data-ttu-id="70624-122">Określa lokalizację obszaru wdrożenia, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="70624-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="70624-123">Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="70624-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="70624-124">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="70624-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="70624-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="70624-125">-Sku</span></span>
<span data-ttu-id="70624-126">Określa nową wartość warstwy obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="70624-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="70624-127">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="70624-127">Valid values are:</span></span>
- <span data-ttu-id="70624-128">Deweloper</span><span class="sxs-lookup"><span data-stu-id="70624-128">Developer</span></span>
- <span data-ttu-id="70624-129">Standard</span><span class="sxs-lookup"><span data-stu-id="70624-129">Standard</span></span>
- <span data-ttu-id="70624-130">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="70624-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70624-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70624-131">-VirtualNetwork</span></span>
<span data-ttu-id="70624-132">Określa konfigurację sieci wirtualnej dla obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="70624-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="70624-133">Przekazanie $null spowoduje usunięcie konfiguracji sieci wirtualnej dla tego regionu.</span><span class="sxs-lookup"><span data-stu-id="70624-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="70624-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70624-134">CommonParameters</span></span>
<span data-ttu-id="70624-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70624-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70624-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70624-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70624-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70624-137">INPUTS</span></span>

### <span data-ttu-id="70624-138">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="70624-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="70624-139">System. String</span><span class="sxs-lookup"><span data-stu-id="70624-139">System.String</span></span>

### <span data-ttu-id="70624-140">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="70624-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="70624-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="70624-141">System.Int32</span></span>

### <span data-ttu-id="70624-142">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="70624-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="70624-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70624-143">OUTPUTS</span></span>

### <span data-ttu-id="70624-144">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="70624-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="70624-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70624-145">NOTES</span></span>

## <span data-ttu-id="70624-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70624-146">RELATED LINKS</span></span>

[<span data-ttu-id="70624-147">Dodaj-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="70624-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="70624-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="70624-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="70624-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="70624-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
