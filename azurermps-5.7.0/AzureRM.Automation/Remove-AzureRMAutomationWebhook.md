---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: 465e3ecd3f80b03eecb58309b18c91cd69c0d5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719582"
---
# <span data-ttu-id="f8a53-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="f8a53-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="f8a53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8a53-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a53-103">Usuwa element webhook z elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f8a53-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8a53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8a53-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8a53-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8a53-105">DESCRIPTION</span></span>
<span data-ttu-id="f8a53-106">Polecenie cmdlet **Remove-AzureRmAutomationWebhook** usuwa element webhook z elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f8a53-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="f8a53-107">Element webhook zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="f8a53-107">The webhook is deleted.</span></span>

## <span data-ttu-id="f8a53-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8a53-108">EXAMPLES</span></span>

### <span data-ttu-id="f8a53-109">Przykład 1: usuwanie elementu webhook</span><span class="sxs-lookup"><span data-stu-id="f8a53-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="f8a53-110">To polecenie usuwa element webhook o nazwie Webhook11 na koncie automatyzacji o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="f8a53-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="f8a53-111">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="f8a53-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f8a53-112">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f8a53-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f8a53-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8a53-113">PARAMETERS</span></span>

### <span data-ttu-id="f8a53-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8a53-114">-AutomationAccountName</span></span>
<span data-ttu-id="f8a53-115">Określa nazwę konta automatyzacji, na podstawie którego to polecenie cmdlet usuwa element webhook.</span><span class="sxs-lookup"><span data-stu-id="f8a53-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="f8a53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a53-116">-DefaultProfile</span></span>
<span data-ttu-id="f8a53-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f8a53-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8a53-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8a53-118">-Name</span></span>
<span data-ttu-id="f8a53-119">Określa nazwę elementu webhook, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8a53-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f8a53-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a53-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8a53-121">Określa nazwę grupy zasobów, dla której ten aplet polecenia usunie element webhook.</span><span class="sxs-lookup"><span data-stu-id="f8a53-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="f8a53-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8a53-122">-Confirm</span></span>
<span data-ttu-id="f8a53-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8a53-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a53-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8a53-124">-WhatIf</span></span>
<span data-ttu-id="f8a53-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8a53-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8a53-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8a53-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a53-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a53-127">CommonParameters</span></span>
<span data-ttu-id="f8a53-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8a53-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a53-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8a53-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a53-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8a53-130">INPUTS</span></span>

### <span data-ttu-id="f8a53-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f8a53-131">None</span></span>
<span data-ttu-id="f8a53-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f8a53-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8a53-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8a53-133">OUTPUTS</span></span>

## <span data-ttu-id="f8a53-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8a53-134">NOTES</span></span>

## <span data-ttu-id="f8a53-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8a53-135">RELATED LINKS</span></span>

[<span data-ttu-id="f8a53-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="f8a53-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="f8a53-137">Nowe — AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="f8a53-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="f8a53-138">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="f8a53-138">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


