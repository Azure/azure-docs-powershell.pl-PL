---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ea4b734eba1ed1a37a72e756c32acc3d6ad2a32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547712"
---
# <span data-ttu-id="8ac17-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8ac17-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="8ac17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ac17-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac17-103">Dodaje nowe regiony wdrażania do wystąpienia PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8ac17-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ac17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ac17-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ac17-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8ac17-105">DESCRIPTION</span></span>
<span data-ttu-id="8ac17-106">Polecenie cmdlet **Add-AzureRmApiManagementRegion** dodaje nowe wystąpienie typu **PsApiManagementRegion** do kolekcji **AdditionalRegions** o podanym wystąpieniu typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="8ac17-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="8ac17-107">To polecenie cmdlet nie wdraża samych elementów, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="8ac17-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="8ac17-108">W celu zaktualizowania wdrożenia funkcji zarządzania interfejsem API przeszedł zmodyfikowane wystąpienie **PsApiManagement** , aby zaktualizować-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="8ac17-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="8ac17-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ac17-109">EXAMPLES</span></span>

### <span data-ttu-id="8ac17-110">Przykład 1: Dodawanie nowych regionów wdrożenia do wystąpienia PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ac17-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="8ac17-111">To polecenie dodaje dwie jednostki SKU Premium oraz region o nazwie wschód do **PsApiManagement** wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8ac17-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="8ac17-112">Przykład 2: Dodawanie nowych regionów wdrażania do wystąpienia usługi PsApiManagement, a następnie aktualizowanie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="8ac17-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="8ac17-113">To polecenie pobiera obiekt **PsApiManagement** , dodaje dwie jednostki SKU Premium dla regionu o nazwie wschód USA, a następnie aktualizuje wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="8ac17-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="8ac17-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ac17-114">PARAMETERS</span></span>

### <span data-ttu-id="8ac17-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ac17-115">-ApiManagement</span></span>
<span data-ttu-id="8ac17-116">Określa wystąpienie **PsApiManagement** , do którego są dodawane dodatkowe regiony wdrażania.</span><span class="sxs-lookup"><span data-stu-id="8ac17-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="8ac17-117">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="8ac17-117">-Capacity</span></span>
<span data-ttu-id="8ac17-118">Określa pojemność jednostki składowania zapasu w obszarze wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8ac17-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="8ac17-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac17-119">-DefaultProfile</span></span>
<span data-ttu-id="8ac17-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac17-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ac17-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8ac17-121">-Location</span></span>
<span data-ttu-id="8ac17-122">Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="8ac17-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="8ac17-123">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="8ac17-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="8ac17-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="8ac17-124">-Sku</span></span>
<span data-ttu-id="8ac17-125">Określa poziom obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8ac17-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="8ac17-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="8ac17-126">Valid values are:</span></span> 
- <span data-ttu-id="8ac17-127">Deweloper</span><span class="sxs-lookup"><span data-stu-id="8ac17-127">Developer</span></span>
- <span data-ttu-id="8ac17-128">Standard</span><span class="sxs-lookup"><span data-stu-id="8ac17-128">Standard</span></span>
- <span data-ttu-id="8ac17-129">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="8ac17-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac17-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ac17-130">-VirtualNetwork</span></span>
<span data-ttu-id="8ac17-131">Określa konfigurację sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ac17-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="8ac17-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac17-132">CommonParameters</span></span>
<span data-ttu-id="8ac17-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac17-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac17-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac17-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac17-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ac17-135">INPUTS</span></span>

### <span data-ttu-id="8ac17-136">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ac17-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="8ac17-137">Parametry: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ac17-137">Parameters: ApiManagement (ByValue)</span></span>

## <span data-ttu-id="8ac17-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ac17-138">OUTPUTS</span></span>

### <span data-ttu-id="8ac17-139">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ac17-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8ac17-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ac17-140">NOTES</span></span>
* <span data-ttu-id="8ac17-141">Polecenie cmdlet zapisuje zaktualizowaną instancję **PsApiManagement** w potoku.</span><span class="sxs-lookup"><span data-stu-id="8ac17-141">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="8ac17-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ac17-142">RELATED LINKS</span></span>

[<span data-ttu-id="8ac17-143">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8ac17-143">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="8ac17-144">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="8ac17-144">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="8ac17-145">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="8ac17-145">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


