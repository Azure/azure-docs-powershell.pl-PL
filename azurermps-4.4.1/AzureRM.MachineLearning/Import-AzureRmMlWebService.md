---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: d85767623d88c9fd7d0a00ea98e575953132d3f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719290"
---
# <span data-ttu-id="63e83-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="63e83-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="63e83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63e83-102">SYNOPSIS</span></span>
<span data-ttu-id="63e83-103">Importuje obiekt JSON do definicji usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="63e83-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63e83-104">SYNTAX</span></span>

### <span data-ttu-id="63e83-105">Importowanie z pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="63e83-105">Import from JSON file.</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63e83-106">Importowanie z ciągu JSON.</span><span class="sxs-lookup"><span data-stu-id="63e83-106">Import from JSON string.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63e83-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63e83-107">DESCRIPTION</span></span>
<span data-ttu-id="63e83-108">Import-AzureRmMlWebService polecenia cmdlet Imports, określonego bezpośrednio lub w pliku, do którego istnieje odwołanie, oraz tworzenie obiektu definicji usługi sieci Web, który może zostać przekazany do New-AzureRmMlWebService polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e83-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="63e83-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63e83-109">EXAMPLES</span></span>

### <span data-ttu-id="63e83-110">--------------------------Przykład 1: Importowanie z ciągu--------------------------</span><span class="sxs-lookup"><span data-stu-id="63e83-110">--------------------------  Example 1: Import from string  --------------------------</span></span>
<span data-ttu-id="63e83-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="63e83-111">@{paragraph=PS C:\\\>}</span></span>





```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="63e83-112">--------------------------Przykład 2: Importowanie z ścieżki pliku--------------------------</span><span class="sxs-lookup"><span data-stu-id="63e83-112">--------------------------  Example 2: Import from file path  --------------------------</span></span>
<span data-ttu-id="63e83-113">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="63e83-113">@{paragraph=PS C:\\\>}</span></span>





```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="63e83-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63e83-114">PARAMETERS</span></span>

### <span data-ttu-id="63e83-115">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="63e83-115">-InputFile</span></span>
<span data-ttu-id="63e83-116">Ścieżka do pliku zawierającego definicję usługi sieci Web do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="63e83-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: Import from JSON file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e83-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="63e83-117">-JsonString</span></span>
<span data-ttu-id="63e83-118">Ciąg sformatowany w notacji JSON zawierający definicję usługi sieci Web do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="63e83-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: Import from JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e83-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e83-119">-DefaultProfile</span></span>
<span data-ttu-id="63e83-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63e83-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e83-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e83-121">CommonParameters</span></span>
<span data-ttu-id="63e83-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e83-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e83-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e83-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e83-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63e83-124">INPUTS</span></span>

## <span data-ttu-id="63e83-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63e83-125">OUTPUTS</span></span>

### <span data-ttu-id="63e83-126">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="63e83-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="63e83-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63e83-127">NOTES</span></span>
<span data-ttu-id="63e83-128">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="63e83-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="63e83-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63e83-129">RELATED LINKS</span></span>

