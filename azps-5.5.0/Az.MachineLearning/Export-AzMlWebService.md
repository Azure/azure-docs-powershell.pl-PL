---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241355"
---
# <span data-ttu-id="1e344-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="1e344-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="1e344-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e344-102">SYNOPSIS</span></span>
<span data-ttu-id="1e344-103">Eksportuje obiekt definicji usługi sieci Web jako ciąg sformatowany JSON.</span><span class="sxs-lookup"><span data-stu-id="1e344-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="1e344-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e344-104">SYNTAX</span></span>

### <span data-ttu-id="1e344-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="1e344-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e344-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="1e344-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e344-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e344-107">DESCRIPTION</span></span>
<span data-ttu-id="1e344-108">Eksportuje obiekt definicji dla określonej usługi sieci Web jako ciąg sformatowany JSON.</span><span class="sxs-lookup"><span data-stu-id="1e344-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="1e344-109">Możesz od razu zwrócić ciąg lub zapisać go w pliku.</span><span class="sxs-lookup"><span data-stu-id="1e344-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="1e344-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e344-110">EXAMPLES</span></span>

### <span data-ttu-id="1e344-111">Przykład 1. Eksportowanie jako ciąg</span><span class="sxs-lookup"><span data-stu-id="1e344-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="1e344-112">Przykład 2. Eksportowanie do pliku</span><span class="sxs-lookup"><span data-stu-id="1e344-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="1e344-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e344-113">PARAMETERS</span></span>

### <span data-ttu-id="1e344-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e344-114">-DefaultProfile</span></span>
<span data-ttu-id="1e344-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1e344-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e344-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1e344-116">-Force</span></span>
<span data-ttu-id="1e344-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e344-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1e344-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="1e344-118">-OutputFile</span></span>
<span data-ttu-id="1e344-119">Ścieżka pliku eksportowanej definicji.</span><span class="sxs-lookup"><span data-stu-id="1e344-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="1e344-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="1e344-120">-ToJsonString</span></span>
<span data-ttu-id="1e344-121">Określa, że definicja zostanie wyeksportowana jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="1e344-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="1e344-122">- WebService</span><span class="sxs-lookup"><span data-stu-id="1e344-122">-WebService</span></span>
<span data-ttu-id="1e344-123">Obiekt definicji usługi sieci Web do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="1e344-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="1e344-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e344-124">-Confirm</span></span>
<span data-ttu-id="1e344-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e344-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e344-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e344-126">-WhatIf</span></span>
<span data-ttu-id="1e344-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e344-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e344-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1e344-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e344-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e344-129">CommonParameters</span></span>
<span data-ttu-id="1e344-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e344-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e344-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e344-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e344-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e344-132">INPUTS</span></span>

### <span data-ttu-id="1e344-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="1e344-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="1e344-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e344-134">OUTPUTS</span></span>

### <span data-ttu-id="1e344-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1e344-135">System.String</span></span>

## <span data-ttu-id="1e344-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e344-136">NOTES</span></span>
<span data-ttu-id="1e344-137">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="1e344-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1e344-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e344-138">RELATED LINKS</span></span>
