---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 8fa14eef62ac0e8a296349ff3a47cd67086bc3ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710556"
---
# <span data-ttu-id="d03c3-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="d03c3-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="d03c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d03c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d03c3-103">Pobiera zadania synchronizacji kontroli źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d03c3-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="d03c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d03c3-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d03c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d03c3-105">DESCRIPTION</span></span>
<span data-ttu-id="d03c3-106">Polecenie cmdlet Get-AzAutomationSourceControlSyncJob pobiera zadania synchronizacji kontroli źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d03c3-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="d03c3-107">Aby uzyskać określone zadanie synchronizacji kontroli źródła, określ jego identyfikator.</span><span class="sxs-lookup"><span data-stu-id="d03c3-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="d03c3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d03c3-108">EXAMPLES</span></span>

### <span data-ttu-id="d03c3-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d03c3-109">Example 1</span></span>
<span data-ttu-id="d03c3-110">To polecenie pobiera wszystkie zadania synchronizacji kontroli źródła automatyzacji dla VSTSNative kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="d03c3-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="d03c3-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d03c3-111">Example 2</span></span>
<span data-ttu-id="d03c3-112">To polecenie pobiera zadanie synchronizacji kontroli źródła z identyfikatorem 08d6d266-27b6-463c-Beea-bc48a67ace15 dla VSTSNative kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="d03c3-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="d03c3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d03c3-113">PARAMETERS</span></span>

### <span data-ttu-id="d03c3-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d03c3-114">-AutomationAccountName</span></span>
<span data-ttu-id="d03c3-115">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d03c3-115">The automation account name.</span></span>

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

### <span data-ttu-id="d03c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03c3-116">-DefaultProfile</span></span>
<span data-ttu-id="d03c3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d03c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d03c3-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="d03c3-118">-JobId</span></span>
<span data-ttu-id="d03c3-119">Identyfikator zadania synchronizacji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="d03c3-119">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d03c3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d03c3-120">-ResourceGroupName</span></span>
<span data-ttu-id="d03c3-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d03c3-121">The resource group name.</span></span>

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

### <span data-ttu-id="d03c3-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="d03c3-122">-SourceControlName</span></span>
<span data-ttu-id="d03c3-123">Nazwa kontrolki źródła zadania.</span><span class="sxs-lookup"><span data-stu-id="d03c3-123">The source control name of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d03c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03c3-124">CommonParameters</span></span>
<span data-ttu-id="d03c3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d03c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03c3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d03c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03c3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d03c3-127">INPUTS</span></span>

### <span data-ttu-id="d03c3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d03c3-128">System.String</span></span>

### <span data-ttu-id="d03c3-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d03c3-129">System.Guid</span></span>

## <span data-ttu-id="d03c3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d03c3-130">OUTPUTS</span></span>

### <span data-ttu-id="d03c3-131">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="d03c3-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="d03c3-132">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="d03c3-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="d03c3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d03c3-133">NOTES</span></span>

## <span data-ttu-id="d03c3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d03c3-134">RELATED LINKS</span></span>
