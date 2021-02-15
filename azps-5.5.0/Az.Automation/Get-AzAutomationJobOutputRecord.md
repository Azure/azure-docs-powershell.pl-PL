---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244258"
---
# <span data-ttu-id="56540-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="56540-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="56540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56540-102">SYNOPSIS</span></span>
<span data-ttu-id="56540-103">Pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="56540-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="56540-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56540-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56540-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="56540-105">DESCRIPTION</span></span>
<span data-ttu-id="56540-106">Polecenie **cmdlet Get-AzAutomationJobOutputRecord** pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="56540-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="56540-107">Mimo że **polecenie cmdlet Get-AzAutomationJobOutput** wyświetla jeden lub więcej rekordów wyjściowych zadań, zwraca tylko podsumowanie wartości dowolnego rekordu wyjściowego jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="56540-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="56540-108">Nie zwraca pełnej wartości wartości wyjściowej rekordu wyjściowego w oryginalnym typie.</span><span class="sxs-lookup"><span data-stu-id="56540-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="56540-109">Ponadto podsumowanie ma maksymalną długość, która może przekraczać pełną wartość w wynikach tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56540-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="56540-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56540-110">EXAMPLES</span></span>

### <span data-ttu-id="56540-111">Przykład 1. Uzyskiwanie pełnych wyników zadania automatyzacji</span><span class="sxs-lookup"><span data-stu-id="56540-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="56540-112">To polecenie pobiera pełne dane wyjściowe zadania o określonym identyfikatorze zadania.</span><span class="sxs-lookup"><span data-stu-id="56540-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="56540-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56540-113">PARAMETERS</span></span>

### <span data-ttu-id="56540-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="56540-114">-AutomationAccountName</span></span>
<span data-ttu-id="56540-115">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet uzyskuje rekord wyjściowy zadania.</span><span class="sxs-lookup"><span data-stu-id="56540-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56540-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56540-116">-DefaultProfile</span></span>
<span data-ttu-id="56540-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="56540-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56540-118">— Id</span><span class="sxs-lookup"><span data-stu-id="56540-118">-Id</span></span>
<span data-ttu-id="56540-119">Określa identyfikator rekordu wyjściowego zadania dla tego polecenia cmdlet do pobrania.</span><span class="sxs-lookup"><span data-stu-id="56540-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56540-120">- JobId</span><span class="sxs-lookup"><span data-stu-id="56540-120">-JobId</span></span>
<span data-ttu-id="56540-121">Określa identyfikator zadania, dla którego to polecenie cmdlet uzyskuje rekord wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="56540-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56540-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56540-122">-ResourceGroupName</span></span>
<span data-ttu-id="56540-123">Określa nazwę grupy zasobów, dla której to polecenie cmdlet uzyskuje rekord wyjściowy zadania.</span><span class="sxs-lookup"><span data-stu-id="56540-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56540-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56540-124">CommonParameters</span></span>
<span data-ttu-id="56540-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56540-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56540-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56540-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56540-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56540-127">INPUTS</span></span>

### <span data-ttu-id="56540-128">System.Guid</span><span class="sxs-lookup"><span data-stu-id="56540-128">System.Guid</span></span>

### <span data-ttu-id="56540-129">System.String</span><span class="sxs-lookup"><span data-stu-id="56540-129">System.String</span></span>

## <span data-ttu-id="56540-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56540-130">OUTPUTS</span></span>

### <span data-ttu-id="56540-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="56540-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="56540-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56540-132">NOTES</span></span>

## <span data-ttu-id="56540-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56540-133">RELATED LINKS</span></span>

[<span data-ttu-id="56540-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="56540-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


