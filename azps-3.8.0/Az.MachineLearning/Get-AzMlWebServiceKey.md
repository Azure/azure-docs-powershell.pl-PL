---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895385"
---
# <span data-ttu-id="57ba4-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="57ba4-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="57ba4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="57ba4-103">Pobiera klucze usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="57ba4-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="57ba4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57ba4-104">SYNTAX</span></span>

### <span data-ttu-id="57ba4-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="57ba4-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57ba4-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="57ba4-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57ba4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="57ba4-107">DESCRIPTION</span></span>
<span data-ttu-id="57ba4-108">Pobiera klucze dostępu interfejsów API środowiska obsługi usługi Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="57ba4-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="57ba4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57ba4-109">EXAMPLES</span></span>

### <span data-ttu-id="57ba4-110">Przykład 1 — Pobierz klucze dla usługi sieci Web określonego przez grupę i nazwę zasobu</span><span class="sxs-lookup"><span data-stu-id="57ba4-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="57ba4-111">Przykład 2 — uzyskiwanie klawiszy dla wystąpienia usługi sieci Web</span><span class="sxs-lookup"><span data-stu-id="57ba4-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="57ba4-112">$mlService to obiekt typu Microsoft. Azure. Management. MachineLearning. WebServices. models. WebService.</span><span class="sxs-lookup"><span data-stu-id="57ba4-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="57ba4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57ba4-113">PARAMETERS</span></span>

### <span data-ttu-id="57ba4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ba4-114">-DefaultProfile</span></span>
<span data-ttu-id="57ba4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="57ba4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57ba4-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="57ba4-116">-MlWebService</span></span>
<span data-ttu-id="57ba4-117">Nazwa usługi sieci Web, do której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="57ba4-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="57ba4-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57ba4-118">-Name</span></span>
<span data-ttu-id="57ba4-119">Nazwa usługi sieci Web, do której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="57ba4-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="57ba4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ba4-120">-ResourceGroupName</span></span>
<span data-ttu-id="57ba4-121">Grupa zasobów dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="57ba4-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="57ba4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ba4-122">CommonParameters</span></span>
<span data-ttu-id="57ba4-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ba4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ba4-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ba4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ba4-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57ba4-125">INPUTS</span></span>

### <span data-ttu-id="57ba4-126">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="57ba4-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="57ba4-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57ba4-127">OUTPUTS</span></span>

### <span data-ttu-id="57ba4-128">Microsoft. Azure. Management. MachineLearning. WebServices. models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="57ba4-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="57ba4-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57ba4-129">NOTES</span></span>
<span data-ttu-id="57ba4-130">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="57ba4-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="57ba4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57ba4-131">RELATED LINKS</span></span>
