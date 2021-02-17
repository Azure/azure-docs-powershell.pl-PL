---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: aebcb8be906811607aefee7dbdc2c7630b9e391e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401185"
---
# <span data-ttu-id="c9675-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c9675-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="c9675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9675-102">SYNOPSIS</span></span>
<span data-ttu-id="c9675-103">Dodaje nowe regiony wdrażania do wystąpienia programu PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c9675-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="c9675-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9675-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9675-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9675-105">DESCRIPTION</span></span>
<span data-ttu-id="c9675-106">Polecenie cmdlet **Add-AzApiManagementRegion** dodaje nowe wystąpienie typu **PsApiManagementRegion** do kolekcji **AdditionalRegions** podanego wystąpienia typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="c9675-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="c9675-107">To polecenie cmdlet nie wdraża niczego samodzielnie, ale aktualizuje wystąpienie programu **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="c9675-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="c9675-108">Aby zaktualizować wdrożenie zarządzania interfejsem API pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c9675-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="c9675-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9675-109">EXAMPLES</span></span>

### <span data-ttu-id="c9675-110">Przykład 1. Dodawanie nowych regionów wdrażania do wystąpienia programu PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c9675-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="c9675-111">To polecenie dodaje dwie jednostki SKU premium i region o nazwie Wschód USA do wystąpienia **PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="c9675-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="c9675-112">Przykład 2. Dodawanie nowych regionów wdrażania do wystąpienia programu PsApiManagement, a następnie aktualizowanie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="c9675-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Set-AzApiManagement
```

<span data-ttu-id="c9675-113">To polecenie pobiera **obiekt PsApiManagement,** dodaje dwie jednostki SKU premium dla regionu o nazwie Wschód USA, a następnie aktualizuje wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="c9675-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="c9675-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9675-114">PARAMETERS</span></span>

### <span data-ttu-id="c9675-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c9675-115">-ApiManagement</span></span>
<span data-ttu-id="c9675-116">Określa wystąpienie **programu PsApiManagement,** do których to polecenie cmdlet dodaje dodatkowe regiony wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c9675-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="c9675-117">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="c9675-117">-Capacity</span></span>
<span data-ttu-id="c9675-118">Określa pojemność sku w regionie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="c9675-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="c9675-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9675-119">-DefaultProfile</span></span>
<span data-ttu-id="c9675-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9675-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9675-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c9675-121">-Location</span></span>
<span data-ttu-id="c9675-122">Określa lokalizację nowego regionu wdrażania pośród obsługiwanego regionu usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="c9675-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="c9675-123">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | gdzie {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object lokalizacji</span><span class="sxs-lookup"><span data-stu-id="c9675-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="c9675-124">- SKU</span><span class="sxs-lookup"><span data-stu-id="c9675-124">-Sku</span></span>
<span data-ttu-id="c9675-125">Określa warstwę obszaru wdrażania.</span><span class="sxs-lookup"><span data-stu-id="c9675-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="c9675-126">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="c9675-126">Valid values are:</span></span>
- <span data-ttu-id="c9675-127">Deweloper</span><span class="sxs-lookup"><span data-stu-id="c9675-127">Developer</span></span>
- <span data-ttu-id="c9675-128">Standardowe</span><span class="sxs-lookup"><span data-stu-id="c9675-128">Standard</span></span>
- <span data-ttu-id="c9675-129">Premium</span><span class="sxs-lookup"><span data-stu-id="c9675-129">Premium</span></span>

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

### <span data-ttu-id="c9675-130">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c9675-130">-VirtualNetwork</span></span>
<span data-ttu-id="c9675-131">Określa konfigurację sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c9675-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="c9675-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9675-132">CommonParameters</span></span>
<span data-ttu-id="c9675-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9675-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9675-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9675-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9675-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9675-135">INPUTS</span></span>

### <span data-ttu-id="c9675-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c9675-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c9675-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9675-137">OUTPUTS</span></span>

### <span data-ttu-id="c9675-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c9675-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c9675-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9675-139">NOTES</span></span>
* <span data-ttu-id="c9675-140">Polecenie cmdlet zapisuje w potoku zaktualizowane wystąpienie polecenia **PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="c9675-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="c9675-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9675-141">RELATED LINKS</span></span>

[<span data-ttu-id="c9675-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c9675-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="c9675-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c9675-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="c9675-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c9675-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


