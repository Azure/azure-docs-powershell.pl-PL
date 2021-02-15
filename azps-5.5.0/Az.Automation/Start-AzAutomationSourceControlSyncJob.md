---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182083"
---
# <span data-ttu-id="fc84f-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="fc84f-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="fc84f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc84f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc84f-103">Uruchamia zadanie synchronizacji kontrolki źródła automatyzacji Azure.</span><span class="sxs-lookup"><span data-stu-id="fc84f-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="fc84f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fc84f-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc84f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fc84f-105">DESCRIPTION</span></span>
<span data-ttu-id="fc84f-106">Polecenie Start-AzAutomationSourceControlSyncJob uruchamia zadanie synchronizacji kontrolki źródła automatyzacji Azure dla danej nazwy kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="fc84f-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="fc84f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fc84f-107">EXAMPLES</span></span>

### <span data-ttu-id="fc84f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc84f-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="fc84f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc84f-109">PARAMETERS</span></span>

### <span data-ttu-id="fc84f-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fc84f-110">-AutomationAccountName</span></span>
<span data-ttu-id="fc84f-111">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="fc84f-111">The automation account name.</span></span>

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

### <span data-ttu-id="fc84f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc84f-112">-DefaultProfile</span></span>
<span data-ttu-id="fc84f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc84f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc84f-114">- JobId</span><span class="sxs-lookup"><span data-stu-id="fc84f-114">-JobId</span></span>
<span data-ttu-id="fc84f-115">Identyfikator zadania synchronizacji kontrolki źródłowej.</span><span class="sxs-lookup"><span data-stu-id="fc84f-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="fc84f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc84f-116">-ResourceGroupName</span></span>
<span data-ttu-id="fc84f-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc84f-117">The resource group name.</span></span>

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

### <span data-ttu-id="fc84f-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="fc84f-118">-SourceControlName</span></span>
<span data-ttu-id="fc84f-119">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="fc84f-119">The source control name.</span></span>

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

### <span data-ttu-id="fc84f-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc84f-120">-Confirm</span></span>
<span data-ttu-id="fc84f-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fc84f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc84f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc84f-122">-WhatIf</span></span>
<span data-ttu-id="fc84f-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc84f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc84f-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fc84f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc84f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc84f-125">CommonParameters</span></span>
<span data-ttu-id="fc84f-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc84f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc84f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc84f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc84f-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc84f-128">INPUTS</span></span>

### <span data-ttu-id="fc84f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fc84f-129">System.String</span></span>

## <span data-ttu-id="fc84f-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc84f-130">OUTPUTS</span></span>

### <span data-ttu-id="fc84f-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="fc84f-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="fc84f-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fc84f-132">NOTES</span></span>

## <span data-ttu-id="fc84f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc84f-133">RELATED LINKS</span></span>
