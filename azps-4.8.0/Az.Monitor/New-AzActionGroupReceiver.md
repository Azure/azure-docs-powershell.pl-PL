---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220776"
---
# <span data-ttu-id="61f84-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="61f84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61f84-102">SYNOPSIS</span></span>
<span data-ttu-id="61f84-103">Tworzy nowy odbiorcę grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="61f84-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="61f84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61f84-104">SYNTAX</span></span>

### <span data-ttu-id="61f84-105">NewEmailReceiver (domyślny)</span><span class="sxs-lookup"><span data-stu-id="61f84-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f84-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f84-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f84-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f84-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f84-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f84-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f84-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f84-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f84-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61f84-115">Opis</span><span class="sxs-lookup"><span data-stu-id="61f84-115">DESCRIPTION</span></span>
<span data-ttu-id="61f84-116">Polecenie cmdlet **New-AzActionGroupReceiver** umożliwia utworzenie nowego adresata grupy akcji w pamięci.</span><span class="sxs-lookup"><span data-stu-id="61f84-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="61f84-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61f84-117">EXAMPLES</span></span>

### <span data-ttu-id="61f84-118">Przykład 1: Utwórz nowy odbiornik poczty E-mail w pamięci.</span><span class="sxs-lookup"><span data-stu-id="61f84-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="61f84-119">To polecenie tworzy nowy odbiornik poczty E-mail w pamięci.</span><span class="sxs-lookup"><span data-stu-id="61f84-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="61f84-120">Przykład 2: Utwórz nowy odbiornik SMS w pamięci.</span><span class="sxs-lookup"><span data-stu-id="61f84-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="61f84-121">To polecenie tworzy nowy odbiornik SMS w pamięci.</span><span class="sxs-lookup"><span data-stu-id="61f84-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="61f84-122">Przykład 3: Tworzenie nowego odbiornika webhook w pamięci.</span><span class="sxs-lookup"><span data-stu-id="61f84-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="61f84-123">To polecenie tworzy nowy odbiornik elementu webhook w pamięci.</span><span class="sxs-lookup"><span data-stu-id="61f84-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="61f84-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61f84-124">PARAMETERS</span></span>

