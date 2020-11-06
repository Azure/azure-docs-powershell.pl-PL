---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 802a3be7aca857b798f1e853bec499c5397b6e65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542539"
---
# <span data-ttu-id="a4238-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="a4238-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="a4238-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4238-102">SYNOPSIS</span></span>
<span data-ttu-id="a4238-103">Pobiera informacje podsumowujące dotyczące jednej lub wielu usług sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a4238-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4238-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4238-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4238-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4238-105">DESCRIPTION</span></span>
<span data-ttu-id="a4238-106">Pobiera informacje o defintion usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a4238-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="a4238-107">W zależności od przekazanego paramenters polecenie cmdlet zwraca defintion dla konkretnej usługi sieci Web, kolekcję defintions dla usług sieci Web dla określonej grupy zasobów w ramach bieżącego abonamentu lub kolekcję defintions dla usług sieci Web w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a4238-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="a4238-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4238-108">EXAMPLES</span></span>

### <span data-ttu-id="a4238-109">--------------------------Przykład 1: uzyskiwanie szczegółowych informacji o konkretnej usłudze sieci Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4238-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="a4238-110">--------------------------Przykład 2: pobieranie wszystkich zasobów usług sieci Web w bieżącej subskrypcji--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4238-110">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
```
Get-AzureRmMlWebService
```

### <span data-ttu-id="a4238-111">--------------------------Przykład 3: pobieranie wszystkich usług sieci Web w bieżącej subskrypcji i danej grupie zasobów--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4238-111">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="a4238-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4238-112">PARAMETERS</span></span>

### <span data-ttu-id="a4238-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4238-113">-DefaultProfile</span></span>
<span data-ttu-id="a4238-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a4238-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4238-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4238-115">-Name</span></span>
<span data-ttu-id="a4238-116">Nazwa usługi sieci Web, do której są pobierane dane szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="a4238-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4238-117">-Region</span><span class="sxs-lookup"><span data-stu-id="a4238-117">-Region</span></span>
<span data-ttu-id="a4238-118">Nazwa Regio</span><span class="sxs-lookup"><span data-stu-id="a4238-118">The name of regio</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4238-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4238-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4238-120">Grupa zasobów, z której są pobierane szczegóły dotyczące usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a4238-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4238-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4238-121">CommonParameters</span></span>
<span data-ttu-id="a4238-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4238-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4238-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4238-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4238-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4238-124">INPUTS</span></span>

### <span data-ttu-id="a4238-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a4238-125">None</span></span>
<span data-ttu-id="a4238-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a4238-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4238-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4238-127">OUTPUTS</span></span>

### <span data-ttu-id="a4238-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a4238-128">None</span></span>

## <span data-ttu-id="a4238-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4238-129">NOTES</span></span>
<span data-ttu-id="a4238-130">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="a4238-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a4238-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4238-131">RELATED LINKS</span></span>

