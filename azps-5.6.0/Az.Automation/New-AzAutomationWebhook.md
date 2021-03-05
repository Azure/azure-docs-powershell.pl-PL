---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 520efcb6cccc3c3d4c0afc3b532d528c11c305c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995737"
---
# <span data-ttu-id="a9952-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a9952-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="a9952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9952-102">SYNOPSIS</span></span>
<span data-ttu-id="a9952-103">Tworzy witrynę sieci Web dla podręcznika uruchamiania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a9952-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="a9952-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9952-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9952-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9952-105">DESCRIPTION</span></span>
<span data-ttu-id="a9952-106">Polecenie **cmdlet New-AzAutomationWebhook** tworzy witrynę webhook dla podręcznika Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a9952-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="a9952-107">Pamiętaj, aby zapisać adres URL webhook, który zwraca to polecenie cmdlet, ponieważ nie można go odzyskać ponownie.</span><span class="sxs-lookup"><span data-stu-id="a9952-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="a9952-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9952-108">EXAMPLES</span></span>

### <span data-ttu-id="a9952-109">Przykład 1. Tworzenie witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="a9952-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="a9952-110">To polecenie tworzy dla podręcznika o nazwie ContosoRunbook webhook o nazwie Webhook06 na koncie automatyzacji o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a9952-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a9952-111">Polecenie przechowuje webhook w $Webhook zmienną.</span><span class="sxs-lookup"><span data-stu-id="a9952-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="a9952-112">Webhook jest włączony.</span><span class="sxs-lookup"><span data-stu-id="a9952-112">The webhook is enabled.</span></span>
<span data-ttu-id="a9952-113">Webhook wygasa w określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="a9952-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="a9952-114">To polecenie nie zawiera żadnych wartości parametrów webhook.</span><span class="sxs-lookup"><span data-stu-id="a9952-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="a9952-115">To polecenie określa *parametr Force.*</span><span class="sxs-lookup"><span data-stu-id="a9952-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a9952-116">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9952-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a9952-117">Przykład 2. Tworzenie webhooku z parametrami</span><span class="sxs-lookup"><span data-stu-id="a9952-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="a9952-118">Pierwsze polecenie tworzy słownik parametrów i zapisuje je w $Params zmienną.</span><span class="sxs-lookup"><span data-stu-id="a9952-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="a9952-119">Drugie polecenie tworzy webhook Webhook o nazwie Webhook11 dla podręcznika o nazwie ContosoRunbook w koncie automatyzacji o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a9952-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a9952-120">To polecenie przypisuje parametry w $Params sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a9952-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="a9952-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9952-121">PARAMETERS</span></span>

### <span data-ttu-id="a9952-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9952-122">-AutomationAccountName</span></span>
<span data-ttu-id="a9952-123">Określa nazwę konta automatyzacji, na którym to polecenie cmdlet tworzy element webhook.</span><span class="sxs-lookup"><span data-stu-id="a9952-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="a9952-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9952-124">-DefaultProfile</span></span>
<span data-ttu-id="a9952-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a9952-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9952-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a9952-126">-ExpiryTime</span></span>
<span data-ttu-id="a9952-127">Określa czas wygaśnięcia obiektu **DateTimeOffset** dla sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a9952-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a9952-128">Możesz określić ciąg lub wartość **datetime,** która może zostać przekonwertowana na prawidłowy **dateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="a9952-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9952-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a9952-129">-Force</span></span>
<span data-ttu-id="a9952-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="a9952-130">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9952-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a9952-131">-IsEnabled</span></span>
<span data-ttu-id="a9952-132">Określa, czy sieć Webhook jest włączona.</span><span class="sxs-lookup"><span data-stu-id="a9952-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9952-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9952-133">-Name</span></span>
<span data-ttu-id="a9952-134">Określa nazwę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a9952-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="a9952-135">— Parametry</span><span class="sxs-lookup"><span data-stu-id="a9952-135">-Parameters</span></span>
<span data-ttu-id="a9952-136">Określa słownik par klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="a9952-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="a9952-137">Klucze to nazwy parametrów podręcznika obsługi.</span><span class="sxs-lookup"><span data-stu-id="a9952-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="a9952-138">Wartości są wartościami parametrów podręcznika uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="a9952-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="a9952-139">Po uruchomieniu podręcznika w odpowiedzi na witrynę internetową te parametry są przekazywane do tego podręcznika.</span><span class="sxs-lookup"><span data-stu-id="a9952-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9952-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9952-140">-ResourceGroupName</span></span>
<span data-ttu-id="a9952-141">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy witrynę webhook.</span><span class="sxs-lookup"><span data-stu-id="a9952-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="a9952-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a9952-142">-RunbookName</span></span>
<span data-ttu-id="a9952-143">Określa nazwę podręcznika do skojarzenia z siecią Webhook.</span><span class="sxs-lookup"><span data-stu-id="a9952-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9952-144">- RunOn</span><span class="sxs-lookup"><span data-stu-id="a9952-144">-RunOn</span></span>
<span data-ttu-id="a9952-145">Opcjonalna nazwa grupy pracowników hybrydowych, która powinna wykonywać podręcznik</span><span class="sxs-lookup"><span data-stu-id="a9952-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9952-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9952-146">-Confirm</span></span>
<span data-ttu-id="a9952-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9952-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9952-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9952-148">-WhatIf</span></span>
<span data-ttu-id="a9952-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9952-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9952-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a9952-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9952-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9952-151">CommonParameters</span></span>
<span data-ttu-id="a9952-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9952-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9952-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9952-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9952-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9952-154">INPUTS</span></span>

### <span data-ttu-id="a9952-155">System.String</span><span class="sxs-lookup"><span data-stu-id="a9952-155">System.String</span></span>

### <span data-ttu-id="a9952-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9952-156">System.Boolean</span></span>

### <span data-ttu-id="a9952-157">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a9952-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="a9952-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9952-158">OUTPUTS</span></span>

### <span data-ttu-id="a9952-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="a9952-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="a9952-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9952-160">NOTES</span></span>

## <span data-ttu-id="a9952-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9952-161">RELATED LINKS</span></span>

[<span data-ttu-id="a9952-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a9952-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="a9952-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a9952-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="a9952-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a9952-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