### <span data-ttu-id="61f84-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="61f84-126">Tworzenie ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="61f84-127">-AutomationAccountId</span></span>
<span data-ttu-id="61f84-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="61f84-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="61f84-130">Tworzenie AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="61f84-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="61f84-132">Identyfikator URI, pod którym mają być wysyłane punkty internetowe</span><span class="sxs-lookup"><span data-stu-id="61f84-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="61f84-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="61f84-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="61f84-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="61f84-136">Tworzenie AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="61f84-138">Tworzenie ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="61f84-139">-CallbackUrl</span></span>
<span data-ttu-id="61f84-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="61f84-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="61f84-141">-ConnectionId</span></span>
<span data-ttu-id="61f84-142">Identyfikator połączenia ITSM tego odbiornika</span><span class="sxs-lookup"><span data-stu-id="61f84-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="61f84-143">-CountryCode</span></span>
<span data-ttu-id="61f84-144">Określa numer kierunkowy kraju odbiorcy wiadomości SMS.</span><span class="sxs-lookup"><span data-stu-id="61f84-144">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f84-145">-DefaultProfile</span></span>
<span data-ttu-id="61f84-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="61f84-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61f84-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="61f84-147">-EmailAddress</span></span>
<span data-ttu-id="61f84-148">Określa adres odbiorcy poczty E-mail.</span><span class="sxs-lookup"><span data-stu-id="61f84-148">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-149">-EmailReceiver</span></span>
<span data-ttu-id="61f84-150">Określa, aby utworzyć odbiorcę poczty E-mail</span><span class="sxs-lookup"><span data-stu-id="61f84-150">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="61f84-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="61f84-152">Identyfikator zasobu aplikacji funkcji</span><span class="sxs-lookup"><span data-stu-id="61f84-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-153">-NazwaFunkcji</span><span class="sxs-lookup"><span data-stu-id="61f84-153">-FunctionName</span></span>
<span data-ttu-id="61f84-154">Funkcja .Name</span><span class="sxs-lookup"><span data-stu-id="61f84-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="61f84-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="61f84-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="61f84-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="61f84-157">-IdentifierUri</span></span>
<span data-ttu-id="61f84-158">Identyfikator URI identyfikatora dla uwierzytelniania w usłudze AAD</span><span class="sxs-lookup"><span data-stu-id="61f84-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="61f84-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="61f84-160">wskazuje, czy to wystąpienie jest globalnym elementem Runbook</span><span class="sxs-lookup"><span data-stu-id="61f84-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-161">-ItsmReceiver</span></span>
<span data-ttu-id="61f84-162">Tworzenie ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-163">-LogicAppReceiver</span></span>
<span data-ttu-id="61f84-164">Tworzenie LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-165">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61f84-165">-Name</span></span>
<span data-ttu-id="61f84-166">Określa nazwę odbiornika.</span><span class="sxs-lookup"><span data-stu-id="61f84-166">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="61f84-167">-ObjectId</span></span>
<span data-ttu-id="61f84-168">Identyfikator obiektu aplikacji webhook dla uwierzytelniania w usłudze AAD</span><span class="sxs-lookup"><span data-stu-id="61f84-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-169">-Rachunek</span><span class="sxs-lookup"><span data-stu-id="61f84-169">-PhoneNumber</span></span>
<span data-ttu-id="61f84-170">Określa numer telefonu odbiornika SMS.</span><span class="sxs-lookup"><span data-stu-id="61f84-170">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-171">-Region</span><span class="sxs-lookup"><span data-stu-id="61f84-171">-Region</span></span>
<span data-ttu-id="61f84-172">Region ITSM tego odbiorcy</span><span class="sxs-lookup"><span data-stu-id="61f84-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61f84-173">-ResourceId</span></span>
<span data-ttu-id="61f84-174">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="61f84-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="61f84-175">-RoleId</span></span>
<span data-ttu-id="61f84-176">Identyfikator roli ARM odbiornika</span><span class="sxs-lookup"><span data-stu-id="61f84-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-177">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="61f84-177">-RunbookName</span></span>
<span data-ttu-id="61f84-178">Element Runbookname</span><span class="sxs-lookup"><span data-stu-id="61f84-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="61f84-179">-ServiceUri</span></span>
<span data-ttu-id="61f84-180">Określa identyfikator URI odbiornika webhook.</span><span class="sxs-lookup"><span data-stu-id="61f84-180">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-181">-SmsReceiver</span></span>
<span data-ttu-id="61f84-182">Określa, aby utworzyć odbiorcę wiadomości SMS</span><span class="sxs-lookup"><span data-stu-id="61f84-182">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-183">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="61f84-183">-TenantId</span></span>
<span data-ttu-id="61f84-184">Identyfikator dzierżawy dla uwierzytelniania w usłudze AAD</span><span class="sxs-lookup"><span data-stu-id="61f84-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="61f84-185">-TicketConfiguration</span></span>
<span data-ttu-id="61f84-186">ITSM TicketConfiguration tego odbiornika</span><span class="sxs-lookup"><span data-stu-id="61f84-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="61f84-187">-UseAadAuth</span></span>
<span data-ttu-id="61f84-188">Flaga używania Dodaj uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="61f84-188">the flag to use add auth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="61f84-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="61f84-190">Flaga, czy używać typowego schematu alertu.</span><span class="sxs-lookup"><span data-stu-id="61f84-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="61f84-191">Ta wartość będzie neglectedfor wiadomość SMS, aplikacja Azure App push, ITSM i recievers głosowe.</span><span class="sxs-lookup"><span data-stu-id="61f84-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="61f84-192">-VoiceCountryCode</span></span>
<span data-ttu-id="61f84-193">Numer kierunkowy kraju odbiornika rozmówcy</span><span class="sxs-lookup"><span data-stu-id="61f84-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="61f84-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="61f84-195">Numer telefonu odbiornika rozmówcy</span><span class="sxs-lookup"><span data-stu-id="61f84-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-196">-VoiceReceiver</span></span>
<span data-ttu-id="61f84-197">Tworzenie odbiornika głosowego</span><span class="sxs-lookup"><span data-stu-id="61f84-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="61f84-198">-WebhookReceiver</span></span>
<span data-ttu-id="61f84-199">Określa, aby utworzyć odbiornik elementu webhook</span><span class="sxs-lookup"><span data-stu-id="61f84-199">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="61f84-200">-WebhookResourceId</span></span>
<span data-ttu-id="61f84-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="61f84-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="61f84-202">-WorkspaceId</span></span>
<span data-ttu-id="61f84-203">Identyfikator obszaru roboczego ITSM dla tego odbiornika</span><span class="sxs-lookup"><span data-stu-id="61f84-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f84-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f84-204">CommonParameters</span></span>
<span data-ttu-id="61f84-205">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f84-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f84-206">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61f84-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f84-207">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61f84-207">INPUTS</span></span>

### <span data-ttu-id="61f84-208">System. String</span><span class="sxs-lookup"><span data-stu-id="61f84-208">System.String</span></span>

### <span data-ttu-id="61f84-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61f84-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="61f84-210">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61f84-210">OUTPUTS</span></span>

### <span data-ttu-id="61f84-211">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="61f84-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="61f84-212">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61f84-212">NOTES</span></span>

## <span data-ttu-id="61f84-213">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61f84-213">RELATED LINKS</span></span>

<span data-ttu-id="61f84-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="61f84-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
