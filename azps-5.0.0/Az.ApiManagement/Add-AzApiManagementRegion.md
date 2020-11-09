---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307729"
---
# <span data-ttu-id="d0f1c-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="d0f1c-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="d0f1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f1c-103">Dodaje nowe regiony wdrażania do wystąpienia PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="d0f1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0f1c-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0f1c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0f1c-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f1c-106">Polecenie cmdlet **Add-AzApiManagementRegion** dodaje nowe wystąpienie typu **PsApiManagementRegion** do kolekcji **AdditionalRegions** o podanym wystąpieniu typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="d0f1c-107">To polecenie cmdlet nie wdraża samych elementów, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="d0f1c-108">Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, przeszedł zmodyfikowane wystąpienie **PsApiManagement** do Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="d0f1c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0f1c-109">EXAMPLES</span></span>

### <span data-ttu-id="d0f1c-110">Przykład 1: Dodawanie nowych regionów wdrożenia do wystąpienia PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d0f1c-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="d0f1c-111">To polecenie dodaje dwie jednostki SKU Premium oraz region o nazwie wschód do **PsApiManagement** wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="d0f1c-112">Przykład 2: Dodawanie nowych regionów wdrażania do wystąpienia usługi PsApiManagement, a następnie aktualizowanie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="d0f1c-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="d0f1c-113">To polecenie pobiera obiekt **PsApiManagement** , dodaje dwie jednostki SKU Premium dla regionu o nazwie wschód USA, a następnie aktualizuje wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="d0f1c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0f1c-114">PARAMETERS</span></span>

### <span data-ttu-id="d0f1c-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d0f1c-115">-ApiManagement</span></span>
<span data-ttu-id="d0f1c-116">Określa wystąpienie **PsApiManagement** , do którego są dodawane dodatkowe regiony wdrażania.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="d0f1c-117">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="d0f1c-117">-Capacity</span></span>
<span data-ttu-id="d0f1c-118">Określa pojemność jednostki składowania zapasu w obszarze wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="d0f1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f1c-119">-DefaultProfile</span></span>
<span data-ttu-id="d0f1c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0f1c-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d0f1c-121">-Location</span></span>
<span data-ttu-id="d0f1c-122">Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="d0f1c-123">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="d0f1c-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="d0f1c-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="d0f1c-124">-Sku</span></span>
<span data-ttu-id="d0f1c-125">Określa poziom obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="d0f1c-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d0f1c-126">Valid values are:</span></span> 
- <span data-ttu-id="d0f1c-127">Deweloper</span><span class="sxs-lookup"><span data-stu-id="d0f1c-127">Developer</span></span>
- <span data-ttu-id="d0f1c-128">Standard</span><span class="sxs-lookup"><span data-stu-id="d0f1c-128">Standard</span></span>
- <span data-ttu-id="d0f1c-129">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="d0f1c-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f1c-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d0f1c-130">-VirtualNetwork</span></span>
<span data-ttu-id="d0f1c-131">Określa konfigurację sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="d0f1c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f1c-132">CommonParameters</span></span>
<span data-ttu-id="d0f1c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f1c-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0f1c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f1c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0f1c-135">INPUTS</span></span>

### <span data-ttu-id="d0f1c-136">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d0f1c-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="d0f1c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0f1c-137">OUTPUTS</span></span>

### <span data-ttu-id="d0f1c-138">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d0f1c-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="d0f1c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0f1c-139">NOTES</span></span>
* <span data-ttu-id="d0f1c-140">Polecenie cmdlet zapisuje zaktualizowaną instancję **PsApiManagement** w potoku.</span><span class="sxs-lookup"><span data-stu-id="d0f1c-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="d0f1c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0f1c-141">RELATED LINKS</span></span>

[<span data-ttu-id="d0f1c-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="d0f1c-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="d0f1c-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="d0f1c-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="d0f1c-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d0f1c-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


