---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525758"
---
# <span data-ttu-id="ba1dd-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ba1dd-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="ba1dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1dd-103">Usuwa istniejący region wdrożenia z wystąpienia PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba1dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba1dd-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba1dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba1dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ba1dd-106">Polecenie cmdlet **Remove-AzureRmApiManagementRegion** usuwa wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** z kolekcji **AdditionalRegions** dostarczonych z wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="ba1dd-107">To polecenie cmdlet nie powoduje modyfikacji samego wdrożenia, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="ba1dd-108">Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, przepuszczanie zmodyfikowanej **PsApiManagementInstance** w celu **zaktualizowania AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="ba1dd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba1dd-109">EXAMPLES</span></span>

### <span data-ttu-id="ba1dd-110">Przykład 1: usuwanie regionu z wystąpienia programu PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba1dd-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="ba1dd-111">To polecenie usuwa region o nazwie wschód my z wystąpienia **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="ba1dd-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="ba1dd-112">Przykład 2: usuwanie regionu z wystąpienia programu PsApiManagement przy użyciu serii poleceń</span><span class="sxs-lookup"><span data-stu-id="ba1dd-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="ba1dd-113">To pierwsze polecenie uzyskuje wystąpienie **PsApiManagement** z grupy zasobów o nazwie contoso o nazwie ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="ba1dd-114">Polecenie ostatnie powoduje usunięcie regionu o nazwie wschód USA z tego wystąpienia, a następnie zaktualizowanie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="ba1dd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba1dd-115">PARAMETERS</span></span>

### <span data-ttu-id="ba1dd-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba1dd-116">-ApiManagement</span></span>
<span data-ttu-id="ba1dd-117">Określa wystąpienie **PsApiManagement** , z którego to polecenie cmdlet usuwa dodatkowy region wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="ba1dd-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ba1dd-118">-Location</span></span>
<span data-ttu-id="ba1dd-119">Określa lokalizację obszaru, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-119">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="ba1dd-120">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ba1dd-120">Valid values are:</span></span> 

- <span data-ttu-id="ba1dd-121">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="ba1dd-121">North Central US</span></span>
- <span data-ttu-id="ba1dd-122">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="ba1dd-122">South Central US</span></span>
- <span data-ttu-id="ba1dd-123">Centralny stan</span><span class="sxs-lookup"><span data-stu-id="ba1dd-123">Central US</span></span>
- <span data-ttu-id="ba1dd-124">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="ba1dd-124">West Europe</span></span>
- <span data-ttu-id="ba1dd-125">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="ba1dd-125">North Europe</span></span>
- <span data-ttu-id="ba1dd-126">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="ba1dd-126">West US</span></span>
- <span data-ttu-id="ba1dd-127">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="ba1dd-127">East US</span></span>
- <span data-ttu-id="ba1dd-128">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="ba1dd-128">East US 2</span></span>
- <span data-ttu-id="ba1dd-129">Japonia wschodni</span><span class="sxs-lookup"><span data-stu-id="ba1dd-129">Japan East</span></span>
- <span data-ttu-id="ba1dd-130">Japonia Zachodnia</span><span class="sxs-lookup"><span data-stu-id="ba1dd-130">Japan West</span></span>
- <span data-ttu-id="ba1dd-131">Brazylia Południowa</span><span class="sxs-lookup"><span data-stu-id="ba1dd-131">Brazil South</span></span>
- <span data-ttu-id="ba1dd-132">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="ba1dd-132">Southeast Asia</span></span>
- <span data-ttu-id="ba1dd-133">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="ba1dd-133">East Asia</span></span>
- <span data-ttu-id="ba1dd-134">Australia Wschodnia</span><span class="sxs-lookup"><span data-stu-id="ba1dd-134">Australia East</span></span>
- <span data-ttu-id="ba1dd-135">Australia południowy</span><span class="sxs-lookup"><span data-stu-id="ba1dd-135">Australia Southeast</span></span>

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

### <span data-ttu-id="ba1dd-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba1dd-136">-DefaultProfile</span></span>
<span data-ttu-id="ba1dd-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba1dd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1dd-138">CommonParameters</span></span>
<span data-ttu-id="ba1dd-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba1dd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1dd-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba1dd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1dd-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba1dd-141">INPUTS</span></span>

### <span data-ttu-id="ba1dd-142">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba1dd-142">PsApiManagement</span></span>
<span data-ttu-id="ba1dd-143">Parametr "ApiManagement" akceptuje wartość typu "PsApiManagement" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ba1dd-143">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="ba1dd-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba1dd-144">OUTPUTS</span></span>

### <span data-ttu-id="ba1dd-145">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba1dd-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ba1dd-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba1dd-146">NOTES</span></span>

## <span data-ttu-id="ba1dd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba1dd-147">RELATED LINKS</span></span>

[<span data-ttu-id="ba1dd-148">Dodaj-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ba1dd-148">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="ba1dd-149">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ba1dd-149">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


