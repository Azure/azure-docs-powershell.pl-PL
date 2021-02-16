---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187523"
---
# <span data-ttu-id="b41ec-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="b41ec-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="b41ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b41ec-102">SYNOPSIS</span></span>
<span data-ttu-id="b41ec-103">Pobiera klucze usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b41ec-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="b41ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b41ec-104">SYNTAX</span></span>

### <span data-ttu-id="b41ec-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b41ec-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b41ec-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="b41ec-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b41ec-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b41ec-107">DESCRIPTION</span></span>
<span data-ttu-id="b41ec-108">Pobiera klucze dostępu dla interfejsów API środowiska uruchomieniowego usługi sieci Web azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="b41ec-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="b41ec-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b41ec-109">EXAMPLES</span></span>

### <span data-ttu-id="b41ec-110">Przykład 1. Uzyskiwanie kluczy dla usługi sieci Web określonej przez grupę zasobów i nazwę</span><span class="sxs-lookup"><span data-stu-id="b41ec-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="b41ec-111">Przykład 2. Uzyskiwanie kluczy dla wystąpienia usługi sieci Web</span><span class="sxs-lookup"><span data-stu-id="b41ec-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="b41ec-112">$mlService jest obiektem typu Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="b41ec-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="b41ec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b41ec-113">PARAMETERS</span></span>

### <span data-ttu-id="b41ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b41ec-114">-DefaultProfile</span></span>
<span data-ttu-id="b41ec-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b41ec-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b41ec-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="b41ec-116">-MlWebService</span></span>
<span data-ttu-id="b41ec-117">Nazwa usługi sieci Web, dla której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="b41ec-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ec-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b41ec-118">-Name</span></span>
<span data-ttu-id="b41ec-119">Nazwa usługi sieci Web, dla której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="b41ec-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b41ec-120">-ResourceGroupName</span></span>
<span data-ttu-id="b41ec-121">Grupa zasobów dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b41ec-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b41ec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41ec-122">CommonParameters</span></span>
<span data-ttu-id="b41ec-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b41ec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41ec-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b41ec-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41ec-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b41ec-125">INPUTS</span></span>

### <span data-ttu-id="b41ec-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="b41ec-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="b41ec-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b41ec-127">OUTPUTS</span></span>

### <span data-ttu-id="b41ec-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="b41ec-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="b41ec-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b41ec-129">NOTES</span></span>
<span data-ttu-id="b41ec-130">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b41ec-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b41ec-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b41ec-131">RELATED LINKS</span></span>
