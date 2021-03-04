---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: c0169a799db59a66f0d44191e58dae3760ec4128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990536"
---
# <span data-ttu-id="d0e13-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d0e13-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="d0e13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0e13-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e13-103">Zatrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d0e13-103">Stops an Automation job.</span></span>

## <span data-ttu-id="d0e13-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0e13-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0e13-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0e13-105">DESCRIPTION</span></span>
<span data-ttu-id="d0e13-106">Polecenie **cmdlet Stop-AzAutomationJob** zatrzymuje zadanie azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d0e13-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="d0e13-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d0e13-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="d0e13-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0e13-108">EXAMPLES</span></span>

### <span data-ttu-id="d0e13-109">Przykład 1. Zatrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="d0e13-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d0e13-110">To polecenie zatrzymuje zadanie o określonym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="d0e13-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="d0e13-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0e13-111">PARAMETERS</span></span>

### <span data-ttu-id="d0e13-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d0e13-112">-AutomationAccountName</span></span>
<span data-ttu-id="d0e13-113">Określa nazwę konta automatyzacji, na którym to polecenie cmdlet zatrzymuje zadanie.</span><span class="sxs-lookup"><span data-stu-id="d0e13-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="d0e13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e13-114">-DefaultProfile</span></span>
<span data-ttu-id="d0e13-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d0e13-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0e13-116">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="d0e13-116">-Id</span></span>
<span data-ttu-id="d0e13-117">Określa identyfikator zadania, które ma być zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0e13-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d0e13-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e13-118">-ResourceGroupName</span></span>
<span data-ttu-id="d0e13-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0e13-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d0e13-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e13-120">CommonParameters</span></span>
<span data-ttu-id="d0e13-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e13-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e13-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e13-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e13-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0e13-123">INPUTS</span></span>

### <span data-ttu-id="d0e13-124">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d0e13-124">System.Guid</span></span>

### <span data-ttu-id="d0e13-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d0e13-125">System.String</span></span>

## <span data-ttu-id="d0e13-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0e13-126">OUTPUTS</span></span>

### <span data-ttu-id="d0e13-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="d0e13-127">System.Void</span></span>

## <span data-ttu-id="d0e13-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0e13-128">NOTES</span></span>

## <span data-ttu-id="d0e13-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0e13-129">RELATED LINKS</span></span>

[<span data-ttu-id="d0e13-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d0e13-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="d0e13-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d0e13-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="d0e13-132">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d0e13-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="d0e13-133">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d0e13-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


