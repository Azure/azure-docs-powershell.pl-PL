---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: 05adf2476c922fdea17a69bd33f74570309349ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961882"
---
# <span data-ttu-id="dbf47-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="dbf47-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="dbf47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbf47-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf47-103">Pobiera klucze usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dbf47-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="dbf47-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dbf47-104">SYNTAX</span></span>

### <span data-ttu-id="dbf47-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dbf47-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbf47-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="dbf47-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbf47-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dbf47-107">DESCRIPTION</span></span>
<span data-ttu-id="dbf47-108">Pobiera klucze dostępu dla interfejsów API środowiska uruchomieniowego usługi sieci Web azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="dbf47-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="dbf47-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dbf47-109">EXAMPLES</span></span>

### <span data-ttu-id="dbf47-110">Przykład 1. Uzyskiwanie kluczy dla usługi sieci Web określonej przez grupę zasobów i nazwę</span><span class="sxs-lookup"><span data-stu-id="dbf47-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="dbf47-111">Przykład 2. Uzyskiwanie kluczy dla wystąpienia usługi sieci Web</span><span class="sxs-lookup"><span data-stu-id="dbf47-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="dbf47-112">$mlService jest obiektem typu Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="dbf47-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="dbf47-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbf47-113">PARAMETERS</span></span>

### <span data-ttu-id="dbf47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf47-114">-DefaultProfile</span></span>
<span data-ttu-id="dbf47-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="dbf47-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbf47-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="dbf47-116">-MlWebService</span></span>
<span data-ttu-id="dbf47-117">Nazwa usługi sieci Web, dla której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="dbf47-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="dbf47-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dbf47-118">-Name</span></span>
<span data-ttu-id="dbf47-119">Nazwa usługi sieci Web, dla której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="dbf47-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="dbf47-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf47-120">-ResourceGroupName</span></span>
<span data-ttu-id="dbf47-121">Grupa zasobów dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dbf47-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="dbf47-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf47-122">CommonParameters</span></span>
<span data-ttu-id="dbf47-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf47-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf47-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbf47-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf47-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbf47-125">INPUTS</span></span>

### <span data-ttu-id="dbf47-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="dbf47-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="dbf47-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbf47-127">OUTPUTS</span></span>

### <span data-ttu-id="dbf47-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="dbf47-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="dbf47-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dbf47-129">NOTES</span></span>
<span data-ttu-id="dbf47-130">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="dbf47-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dbf47-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbf47-131">RELATED LINKS</span></span>
