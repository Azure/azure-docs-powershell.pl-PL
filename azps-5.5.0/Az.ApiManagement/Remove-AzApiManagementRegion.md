---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244386"
---
# <span data-ttu-id="f88ce-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f88ce-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="f88ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f88ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f88ce-103">Usuwa istniejący region wdrażania z wystąpienia programu PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f88ce-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="f88ce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f88ce-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f88ce-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f88ce-105">DESCRIPTION</span></span>
<span data-ttu-id="f88ce-106">Polecenie cmdlet **Remove-AzApiManagementRegion** usuwa wystąpienie typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** z kolekcji **AdditionalRegions** pod warunkiem wystąpienia typu **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="f88ce-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="f88ce-107">To polecenie cmdlet nie modyfikuje samego wdrożenia, ale aktualizuje wystąpienie polecenia **PsApiManagement** w pamięci.</span><span class="sxs-lookup"><span data-stu-id="f88ce-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="f88ce-108">Aby zaktualizować wdrożenie zarządzania interfejsami API, przekaż zmodyfikowaną wartość **PsApiManagementInstance** do **Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="f88ce-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="f88ce-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f88ce-109">EXAMPLES</span></span>

### <span data-ttu-id="f88ce-110">Przykład 1. Usuwanie regionu z wystąpienia programu PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f88ce-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="f88ce-111">To polecenie usuwa region o nazwie Wschód USA z wystąpienia **PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="f88ce-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="f88ce-112">Przykład 2. Usuwanie regionu z wystąpienia polecenia PsApiManagement przy użyciu serii poleceń</span><span class="sxs-lookup"><span data-stu-id="f88ce-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="f88ce-113">To pierwsze polecenie pobiera wystąpienie **polecenia PsApiManagement** z grupy zasobów o nazwie Contoso O nazwie ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="f88ce-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="f88ce-114">Ostatnie polecenie spowoduje usunięcie z tego wystąpienia regionu o nazwie Wschód USA, a następnie aktualizacja wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f88ce-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="f88ce-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f88ce-115">PARAMETERS</span></span>

### <span data-ttu-id="f88ce-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f88ce-116">-ApiManagement</span></span>
<span data-ttu-id="f88ce-117">Określa wystąpienie **polecenia PsApiManagement,** z których to polecenie cmdlet usuwa dodatkowy region wdrażania.</span><span class="sxs-lookup"><span data-stu-id="f88ce-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="f88ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88ce-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="f88ce-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f88ce-119">-Location</span></span>
<span data-ttu-id="f88ce-120">Określa lokalizację regionu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f88ce-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="f88ce-121">Określa lokalizację nowego regionu wdrażania pośród obsługiwanego regionu usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="f88ce-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="f88ce-122">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | gdzie {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object lokalizacji</span><span class="sxs-lookup"><span data-stu-id="f88ce-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="f88ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88ce-123">CommonParameters</span></span>
<span data-ttu-id="f88ce-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88ce-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f88ce-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88ce-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f88ce-126">INPUTS</span></span>

### <span data-ttu-id="f88ce-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f88ce-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="f88ce-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f88ce-128">System.String</span></span>

## <span data-ttu-id="f88ce-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f88ce-129">OUTPUTS</span></span>

### <span data-ttu-id="f88ce-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f88ce-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f88ce-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f88ce-131">NOTES</span></span>

## <span data-ttu-id="f88ce-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f88ce-132">RELATED LINKS</span></span>

[<span data-ttu-id="f88ce-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f88ce-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="f88ce-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f88ce-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


