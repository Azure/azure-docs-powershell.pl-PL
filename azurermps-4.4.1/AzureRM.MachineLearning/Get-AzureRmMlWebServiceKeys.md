---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553845"
---
# <span data-ttu-id="aed06-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="aed06-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="aed06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aed06-102">SYNOPSIS</span></span>
<span data-ttu-id="aed06-103">Pobiera klucze usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aed06-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aed06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aed06-104">SYNTAX</span></span>

### <span data-ttu-id="aed06-105">Uzyskaj klucze dostępu usług sieci Web usługi Azure ML o nazwie i grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="aed06-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed06-106">Pobierz kesy programu Access dla danego wystąpienia usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aed06-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aed06-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aed06-107">DESCRIPTION</span></span>
<span data-ttu-id="aed06-108">Pobiera klucze dostępu interfejsów API środowiska obsługi usługi Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="aed06-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="aed06-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aed06-109">EXAMPLES</span></span>

### <span data-ttu-id="aed06-110">--------------------------Przykład 1 — Pobierz klucze dla usługi sieci Web określonego przez grupę i nazwę zasobu--------------------------</span><span class="sxs-lookup"><span data-stu-id="aed06-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="aed06-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="aed06-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="aed06-112">--------------------------Przykład 2 — uzyskiwanie klawiszy dla wystąpienia usługi sieci Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="aed06-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="aed06-113">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="aed06-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="aed06-114">$mlService to obiekt typu Microsoft. Azure. Management. MachineLearning. WebServices. models. WebService.</span><span class="sxs-lookup"><span data-stu-id="aed06-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="aed06-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aed06-115">PARAMETERS</span></span>

### <span data-ttu-id="aed06-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="aed06-116">-MlWebService</span></span>
<span data-ttu-id="aed06-117">Nazwa usługi sieci Web, do której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="aed06-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aed06-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aed06-118">-Name</span></span>
<span data-ttu-id="aed06-119">Nazwa usługi sieci Web, do której są pobierane klucze dostępu.</span><span class="sxs-lookup"><span data-stu-id="aed06-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed06-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed06-120">-ResourceGroupName</span></span>
<span data-ttu-id="aed06-121">Grupa zasobów dla usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aed06-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed06-122">-DefaultProfile</span></span>
<span data-ttu-id="aed06-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aed06-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed06-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed06-124">CommonParameters</span></span>
<span data-ttu-id="aed06-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed06-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed06-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed06-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed06-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aed06-127">INPUTS</span></span>

### <span data-ttu-id="aed06-128">Usług</span><span class="sxs-lookup"><span data-stu-id="aed06-128">WebService</span></span>
<span data-ttu-id="aed06-129">Parametr "MlWebService" akceptuje wartość typu "WebService" z procesu</span><span class="sxs-lookup"><span data-stu-id="aed06-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="aed06-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aed06-130">OUTPUTS</span></span>

### <span data-ttu-id="aed06-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aed06-131">None</span></span>

## <span data-ttu-id="aed06-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aed06-132">NOTES</span></span>
<span data-ttu-id="aed06-133">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="aed06-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="aed06-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aed06-134">RELATED LINKS</span></span>

