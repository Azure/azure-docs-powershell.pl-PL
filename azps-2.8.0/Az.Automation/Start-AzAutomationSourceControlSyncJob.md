---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 61e63d2b3c66c17ce32d8b4c7346adba5879f7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706685"
---
# <span data-ttu-id="22afc-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="22afc-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="22afc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22afc-102">SYNOPSIS</span></span>
<span data-ttu-id="22afc-103">Rozpoczyna zadanie synchronizacji kontroli źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="22afc-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="22afc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22afc-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22afc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22afc-105">DESCRIPTION</span></span>
<span data-ttu-id="22afc-106">Polecenie cmdlet Start-AzAutomationSourceControlSyncJob uruchamia zadanie synchronizacji kontroli źródła usługi Azure dla danej nazwy kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="22afc-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="22afc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22afc-107">EXAMPLES</span></span>

### <span data-ttu-id="22afc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22afc-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="22afc-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22afc-109">PARAMETERS</span></span>

### <span data-ttu-id="22afc-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22afc-110">-AutomationAccountName</span></span>
<span data-ttu-id="22afc-111">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="22afc-111">The automation account name.</span></span>

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

### <span data-ttu-id="22afc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22afc-112">-DefaultProfile</span></span>
<span data-ttu-id="22afc-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22afc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22afc-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="22afc-114">-JobId</span></span>
<span data-ttu-id="22afc-115">Identyfikator zadania synchronizacji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="22afc-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22afc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22afc-116">-ResourceGroupName</span></span>
<span data-ttu-id="22afc-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22afc-117">The resource group name.</span></span>

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

### <span data-ttu-id="22afc-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="22afc-118">-SourceControlName</span></span>
<span data-ttu-id="22afc-119">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="22afc-119">The source control name.</span></span>

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

### <span data-ttu-id="22afc-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22afc-120">-Confirm</span></span>
<span data-ttu-id="22afc-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22afc-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22afc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22afc-122">-WhatIf</span></span>
<span data-ttu-id="22afc-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22afc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22afc-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22afc-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22afc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22afc-125">CommonParameters</span></span>
<span data-ttu-id="22afc-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22afc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22afc-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22afc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22afc-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22afc-128">INPUTS</span></span>

### <span data-ttu-id="22afc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="22afc-129">System.String</span></span>

## <span data-ttu-id="22afc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22afc-130">OUTPUTS</span></span>

### <span data-ttu-id="22afc-131">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="22afc-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="22afc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22afc-132">NOTES</span></span>

## <span data-ttu-id="22afc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22afc-133">RELATED LINKS</span></span>