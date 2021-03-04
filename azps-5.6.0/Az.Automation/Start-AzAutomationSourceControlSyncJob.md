---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: f232f876ff77944beb1d506e5763621f9470cd21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957665"
---
# <span data-ttu-id="efeef-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="efeef-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="efeef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efeef-102">SYNOPSIS</span></span>
<span data-ttu-id="efeef-103">Uruchamia zadanie synchronizacji kontrolki źródła automatyzacji Azure.</span><span class="sxs-lookup"><span data-stu-id="efeef-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="efeef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="efeef-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efeef-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="efeef-105">DESCRIPTION</span></span>
<span data-ttu-id="efeef-106">Polecenie Start-AzAutomationSourceControlSyncJob uruchamia zadanie synchronizacji kontrolki źródła automatyzacji Azure dla danej nazwy kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="efeef-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="efeef-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="efeef-107">EXAMPLES</span></span>

### <span data-ttu-id="efeef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="efeef-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="efeef-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efeef-109">PARAMETERS</span></span>

### <span data-ttu-id="efeef-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="efeef-110">-AutomationAccountName</span></span>
<span data-ttu-id="efeef-111">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="efeef-111">The automation account name.</span></span>

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

### <span data-ttu-id="efeef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efeef-112">-DefaultProfile</span></span>
<span data-ttu-id="efeef-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="efeef-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efeef-114">- JobId</span><span class="sxs-lookup"><span data-stu-id="efeef-114">-JobId</span></span>
<span data-ttu-id="efeef-115">Identyfikator zadania synchronizacji kontrolki źródłowej.</span><span class="sxs-lookup"><span data-stu-id="efeef-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="efeef-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efeef-116">-ResourceGroupName</span></span>
<span data-ttu-id="efeef-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="efeef-117">The resource group name.</span></span>

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

### <span data-ttu-id="efeef-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="efeef-118">-SourceControlName</span></span>
<span data-ttu-id="efeef-119">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="efeef-119">The source control name.</span></span>

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

### <span data-ttu-id="efeef-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efeef-120">-Confirm</span></span>
<span data-ttu-id="efeef-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="efeef-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efeef-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efeef-122">-WhatIf</span></span>
<span data-ttu-id="efeef-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efeef-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efeef-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="efeef-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efeef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efeef-125">CommonParameters</span></span>
<span data-ttu-id="efeef-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efeef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efeef-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efeef-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efeef-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efeef-128">INPUTS</span></span>

### <span data-ttu-id="efeef-129">System.String</span><span class="sxs-lookup"><span data-stu-id="efeef-129">System.String</span></span>

## <span data-ttu-id="efeef-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efeef-130">OUTPUTS</span></span>

### <span data-ttu-id="efeef-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="efeef-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="efeef-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="efeef-132">NOTES</span></span>

## <span data-ttu-id="efeef-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efeef-133">RELATED LINKS</span></span>
