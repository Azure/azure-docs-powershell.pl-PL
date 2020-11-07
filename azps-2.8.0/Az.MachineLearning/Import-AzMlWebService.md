---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 7c885da5423e765cca3d18ce18957c0e64bb2c36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704939"
---
# <span data-ttu-id="3b85c-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="3b85c-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="3b85c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b85c-102">SYNOPSIS</span></span>
<span data-ttu-id="3b85c-103">Importuje obiekt JSON do definicji usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="3b85c-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="3b85c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b85c-104">SYNTAX</span></span>

### <span data-ttu-id="3b85c-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="3b85c-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b85c-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="3b85c-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b85c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3b85c-107">DESCRIPTION</span></span>
<span data-ttu-id="3b85c-108">Import-AzMlWebService polecenia cmdlet Imports, określonego bezpośrednio lub w pliku, do którego istnieje odwołanie, oraz tworzenie obiektu definicji usługi sieci Web, który może zostać przekazany do New-AzMlWebService polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b85c-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="3b85c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b85c-109">EXAMPLES</span></span>

### <span data-ttu-id="3b85c-110">Przykład 1: Importowanie z ciągu</span><span class="sxs-lookup"><span data-stu-id="3b85c-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="3b85c-111">Przykład 2: Importowanie z ścieżki pliku</span><span class="sxs-lookup"><span data-stu-id="3b85c-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="3b85c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b85c-112">PARAMETERS</span></span>

### <span data-ttu-id="3b85c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b85c-113">-DefaultProfile</span></span>
<span data-ttu-id="3b85c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3b85c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b85c-115">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="3b85c-115">-InputFile</span></span>
<span data-ttu-id="3b85c-116">Ścieżka do pliku zawierającego definicję usługi sieci Web do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="3b85c-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="3b85c-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="3b85c-117">-JsonString</span></span>
<span data-ttu-id="3b85c-118">Ciąg sformatowany w notacji JSON zawierający definicję usługi sieci Web do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="3b85c-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="3b85c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b85c-119">CommonParameters</span></span>
<span data-ttu-id="3b85c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b85c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b85c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b85c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b85c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b85c-122">INPUTS</span></span>

### <span data-ttu-id="3b85c-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3b85c-123">None</span></span>

## <span data-ttu-id="3b85c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b85c-124">OUTPUTS</span></span>

### <span data-ttu-id="3b85c-125">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="3b85c-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="3b85c-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b85c-126">NOTES</span></span>
<span data-ttu-id="3b85c-127">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="3b85c-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3b85c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b85c-128">RELATED LINKS</span></span>
