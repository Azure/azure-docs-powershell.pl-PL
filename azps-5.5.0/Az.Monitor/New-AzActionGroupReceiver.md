---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192210"
---
# <span data-ttu-id="591a9-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="591a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591a9-102">SYNOPSIS</span></span>
<span data-ttu-id="591a9-103">Tworzy nowego odbiorcy grupy akcji.</span><span class="sxs-lookup"><span data-stu-id="591a9-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="591a9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="591a9-104">SYNTAX</span></span>

### <span data-ttu-id="591a9-105">NewEmailReceiver (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="591a9-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591a9-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591a9-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591a9-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591a9-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591a9-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591a9-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591a9-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591a9-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591a9-114">NewAzureAppPreceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="591a9-115">OPIS</span><span class="sxs-lookup"><span data-stu-id="591a9-115">DESCRIPTION</span></span>
<span data-ttu-id="591a9-116">Polecenie **cmdlet New-AzActionGroupReceiver** tworzy nowego odbiorcy grupy akcji w pamięci.</span><span class="sxs-lookup"><span data-stu-id="591a9-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="591a9-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="591a9-117">EXAMPLES</span></span>

### <span data-ttu-id="591a9-118">Przykład 1. Tworzenie nowego odbiorcy wiadomości e-mail w pamięci.</span><span class="sxs-lookup"><span data-stu-id="591a9-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="591a9-119">To polecenie tworzy nowego odbiorcy wiadomości e-mail w pamięci.</span><span class="sxs-lookup"><span data-stu-id="591a9-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="591a9-120">Przykład 2. Tworzenie nowego odbiorcy WIADOMOŚCI SMS w pamięci.</span><span class="sxs-lookup"><span data-stu-id="591a9-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="591a9-121">To polecenie tworzy nowego odbiorcy wiadomości SMS w pamięci.</span><span class="sxs-lookup"><span data-stu-id="591a9-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="591a9-122">Przykład 3. Tworzenie nowego odbiorcy sieci Web w pamięci.</span><span class="sxs-lookup"><span data-stu-id="591a9-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="591a9-123">To polecenie tworzy nowego słuchawkę sieci Web w pamięci.</span><span class="sxs-lookup"><span data-stu-id="591a9-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="591a9-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="591a9-124">PARAMETERS</span></span>

### <span data-ttu-id="591a9-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="591a9-126">Tworzenie armrolereceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="591a9-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="591a9-127">-AutomationAccountId</span></span>
<span data-ttu-id="591a9-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="591a9-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="591a9-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="591a9-130">Tworzenie przewodnika AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="591a9-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="591a9-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="591a9-132">URI, do którego ma zostać wysłany webhoox</span><span class="sxs-lookup"><span data-stu-id="591a9-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="591a9-133">-AzureAppPmailAddress</span><span class="sxs-lookup"><span data-stu-id="591a9-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="591a9-134">The AzureAppPmailAddress</span><span class="sxs-lookup"><span data-stu-id="591a9-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="591a9-135">-AzureAppPreceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="591a9-136">Tworzenie narzędzia AzureAppPreceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="591a9-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="591a9-138">Tworzenie armrolereceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="591a9-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="591a9-139">-CallbackUrl</span></span>
<span data-ttu-id="591a9-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="591a9-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="591a9-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="591a9-141">-ConnectionId</span></span>
<span data-ttu-id="591a9-142">identyfikator połączenia itsm tego odbiorcy</span><span class="sxs-lookup"><span data-stu-id="591a9-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="591a9-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="591a9-143">-CountryCode</span></span>
<span data-ttu-id="591a9-144">Określa kod kraju odbiorcy SMS.</span><span class="sxs-lookup"><span data-stu-id="591a9-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="591a9-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591a9-145">-DefaultProfile</span></span>
<span data-ttu-id="591a9-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="591a9-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="591a9-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="591a9-147">-EmailAddress</span></span>
<span data-ttu-id="591a9-148">Określa adres odbiorcy wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="591a9-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="591a9-149">- EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-149">-EmailReceiver</span></span>
<span data-ttu-id="591a9-150">Określa, jak utworzyć odbiorcę wiadomości e-mail</span><span class="sxs-lookup"><span data-stu-id="591a9-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="591a9-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="591a9-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="591a9-152">the function app resourceId</span><span class="sxs-lookup"><span data-stu-id="591a9-152">the function app resourceId</span></span>

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

### <span data-ttu-id="591a9-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="591a9-153">-FunctionName</span></span>
<span data-ttu-id="591a9-154">nazwa_funkcji</span><span class="sxs-lookup"><span data-stu-id="591a9-154">the functionName</span></span>

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

