---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: b889a3b061556fc6c5ad4be1dfd118dac49f1f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528321"
---
# <span data-ttu-id="e35b1-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e35b1-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="e35b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e35b1-102">SYNOPSIS</span></span>
<span data-ttu-id="e35b1-103">Modyfikuje element webhook dla elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e35b1-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e35b1-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e35b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e35b1-105">DESCRIPTION</span></span>
<span data-ttu-id="e35b1-106">Polecenie cmdlet **Set-AzureRmAutomationWebhook** modyfikuje element webhook dla elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e35b1-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="e35b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e35b1-107">EXAMPLES</span></span>

### <span data-ttu-id="e35b1-108">Przykład 1. wyłączenie elementu webhook</span><span class="sxs-lookup"><span data-stu-id="e35b1-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="e35b1-109">To polecenie wyłącza element webhook o nazwie Webhook01 na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="e35b1-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="e35b1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e35b1-110">PARAMETERS</span></span>

### <span data-ttu-id="e35b1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e35b1-111">-AutomationAccountName</span></span>
<span data-ttu-id="e35b1-112">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet modyfikuje element webhook.</span><span class="sxs-lookup"><span data-stu-id="e35b1-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e35b1-113">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e35b1-113">-IsEnabled</span></span>
<span data-ttu-id="e35b1-114">Określa, czy element webhook jest włączony.</span><span class="sxs-lookup"><span data-stu-id="e35b1-114">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35b1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e35b1-115">-Name</span></span>
<span data-ttu-id="e35b1-116">Określa nazwę elementu webhook, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e35b1-116">Specifies a name of the webhook that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35b1-117">— Parametry</span><span class="sxs-lookup"><span data-stu-id="e35b1-117">-Parameters</span></span>
<span data-ttu-id="e35b1-118">Określa słownik par kluczy/wartości.</span><span class="sxs-lookup"><span data-stu-id="e35b1-118">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="e35b1-119">Klucze są nazwami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e35b1-119">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="e35b1-120">Wartości są wartościami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e35b1-120">The values are the runbook parameter values.</span></span>
<span data-ttu-id="e35b1-121">Po uruchomieniu elementu Runbook w odpowiedzi na element webhook te parametry są przekazywane do elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e35b1-121">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="e35b1-123">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje element webhook.</span><span class="sxs-lookup"><span data-stu-id="e35b1-123">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e35b1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35b1-124">-DefaultProfile</span></span>
<span data-ttu-id="e35b1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e35b1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e35b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35b1-126">CommonParameters</span></span>
<span data-ttu-id="e35b1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e35b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35b1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35b1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35b1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e35b1-129">INPUTS</span></span>

## <span data-ttu-id="e35b1-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e35b1-130">OUTPUTS</span></span>

### <span data-ttu-id="e35b1-131">Microsoft. Azure. Commands. Automation. model. webhook</span><span class="sxs-lookup"><span data-stu-id="e35b1-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="e35b1-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e35b1-132">NOTES</span></span>

## <span data-ttu-id="e35b1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e35b1-133">RELATED LINKS</span></span>

[<span data-ttu-id="e35b1-134">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e35b1-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="e35b1-135">Nowe — AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e35b1-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="e35b1-136">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e35b1-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


