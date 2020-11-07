---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 6ad682ad80400fa84034b35804c9756775d05eeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708851"
---
# <span data-ttu-id="f7b80-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7b80-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="f7b80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7b80-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b80-103">Usuwa regułę autoryzacji z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f7b80-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="f7b80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7b80-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7b80-105">DESCRIPTION</span></span>
<span data-ttu-id="f7b80-106">Polecenie cmdlet **Remove-AzNotificationHubAuthorizationRule** usuwa regułę autoryzacji współużytkowanego podpisu dostępu (SAS) z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f7b80-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="f7b80-107">Reguły autoryzacji zarządzają dostępem do koncentratorów powiadomień za pomocą tworzenia linków, takich jak identyfikatory URI, na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="f7b80-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="f7b80-108">Poziom uprawnień może być jednym z następujących:</span><span class="sxs-lookup"><span data-stu-id="f7b80-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="f7b80-109">Słuch</span><span class="sxs-lookup"><span data-stu-id="f7b80-109">Listen</span></span>
- <span data-ttu-id="f7b80-110">Wyślij</span><span class="sxs-lookup"><span data-stu-id="f7b80-110">Send</span></span>
- <span data-ttu-id="f7b80-111">Zarządzanie klientami jest przekierowywane do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="f7b80-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f7b80-112">Na przykład klient, któremu nadano uprawnienie do odsłuchiwania, będzie kierowany na identyfikator URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="f7b80-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="f7b80-113">Usunięcie reguły autoryzacji powoduje również usunięcie odpowiednich uprawnień użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f7b80-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="f7b80-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7b80-114">EXAMPLES</span></span>

### <span data-ttu-id="f7b80-115">Przykład 1: Usuwanie reguły autoryzacji z centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="f7b80-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f7b80-116">To polecenie usuwa regułę autoryzacji o nazwie ListenRule z centrum powiadomień o nazwie ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="f7b80-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="f7b80-117">Po uruchomieniu tego polecenia musisz określić zarówno obszar nazw, jak i grupę zasobów, do których jest przypisany koncentrator.</span><span class="sxs-lookup"><span data-stu-id="f7b80-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="f7b80-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7b80-118">PARAMETERS</span></span>

### <span data-ttu-id="f7b80-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7b80-119">-AuthorizationRule</span></span>
<span data-ttu-id="f7b80-120">Określa nazwę reguły uwierzytelniania SAS, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b80-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f7b80-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b80-121">-DefaultProfile</span></span>
<span data-ttu-id="f7b80-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f7b80-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7b80-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f7b80-123">-Force</span></span>
<span data-ttu-id="f7b80-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f7b80-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f7b80-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f7b80-125">-Namespace</span></span>
<span data-ttu-id="f7b80-126">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f7b80-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="f7b80-127">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f7b80-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f7b80-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f7b80-128">-NotificationHub</span></span>
<span data-ttu-id="f7b80-129">Określa centrum powiadomień, do którego przypisani są reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="f7b80-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="f7b80-130">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów bez względu na platformę.</span><span class="sxs-lookup"><span data-stu-id="f7b80-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="f7b80-131">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f7b80-131">-ResourceGroup</span></span>
<span data-ttu-id="f7b80-132">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f7b80-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="f7b80-133">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b80-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f7b80-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7b80-134">-Confirm</span></span>
<span data-ttu-id="f7b80-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b80-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b80-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b80-136">-WhatIf</span></span>
<span data-ttu-id="f7b80-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b80-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7b80-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7b80-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b80-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b80-139">CommonParameters</span></span>
<span data-ttu-id="f7b80-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b80-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b80-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7b80-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b80-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7b80-142">INPUTS</span></span>

### <span data-ttu-id="f7b80-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f7b80-143">System.String</span></span>

## <span data-ttu-id="f7b80-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7b80-144">OUTPUTS</span></span>

### <span data-ttu-id="f7b80-145">System. void</span><span class="sxs-lookup"><span data-stu-id="f7b80-145">System.Void</span></span>

## <span data-ttu-id="f7b80-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7b80-146">NOTES</span></span>

## <span data-ttu-id="f7b80-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7b80-147">RELATED LINKS</span></span>

[<span data-ttu-id="f7b80-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7b80-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="f7b80-149">Nowe — AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7b80-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="f7b80-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7b80-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