### <span data-ttu-id="591a9-155">- HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="591a9-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="591a9-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="591a9-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="591a9-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="591a9-157">-IdentifierUri</span></span>
<span data-ttu-id="591a9-158">Identyfikator uri identyfikatora dla aad auth</span><span class="sxs-lookup"><span data-stu-id="591a9-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="591a9-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="591a9-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="591a9-160">wskazuje, czy to wystąpienie jest globalnym podręcznikiem uruchamiania</span><span class="sxs-lookup"><span data-stu-id="591a9-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="591a9-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-161">-ItsmReceiver</span></span>
<span data-ttu-id="591a9-162">Tworzenie rekordu ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="591a9-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-163">-LogicAppReceiver</span></span>
<span data-ttu-id="591a9-164">Tworzenie aplikacji LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="591a9-165">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="591a9-165">-Name</span></span>
<span data-ttu-id="591a9-166">Określa nazwę odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="591a9-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="591a9-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="591a9-167">-ObjectId</span></span>
<span data-ttu-id="591a9-168">Identyfikator obiektu aplikacji WebHook dla uwierzytelniania aad</span><span class="sxs-lookup"><span data-stu-id="591a9-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="591a9-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="591a9-169">-PhoneNumber</span></span>
<span data-ttu-id="591a9-170">Określa numer telefonu dla odbiorcy WIADOMOŚCI SMS.</span><span class="sxs-lookup"><span data-stu-id="591a9-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="591a9-171">— Region</span><span class="sxs-lookup"><span data-stu-id="591a9-171">-Region</span></span>
<span data-ttu-id="591a9-172">region itsm tego odbiorcy</span><span class="sxs-lookup"><span data-stu-id="591a9-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="591a9-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="591a9-173">-ResourceId</span></span>
<span data-ttu-id="591a9-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="591a9-174">the ResourceId</span></span>

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

### <span data-ttu-id="591a9-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="591a9-175">-RoleId</span></span>
<span data-ttu-id="591a9-176">Identyfikator roli arm odbiorcy</span><span class="sxs-lookup"><span data-stu-id="591a9-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="591a9-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="591a9-177">-RunbookName</span></span>
<span data-ttu-id="591a9-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="591a9-178">the RunbookName</span></span>

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

### <span data-ttu-id="591a9-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="591a9-179">-ServiceUri</span></span>
<span data-ttu-id="591a9-180">Określa URI dla odbiorcy sieci Web.</span><span class="sxs-lookup"><span data-stu-id="591a9-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="591a9-181">- SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-181">-SmsReceiver</span></span>
<span data-ttu-id="591a9-182">Określa, jak utworzyć słuchawkę SMS</span><span class="sxs-lookup"><span data-stu-id="591a9-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="591a9-183">- TenantId</span><span class="sxs-lookup"><span data-stu-id="591a9-183">-TenantId</span></span>
<span data-ttu-id="591a9-184">Identyfikator dzierżawy dla uwierzytelniania aad</span><span class="sxs-lookup"><span data-stu-id="591a9-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="591a9-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="591a9-185">-TicketConfiguration</span></span>
<span data-ttu-id="591a9-186">itsm TicketConfiguration tego odbiorcy</span><span class="sxs-lookup"><span data-stu-id="591a9-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="591a9-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="591a9-187">-UseAadAuth</span></span>
<span data-ttu-id="591a9-188">Flaga do używania funkcji Dodaj uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="591a9-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="591a9-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="591a9-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="591a9-190">Flaga oznacza, czy należy używać wspólnego schematu alertów.</span><span class="sxs-lookup"><span data-stu-id="591a9-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="591a9-191">Ta wartość nie będzie pomijana w przypadku sms-ów, wypychania aplikacji Azure, funkcji ITSM i funkcji głosowych.</span><span class="sxs-lookup"><span data-stu-id="591a9-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="591a9-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="591a9-192">-VoiceCountryCode</span></span>
<span data-ttu-id="591a9-193">Kod kraju odbiorcy głosu</span><span class="sxs-lookup"><span data-stu-id="591a9-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="591a9-194">— VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="591a9-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="591a9-195">Numer telefonu odbiorcy głosu</span><span class="sxs-lookup"><span data-stu-id="591a9-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="591a9-196">- VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-196">-VoiceReceiver</span></span>
<span data-ttu-id="591a9-197">Tworzenie odbiorcy głosu</span><span class="sxs-lookup"><span data-stu-id="591a9-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="591a9-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="591a9-198">-WebhookReceiver</span></span>
<span data-ttu-id="591a9-199">Określa, jak utworzyć słuchawkę sieci Web</span><span class="sxs-lookup"><span data-stu-id="591a9-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="591a9-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="591a9-200">-WebhookResourceId</span></span>
<span data-ttu-id="591a9-201">The WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="591a9-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="591a9-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="591a9-202">-WorkspaceId</span></span>
<span data-ttu-id="591a9-203">Identyfikator obszaru roboczego itsm tego odbiorcy</span><span class="sxs-lookup"><span data-stu-id="591a9-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="591a9-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591a9-204">CommonParameters</span></span>
<span data-ttu-id="591a9-205">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591a9-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591a9-206">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="591a9-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591a9-207">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="591a9-207">INPUTS</span></span>

### <span data-ttu-id="591a9-208">System.String</span><span class="sxs-lookup"><span data-stu-id="591a9-208">System.String</span></span>

### <span data-ttu-id="591a9-209">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="591a9-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="591a9-210">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="591a9-210">OUTPUTS</span></span>

### <span data-ttu-id="591a9-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="591a9-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="591a9-212">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="591a9-212">NOTES</span></span>

## <span data-ttu-id="591a9-213">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="591a9-213">RELATED LINKS</span></span>

<span data-ttu-id="591a9-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="591a9-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
