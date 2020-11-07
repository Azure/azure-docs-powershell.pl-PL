---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 607976539e6bf93a0fa947741a4af4d4a7d34b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716950"
---
# <span data-ttu-id="831d1-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="831d1-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="831d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="831d1-102">SYNOPSIS</span></span>
<span data-ttu-id="831d1-103">Umożliwia utworzenie elementu webhook autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="831d1-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="831d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="831d1-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="831d1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="831d1-105">DESCRIPTION</span></span>
<span data-ttu-id="831d1-106">Polecenie cmdlet **New-AzureRmAutoscaleWebhook** umożliwia utworzenie elementu webscale.</span><span class="sxs-lookup"><span data-stu-id="831d1-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="831d1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="831d1-107">EXAMPLES</span></span>

## <span data-ttu-id="831d1-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="831d1-108">PARAMETERS</span></span>

### <span data-ttu-id="831d1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831d1-109">-DefaultProfile</span></span>
<span data-ttu-id="831d1-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="831d1-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="831d1-111">-Property</span><span class="sxs-lookup"><span data-stu-id="831d1-111">-Property</span></span>
<span data-ttu-id="831d1-112">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="831d1-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="831d1-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="831d1-113">-ServiceUri</span></span>
<span data-ttu-id="831d1-114">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="831d1-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="831d1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831d1-115">CommonParameters</span></span>
<span data-ttu-id="831d1-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="831d1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831d1-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="831d1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831d1-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="831d1-118">INPUTS</span></span>

### <span data-ttu-id="831d1-119">System. String</span><span class="sxs-lookup"><span data-stu-id="831d1-119">System.String</span></span>

### <span data-ttu-id="831d1-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="831d1-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="831d1-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="831d1-121">OUTPUTS</span></span>

### <span data-ttu-id="831d1-122">Microsoft. Azure. Management. Monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="831d1-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="831d1-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="831d1-123">NOTES</span></span>

## <span data-ttu-id="831d1-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="831d1-124">RELATED LINKS</span></span>

[<span data-ttu-id="831d1-125">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="831d1-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


