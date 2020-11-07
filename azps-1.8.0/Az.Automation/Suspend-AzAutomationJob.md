---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 850ff932bdae35bd21ab83c745b5da8c056d778d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710449"
---
# <span data-ttu-id="33886-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="33886-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="33886-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33886-102">SYNOPSIS</span></span>
<span data-ttu-id="33886-103">Wstrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="33886-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="33886-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33886-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33886-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33886-105">DESCRIPTION</span></span>
<span data-ttu-id="33886-106">Polecenie cmdlet **Suspend-AzAutomationJob** zawiesza zadanie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="33886-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="33886-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="33886-107">Specify a running Automation job.</span></span>
<span data-ttu-id="33886-108">Aby wznowić zawieszone zadanie, użyj polecenia cmdlet Resume-AzAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="33886-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="33886-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33886-109">EXAMPLES</span></span>

### <span data-ttu-id="33886-110">Przykład 1: Wstrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="33886-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="33886-111">To polecenie zawiesza zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="33886-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="33886-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33886-112">PARAMETERS</span></span>

### <span data-ttu-id="33886-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="33886-113">-AutomationAccountName</span></span>
<span data-ttu-id="33886-114">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet zawiesza zadanie.</span><span class="sxs-lookup"><span data-stu-id="33886-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="33886-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33886-115">-DefaultProfile</span></span>
<span data-ttu-id="33886-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="33886-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33886-117">-ID</span><span class="sxs-lookup"><span data-stu-id="33886-117">-Id</span></span>
<span data-ttu-id="33886-118">Określa identyfikator zadania zawieszanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33886-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33886-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33886-119">-ResourceGroupName</span></span>
<span data-ttu-id="33886-120">Określa identyfikator zadania zawieszanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33886-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="33886-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33886-121">CommonParameters</span></span>
<span data-ttu-id="33886-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33886-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33886-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33886-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33886-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33886-124">INPUTS</span></span>

### <span data-ttu-id="33886-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="33886-125">System.Guid</span></span>

### <span data-ttu-id="33886-126">System. String</span><span class="sxs-lookup"><span data-stu-id="33886-126">System.String</span></span>

## <span data-ttu-id="33886-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33886-127">OUTPUTS</span></span>

### <span data-ttu-id="33886-128">System. void</span><span class="sxs-lookup"><span data-stu-id="33886-128">System.Void</span></span>

## <span data-ttu-id="33886-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33886-129">NOTES</span></span>

## <span data-ttu-id="33886-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33886-130">RELATED LINKS</span></span>

[<span data-ttu-id="33886-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="33886-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="33886-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="33886-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="33886-133">Życiorys — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="33886-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="33886-134">Zatrzymaj — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="33886-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

