---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053620"
---
# <span data-ttu-id="06867-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="06867-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="06867-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06867-102">SYNOPSIS</span></span>
<span data-ttu-id="06867-103">Wstrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="06867-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="06867-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06867-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06867-105">Opis</span><span class="sxs-lookup"><span data-stu-id="06867-105">DESCRIPTION</span></span>
<span data-ttu-id="06867-106">Polecenie cmdlet **Suspend-AzAutomationJob** zawiesza zadanie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="06867-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="06867-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="06867-107">Specify a running Automation job.</span></span>
<span data-ttu-id="06867-108">Aby wznowić zawieszone zadanie, użyj polecenia cmdlet Resume-AzAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="06867-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="06867-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06867-109">EXAMPLES</span></span>

### <span data-ttu-id="06867-110">Przykład 1: Wstrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="06867-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="06867-111">To polecenie zawiesza zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="06867-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="06867-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06867-112">PARAMETERS</span></span>

### <span data-ttu-id="06867-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="06867-113">-AutomationAccountName</span></span>
<span data-ttu-id="06867-114">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet zawiesza zadanie.</span><span class="sxs-lookup"><span data-stu-id="06867-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="06867-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06867-115">-DefaultProfile</span></span>
<span data-ttu-id="06867-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="06867-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06867-117">-ID</span><span class="sxs-lookup"><span data-stu-id="06867-117">-Id</span></span>
<span data-ttu-id="06867-118">Określa identyfikator zadania zawieszanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06867-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="06867-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06867-119">-ResourceGroupName</span></span>
<span data-ttu-id="06867-120">Określa identyfikator zadania zawieszanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06867-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="06867-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06867-121">CommonParameters</span></span>
<span data-ttu-id="06867-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06867-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06867-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06867-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06867-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06867-124">INPUTS</span></span>

### <span data-ttu-id="06867-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="06867-125">System.Guid</span></span>

### <span data-ttu-id="06867-126">System. String</span><span class="sxs-lookup"><span data-stu-id="06867-126">System.String</span></span>

## <span data-ttu-id="06867-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06867-127">OUTPUTS</span></span>

### <span data-ttu-id="06867-128">System. void</span><span class="sxs-lookup"><span data-stu-id="06867-128">System.Void</span></span>

## <span data-ttu-id="06867-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06867-129">NOTES</span></span>

## <span data-ttu-id="06867-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06867-130">RELATED LINKS</span></span>

[<span data-ttu-id="06867-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="06867-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="06867-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="06867-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="06867-133">Życiorys — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="06867-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="06867-134">Zatrzymaj — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="06867-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


