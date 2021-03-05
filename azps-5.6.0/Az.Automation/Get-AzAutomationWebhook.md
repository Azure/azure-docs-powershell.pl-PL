---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 00125a7ad3d74d3e710b782d0be7fdb20004ef4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014113"
---
# <span data-ttu-id="7b075-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7b075-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="7b075-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b075-102">SYNOPSIS</span></span>
<span data-ttu-id="7b075-103">Pobiera webhoox z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="7b075-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="7b075-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7b075-104">SYNTAX</span></span>

### <span data-ttu-id="7b075-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7b075-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b075-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7b075-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b075-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="7b075-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b075-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7b075-108">DESCRIPTION</span></span>
<span data-ttu-id="7b075-109">Polecenie **cmdlet Get-AzAutomationWebhook** pobiera webhokowy.</span><span class="sxs-lookup"><span data-stu-id="7b075-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="7b075-110">Aby uzyskać określoną nazwę sieci Webhoox, określ nazwę narzędzia WebHook lub nazwę podręcznika azure Automation Runbook, aby połączyć się z tym siecią Webhoox.</span><span class="sxs-lookup"><span data-stu-id="7b075-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span><br>
<span data-ttu-id="7b075-111">**Uwaga:** Ze względu na problemy z zabezpieczeniami wartość WebhookUri jest zwracana jako pusty ciąg.</span><span class="sxs-lookup"><span data-stu-id="7b075-111">**Note:** The WebhookUri is returned as empty string due to security concerns.</span></span> <span data-ttu-id="7b075-112">Pamiętaj o zapisaniu adresu URL webhook zwracanego przez polecenie cmdlet **New-AzAutomationWebhook,** ponieważ nie można go pobrać za pomocą polecenia **Get-AzAutomationWebhook.**</span><span class="sxs-lookup"><span data-stu-id="7b075-112">Please make sure to save the webhook URL that **New-AzAutomationWebhook** cmdlet returns, because it cannot be retrieved by using **Get-AzAutomationWebhook**.</span></span>

## <span data-ttu-id="7b075-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7b075-113">EXAMPLES</span></span>

### <span data-ttu-id="7b075-114">Przykład 1. Uzyskiwanie wszystkich składników WebHoox dla podręcznika runbook</span><span class="sxs-lookup"><span data-stu-id="7b075-114">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="7b075-115">To polecenie pobiera wszystkie zasoby sieci Web dla podręcznika runbook o nazwie Runbook03 w koncie automatyzacji o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7b075-115">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7b075-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b075-116">PARAMETERS</span></span>

### <span data-ttu-id="7b075-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7b075-117">-AutomationAccountName</span></span>
<span data-ttu-id="7b075-118">Określa nazwę konta automatyzacji, na którym to polecenie cmdlet uzyskuje nazwę webhook.</span><span class="sxs-lookup"><span data-stu-id="7b075-118">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="7b075-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b075-119">-DefaultProfile</span></span>
<span data-ttu-id="7b075-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="7b075-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b075-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7b075-121">-Name</span></span>
<span data-ttu-id="7b075-122">Określa nazwę sieci Web, do których uzyskuje się to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b075-122">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b075-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b075-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b075-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera nazwę webhoox.</span><span class="sxs-lookup"><span data-stu-id="7b075-124">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="7b075-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="7b075-125">-RunbookName</span></span>
<span data-ttu-id="7b075-126">Określa nazwę podręcznika, dla którego to polecenie cmdlet pobiera nazwę webhoox.</span><span class="sxs-lookup"><span data-stu-id="7b075-126">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b075-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b075-127">CommonParameters</span></span>
<span data-ttu-id="7b075-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b075-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b075-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b075-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b075-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b075-130">INPUTS</span></span>

### <span data-ttu-id="7b075-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7b075-131">System.String</span></span>

## <span data-ttu-id="7b075-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b075-132">OUTPUTS</span></span>

### <span data-ttu-id="7b075-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="7b075-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="7b075-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7b075-134">NOTES</span></span>

## <span data-ttu-id="7b075-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b075-135">RELATED LINKS</span></span>

[<span data-ttu-id="7b075-136">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7b075-136">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="7b075-137">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7b075-137">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="7b075-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7b075-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


