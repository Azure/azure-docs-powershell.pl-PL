---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199602"
---
# <span data-ttu-id="82567-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="82567-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="82567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82567-102">SYNOPSIS</span></span>
<span data-ttu-id="82567-103">Zawiesza zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="82567-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="82567-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="82567-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82567-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="82567-105">DESCRIPTION</span></span>
<span data-ttu-id="82567-106">Polecenie cmdlet **Suspend-AzAutomationJob** zawiesza zadanie automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="82567-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="82567-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="82567-107">Specify a running Automation job.</span></span>
<span data-ttu-id="82567-108">Aby wznowić zawieszone zadanie, użyj Resume-AzAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82567-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="82567-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="82567-109">EXAMPLES</span></span>

### <span data-ttu-id="82567-110">Przykład 1. Zawieszanie zadania</span><span class="sxs-lookup"><span data-stu-id="82567-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="82567-111">To polecenie powoduje zawieszenie zadania o określonym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="82567-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="82567-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82567-112">PARAMETERS</span></span>

### <span data-ttu-id="82567-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82567-113">-AutomationAccountName</span></span>
<span data-ttu-id="82567-114">Określa nazwę konta automatyzacji, na którym to polecenie cmdlet zawiesza zadanie.</span><span class="sxs-lookup"><span data-stu-id="82567-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="82567-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82567-115">-DefaultProfile</span></span>
<span data-ttu-id="82567-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="82567-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82567-117">— Id</span><span class="sxs-lookup"><span data-stu-id="82567-117">-Id</span></span>
<span data-ttu-id="82567-118">Określa identyfikator zadania, które to polecenie cmdlet zawiesza.</span><span class="sxs-lookup"><span data-stu-id="82567-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="82567-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82567-119">-ResourceGroupName</span></span>
<span data-ttu-id="82567-120">Określa identyfikator zadania, które to polecenie cmdlet zawiesza.</span><span class="sxs-lookup"><span data-stu-id="82567-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="82567-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82567-121">CommonParameters</span></span>
<span data-ttu-id="82567-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82567-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82567-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82567-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82567-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82567-124">INPUTS</span></span>

### <span data-ttu-id="82567-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="82567-125">System.Guid</span></span>

### <span data-ttu-id="82567-126">System.String</span><span class="sxs-lookup"><span data-stu-id="82567-126">System.String</span></span>

## <span data-ttu-id="82567-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82567-127">OUTPUTS</span></span>

### <span data-ttu-id="82567-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="82567-128">System.Void</span></span>

## <span data-ttu-id="82567-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="82567-129">NOTES</span></span>

## <span data-ttu-id="82567-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82567-130">RELATED LINKS</span></span>

[<span data-ttu-id="82567-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="82567-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="82567-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="82567-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="82567-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="82567-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="82567-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="82567-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


