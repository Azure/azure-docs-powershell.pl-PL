---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
ms.openlocfilehash: fe6170842bcacf4d7fb0c8e442dc988c03c67e35
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898481"
---
# <span data-ttu-id="082e2-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="082e2-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="082e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="082e2-102">SYNOPSIS</span></span>
<span data-ttu-id="082e2-103">Umożliwia utworzenie elementu webhook autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="082e2-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="082e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="082e2-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="082e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="082e2-105">DESCRIPTION</span></span>
<span data-ttu-id="082e2-106">Polecenie cmdlet **New-AzureRmAutoscaleWebhook** umożliwia utworzenie elementu webscale.</span><span class="sxs-lookup"><span data-stu-id="082e2-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="082e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="082e2-107">EXAMPLES</span></span>

## <span data-ttu-id="082e2-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="082e2-108">PARAMETERS</span></span>

### <span data-ttu-id="082e2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082e2-109">-DefaultProfile</span></span>
<span data-ttu-id="082e2-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="082e2-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="082e2-111">-Property</span><span class="sxs-lookup"><span data-stu-id="082e2-111">-Property</span></span>
<span data-ttu-id="082e2-112">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="082e2-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="082e2-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="082e2-113">-ServiceUri</span></span>
<span data-ttu-id="082e2-114">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="082e2-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="082e2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082e2-115">CommonParameters</span></span>
<span data-ttu-id="082e2-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="082e2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082e2-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="082e2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082e2-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="082e2-118">INPUTS</span></span>

### <span data-ttu-id="082e2-119">System. String</span><span class="sxs-lookup"><span data-stu-id="082e2-119">System.String</span></span>

### <span data-ttu-id="082e2-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="082e2-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="082e2-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="082e2-121">OUTPUTS</span></span>

### <span data-ttu-id="082e2-122">Microsoft. Azure. Management. Monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="082e2-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="082e2-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="082e2-123">NOTES</span></span>

## <span data-ttu-id="082e2-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="082e2-124">RELATED LINKS</span></span>

[<span data-ttu-id="082e2-125">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="082e2-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


