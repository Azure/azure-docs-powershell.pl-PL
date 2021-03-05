---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: b5bfac31babfd4bc848f9619dc8eb8cecd1c3eaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012897"
---
# <span data-ttu-id="ecc5f-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ecc5f-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="ecc5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc5f-103">Tworzy obiekt typu Azns Action Group</span><span class="sxs-lookup"><span data-stu-id="ecc5f-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="ecc5f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ecc5f-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecc5f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ecc5f-105">DESCRIPTION</span></span>
<span data-ttu-id="ecc5f-106">Tworzy obiekt typu Azns Action Group.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="ecc5f-107">Ten obiekt zostanie przekazany do polecenia tworzącego regułę alertu dziennika.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="ecc5f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ecc5f-108">EXAMPLES</span></span>

### <span data-ttu-id="ecc5f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ecc5f-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="ecc5f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecc5f-110">PARAMETERS</span></span>

### <span data-ttu-id="ecc5f-111">- ActionGroup</span><span class="sxs-lookup"><span data-stu-id="ecc5f-111">-ActionGroup</span></span>
<span data-ttu-id="ecc5f-112">Lista grup akcji, do których chcesz wysłać powiadomienie</span><span class="sxs-lookup"><span data-stu-id="ecc5f-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="ecc5f-113">- CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="ecc5f-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="ecc5f-114">Dostosowany ład w sieci Webhook</span><span class="sxs-lookup"><span data-stu-id="ecc5f-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="ecc5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc5f-115">-DefaultProfile</span></span>
<span data-ttu-id="ecc5f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecc5f-117">- EmailSubject</span><span class="sxs-lookup"><span data-stu-id="ecc5f-117">-EmailSubject</span></span>
<span data-ttu-id="ecc5f-118">Temat wiadomości e-mail z powiadomieniem o alertach</span><span class="sxs-lookup"><span data-stu-id="ecc5f-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="ecc5f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc5f-119">CommonParameters</span></span>
<span data-ttu-id="ecc5f-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc5f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc5f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecc5f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc5f-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecc5f-122">INPUTS</span></span>

### <span data-ttu-id="ecc5f-123">Brak</span><span class="sxs-lookup"><span data-stu-id="ecc5f-123">None</span></span>

## <span data-ttu-id="ecc5f-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecc5f-124">OUTPUTS</span></span>

### <span data-ttu-id="ecc5f-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="ecc5f-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="ecc5f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ecc5f-126">NOTES</span></span>

## <span data-ttu-id="ecc5f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecc5f-127">RELATED LINKS</span></span>
