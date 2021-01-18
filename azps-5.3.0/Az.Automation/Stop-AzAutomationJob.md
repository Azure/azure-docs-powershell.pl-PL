---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502234"
---
# <span data-ttu-id="911bc-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="911bc-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="911bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="911bc-102">SYNOPSIS</span></span>
<span data-ttu-id="911bc-103">Zatrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="911bc-103">Stops an Automation job.</span></span>

## <span data-ttu-id="911bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="911bc-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="911bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="911bc-105">DESCRIPTION</span></span>
<span data-ttu-id="911bc-106">Polecenie cmdlet **stop-AzAutomationJob** zatrzymuje zadanie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="911bc-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="911bc-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="911bc-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="911bc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="911bc-108">EXAMPLES</span></span>

### <span data-ttu-id="911bc-109">Przykład 1: Zatrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="911bc-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="911bc-110">To polecenie zatrzymuje zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="911bc-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="911bc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="911bc-111">PARAMETERS</span></span>

### <span data-ttu-id="911bc-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="911bc-112">-AutomationAccountName</span></span>
<span data-ttu-id="911bc-113">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet zatrzymuje zadanie.</span><span class="sxs-lookup"><span data-stu-id="911bc-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="911bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="911bc-114">-DefaultProfile</span></span>
<span data-ttu-id="911bc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="911bc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="911bc-116">-ID</span><span class="sxs-lookup"><span data-stu-id="911bc-116">-Id</span></span>
<span data-ttu-id="911bc-117">Określa identyfikator zadania, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="911bc-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="911bc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="911bc-118">-ResourceGroupName</span></span>
<span data-ttu-id="911bc-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="911bc-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="911bc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="911bc-120">CommonParameters</span></span>
<span data-ttu-id="911bc-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="911bc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="911bc-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="911bc-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="911bc-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="911bc-123">INPUTS</span></span>

### <span data-ttu-id="911bc-124">System. GUID</span><span class="sxs-lookup"><span data-stu-id="911bc-124">System.Guid</span></span>

### <span data-ttu-id="911bc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="911bc-125">System.String</span></span>

## <span data-ttu-id="911bc-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="911bc-126">OUTPUTS</span></span>

### <span data-ttu-id="911bc-127">System. void</span><span class="sxs-lookup"><span data-stu-id="911bc-127">System.Void</span></span>

## <span data-ttu-id="911bc-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="911bc-128">NOTES</span></span>

## <span data-ttu-id="911bc-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="911bc-129">RELATED LINKS</span></span>

[<span data-ttu-id="911bc-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="911bc-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="911bc-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="911bc-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="911bc-132">Życiorys — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="911bc-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="911bc-133">Suspend — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="911bc-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


