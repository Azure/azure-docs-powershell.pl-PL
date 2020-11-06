---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553849"
---
# <span data-ttu-id="dd49c-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="dd49c-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="dd49c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd49c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd49c-103">Pobiera informacje podsumowujące dotyczące jednej lub wielu usług sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dd49c-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd49c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd49c-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd49c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd49c-105">DESCRIPTION</span></span>
<span data-ttu-id="dd49c-106">Pobiera informacje o defintion usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dd49c-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="dd49c-107">W zależności od przekazanego paramenters polecenie cmdlet zwraca defintion dla konkretnej usługi sieci Web, kolekcję defintions dla usług sieci Web dla określonej grupy zasobów w ramach bieżącego abonamentu lub kolekcję defintions dla usług sieci Web w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dd49c-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="dd49c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd49c-108">EXAMPLES</span></span>

### <span data-ttu-id="dd49c-109">--------------------------Przykład 1: uzyskiwanie szczegółowych informacji o konkretnej usłudze sieci Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd49c-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="dd49c-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="dd49c-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="dd49c-111">--------------------------Przykład 2: pobieranie wszystkich zasobów usług sieci Web w bieżącej subskrypcji--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd49c-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="dd49c-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="dd49c-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="dd49c-113">--------------------------Przykład 3: pobieranie wszystkich usług sieci Web w bieżącej subskrypcji i danej grupie zasobów--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd49c-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="dd49c-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="dd49c-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="dd49c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd49c-115">PARAMETERS</span></span>

### <span data-ttu-id="dd49c-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd49c-116">-Name</span></span>
<span data-ttu-id="dd49c-117">Nazwa usługi sieci Web, do której są pobierane dane szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="dd49c-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="dd49c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd49c-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd49c-119">Grupa zasobów, z której są pobierane szczegóły dotyczące usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="dd49c-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="dd49c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd49c-120">-DefaultProfile</span></span>
<span data-ttu-id="dd49c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd49c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd49c-122">-Region</span><span class="sxs-lookup"><span data-stu-id="dd49c-122">-Region</span></span>
<span data-ttu-id="dd49c-123">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="dd49c-123">The name of region</span></span>

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

### <span data-ttu-id="dd49c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd49c-124">CommonParameters</span></span>
<span data-ttu-id="dd49c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd49c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd49c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd49c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd49c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd49c-127">INPUTS</span></span>

## <span data-ttu-id="dd49c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd49c-128">OUTPUTS</span></span>

### <span data-ttu-id="dd49c-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dd49c-129">None</span></span>

## <span data-ttu-id="dd49c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd49c-130">NOTES</span></span>
<span data-ttu-id="dd49c-131">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="dd49c-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dd49c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd49c-132">RELATED LINKS</span></span>

