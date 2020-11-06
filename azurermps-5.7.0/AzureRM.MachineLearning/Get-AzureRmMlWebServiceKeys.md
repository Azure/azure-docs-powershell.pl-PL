---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546764"
---
# <span data-ttu-id="75d37-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="75d37-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="75d37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75d37-102">SYNOPSIS</span></span>
<span data-ttu-id="75d37-103">Pobiera klucze usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="75d37-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75d37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75d37-104">SYNTAX</span></span>

### <span data-ttu-id="75d37-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="75d37-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d37-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="75d37-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75d37-107">Opis</span><span class="sxs-lookup"><span data-stu-id="75d37-107">DESCRIPTION</span></span>
<span data-ttu-id="75d37-108">Pobiera klucze dostępu interfejsów API środowiska obsługi usługi Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="75d37-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="75d37-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75d37-109">EXAMPLES</span></span>

### <span data-ttu-id="75d37-110">--------------------------Przykład 1 — Pobierz klucze dla usługi sieci Web określonego przez grupę i nazwę zasobu--------------------------</span><span class="sxs-lookup"><span data-stu-id="75d37-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="75d37-111">--------------------------Przykład 2 — uzyskiwanie klawiszy dla wystąpienia usługi sieci Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="75d37-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="75d37-112">$mlService to obiekt typu Microsoft. Azure. Management. MachineLearning. WebServices. models. WebService.</span><span class="sxs-lookup"><span data-stu-id="75d37-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="75d37-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75d37-113">PARAMETERS</span></span>

### <span data-ttu-id="75d37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d37-114">-DefaultProfile</span></span>
<span data-ttu-id="75d37-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="75d37-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d37-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="75d37-116">-MlWebService</span></span>
<span data-ttu-id="75d37-117">Nazwa usługi sieci Web, do której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="75d37-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75d37-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75d37-118">-Name</span></span>
<span data-ttu-id="75d37-119">Nazwa usługi sieci Web, do której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="75d37-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d37-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d37-120">-ResourceGroupName</span></span>
<span data-ttu-id="75d37-121">Grupa zasobów dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="75d37-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d37-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d37-122">CommonParameters</span></span>
<span data-ttu-id="75d37-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d37-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d37-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d37-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d37-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75d37-125">INPUTS</span></span>

### <span data-ttu-id="75d37-126">Usług</span><span class="sxs-lookup"><span data-stu-id="75d37-126">WebService</span></span>
<span data-ttu-id="75d37-127">Parametr "MlWebService" akceptuje wartość typu "WebService" z procesu</span><span class="sxs-lookup"><span data-stu-id="75d37-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="75d37-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75d37-128">OUTPUTS</span></span>

### <span data-ttu-id="75d37-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="75d37-129">None</span></span>

## <span data-ttu-id="75d37-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75d37-130">NOTES</span></span>
<span data-ttu-id="75d37-131">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="75d37-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="75d37-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75d37-132">RELATED LINKS</span></span>

