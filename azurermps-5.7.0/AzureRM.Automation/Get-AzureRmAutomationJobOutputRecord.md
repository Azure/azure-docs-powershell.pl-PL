---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: 18551d6d839991cf0eb9e020c62fa0a24207d1e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546920"
---
# <span data-ttu-id="90fa5-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="90fa5-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="90fa5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="90fa5-103">Pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="90fa5-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90fa5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90fa5-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90fa5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90fa5-105">DESCRIPTION</span></span>
<span data-ttu-id="90fa5-106">Polecenie cmdlet **Get-AzureRmAutomationJobOutputRecord** pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="90fa5-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>

<span data-ttu-id="90fa5-107">Mimo że polecenie cmdlet **Get-AzureRmAutomationJobOutput** wyświetla co najmniej jeden rekord wyjściowy zadania, zwraca on tylko podsumowanie wartości dowolnego rekordu wyjściowego.</span><span class="sxs-lookup"><span data-stu-id="90fa5-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="90fa5-108">Nie zwraca pełnej wartości zwróconej wartości w rekordzie wyjściowym w pierwotnym typie.</span><span class="sxs-lookup"><span data-stu-id="90fa5-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="90fa5-109">Ponadto, podsumowanie ma maksymalną długość, co może spowodować przekroczenie pełnej wartości tego wyjścia.</span><span class="sxs-lookup"><span data-stu-id="90fa5-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="90fa5-110">W przeciwieństwie do polecenia **Get-AzureRmAutomationJobOutput** , to polecenie cmdlet zwraca pełną wartość w oryginalnie wyprowadzonym typie, w odniesieniu do dowolnych wartości w rekordach wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="90fa5-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="90fa5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90fa5-111">EXAMPLES</span></span>

### <span data-ttu-id="90fa5-112">Przykład 1: uzyskiwanie pełnego wyniku zadania automatyzacji</span><span class="sxs-lookup"><span data-stu-id="90fa5-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="90fa5-113">To polecenie pobiera pełne dane wyjściowe zadania o określonym IDENTYFIKATORze zadania.</span><span class="sxs-lookup"><span data-stu-id="90fa5-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="90fa5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90fa5-114">PARAMETERS</span></span>

### <span data-ttu-id="90fa5-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="90fa5-115">-AutomationAccountName</span></span>
<span data-ttu-id="90fa5-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera rekord wyjściowy zadania.</span><span class="sxs-lookup"><span data-stu-id="90fa5-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90fa5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90fa5-117">-DefaultProfile</span></span>
<span data-ttu-id="90fa5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="90fa5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fa5-119">-ID</span><span class="sxs-lookup"><span data-stu-id="90fa5-119">-Id</span></span>
<span data-ttu-id="90fa5-120">Określa identyfikator rekordu wyjściowego zadania dla tego polecenia cmdlet, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="90fa5-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90fa5-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="90fa5-121">-JobId</span></span>
<span data-ttu-id="90fa5-122">Określa identyfikator zadania, dla którego ten polecenie cmdlet pobiera rekord wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="90fa5-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90fa5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90fa5-123">-ResourceGroupName</span></span>
<span data-ttu-id="90fa5-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera rekord wyjściowy zadania.</span><span class="sxs-lookup"><span data-stu-id="90fa5-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90fa5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90fa5-125">CommonParameters</span></span>
<span data-ttu-id="90fa5-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90fa5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90fa5-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90fa5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90fa5-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90fa5-128">INPUTS</span></span>

### <span data-ttu-id="90fa5-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90fa5-129">None</span></span>
<span data-ttu-id="90fa5-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="90fa5-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90fa5-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90fa5-131">OUTPUTS</span></span>

### <span data-ttu-id="90fa5-132">Microsoft. Azure. Commands. Automation. model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="90fa5-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="90fa5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90fa5-133">NOTES</span></span>

## <span data-ttu-id="90fa5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90fa5-134">RELATED LINKS</span></span>

[<span data-ttu-id="90fa5-135">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="90fa5-135">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)


