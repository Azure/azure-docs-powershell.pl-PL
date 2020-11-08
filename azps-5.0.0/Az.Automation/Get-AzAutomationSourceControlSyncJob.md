---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: a6d8a618ea9561c244b161407807ddfbe99b854a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232323"
---
# <span data-ttu-id="2545b-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="2545b-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="2545b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2545b-102">SYNOPSIS</span></span>
<span data-ttu-id="2545b-103">Pobiera zadania synchronizacji kontroli źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2545b-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="2545b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2545b-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2545b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2545b-105">DESCRIPTION</span></span>
<span data-ttu-id="2545b-106">Polecenie cmdlet Get-AzAutomationSourceControlSyncJob pobiera zadania synchronizacji kontroli źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2545b-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="2545b-107">Aby uzyskać określone zadanie synchronizacji kontroli źródła, określ jego identyfikator.</span><span class="sxs-lookup"><span data-stu-id="2545b-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="2545b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2545b-108">EXAMPLES</span></span>

### <span data-ttu-id="2545b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2545b-109">Example 1</span></span>
<span data-ttu-id="2545b-110">To polecenie pobiera wszystkie zadania synchronizacji kontroli źródła automatyzacji dla VSTSNative kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2545b-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="2545b-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2545b-111">Example 2</span></span>
<span data-ttu-id="2545b-112">To polecenie pobiera zadanie synchronizacji kontroli źródła z identyfikatorem 08d6d266-27b6-463c-Beea-bc48a67ace15 dla VSTSNative kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2545b-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative" `
                                                  -JobId "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

### <span data-ttu-id="2545b-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2545b-113">Example 3</span></span>

<span data-ttu-id="2545b-114">Pobiera zadania synchronizacji kontroli źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2545b-114">Gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="2545b-115">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="2545b-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAutomationSourceControlSyncJob -AutomationAccountName 'devAccount' -JobId 00000000-0000-0000-0000-00000000000000000 -ResourceGroupName 'rg1' -SourceControlName 'VSTSNative'
```

## <span data-ttu-id="2545b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2545b-116">PARAMETERS</span></span>

### <span data-ttu-id="2545b-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2545b-117">-AutomationAccountName</span></span>
<span data-ttu-id="2545b-118">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2545b-118">The automation account name.</span></span>

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

### <span data-ttu-id="2545b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2545b-119">-DefaultProfile</span></span>
<span data-ttu-id="2545b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2545b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2545b-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="2545b-121">-JobId</span></span>
<span data-ttu-id="2545b-122">Identyfikator zadania synchronizacji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="2545b-122">The source control sync job id.</span></span>

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

### <span data-ttu-id="2545b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2545b-123">-ResourceGroupName</span></span>
<span data-ttu-id="2545b-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2545b-124">The resource group name.</span></span>

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

### <span data-ttu-id="2545b-125">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="2545b-125">-SourceControlName</span></span>
<span data-ttu-id="2545b-126">Nazwa kontrolki źródła zadania.</span><span class="sxs-lookup"><span data-stu-id="2545b-126">The source control name of the job.</span></span>

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

### <span data-ttu-id="2545b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2545b-127">CommonParameters</span></span>
<span data-ttu-id="2545b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2545b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2545b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2545b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2545b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2545b-130">INPUTS</span></span>

### <span data-ttu-id="2545b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2545b-131">System.String</span></span>

### <span data-ttu-id="2545b-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2545b-132">System.Guid</span></span>

## <span data-ttu-id="2545b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2545b-133">OUTPUTS</span></span>

### <span data-ttu-id="2545b-134">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="2545b-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="2545b-135">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="2545b-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="2545b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2545b-136">NOTES</span></span>

## <span data-ttu-id="2545b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2545b-137">RELATED LINKS</span></span>
