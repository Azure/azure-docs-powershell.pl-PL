---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ccd7379a07b83b3ed45eff5f8095b950868810c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717978"
---
# <span data-ttu-id="3809b-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3809b-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="3809b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3809b-102">SYNOPSIS</span></span>
<span data-ttu-id="3809b-103">Usuwa istniejący region wdrożenia z wystąpienia PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3809b-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3809b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3809b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3809b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3809b-105">DESCRIPTION</span></span>
<span data-ttu-id="3809b-106">Polecenie cmdlet **Remove-AzureRmApiManagementRegion** usuwa wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** z kolekcji **AdditionalRegions** dostarczonych z wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="3809b-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="3809b-107">To polecenie cmdlet nie powoduje modyfikacji samego wdrożenia, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="3809b-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="3809b-108">Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, przepuszczanie zmodyfikowanej **PsApiManagementInstance** w celu **zaktualizowania AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="3809b-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="3809b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3809b-109">EXAMPLES</span></span>

### <span data-ttu-id="3809b-110">Przykład 1: usuwanie regionu z wystąpienia programu PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3809b-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="3809b-111">To polecenie usuwa region o nazwie wschód my z wystąpienia **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="3809b-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="3809b-112">Przykład 2: usuwanie regionu z wystąpienia programu PsApiManagement przy użyciu serii poleceń</span><span class="sxs-lookup"><span data-stu-id="3809b-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="3809b-113">To pierwsze polecenie uzyskuje wystąpienie **PsApiManagement** z grupy zasobów o nazwie contoso o nazwie ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="3809b-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="3809b-114">Polecenie ostatnie powoduje usunięcie regionu o nazwie wschód USA z tego wystąpienia, a następnie zaktualizowanie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3809b-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="3809b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3809b-115">PARAMETERS</span></span>

### <span data-ttu-id="3809b-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3809b-116">-ApiManagement</span></span>
<span data-ttu-id="3809b-117">Określa wystąpienie **PsApiManagement** , z którego to polecenie cmdlet usuwa dodatkowy region wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3809b-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="3809b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3809b-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="3809b-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3809b-119">-Location</span></span>
<span data-ttu-id="3809b-120">Określa lokalizację obszaru, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3809b-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="3809b-121">Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3809b-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="3809b-122">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="3809b-122">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="3809b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3809b-123">CommonParameters</span></span>
<span data-ttu-id="3809b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3809b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3809b-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3809b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3809b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3809b-126">INPUTS</span></span>

### <span data-ttu-id="3809b-127">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3809b-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="3809b-128">Parametry: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3809b-128">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="3809b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3809b-129">System.String</span></span>

## <span data-ttu-id="3809b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3809b-130">OUTPUTS</span></span>

### <span data-ttu-id="3809b-131">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3809b-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3809b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3809b-132">NOTES</span></span>

## <span data-ttu-id="3809b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3809b-133">RELATED LINKS</span></span>

[<span data-ttu-id="3809b-134">Dodaj-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3809b-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="3809b-135">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3809b-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


