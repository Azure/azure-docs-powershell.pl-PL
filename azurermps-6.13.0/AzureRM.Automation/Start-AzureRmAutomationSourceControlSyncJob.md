---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 4a5864e9572a21442a5333232fe5f705fb1b5687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524609"
---
# <span data-ttu-id="fb4ee-101">Start-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="fb4ee-101">Start-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="fb4ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4ee-103">Rozpoczyna zadanie synchronizacji kontroli źródła usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-103">Starts an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb4ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb4ee-104">SYNTAX</span></span>

```
Start-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb4ee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fb4ee-105">DESCRIPTION</span></span>
<span data-ttu-id="fb4ee-106">Polecenie cmdlet Start-AzureRmAutomationSourceControlSyncJob uruchamia zadanie synchronizacji kontrolki źródłowych Azure Automation dla podanej nazwy kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-106">The Start-AzureRmAutomationSourceControlSyncJob cmdlet starts a Azure Automation souce control sync job for the given source control name.</span></span>

## <span data-ttu-id="fb4ee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb4ee-107">EXAMPLES</span></span>

### <span data-ttu-id="fb4ee-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb4ee-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="fb4ee-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb4ee-109">PARAMETERS</span></span>

### <span data-ttu-id="fb4ee-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fb4ee-110">-AutomationAccountName</span></span>
<span data-ttu-id="fb4ee-111">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-111">The automation account name.</span></span>

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

### <span data-ttu-id="fb4ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4ee-112">-DefaultProfile</span></span>
<span data-ttu-id="fb4ee-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb4ee-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="fb4ee-114">-JobId</span></span>
<span data-ttu-id="fb4ee-115">Identyfikator zadania synchronizacji kontroli źródła.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="fb4ee-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4ee-116">-ResourceGroupName</span></span>
<span data-ttu-id="fb4ee-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-117">The resource group name.</span></span>

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

### <span data-ttu-id="fb4ee-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="fb4ee-118">-SourceControlName</span></span>
<span data-ttu-id="fb4ee-119">Nazwa kontrolki źródła.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-119">The source control name.</span></span>

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

### <span data-ttu-id="fb4ee-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb4ee-120">-Confirm</span></span>
<span data-ttu-id="fb4ee-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb4ee-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb4ee-122">-WhatIf</span></span>
<span data-ttu-id="fb4ee-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb4ee-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb4ee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4ee-125">CommonParameters</span></span>
<span data-ttu-id="fb4ee-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4ee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4ee-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4ee-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4ee-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb4ee-128">INPUTS</span></span>

### <span data-ttu-id="fb4ee-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fb4ee-129">System.String</span></span>

## <span data-ttu-id="fb4ee-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb4ee-130">OUTPUTS</span></span>

### <span data-ttu-id="fb4ee-131">Microsoft. Azure. Commands. Automation. model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="fb4ee-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="fb4ee-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb4ee-132">NOTES</span></span>

## <span data-ttu-id="fb4ee-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb4ee-133">RELATED LINKS</span></span>
