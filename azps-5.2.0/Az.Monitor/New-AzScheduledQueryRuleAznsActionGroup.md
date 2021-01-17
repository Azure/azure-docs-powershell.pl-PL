---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371870"
---
# <span data-ttu-id="9173d-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="9173d-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="9173d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9173d-102">SYNOPSIS</span></span>
<span data-ttu-id="9173d-103">Tworzy obiekt typu grupa akcji Azns</span><span class="sxs-lookup"><span data-stu-id="9173d-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="9173d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9173d-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9173d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9173d-105">DESCRIPTION</span></span>
<span data-ttu-id="9173d-106">Tworzy obiekt typu grupa akcji Azns.</span><span class="sxs-lookup"><span data-stu-id="9173d-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="9173d-107">Ten obiekt ma zostać przekazany do polecenia, które umożliwia utworzenie reguły alertów dziennika.</span><span class="sxs-lookup"><span data-stu-id="9173d-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="9173d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9173d-108">EXAMPLES</span></span>

### <span data-ttu-id="9173d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9173d-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="9173d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9173d-110">PARAMETERS</span></span>

### <span data-ttu-id="9173d-111">-Action</span><span class="sxs-lookup"><span data-stu-id="9173d-111">-ActionGroup</span></span>
<span data-ttu-id="9173d-112">Lista grup akcji, do których ma zostać wysłane powiadomienie</span><span class="sxs-lookup"><span data-stu-id="9173d-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="9173d-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="9173d-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="9173d-114">Dostosowany ładunek elementu webhook</span><span class="sxs-lookup"><span data-stu-id="9173d-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="9173d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9173d-115">-DefaultProfile</span></span>
<span data-ttu-id="9173d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9173d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9173d-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="9173d-117">-EmailSubject</span></span>
<span data-ttu-id="9173d-118">Temat wiadomości e-mail z powiadomieniem o alercie</span><span class="sxs-lookup"><span data-stu-id="9173d-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="9173d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9173d-119">CommonParameters</span></span>
<span data-ttu-id="9173d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9173d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9173d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9173d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9173d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9173d-122">INPUTS</span></span>

### <span data-ttu-id="9173d-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9173d-123">None</span></span>

## <span data-ttu-id="9173d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9173d-124">OUTPUTS</span></span>

### <span data-ttu-id="9173d-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="9173d-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="9173d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9173d-126">NOTES</span></span>

## <span data-ttu-id="9173d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9173d-127">RELATED LINKS</span></span>
