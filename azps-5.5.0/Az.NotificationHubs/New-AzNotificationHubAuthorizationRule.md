---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 5cfdf1eb7bfbb08d0658f4245d9e45804403135f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202372"
---
# <span data-ttu-id="bac2a-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bac2a-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="bac2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac2a-102">SYNOPSIS</span></span>
<span data-ttu-id="bac2a-103">Tworzy regułę autoryzacji i przypisuje regułę do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="bac2a-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="bac2a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bac2a-104">SYNTAX</span></span>

### <span data-ttu-id="bac2a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="bac2a-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bac2a-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="bac2a-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bac2a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bac2a-107">DESCRIPTION</span></span>
<span data-ttu-id="bac2a-108">Polecenie **cmdlet New-AzNotificationHubAuthorizationRule** tworzy regułę autoryzacji centrum powiadomień sygnatury dostępu udostępnionego (SAS).</span><span class="sxs-lookup"><span data-stu-id="bac2a-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="bac2a-109">Reguły autoryzacji służą do zarządzania dostępem do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="bac2a-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="bac2a-110">Jest to wykonywane przez utworzenie linków jako URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="bac2a-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="bac2a-111">Klienci są kierowani do jednego z tych URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="bac2a-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="bac2a-112">Na przykład klient, który otrzymał uprawnienie Posłuchaj, zostanie przekierowyowany do URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="bac2a-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="bac2a-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bac2a-113">EXAMPLES</span></span>

### <span data-ttu-id="bac2a-114">Przykład 1. Tworzenie reguły autoryzacji centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="bac2a-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="bac2a-115">To polecenie tworzy nową regułę autoryzacji i przypisuje ją do centrum powiadomień o nazwie ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="bac2a-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="bac2a-116">To centrum znajduje się w przestrzeni nazw ContosoNamespace i jest przypisane do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="bac2a-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="bac2a-117">Zwróć uwagę, że wszystkie informacje o konfiguracji reguły, łącznie z nazwą reguły, będą pochodzić z pliku wejściowego, C:\Configuration\ExternalAccessRule.jswł.</span><span class="sxs-lookup"><span data-stu-id="bac2a-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="bac2a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bac2a-118">PARAMETERS</span></span>

### <span data-ttu-id="bac2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac2a-119">-DefaultProfile</span></span>
<span data-ttu-id="bac2a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="bac2a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bac2a-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="bac2a-121">-InputFile</span></span>
<span data-ttu-id="bac2a-122">Określa plik wejściowy reguły autoryzacji, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bac2a-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bac2a-123">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="bac2a-123">-Namespace</span></span>
<span data-ttu-id="bac2a-124">Określa przestrzeń nazw, do której są przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="bac2a-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="bac2a-125">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="bac2a-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="bac2a-126">- NotificationHub</span><span class="sxs-lookup"><span data-stu-id="bac2a-126">-NotificationHub</span></span>
<span data-ttu-id="bac2a-127">Określa centrum powiadomień, do których zostaną przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="bac2a-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="bac2a-128">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="bac2a-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="bac2a-129">Pamiętaj, że musisz określić nazwę istniejącego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="bac2a-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="bac2a-130">Polecenie **cmdlet New-AzNotificationHubAuthorizationRule** nie może tworzyć nowych centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="bac2a-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="bac2a-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bac2a-131">-ResourceGroup</span></span>
<span data-ttu-id="bac2a-132">Określa grupę zasobów, do która jest przypisana centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="bac2a-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="bac2a-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="bac2a-133">-SASRule</span></span>
<span data-ttu-id="bac2a-134">Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji dla nowych reguł.</span><span class="sxs-lookup"><span data-stu-id="bac2a-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="bac2a-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bac2a-135">-Confirm</span></span>
<span data-ttu-id="bac2a-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bac2a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bac2a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac2a-137">-WhatIf</span></span>
<span data-ttu-id="bac2a-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bac2a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bac2a-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bac2a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bac2a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac2a-140">CommonParameters</span></span>
<span data-ttu-id="bac2a-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bac2a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac2a-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac2a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac2a-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bac2a-143">INPUTS</span></span>

### <span data-ttu-id="bac2a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bac2a-144">System.String</span></span>

## <span data-ttu-id="bac2a-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bac2a-145">OUTPUTS</span></span>

### <span data-ttu-id="bac2a-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="bac2a-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="bac2a-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bac2a-147">NOTES</span></span>

## <span data-ttu-id="bac2a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bac2a-148">RELATED LINKS</span></span>

[<span data-ttu-id="bac2a-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bac2a-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="bac2a-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bac2a-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="bac2a-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bac2a-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


