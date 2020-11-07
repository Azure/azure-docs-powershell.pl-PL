---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: b180dabec976164eac70106b49378d832fb00db8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704674"
---
# <span data-ttu-id="ddcec-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ddcec-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="ddcec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ddcec-102">SYNOPSIS</span></span>
<span data-ttu-id="ddcec-103">Dodaje nowe regiony wdrażania do wystąpienia PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ddcec-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="ddcec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ddcec-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddcec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ddcec-105">DESCRIPTION</span></span>
<span data-ttu-id="ddcec-106">Polecenie cmdlet **Add-AzApiManagementRegion** dodaje nowe wystąpienie typu **PsApiManagementRegion** do kolekcji **AdditionalRegions** o podanym wystąpieniu typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="ddcec-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="ddcec-107">To polecenie cmdlet nie wdraża samych elementów, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ddcec-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="ddcec-108">W celu zaktualizowania wdrożenia funkcji zarządzania interfejsem API przeszedł zmodyfikowane wystąpienie **PsApiManagement** , aby zaktualizować-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="ddcec-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzApiManagementDeployment.</span></span>

## <span data-ttu-id="ddcec-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ddcec-109">EXAMPLES</span></span>

### <span data-ttu-id="ddcec-110">Przykład 1: Dodawanie nowych regionów wdrożenia do wystąpienia PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddcec-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="ddcec-111">To polecenie dodaje dwie jednostki SKU Premium oraz region o nazwie wschód do **PsApiManagement** wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="ddcec-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="ddcec-112">Przykład 2: Dodawanie nowych regionów wdrażania do wystąpienia usługi PsApiManagement, a następnie aktualizowanie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="ddcec-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzApiManagementDeployment
```

<span data-ttu-id="ddcec-113">To polecenie pobiera obiekt **PsApiManagement** , dodaje dwie jednostki SKU Premium dla regionu o nazwie wschód USA, a następnie aktualizuje wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="ddcec-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="ddcec-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ddcec-114">PARAMETERS</span></span>

### <span data-ttu-id="ddcec-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddcec-115">-ApiManagement</span></span>
<span data-ttu-id="ddcec-116">Określa wystąpienie **PsApiManagement** , do którego są dodawane dodatkowe regiony wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ddcec-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="ddcec-117">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="ddcec-117">-Capacity</span></span>
<span data-ttu-id="ddcec-118">Określa pojemność jednostki składowania zapasu w obszarze wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ddcec-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="ddcec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddcec-119">-DefaultProfile</span></span>
<span data-ttu-id="ddcec-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ddcec-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddcec-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ddcec-121">-Location</span></span>
<span data-ttu-id="ddcec-122">Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ddcec-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="ddcec-123">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="ddcec-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="ddcec-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="ddcec-124">-Sku</span></span>
<span data-ttu-id="ddcec-125">Określa poziom obszaru wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ddcec-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="ddcec-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ddcec-126">Valid values are:</span></span> 
- <span data-ttu-id="ddcec-127">Deweloper</span><span class="sxs-lookup"><span data-stu-id="ddcec-127">Developer</span></span>
- <span data-ttu-id="ddcec-128">Standard</span><span class="sxs-lookup"><span data-stu-id="ddcec-128">Standard</span></span>
- <span data-ttu-id="ddcec-129">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="ddcec-129">Premium</span></span>

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

### <span data-ttu-id="ddcec-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ddcec-130">-VirtualNetwork</span></span>
<span data-ttu-id="ddcec-131">Określa konfigurację sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ddcec-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="ddcec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddcec-132">CommonParameters</span></span>
<span data-ttu-id="ddcec-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddcec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddcec-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddcec-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddcec-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddcec-135">INPUTS</span></span>

### <span data-ttu-id="ddcec-136">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddcec-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ddcec-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ddcec-137">OUTPUTS</span></span>

### <span data-ttu-id="ddcec-138">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddcec-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ddcec-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ddcec-139">NOTES</span></span>
* <span data-ttu-id="ddcec-140">Polecenie cmdlet zapisuje zaktualizowaną instancję **PsApiManagement** w potoku.</span><span class="sxs-lookup"><span data-stu-id="ddcec-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="ddcec-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddcec-141">RELATED LINKS</span></span>

[<span data-ttu-id="ddcec-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ddcec-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="ddcec-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ddcec-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="ddcec-144">Update-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ddcec-144">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)


