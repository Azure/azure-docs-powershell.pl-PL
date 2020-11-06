---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 8b94ad5728e7852bb3cd834e7479a29cc11c1698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549747"
---
# <span data-ttu-id="bf9c4-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="bf9c4-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="bf9c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf9c4-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9c4-103">Umożliwia utworzenie elementu webhook autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf9c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf9c4-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf9c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf9c4-105">DESCRIPTION</span></span>
<span data-ttu-id="bf9c4-106">Polecenie cmdlet **New-AzureRmAutoscaleWebhook** umożliwia utworzenie elementu webscale.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="bf9c4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf9c4-107">EXAMPLES</span></span>

## <span data-ttu-id="bf9c4-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf9c4-108">PARAMETERS</span></span>

### <span data-ttu-id="bf9c4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9c4-109">-DefaultProfile</span></span>
<span data-ttu-id="bf9c4-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bf9c4-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9c4-111">-Property</span><span class="sxs-lookup"><span data-stu-id="bf9c4-111">-Property</span></span>
<span data-ttu-id="bf9c4-112">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="bf9c4-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Properties

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9c4-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="bf9c4-113">-ServiceUri</span></span>
<span data-ttu-id="bf9c4-114">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-114">Specifies the service URI.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9c4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9c4-115">CommonParameters</span></span>
<span data-ttu-id="bf9c4-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9c4-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf9c4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9c4-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf9c4-118">INPUTS</span></span>

### <span data-ttu-id="bf9c4-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bf9c4-119">None</span></span>
<span data-ttu-id="bf9c4-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf9c4-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf9c4-121">OUTPUTS</span></span>

### <span data-ttu-id="bf9c4-122">Microsoft. Azure. Management. Monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="bf9c4-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="bf9c4-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf9c4-123">NOTES</span></span>

## <span data-ttu-id="bf9c4-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf9c4-124">RELATED LINKS</span></span>

[<span data-ttu-id="bf9c4-125">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="bf9c4-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


