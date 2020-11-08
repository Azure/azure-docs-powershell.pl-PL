---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: e43cb76db410752aef0a0cffc72d3d5bb6f8e28f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051641"
---
# <span data-ttu-id="a9079-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="a9079-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="a9079-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9079-102">SYNOPSIS</span></span>
<span data-ttu-id="a9079-103">Pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a9079-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="a9079-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9079-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9079-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9079-105">DESCRIPTION</span></span>
<span data-ttu-id="a9079-106">Polecenie cmdlet **Get-AzAutomationJobOutputRecord** pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a9079-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="a9079-107">Mimo że polecenie cmdlet **Get-AzAutomationJobOutput** wyświetla co najmniej jeden rekord wyjściowy zadania, zwraca on tylko podsumowanie wartości dowolnego rekordu wyjściowego.</span><span class="sxs-lookup"><span data-stu-id="a9079-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="a9079-108">Nie zwraca pełnej wartości zwróconej wartości w rekordzie wyjściowym w pierwotnym typie.</span><span class="sxs-lookup"><span data-stu-id="a9079-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="a9079-109">Ponadto, podsumowanie ma maksymalną długość, co może spowodować przekroczenie pełnej wartości tego wyjścia.</span><span class="sxs-lookup"><span data-stu-id="a9079-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="a9079-110">W przeciwieństwie do polecenia **Get-AzAutomationJobOutput** , to polecenie cmdlet zwraca pełną wartość w oryginalnie wyprowadzonym typie, w odniesieniu do dowolnych wartości w rekordach wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a9079-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="a9079-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9079-111">EXAMPLES</span></span>

### <span data-ttu-id="a9079-112">Przykład 1: uzyskiwanie pełnego wyniku zadania automatyzacji</span><span class="sxs-lookup"><span data-stu-id="a9079-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="a9079-113">To polecenie pobiera pełne dane wyjściowe zadania o określonym IDENTYFIKATORze zadania.</span><span class="sxs-lookup"><span data-stu-id="a9079-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="a9079-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9079-114">PARAMETERS</span></span>

### <span data-ttu-id="a9079-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9079-115">-AutomationAccountName</span></span>
<span data-ttu-id="a9079-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera rekord wyjściowy zadania.</span><span class="sxs-lookup"><span data-stu-id="a9079-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="a9079-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9079-117">-DefaultProfile</span></span>
<span data-ttu-id="a9079-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a9079-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9079-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a9079-119">-Id</span></span>
<span data-ttu-id="a9079-120">Określa identyfikator rekordu wyjściowego zadania dla tego polecenia cmdlet, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="a9079-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="a9079-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="a9079-121">-JobId</span></span>
<span data-ttu-id="a9079-122">Określa identyfikator zadania, dla którego ten polecenie cmdlet pobiera rekord wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="a9079-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="a9079-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9079-123">-ResourceGroupName</span></span>
<span data-ttu-id="a9079-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera rekord wyjściowy zadania.</span><span class="sxs-lookup"><span data-stu-id="a9079-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="a9079-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9079-125">CommonParameters</span></span>
<span data-ttu-id="a9079-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9079-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9079-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9079-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9079-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9079-128">INPUTS</span></span>

### <span data-ttu-id="a9079-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a9079-129">System.Guid</span></span>

### <span data-ttu-id="a9079-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a9079-130">System.String</span></span>

## <span data-ttu-id="a9079-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9079-131">OUTPUTS</span></span>

### <span data-ttu-id="a9079-132">Microsoft. Azure. Commands. Automation. model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="a9079-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="a9079-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9079-133">NOTES</span></span>

## <span data-ttu-id="a9079-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9079-134">RELATED LINKS</span></span>

[<span data-ttu-id="a9079-135">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a9079-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


