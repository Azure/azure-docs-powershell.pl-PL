---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062665"
---
# <span data-ttu-id="f8ef8-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="f8ef8-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="f8ef8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8ef8-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ef8-103">Eksportuje obiekt definicji usługi sieci Web jako ciąg sformatowany JSON.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="f8ef8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8ef8-104">SYNTAX</span></span>

### <span data-ttu-id="f8ef8-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="f8ef8-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8ef8-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="f8ef8-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8ef8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f8ef8-107">DESCRIPTION</span></span>
<span data-ttu-id="f8ef8-108">Eksportuje obiekt definicji określonej usługi sieci Web jako ciąg sformatowany JSON.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="f8ef8-109">Możesz zwrócić ciąg natychmiast lub zapisać go w pliku.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="f8ef8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8ef8-110">EXAMPLES</span></span>

### <span data-ttu-id="f8ef8-111">Przykład 1. Eksportowanie jako ciąg</span><span class="sxs-lookup"><span data-stu-id="f8ef8-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="f8ef8-112">Przykład 2: Eksportowanie do pliku</span><span class="sxs-lookup"><span data-stu-id="f8ef8-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="f8ef8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8ef8-113">PARAMETERS</span></span>

### <span data-ttu-id="f8ef8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ef8-114">-DefaultProfile</span></span>
<span data-ttu-id="f8ef8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f8ef8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8ef8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f8ef8-116">-Force</span></span>
<span data-ttu-id="f8ef8-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f8ef8-118">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="f8ef8-118">-OutputFile</span></span>
<span data-ttu-id="f8ef8-119">Ścieżka pliku eksportowanej definicji.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="f8ef8-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="f8ef8-120">-ToJsonString</span></span>
<span data-ttu-id="f8ef8-121">Określa, że definicja będzie eksportowana jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="f8ef8-122">— Usługa WebService</span><span class="sxs-lookup"><span data-stu-id="f8ef8-122">-WebService</span></span>
<span data-ttu-id="f8ef8-123">Obiekt definicji usługi sieci Web, który ma zostać wyeksportowany.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="f8ef8-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8ef8-124">-Confirm</span></span>
<span data-ttu-id="f8ef8-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ef8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ef8-126">-WhatIf</span></span>
<span data-ttu-id="f8ef8-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8ef8-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ef8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ef8-129">CommonParameters</span></span>
<span data-ttu-id="f8ef8-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ef8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ef8-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ef8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ef8-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8ef8-132">INPUTS</span></span>

### <span data-ttu-id="f8ef8-133">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="f8ef8-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f8ef8-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8ef8-134">OUTPUTS</span></span>

### <span data-ttu-id="f8ef8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f8ef8-135">System.String</span></span>

## <span data-ttu-id="f8ef8-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8ef8-136">NOTES</span></span>
<span data-ttu-id="f8ef8-137">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="f8ef8-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f8ef8-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8ef8-138">RELATED LINKS</span></span>
