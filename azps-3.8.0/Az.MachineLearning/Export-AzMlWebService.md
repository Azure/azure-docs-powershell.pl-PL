---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051755"
---
# <span data-ttu-id="2b9de-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="2b9de-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="2b9de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b9de-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9de-103">Eksportuje obiekt definicji usługi sieci Web jako ciąg sformatowany JSON.</span><span class="sxs-lookup"><span data-stu-id="2b9de-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="2b9de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b9de-104">SYNTAX</span></span>

### <span data-ttu-id="2b9de-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="2b9de-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b9de-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="2b9de-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b9de-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2b9de-107">DESCRIPTION</span></span>
<span data-ttu-id="2b9de-108">Eksportuje obiekt definicji określonej usługi sieci Web jako ciąg sformatowany JSON.</span><span class="sxs-lookup"><span data-stu-id="2b9de-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="2b9de-109">Możesz zwrócić ciąg natychmiast lub zapisać go w pliku.</span><span class="sxs-lookup"><span data-stu-id="2b9de-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="2b9de-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b9de-110">EXAMPLES</span></span>

### <span data-ttu-id="2b9de-111">Przykład 1. Eksportowanie jako ciąg</span><span class="sxs-lookup"><span data-stu-id="2b9de-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="2b9de-112">Przykład 2: Eksportowanie do pliku</span><span class="sxs-lookup"><span data-stu-id="2b9de-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="2b9de-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b9de-113">PARAMETERS</span></span>

### <span data-ttu-id="2b9de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9de-114">-DefaultProfile</span></span>
<span data-ttu-id="2b9de-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2b9de-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b9de-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2b9de-116">-Force</span></span>
<span data-ttu-id="2b9de-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2b9de-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2b9de-118">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="2b9de-118">-OutputFile</span></span>
<span data-ttu-id="2b9de-119">Ścieżka pliku eksportowanej definicji.</span><span class="sxs-lookup"><span data-stu-id="2b9de-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9de-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="2b9de-120">-ToJsonString</span></span>
<span data-ttu-id="2b9de-121">Określa, że definicja będzie eksportowana jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="2b9de-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9de-122">— Usługa WebService</span><span class="sxs-lookup"><span data-stu-id="2b9de-122">-WebService</span></span>
<span data-ttu-id="2b9de-123">Obiekt definicji usługi sieci Web, który ma zostać wyeksportowany.</span><span class="sxs-lookup"><span data-stu-id="2b9de-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="2b9de-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b9de-124">-Confirm</span></span>
<span data-ttu-id="2b9de-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b9de-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9de-126">-WhatIf</span></span>
<span data-ttu-id="2b9de-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b9de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b9de-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b9de-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9de-129">CommonParameters</span></span>
<span data-ttu-id="2b9de-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b9de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9de-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b9de-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9de-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b9de-132">INPUTS</span></span>

### <span data-ttu-id="2b9de-133">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="2b9de-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2b9de-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b9de-134">OUTPUTS</span></span>

### <span data-ttu-id="2b9de-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2b9de-135">System.String</span></span>

## <span data-ttu-id="2b9de-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b9de-136">NOTES</span></span>
<span data-ttu-id="2b9de-137">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="2b9de-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2b9de-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b9de-138">RELATED LINKS</span></span>
