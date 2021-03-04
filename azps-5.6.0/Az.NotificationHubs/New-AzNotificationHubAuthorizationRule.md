---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 74ad4f80a25250129d050ed3a2769dca6f776376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951274"
---
# <span data-ttu-id="cf06d-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf06d-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="cf06d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf06d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf06d-103">Tworzy regułę autoryzacji i przypisuje regułę do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cf06d-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="cf06d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf06d-104">SYNTAX</span></span>

### <span data-ttu-id="cf06d-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf06d-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf06d-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf06d-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf06d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf06d-107">DESCRIPTION</span></span>
<span data-ttu-id="cf06d-108">Polecenie **cmdlet New-AzNotificationHubAuthorizationRule** tworzy regułę autoryzacji centrum powiadomień sygnatury dostępu udostępnionego (SAS).</span><span class="sxs-lookup"><span data-stu-id="cf06d-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="cf06d-109">Reguły autoryzacji służą do zarządzania dostępem do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cf06d-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="cf06d-110">Jest to wykonywane przez utworzenie linków jako URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="cf06d-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="cf06d-111">Klienci są kierowani do jednego z tych URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="cf06d-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="cf06d-112">Na przykład klient, który otrzymał uprawnienie Posłuchaj, zostanie przekierowyowany do URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="cf06d-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="cf06d-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf06d-113">EXAMPLES</span></span>

### <span data-ttu-id="cf06d-114">Przykład 1. Tworzenie reguły autoryzacji centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="cf06d-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="cf06d-115">To polecenie tworzy nową regułę autoryzacji i przypisuje ją do centrum powiadomień o nazwie ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="cf06d-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="cf06d-116">To centrum znajduje się w przestrzeni nazw ContosoNamespace i jest przypisane do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="cf06d-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="cf06d-117">Zwróć uwagę, że wszystkie informacje o konfiguracji reguły, łącznie z nazwą reguły, będą pochodzić z pliku wejściowego, C:\Configuration\ExternalAccessRule.jswł.</span><span class="sxs-lookup"><span data-stu-id="cf06d-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="cf06d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf06d-118">PARAMETERS</span></span>

### <span data-ttu-id="cf06d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf06d-119">-DefaultProfile</span></span>
<span data-ttu-id="cf06d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cf06d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf06d-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="cf06d-121">-InputFile</span></span>
<span data-ttu-id="cf06d-122">Określa plik wejściowy reguły autoryzacji, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf06d-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf06d-123">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="cf06d-123">-Namespace</span></span>
<span data-ttu-id="cf06d-124">Określa przestrzeń nazw, do której są przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="cf06d-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="cf06d-125">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cf06d-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="cf06d-126">- NotificationHub</span><span class="sxs-lookup"><span data-stu-id="cf06d-126">-NotificationHub</span></span>
<span data-ttu-id="cf06d-127">Określa centrum powiadomień, do których zostaną przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="cf06d-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="cf06d-128">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="cf06d-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="cf06d-129">Pamiętaj, że musisz określić nazwę istniejącego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cf06d-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="cf06d-130">Polecenie **cmdlet New-AzNotificationHubAuthorizationRule** nie może tworzyć nowych centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cf06d-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="cf06d-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf06d-131">-ResourceGroup</span></span>
<span data-ttu-id="cf06d-132">Określa grupę zasobów, do która jest przypisana centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cf06d-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="cf06d-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="cf06d-133">-SASRule</span></span>
<span data-ttu-id="cf06d-134">Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji dla nowych reguł.</span><span class="sxs-lookup"><span data-stu-id="cf06d-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf06d-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf06d-135">-Confirm</span></span>
<span data-ttu-id="cf06d-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf06d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf06d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf06d-137">-WhatIf</span></span>
<span data-ttu-id="cf06d-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf06d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf06d-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cf06d-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf06d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf06d-140">CommonParameters</span></span>
<span data-ttu-id="cf06d-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf06d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf06d-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf06d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf06d-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf06d-143">INPUTS</span></span>

### <span data-ttu-id="cf06d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cf06d-144">System.String</span></span>

## <span data-ttu-id="cf06d-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf06d-145">OUTPUTS</span></span>

### <span data-ttu-id="cf06d-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cf06d-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cf06d-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf06d-147">NOTES</span></span>

## <span data-ttu-id="cf06d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf06d-148">RELATED LINKS</span></span>

[<span data-ttu-id="cf06d-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf06d-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="cf06d-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf06d-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="cf06d-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf06d-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


