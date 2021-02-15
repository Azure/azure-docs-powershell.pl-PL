---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244251"
---
# <span data-ttu-id="9371f-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9371f-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="9371f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9371f-102">SYNOPSIS</span></span>
<span data-ttu-id="9371f-103">Zatrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9371f-103">Stops an Automation job.</span></span>

## <span data-ttu-id="9371f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9371f-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9371f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9371f-105">DESCRIPTION</span></span>
<span data-ttu-id="9371f-106">Polecenie **cmdlet Stop-AzAutomationJob** zatrzymuje zadanie azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9371f-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="9371f-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9371f-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="9371f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9371f-108">EXAMPLES</span></span>

### <span data-ttu-id="9371f-109">Przykład 1. Zatrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="9371f-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9371f-110">To polecenie zatrzymuje zadanie o określonym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="9371f-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="9371f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9371f-111">PARAMETERS</span></span>

### <span data-ttu-id="9371f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9371f-112">-AutomationAccountName</span></span>
<span data-ttu-id="9371f-113">Określa nazwę konta automatyzacji, na którym to polecenie cmdlet zatrzymuje zadanie.</span><span class="sxs-lookup"><span data-stu-id="9371f-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="9371f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9371f-114">-DefaultProfile</span></span>
<span data-ttu-id="9371f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9371f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9371f-116">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="9371f-116">-Id</span></span>
<span data-ttu-id="9371f-117">Określa identyfikator zadania, które ma być zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9371f-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="9371f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9371f-118">-ResourceGroupName</span></span>
<span data-ttu-id="9371f-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9371f-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9371f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9371f-120">CommonParameters</span></span>
<span data-ttu-id="9371f-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9371f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9371f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9371f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9371f-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9371f-123">INPUTS</span></span>

### <span data-ttu-id="9371f-124">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9371f-124">System.Guid</span></span>

### <span data-ttu-id="9371f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="9371f-125">System.String</span></span>

## <span data-ttu-id="9371f-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9371f-126">OUTPUTS</span></span>

### <span data-ttu-id="9371f-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="9371f-127">System.Void</span></span>

## <span data-ttu-id="9371f-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9371f-128">NOTES</span></span>

## <span data-ttu-id="9371f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9371f-129">RELATED LINKS</span></span>

[<span data-ttu-id="9371f-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9371f-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="9371f-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="9371f-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="9371f-132">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9371f-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="9371f-133">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9371f-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


