---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: f8923c6f98dad44a56c35cadc4b3e1daedeb1227
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549167"
---
# <span data-ttu-id="e1a73-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="e1a73-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="e1a73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1a73-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a73-103">Eksportuje obiekt definicji usługi sieci Web jako ciąg sformatowany JSON.</span><span class="sxs-lookup"><span data-stu-id="e1a73-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1a73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1a73-104">SYNTAX</span></span>

### <span data-ttu-id="e1a73-105">Eksportuj do pliku.</span><span class="sxs-lookup"><span data-stu-id="e1a73-105">Export to file.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1a73-106">Eksportowanie do ciągu JSON.</span><span class="sxs-lookup"><span data-stu-id="e1a73-106">Export to JSON string.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1a73-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e1a73-107">DESCRIPTION</span></span>
<span data-ttu-id="e1a73-108">Umożliwia wyeksportowanie obiektu definicji dla określonej witryny sieci Web jako ciągu sformatowanego w notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="e1a73-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="e1a73-109">Możesz zwrócić ciąg natychmiast lub zapisać go w pliku.</span><span class="sxs-lookup"><span data-stu-id="e1a73-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="e1a73-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1a73-110">EXAMPLES</span></span>

### <span data-ttu-id="e1a73-111">--------------------------Przykład 1: eksportowanie jako ciąg--------------------------</span><span class="sxs-lookup"><span data-stu-id="e1a73-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
<span data-ttu-id="e1a73-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="e1a73-112">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="e1a73-113">--------------------------Przykład 2: Eksportowanie do pliku--------------------------</span><span class="sxs-lookup"><span data-stu-id="e1a73-113">--------------------------  Example 2: Export to file  --------------------------</span></span>
<span data-ttu-id="e1a73-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="e1a73-114">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="e1a73-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1a73-115">PARAMETERS</span></span>

### <span data-ttu-id="e1a73-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e1a73-116">-Force</span></span>
<span data-ttu-id="e1a73-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e1a73-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a73-118">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="e1a73-118">-OutputFile</span></span>
<span data-ttu-id="e1a73-119">Ścieżka pliku eksportowanej definicji.</span><span class="sxs-lookup"><span data-stu-id="e1a73-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a73-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="e1a73-120">-ToJsonString</span></span>
<span data-ttu-id="e1a73-121">Określa, że definicja będzie eksportowana jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="e1a73-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a73-122">— Usługa WebService</span><span class="sxs-lookup"><span data-stu-id="e1a73-122">-WebService</span></span>
<span data-ttu-id="e1a73-123">Obiekt definicji usługi sieci Web, który ma zostać wyeksportowany.</span><span class="sxs-lookup"><span data-stu-id="e1a73-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a73-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1a73-124">-Confirm</span></span>
<span data-ttu-id="e1a73-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1a73-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a73-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1a73-126">-WhatIf</span></span>
<span data-ttu-id="e1a73-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1a73-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1a73-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1a73-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a73-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a73-129">-DefaultProfile</span></span>
<span data-ttu-id="e1a73-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1a73-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1a73-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a73-131">CommonParameters</span></span>
<span data-ttu-id="e1a73-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1a73-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a73-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a73-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a73-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1a73-134">INPUTS</span></span>

### <span data-ttu-id="e1a73-135">Usług</span><span class="sxs-lookup"><span data-stu-id="e1a73-135">WebService</span></span>
<span data-ttu-id="e1a73-136">Parametr "WebService" akceptuje wartość typu "WebService" z procesu</span><span class="sxs-lookup"><span data-stu-id="e1a73-136">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="e1a73-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1a73-137">OUTPUTS</span></span>

### <span data-ttu-id="e1a73-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e1a73-138">None</span></span>

## <span data-ttu-id="e1a73-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1a73-139">NOTES</span></span>
<span data-ttu-id="e1a73-140">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="e1a73-140">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e1a73-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1a73-141">RELATED LINKS</span></span>

