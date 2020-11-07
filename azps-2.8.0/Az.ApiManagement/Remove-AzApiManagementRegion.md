---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: ca40a9b74dd92b7bcdecdde87e4763f044b3272f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706933"
---
# <span data-ttu-id="ff054-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ff054-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="ff054-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff054-102">SYNOPSIS</span></span>
<span data-ttu-id="ff054-103">Usuwa istniejący region wdrożenia z wystąpienia PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ff054-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="ff054-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff054-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff054-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ff054-105">DESCRIPTION</span></span>
<span data-ttu-id="ff054-106">Polecenie cmdlet **Remove-AzApiManagementRegion** usuwa wystąpienie typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion** z kolekcji **AdditionalRegions** dostarczonych z wystąpienia typu **Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="ff054-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="ff054-107">To polecenie cmdlet nie powoduje modyfikacji samego wdrożenia, ale aktualizuje wystąpienie **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ff054-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="ff054-108">Aby zaktualizować wdrożenie funkcji zarządzania interfejsem API, przekazanie zmodyfikowanego **PsApiManagementInstance** w celu **Ustawienia AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="ff054-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="ff054-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff054-109">EXAMPLES</span></span>

### <span data-ttu-id="ff054-110">Przykład 1: usuwanie regionu z wystąpienia programu PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff054-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="ff054-111">To polecenie usuwa region o nazwie wschód my z wystąpienia **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="ff054-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="ff054-112">Przykład 2: usuwanie regionu z wystąpienia programu PsApiManagement przy użyciu serii poleceń</span><span class="sxs-lookup"><span data-stu-id="ff054-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="ff054-113">To pierwsze polecenie uzyskuje wystąpienie **PsApiManagement** z grupy zasobów o nazwie contoso o nazwie ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="ff054-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="ff054-114">Polecenie ostatnie powoduje usunięcie regionu o nazwie wschód USA z tego wystąpienia, a następnie zaktualizowanie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ff054-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="ff054-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff054-115">PARAMETERS</span></span>

### <span data-ttu-id="ff054-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff054-116">-ApiManagement</span></span>
<span data-ttu-id="ff054-117">Określa wystąpienie **PsApiManagement** , z którego to polecenie cmdlet usuwa dodatkowy region wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ff054-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="ff054-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff054-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="ff054-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ff054-119">-Location</span></span>
<span data-ttu-id="ff054-120">Określa lokalizację obszaru, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff054-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="ff054-121">Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ff054-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="ff054-122">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="ff054-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="ff054-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff054-123">CommonParameters</span></span>
<span data-ttu-id="ff054-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff054-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff054-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff054-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff054-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff054-126">INPUTS</span></span>

### <span data-ttu-id="ff054-127">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff054-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="ff054-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ff054-128">System.String</span></span>

## <span data-ttu-id="ff054-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff054-129">OUTPUTS</span></span>

### <span data-ttu-id="ff054-130">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff054-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ff054-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff054-131">NOTES</span></span>

## <span data-ttu-id="ff054-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff054-132">RELATED LINKS</span></span>

[<span data-ttu-id="ff054-133">Dodaj-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ff054-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="ff054-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="ff054-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

