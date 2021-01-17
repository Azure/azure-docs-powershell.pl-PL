---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 731a2df87ce6ad575e9aa3e10eb124e52ec1b60b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373177"
---
# <span data-ttu-id="25d41-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="25d41-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="25d41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25d41-102">SYNOPSIS</span></span>
<span data-ttu-id="25d41-103">Wznawia zawieszone zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="25d41-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="25d41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25d41-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25d41-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25d41-105">DESCRIPTION</span></span>
<span data-ttu-id="25d41-106">Polecenie cmdlet **Resume-AzAutomationJob** Wznawia zawieszone zadanie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="25d41-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="25d41-107">Określ zawieszone zadanie.</span><span class="sxs-lookup"><span data-stu-id="25d41-107">Specify the suspended job.</span></span>
<span data-ttu-id="25d41-108">Aby zawiesić zadanie, użyj polecenia cmdlet Suspend-AzAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="25d41-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="25d41-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25d41-109">EXAMPLES</span></span>

### <span data-ttu-id="25d41-110">Przykład 1: wznawianie zawieszonego zadania</span><span class="sxs-lookup"><span data-stu-id="25d41-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="25d41-111">To polecenie wznawia zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="25d41-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="25d41-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25d41-112">PARAMETERS</span></span>

### <span data-ttu-id="25d41-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="25d41-113">-AutomationAccountName</span></span>
<span data-ttu-id="25d41-114">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet wznawia zadanie.</span><span class="sxs-lookup"><span data-stu-id="25d41-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="25d41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d41-115">-DefaultProfile</span></span>
<span data-ttu-id="25d41-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25d41-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25d41-117">-ID</span><span class="sxs-lookup"><span data-stu-id="25d41-117">-Id</span></span>
<span data-ttu-id="25d41-118">Określa identyfikator zadania, które zostanie wznowione przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d41-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="25d41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d41-119">-ResourceGroupName</span></span>
<span data-ttu-id="25d41-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet wznawia zadanie.</span><span class="sxs-lookup"><span data-stu-id="25d41-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="25d41-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d41-121">CommonParameters</span></span>
<span data-ttu-id="25d41-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d41-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d41-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d41-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d41-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25d41-124">INPUTS</span></span>

### <span data-ttu-id="25d41-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="25d41-125">System.Guid</span></span>

### <span data-ttu-id="25d41-126">System. String</span><span class="sxs-lookup"><span data-stu-id="25d41-126">System.String</span></span>

## <span data-ttu-id="25d41-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25d41-127">OUTPUTS</span></span>

### <span data-ttu-id="25d41-128">System. void</span><span class="sxs-lookup"><span data-stu-id="25d41-128">System.Void</span></span>

## <span data-ttu-id="25d41-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25d41-129">NOTES</span></span>

## <span data-ttu-id="25d41-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25d41-130">RELATED LINKS</span></span>

[<span data-ttu-id="25d41-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="25d41-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="25d41-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="25d41-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="25d41-133">Zatrzymaj — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="25d41-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="25d41-134">Suspend — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="25d41-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


