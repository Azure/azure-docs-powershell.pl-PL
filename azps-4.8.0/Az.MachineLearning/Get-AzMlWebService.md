---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062664"
---
# <span data-ttu-id="29498-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="29498-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="29498-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29498-102">SYNOPSIS</span></span>
<span data-ttu-id="29498-103">Pobiera informacje podsumowujące dotyczące jednej lub wielu usług sieci Web.</span><span class="sxs-lookup"><span data-stu-id="29498-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="29498-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29498-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29498-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29498-105">DESCRIPTION</span></span>
<span data-ttu-id="29498-106">Pobiera informacje definicji usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="29498-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="29498-107">W zależności od przekazanych parametrów polecenie cmdlet zwraca definicję określonej usługi sieci Web, kolekcję definicji usług sieci Web dla określonej grupy zasobów w ramach bieżącej subskrypcji lub kolekcję definicji usług sieci Web w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="29498-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="29498-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29498-108">EXAMPLES</span></span>

### <span data-ttu-id="29498-109">Przykład 1: uzyskiwanie szczegółowych informacji o konkretnej usłudze sieci Web</span><span class="sxs-lookup"><span data-stu-id="29498-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="29498-110">Przykład 2: pobieranie wszystkich zasobów usług sieci Web w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="29498-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="29498-111">Przykład 3: pobieranie wszystkich usług sieci Web w bieżącej subskrypcji i określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="29498-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="29498-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29498-112">PARAMETERS</span></span>

### <span data-ttu-id="29498-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29498-113">-DefaultProfile</span></span>
<span data-ttu-id="29498-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="29498-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29498-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29498-115">-Name</span></span>
<span data-ttu-id="29498-116">Nazwa usługi sieci Web, do której są pobierane dane szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="29498-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29498-117">-Region</span><span class="sxs-lookup"><span data-stu-id="29498-117">-Region</span></span>
<span data-ttu-id="29498-118">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="29498-118">The name of region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29498-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29498-119">-ResourceGroupName</span></span>
<span data-ttu-id="29498-120">Grupa zasobów, z której są pobierane szczegóły dotyczące usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="29498-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29498-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29498-121">CommonParameters</span></span>
<span data-ttu-id="29498-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29498-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29498-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29498-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29498-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29498-124">INPUTS</span></span>

### <span data-ttu-id="29498-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="29498-125">None</span></span>

## <span data-ttu-id="29498-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29498-126">OUTPUTS</span></span>

### <span data-ttu-id="29498-127">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="29498-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="29498-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29498-128">NOTES</span></span>
<span data-ttu-id="29498-129">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="29498-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="29498-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29498-130">RELATED LINKS</span></span>
