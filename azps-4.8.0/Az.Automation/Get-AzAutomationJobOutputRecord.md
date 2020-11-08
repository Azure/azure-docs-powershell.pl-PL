---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062428"
---
# <span data-ttu-id="a91f3-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="a91f3-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="a91f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a91f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a91f3-103">Pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a91f3-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="a91f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a91f3-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a91f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a91f3-105">DESCRIPTION</span></span>
<span data-ttu-id="a91f3-106">Polecenie cmdlet **Get-AzAutomationJobOutputRecord** pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a91f3-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="a91f3-107">Mimo że polecenie cmdlet **Get-AzAutomationJobOutput** wyświetla co najmniej jeden rekord wyjściowy zadania, zwraca on tylko podsumowanie wartości dowolnego rekordu wyjściowego.</span><span class="sxs-lookup"><span data-stu-id="a91f3-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="a91f3-108">Nie zwraca pełnej wartości zwróconej wartości w rekordzie wyjściowym w pierwotnym typie.</span><span class="sxs-lookup"><span data-stu-id="a91f3-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="a91f3-109">Ponadto, podsumowanie ma maksymalną długość, co może spowodować przekroczenie pełnej wartości tego wyjścia.</span><span class="sxs-lookup"><span data-stu-id="a91f3-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="a91f3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a91f3-110">EXAMPLES</span></span>

### <span data-ttu-id="a91f3-111">Przykład 1: uzyskiwanie pełnego wyniku zadania automatyzacji</span><span class="sxs-lookup"><span data-stu-id="a91f3-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="a91f3-112">To polecenie pobiera pełne dane wyjściowe zadania o określonym IDENTYFIKATORze zadania.</span><span class="sxs-lookup"><span data-stu-id="a91f3-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="a91f3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a91f3-113">PARAMETERS</span></span>

### <span data-ttu-id="a91f3-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a91f3-114">-AutomationAccountName</span></span>
<span data-ttu-id="a91f3-115">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera rekord wyjściowy zadania.</span><span class="sxs-lookup"><span data-stu-id="a91f3-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="a91f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a91f3-116">-DefaultProfile</span></span>
<span data-ttu-id="a91f3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a91f3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a91f3-118">-ID</span><span class="sxs-lookup"><span data-stu-id="a91f3-118">-Id</span></span>
<span data-ttu-id="a91f3-119">Określa identyfikator rekordu wyjściowego zadania dla tego polecenia cmdlet, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="a91f3-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="a91f3-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="a91f3-120">-JobId</span></span>
<span data-ttu-id="a91f3-121">Określa identyfikator zadania, dla którego ten polecenie cmdlet pobiera rekord wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="a91f3-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="a91f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a91f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="a91f3-123">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera rekord wyjściowy zadania.</span><span class="sxs-lookup"><span data-stu-id="a91f3-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="a91f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a91f3-124">CommonParameters</span></span>
<span data-ttu-id="a91f3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a91f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a91f3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a91f3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a91f3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a91f3-127">INPUTS</span></span>

### <span data-ttu-id="a91f3-128">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a91f3-128">System.Guid</span></span>

### <span data-ttu-id="a91f3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a91f3-129">System.String</span></span>

## <span data-ttu-id="a91f3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a91f3-130">OUTPUTS</span></span>

### <span data-ttu-id="a91f3-131">Microsoft. Azure. Commands. Automation. model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="a91f3-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="a91f3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a91f3-132">NOTES</span></span>

## <span data-ttu-id="a91f3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a91f3-133">RELATED LINKS</span></span>

[<span data-ttu-id="a91f3-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a91f3-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


