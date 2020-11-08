---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062420"
---
# <span data-ttu-id="25dc7-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="25dc7-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="25dc7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="25dc7-103">Umożliwia pobieranie punktów webhook z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="25dc7-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="25dc7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25dc7-104">SYNTAX</span></span>

### <span data-ttu-id="25dc7-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="25dc7-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25dc7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="25dc7-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25dc7-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="25dc7-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25dc7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="25dc7-108">DESCRIPTION</span></span>
<span data-ttu-id="25dc7-109">Polecenie cmdlet **Get-AzAutomationWebhook** pobiera webhooks.</span><span class="sxs-lookup"><span data-stu-id="25dc7-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="25dc7-110">Aby uzyskać konkretne elementy webhook, określ nazwę elementu webhook lub określ nazwę elementu Runbook usługi Azure Automation, aby uzyskać połączenie z nim elementów webhook.</span><span class="sxs-lookup"><span data-stu-id="25dc7-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="25dc7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25dc7-111">EXAMPLES</span></span>

### <span data-ttu-id="25dc7-112">Przykład 1: pobieranie wszystkich elementów webhook dla elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="25dc7-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="25dc7-113">To polecenie pobiera wszystkie elementy webhook dla elementu Runbook o nazwie Runbook03 na koncie automatyzacji o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="25dc7-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="25dc7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25dc7-114">PARAMETERS</span></span>

### <span data-ttu-id="25dc7-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="25dc7-115">-AutomationAccountName</span></span>
<span data-ttu-id="25dc7-116">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet pobiera element webhook.</span><span class="sxs-lookup"><span data-stu-id="25dc7-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="25dc7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25dc7-117">-DefaultProfile</span></span>
<span data-ttu-id="25dc7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25dc7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25dc7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25dc7-119">-Name</span></span>
<span data-ttu-id="25dc7-120">Określa nazwę elementu webhook, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25dc7-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="25dc7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25dc7-121">-ResourceGroupName</span></span>
<span data-ttu-id="25dc7-122">Określa nazwę grupy zasobów, dla której to polecenie cmdlet ma pobierać element webhook.</span><span class="sxs-lookup"><span data-stu-id="25dc7-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="25dc7-123">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="25dc7-123">-RunbookName</span></span>
<span data-ttu-id="25dc7-124">Określa nazwę elementu Runbook, dla którego to polecenie cmdlet pobiera elementy webhook.</span><span class="sxs-lookup"><span data-stu-id="25dc7-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="25dc7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25dc7-125">CommonParameters</span></span>
<span data-ttu-id="25dc7-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25dc7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25dc7-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25dc7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25dc7-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25dc7-128">INPUTS</span></span>

### <span data-ttu-id="25dc7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="25dc7-129">System.String</span></span>

## <span data-ttu-id="25dc7-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25dc7-130">OUTPUTS</span></span>

### <span data-ttu-id="25dc7-131">Microsoft. Azure. Commands. Automation. model. webhook</span><span class="sxs-lookup"><span data-stu-id="25dc7-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="25dc7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25dc7-132">NOTES</span></span>

## <span data-ttu-id="25dc7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25dc7-133">RELATED LINKS</span></span>

[<span data-ttu-id="25dc7-134">Nowe — AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="25dc7-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="25dc7-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="25dc7-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="25dc7-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="25dc7-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


