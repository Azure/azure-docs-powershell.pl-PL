---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: b54e7cf5af7eadd0ea56687a336175650b55daa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545155"
---
# <span data-ttu-id="a8852-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="a8852-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="a8852-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8852-102">SYNOPSIS</span></span>
<span data-ttu-id="a8852-103">Importuje obiekt JSON do definicji usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a8852-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8852-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8852-104">SYNTAX</span></span>

### <span data-ttu-id="a8852-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="a8852-105">ImportFromJSONFile</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8852-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="a8852-106">ImportFromJSONString.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8852-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a8852-107">DESCRIPTION</span></span>
<span data-ttu-id="a8852-108">Import-AzureRmMlWebService polecenia cmdlet Imports, określonego bezpośrednio lub w pliku, do którego istnieje odwołanie, oraz tworzenie obiektu definicji usługi sieci Web, który może zostać przekazany do New-AzureRmMlWebService polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8852-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="a8852-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8852-109">EXAMPLES</span></span>

### <span data-ttu-id="a8852-110">Przykład 1: Importowanie z ciągu</span><span class="sxs-lookup"><span data-stu-id="a8852-110">Example 1: Import from string</span></span>
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="a8852-111">Przykład 2: Importowanie z ścieżki pliku</span><span class="sxs-lookup"><span data-stu-id="a8852-111">Example 2: Import from file path</span></span>
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="a8852-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8852-112">PARAMETERS</span></span>

### <span data-ttu-id="a8852-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8852-113">-DefaultProfile</span></span>
<span data-ttu-id="a8852-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a8852-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8852-115">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="a8852-115">-InputFile</span></span>
<span data-ttu-id="a8852-116">Ścieżka do pliku zawierającego definicję usługi sieci Web do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="a8852-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8852-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="a8852-117">-JsonString</span></span>
<span data-ttu-id="a8852-118">Ciąg sformatowany w notacji JSON zawierający definicję usługi sieci Web do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="a8852-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8852-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8852-119">CommonParameters</span></span>
<span data-ttu-id="a8852-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8852-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8852-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8852-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8852-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8852-122">INPUTS</span></span>

### <span data-ttu-id="a8852-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a8852-123">None</span></span>

## <span data-ttu-id="a8852-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8852-124">OUTPUTS</span></span>

### <span data-ttu-id="a8852-125">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="a8852-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="a8852-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8852-126">NOTES</span></span>
<span data-ttu-id="a8852-127">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="a8852-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a8852-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8852-128">RELATED LINKS</span></span>
