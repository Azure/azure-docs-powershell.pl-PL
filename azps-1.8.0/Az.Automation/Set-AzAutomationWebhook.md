---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 39e0fda02eb41ed591562d9cfc1f7902fa43c38a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710458"
---
# <span data-ttu-id="8461c-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="8461c-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="8461c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8461c-102">SYNOPSIS</span></span>
<span data-ttu-id="8461c-103">Modyfikuje element webhook dla elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="8461c-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="8461c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8461c-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8461c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8461c-105">DESCRIPTION</span></span>
<span data-ttu-id="8461c-106">Polecenie cmdlet **Set-AzAutomationWebhook** modyfikuje element webhook dla elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8461c-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="8461c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8461c-107">EXAMPLES</span></span>

### <span data-ttu-id="8461c-108">Przykład 1. wyłączenie elementu webhook</span><span class="sxs-lookup"><span data-stu-id="8461c-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="8461c-109">To polecenie wyłącza element webhook o nazwie Webhook01 na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="8461c-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="8461c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8461c-110">PARAMETERS</span></span>

### <span data-ttu-id="8461c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8461c-111">-AutomationAccountName</span></span>
<span data-ttu-id="8461c-112">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet modyfikuje element webhook.</span><span class="sxs-lookup"><span data-stu-id="8461c-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="8461c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8461c-113">-DefaultProfile</span></span>
<span data-ttu-id="8461c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8461c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8461c-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="8461c-115">-IsEnabled</span></span>
<span data-ttu-id="8461c-116">Określa, czy element webhook jest włączony.</span><span class="sxs-lookup"><span data-stu-id="8461c-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="8461c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8461c-117">-Name</span></span>
<span data-ttu-id="8461c-118">Określa nazwę elementu webhook, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8461c-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8461c-119">— Parametry</span><span class="sxs-lookup"><span data-stu-id="8461c-119">-Parameters</span></span>
<span data-ttu-id="8461c-120">Określa słownik par kluczy/wartości.</span><span class="sxs-lookup"><span data-stu-id="8461c-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="8461c-121">Klucze są nazwami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="8461c-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="8461c-122">Wartości są wartościami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="8461c-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="8461c-123">Po uruchomieniu elementu Runbook w odpowiedzi na element webhook te parametry są przekazywane do elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="8461c-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="8461c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8461c-124">-ResourceGroupName</span></span>
<span data-ttu-id="8461c-125">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje element webhook.</span><span class="sxs-lookup"><span data-stu-id="8461c-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="8461c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8461c-126">CommonParameters</span></span>
<span data-ttu-id="8461c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8461c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8461c-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8461c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8461c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8461c-129">INPUTS</span></span>

### <span data-ttu-id="8461c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8461c-130">System.String</span></span>

### <span data-ttu-id="8461c-131">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8461c-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8461c-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="8461c-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="8461c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8461c-133">OUTPUTS</span></span>

### <span data-ttu-id="8461c-134">Microsoft. Azure. Commands. Automation. model. webhook</span><span class="sxs-lookup"><span data-stu-id="8461c-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="8461c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8461c-135">NOTES</span></span>

## <span data-ttu-id="8461c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8461c-136">RELATED LINKS</span></span>

[<span data-ttu-id="8461c-137">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="8461c-137">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="8461c-138">Nowe — AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="8461c-138">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="8461c-139">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="8461c-139">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


