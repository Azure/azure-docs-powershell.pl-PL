---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: 417ab3f7f787a76041caceebbfcf32f9733717b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553696"
---
# <span data-ttu-id="e9707-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e9707-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="e9707-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9707-102">SYNOPSIS</span></span>
<span data-ttu-id="e9707-103">Tworzy element webhook dla elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e9707-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9707-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9707-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9707-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e9707-105">DESCRIPTION</span></span>
<span data-ttu-id="e9707-106">Polecenie cmdlet **New-AzureRmAutomationWebhook** tworzy element webhook dla elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e9707-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="e9707-107">Upewnij się, że został zapisany adres URL elementu webhook, który jest zwracany przez to polecenie cmdlet, ponieważ nie można go ponownie pobrać.</span><span class="sxs-lookup"><span data-stu-id="e9707-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="e9707-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9707-108">EXAMPLES</span></span>

### <span data-ttu-id="e9707-109">Przykład 1: Tworzenie elementu webhook</span><span class="sxs-lookup"><span data-stu-id="e9707-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="e9707-110">To polecenie tworzy element webhook o nazwie Webhook06 dla elementu Runbook o nazwie ContosoRunbook na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="e9707-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="e9707-111">Polecenie zapisuje element webhook w zmiennej $Webhook.</span><span class="sxs-lookup"><span data-stu-id="e9707-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="e9707-112">Element webhook jest włączony.</span><span class="sxs-lookup"><span data-stu-id="e9707-112">The webhook is enabled.</span></span>
<span data-ttu-id="e9707-113">Element webhook wygaśnie o określonej godzinie.</span><span class="sxs-lookup"><span data-stu-id="e9707-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="e9707-114">To polecenie nie zawiera żadnych wartości parametrów elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="e9707-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="e9707-115">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="e9707-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e9707-116">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e9707-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e9707-117">Przykład 2: Tworzenie elementu webhook za pomocą parametrów</span><span class="sxs-lookup"><span data-stu-id="e9707-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="e9707-118">Pierwsze polecenie tworzy słownik parametrów i zapisuje je w zmiennej $Params.</span><span class="sxs-lookup"><span data-stu-id="e9707-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="e9707-119">Drugie polecenie tworzy element webhook o nazwie Webhook11 dla elementu Runbook o nazwie ContosoRunbook na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="e9707-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="e9707-120">Polecenie przypisuje parametry w $Params do elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="e9707-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="e9707-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9707-121">PARAMETERS</span></span>

### <span data-ttu-id="e9707-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9707-122">-AutomationAccountName</span></span>
<span data-ttu-id="e9707-123">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet tworzy element webhook.</span><span class="sxs-lookup"><span data-stu-id="e9707-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="e9707-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9707-124">-DefaultProfile</span></span>
<span data-ttu-id="e9707-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e9707-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9707-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e9707-126">-ExpiryTime</span></span>
<span data-ttu-id="e9707-127">Określa czas wygaśnięcia elementu webhook jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="e9707-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="e9707-128">Możesz określić ciąg lub **datę/godzinę** , które można przekonwertować na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="e9707-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9707-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e9707-129">-Force</span></span>
<span data-ttu-id="e9707-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="e9707-130">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9707-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e9707-131">-IsEnabled</span></span>
<span data-ttu-id="e9707-132">Określa, czy element webhook jest włączony.</span><span class="sxs-lookup"><span data-stu-id="e9707-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9707-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9707-133">-Name</span></span>
<span data-ttu-id="e9707-134">Określa nazwę elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="e9707-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="e9707-135">— Parametry</span><span class="sxs-lookup"><span data-stu-id="e9707-135">-Parameters</span></span>
<span data-ttu-id="e9707-136">Określa słownik par kluczy/wartości.</span><span class="sxs-lookup"><span data-stu-id="e9707-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="e9707-137">Klucze są nazwami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e9707-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="e9707-138">Wartości są wartościami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e9707-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="e9707-139">Po uruchomieniu elementu Runbook w odpowiedzi na element webhook te parametry są przekazywane do elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e9707-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9707-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9707-140">-ResourceGroupName</span></span>
<span data-ttu-id="e9707-141">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy element webhook.</span><span class="sxs-lookup"><span data-stu-id="e9707-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="e9707-142">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="e9707-142">-RunbookName</span></span>
<span data-ttu-id="e9707-143">Określa nazwę elementu Runbook, który ma być skojarzony z elementem webhook.</span><span class="sxs-lookup"><span data-stu-id="e9707-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9707-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="e9707-144">-RunOn</span></span>
<span data-ttu-id="e9707-145">Opcjonalna nazwa grupy hybrydowej procesu roboczego, która powinna uruchamiać element Runbook</span><span class="sxs-lookup"><span data-stu-id="e9707-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9707-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9707-146">-Confirm</span></span>
<span data-ttu-id="e9707-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9707-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9707-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9707-148">-WhatIf</span></span>
<span data-ttu-id="e9707-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9707-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9707-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9707-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9707-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9707-151">CommonParameters</span></span>
<span data-ttu-id="e9707-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9707-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9707-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9707-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9707-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9707-154">INPUTS</span></span>

### <span data-ttu-id="e9707-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e9707-155">None</span></span>
<span data-ttu-id="e9707-156">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e9707-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9707-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9707-157">OUTPUTS</span></span>

### <span data-ttu-id="e9707-158">Microsoft. Azure. Commands. Automation. model. webhook</span><span class="sxs-lookup"><span data-stu-id="e9707-158">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="e9707-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9707-159">NOTES</span></span>

## <span data-ttu-id="e9707-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9707-160">RELATED LINKS</span></span>

[<span data-ttu-id="e9707-161">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e9707-161">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="e9707-162">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e9707-162">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="e9707-163">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e9707-163">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


