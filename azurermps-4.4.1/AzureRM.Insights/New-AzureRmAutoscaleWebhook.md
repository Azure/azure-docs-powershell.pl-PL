---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 2fc67e4f50d3c0a045ed6f0e6d82d5bf46d10c25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549999"
---
# <span data-ttu-id="920ce-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="920ce-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="920ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="920ce-102">SYNOPSIS</span></span>
<span data-ttu-id="920ce-103">Umożliwia utworzenie elementu webhook autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="920ce-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="920ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="920ce-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="920ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="920ce-105">DESCRIPTION</span></span>
<span data-ttu-id="920ce-106">Polecenie cmdlet **New-AzureRmAutoscaleWebhook** umożliwia utworzenie elementu webscale.</span><span class="sxs-lookup"><span data-stu-id="920ce-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="920ce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="920ce-107">EXAMPLES</span></span>

## <span data-ttu-id="920ce-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="920ce-108">PARAMETERS</span></span>

### <span data-ttu-id="920ce-109">-Properties</span><span class="sxs-lookup"><span data-stu-id="920ce-109">-Properties</span></span>
<span data-ttu-id="920ce-110">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="920ce-110">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="920ce-111">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="920ce-111">-ServiceUri</span></span>
<span data-ttu-id="920ce-112">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="920ce-112">Specifies the service URI.</span></span>

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

### <span data-ttu-id="920ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="920ce-113">-DefaultProfile</span></span>
<span data-ttu-id="920ce-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="920ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="920ce-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="920ce-115">CommonParameters</span></span>
<span data-ttu-id="920ce-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="920ce-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="920ce-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="920ce-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="920ce-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="920ce-118">INPUTS</span></span>

## <span data-ttu-id="920ce-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="920ce-119">OUTPUTS</span></span>

### <span data-ttu-id="920ce-120">Microsoft. Azure. Management. Monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="920ce-120">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="920ce-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="920ce-121">NOTES</span></span>

## <span data-ttu-id="920ce-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="920ce-122">RELATED LINKS</span></span>

[<span data-ttu-id="920ce-123">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="920ce-123">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


