---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184923"
---
# <span data-ttu-id="671cd-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="671cd-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="671cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="671cd-102">SYNOPSIS</span></span>
<span data-ttu-id="671cd-103">Tworzy obiekt typu Azns Action Group</span><span class="sxs-lookup"><span data-stu-id="671cd-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="671cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="671cd-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="671cd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="671cd-105">DESCRIPTION</span></span>
<span data-ttu-id="671cd-106">Tworzy obiekt typu Azns Action Group.</span><span class="sxs-lookup"><span data-stu-id="671cd-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="671cd-107">Ten obiekt zostanie przekazany do polecenia tworzącego regułę alertu dziennika.</span><span class="sxs-lookup"><span data-stu-id="671cd-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="671cd-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="671cd-108">EXAMPLES</span></span>

### <span data-ttu-id="671cd-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="671cd-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="671cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="671cd-110">PARAMETERS</span></span>

### <span data-ttu-id="671cd-111">- ActionGroup</span><span class="sxs-lookup"><span data-stu-id="671cd-111">-ActionGroup</span></span>
<span data-ttu-id="671cd-112">Lista grup akcji, do których chcesz wysłać powiadomienie</span><span class="sxs-lookup"><span data-stu-id="671cd-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="671cd-113">- CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="671cd-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="671cd-114">Dostosowany ład w sieci Webhook</span><span class="sxs-lookup"><span data-stu-id="671cd-114">The customized webhook payload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="671cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="671cd-115">-DefaultProfile</span></span>
<span data-ttu-id="671cd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="671cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="671cd-117">- EmailSubject</span><span class="sxs-lookup"><span data-stu-id="671cd-117">-EmailSubject</span></span>
<span data-ttu-id="671cd-118">Temat wiadomości e-mail z powiadomieniem o alertach</span><span class="sxs-lookup"><span data-stu-id="671cd-118">The email subject of alert notification</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="671cd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="671cd-119">CommonParameters</span></span>
<span data-ttu-id="671cd-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="671cd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="671cd-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="671cd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="671cd-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="671cd-122">INPUTS</span></span>

### <span data-ttu-id="671cd-123">Brak</span><span class="sxs-lookup"><span data-stu-id="671cd-123">None</span></span>

## <span data-ttu-id="671cd-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="671cd-124">OUTPUTS</span></span>

### <span data-ttu-id="671cd-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="671cd-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="671cd-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="671cd-126">NOTES</span></span>

## <span data-ttu-id="671cd-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="671cd-127">RELATED LINKS</span></span>
