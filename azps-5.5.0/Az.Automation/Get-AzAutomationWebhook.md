---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201138"
---
# <span data-ttu-id="82d7d-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="82d7d-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="82d7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="82d7d-103">Pobiera webhoox z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="82d7d-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="82d7d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="82d7d-104">SYNTAX</span></span>

### <span data-ttu-id="82d7d-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="82d7d-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82d7d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="82d7d-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82d7d-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="82d7d-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82d7d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="82d7d-108">DESCRIPTION</span></span>
<span data-ttu-id="82d7d-109">Polecenie **cmdlet Get-AzAutomationWebhook** pobiera webhoox.</span><span class="sxs-lookup"><span data-stu-id="82d7d-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="82d7d-110">Aby uzyskać określoną nazwę sieci Webhoox, określ nazwę narzędzia WebHook lub nazwę podręcznika azure Automation Runbook, aby połączyć się z nim sieci Webhoox.</span><span class="sxs-lookup"><span data-stu-id="82d7d-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="82d7d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="82d7d-111">EXAMPLES</span></span>

### <span data-ttu-id="82d7d-112">Przykład 1. Uzyskiwanie wszystkich składników WebHoox dla podręcznika runbook</span><span class="sxs-lookup"><span data-stu-id="82d7d-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="82d7d-113">To polecenie pobiera wszystkie zasoby sieci Web dla podręcznika runbook o nazwie Runbook03 w koncie automatyzacji o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="82d7d-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="82d7d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82d7d-114">PARAMETERS</span></span>

### <span data-ttu-id="82d7d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82d7d-115">-AutomationAccountName</span></span>
<span data-ttu-id="82d7d-116">Określa nazwę konta automatyzacji, na którym to polecenie cmdlet uzyskuje nazwę webhook.</span><span class="sxs-lookup"><span data-stu-id="82d7d-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="82d7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d7d-117">-DefaultProfile</span></span>
<span data-ttu-id="82d7d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="82d7d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82d7d-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="82d7d-119">-Name</span></span>
<span data-ttu-id="82d7d-120">Określa nazwę sieci Web, do których uzyskuje się to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82d7d-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="82d7d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d7d-121">-ResourceGroupName</span></span>
<span data-ttu-id="82d7d-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera nazwę webhoox.</span><span class="sxs-lookup"><span data-stu-id="82d7d-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="82d7d-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="82d7d-123">-RunbookName</span></span>
<span data-ttu-id="82d7d-124">Określa nazwę podręcznika, dla którego to polecenie cmdlet pobiera nazwę webhoox.</span><span class="sxs-lookup"><span data-stu-id="82d7d-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="82d7d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d7d-125">CommonParameters</span></span>
<span data-ttu-id="82d7d-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d7d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d7d-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82d7d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d7d-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82d7d-128">INPUTS</span></span>

### <span data-ttu-id="82d7d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="82d7d-129">System.String</span></span>

## <span data-ttu-id="82d7d-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82d7d-130">OUTPUTS</span></span>

### <span data-ttu-id="82d7d-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="82d7d-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="82d7d-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="82d7d-132">NOTES</span></span>

## <span data-ttu-id="82d7d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82d7d-133">RELATED LINKS</span></span>

[<span data-ttu-id="82d7d-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="82d7d-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="82d7d-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="82d7d-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="82d7d-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="82d7d-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


