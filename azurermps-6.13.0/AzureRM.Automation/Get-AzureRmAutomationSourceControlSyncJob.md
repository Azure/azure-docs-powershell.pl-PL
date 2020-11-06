---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 213df264e4ecd458c8505d521556f49265577333
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550368"
---
# <span data-ttu-id="7ea07-101">Get-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="7ea07-101">Get-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="7ea07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ea07-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea07-103">Pobiera zadania synchronizacji kontroli źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7ea07-103">Gets Azure Automation source control sync jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ea07-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ea07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ea07-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea07-106">Polecenie cmdlet Get-AzureRmAutomationSourceControlSyncJob pobiera zadania synchronizacji kontroli źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7ea07-106">The Get-AzureRmAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="7ea07-107">Aby uzyskać określone zadanie synchronizacji kontroli źródła, określ jego identyfikator.</span><span class="sxs-lookup"><span data-stu-id="7ea07-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="7ea07-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ea07-108">EXAMPLES</span></span>

### <span data-ttu-id="7ea07-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ea07-109">Example 1</span></span>
<span data-ttu-id="7ea07-110">To polecenie pobiera wszystkie zadania synchronizacji kontroli źródła automatyzacji dla VSTSNative kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="7ea07-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="7ea07-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7ea07-111">Example 2</span></span>
<span data-ttu-id="7ea07-112">To polecenie pobiera zadanie synchronizacji kontroli źródła z identyfikatorem 08d6d266-27b6-463c-Beea-bc48a67ace15 dla VSTSNative kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="7ea07-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="7ea07-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ea07-113">PARAMETERS</span></span>

### <span data-ttu-id="7ea07-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ea07-114">-AutomationAccountName</span></span>
<span data-ttu-id="7ea07-115">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="7ea07-115">The automation account name.</span></span>

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

### <span data-ttu-id="7ea07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea07-116">-DefaultProfile</span></span>
<span data-ttu-id="7ea07-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea07-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="7ea07-118">-JobId</span></span>
<span data-ttu-id="7ea07-119">Identyfikator zadania synchronizacji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="7ea07-119">The source control sync job id.</span></span>

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

### <span data-ttu-id="7ea07-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea07-120">-ResourceGroupName</span></span>
<span data-ttu-id="7ea07-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ea07-121">The resource group name.</span></span>

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

### <span data-ttu-id="7ea07-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="7ea07-122">-SourceControlName</span></span>
<span data-ttu-id="7ea07-123">Nazwa kontrolki źródła zadania.</span><span class="sxs-lookup"><span data-stu-id="7ea07-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="7ea07-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea07-124">CommonParameters</span></span>
<span data-ttu-id="7ea07-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea07-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea07-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea07-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea07-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ea07-127">INPUTS</span></span>

### <span data-ttu-id="7ea07-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea07-128">System.String</span></span>

### <span data-ttu-id="7ea07-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7ea07-129">System.Guid</span></span>

## <span data-ttu-id="7ea07-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ea07-130">OUTPUTS</span></span>

### <span data-ttu-id="7ea07-131">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="7ea07-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="7ea07-132">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="7ea07-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="7ea07-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ea07-133">NOTES</span></span>

## <span data-ttu-id="7ea07-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ea07-134">RELATED LINKS</span></span>
