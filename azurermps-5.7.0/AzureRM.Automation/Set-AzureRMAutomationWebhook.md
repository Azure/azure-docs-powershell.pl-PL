---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: d0443d5c15dec1324a5fe306ddec7303426449b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548235"
---
# <span data-ttu-id="daf5b-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="daf5b-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="daf5b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="daf5b-102">SYNOPSIS</span></span>
<span data-ttu-id="daf5b-103">Modyfikuje element webhook dla elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="daf5b-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daf5b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="daf5b-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="daf5b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="daf5b-105">DESCRIPTION</span></span>
<span data-ttu-id="daf5b-106">Polecenie cmdlet **Set-AzureRmAutomationWebhook** modyfikuje element webhook dla elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="daf5b-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="daf5b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="daf5b-107">EXAMPLES</span></span>

### <span data-ttu-id="daf5b-108">Przykład 1. wyłączenie elementu webhook</span><span class="sxs-lookup"><span data-stu-id="daf5b-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="daf5b-109">To polecenie wyłącza element webhook o nazwie Webhook01 na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="daf5b-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="daf5b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="daf5b-110">PARAMETERS</span></span>

### <span data-ttu-id="daf5b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="daf5b-111">-AutomationAccountName</span></span>
<span data-ttu-id="daf5b-112">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet modyfikuje element webhook.</span><span class="sxs-lookup"><span data-stu-id="daf5b-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf5b-113">-DefaultProfile</span></span>
<span data-ttu-id="daf5b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="daf5b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daf5b-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="daf5b-115">-IsEnabled</span></span>
<span data-ttu-id="daf5b-116">Określa, czy element webhook jest włączony.</span><span class="sxs-lookup"><span data-stu-id="daf5b-116">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf5b-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="daf5b-117">-Name</span></span>
<span data-ttu-id="daf5b-118">Określa nazwę elementu webhook, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daf5b-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf5b-119">— Parametry</span><span class="sxs-lookup"><span data-stu-id="daf5b-119">-Parameters</span></span>
<span data-ttu-id="daf5b-120">Określa słownik par kluczy/wartości.</span><span class="sxs-lookup"><span data-stu-id="daf5b-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="daf5b-121">Klucze są nazwami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="daf5b-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="daf5b-122">Wartości są wartościami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="daf5b-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="daf5b-123">Po uruchomieniu elementu Runbook w odpowiedzi na element webhook te parametry są przekazywane do elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="daf5b-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="daf5b-125">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje element webhook.</span><span class="sxs-lookup"><span data-stu-id="daf5b-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="daf5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf5b-126">CommonParameters</span></span>
<span data-ttu-id="daf5b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daf5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf5b-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf5b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf5b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daf5b-129">INPUTS</span></span>

### <span data-ttu-id="daf5b-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="daf5b-130">None</span></span>
<span data-ttu-id="daf5b-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="daf5b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="daf5b-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="daf5b-132">OUTPUTS</span></span>

### <span data-ttu-id="daf5b-133">Microsoft. Azure. Commands. Automation. model. webhook</span><span class="sxs-lookup"><span data-stu-id="daf5b-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="daf5b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="daf5b-134">NOTES</span></span>

## <span data-ttu-id="daf5b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daf5b-135">RELATED LINKS</span></span>

[<span data-ttu-id="daf5b-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="daf5b-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="daf5b-137">Nowe — AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="daf5b-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="daf5b-138">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="daf5b-138">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

