---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: a719d841df2d3f211fdb2592ed2a96b507c51e10
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891130"
---
# <span data-ttu-id="716b5-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="716b5-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="716b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="716b5-102">SYNOPSIS</span></span>
<span data-ttu-id="716b5-103">Umożliwia utworzenie elementu webhook autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="716b5-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="716b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="716b5-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="716b5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="716b5-105">DESCRIPTION</span></span>
<span data-ttu-id="716b5-106">Polecenie cmdlet **New-AzAutoscaleWebhook** umożliwia utworzenie elementu webscale.</span><span class="sxs-lookup"><span data-stu-id="716b5-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="716b5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="716b5-107">EXAMPLES</span></span>

## <span data-ttu-id="716b5-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="716b5-108">PARAMETERS</span></span>

### <span data-ttu-id="716b5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716b5-109">-DefaultProfile</span></span>
<span data-ttu-id="716b5-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="716b5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="716b5-111">-Property</span><span class="sxs-lookup"><span data-stu-id="716b5-111">-Property</span></span>
<span data-ttu-id="716b5-112">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="716b5-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="716b5-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="716b5-113">-ServiceUri</span></span>
<span data-ttu-id="716b5-114">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="716b5-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="716b5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716b5-115">CommonParameters</span></span>
<span data-ttu-id="716b5-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="716b5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716b5-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="716b5-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716b5-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="716b5-118">INPUTS</span></span>

### <span data-ttu-id="716b5-119">System. String</span><span class="sxs-lookup"><span data-stu-id="716b5-119">System.String</span></span>

### <span data-ttu-id="716b5-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="716b5-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="716b5-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="716b5-121">OUTPUTS</span></span>

### <span data-ttu-id="716b5-122">Microsoft. Azure. Management. Monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="716b5-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="716b5-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="716b5-123">NOTES</span></span>

## <span data-ttu-id="716b5-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="716b5-124">RELATED LINKS</span></span>

[<span data-ttu-id="716b5-125">Nowe — AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="716b5-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


