---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: bb433499b53a1067e21996fe33fd6e9765dcab4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708881"
---
# <span data-ttu-id="34ed8-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34ed8-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="34ed8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="34ed8-103">Pobiera informacje o regułach autoryzacji skojarzonych z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="34ed8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34ed8-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34ed8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34ed8-105">DESCRIPTION</span></span>
<span data-ttu-id="34ed8-106">Polecenie cmdlet **Get-AzNotificationHubAuthorizationRule** pobiera informacje o regułach autoryzacji podpisu dostępu udostępnionego (SAS) skojarzonych z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="34ed8-107">Polecenie cmdlet zwraca informacje o wszystkich regułach skojarzonych z koncentratorem lub, dołączając parametr *AuthorizationRule* , pobiera informacje na temat określonej reguły.</span><span class="sxs-lookup"><span data-stu-id="34ed8-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="34ed8-108">Reguły autoryzacji zarządzają dostępem do koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="34ed8-109">Reguła autoryzacji utworzy linki jako identyfikator URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="34ed8-110">Klienci są kierowani do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="34ed8-111">Na przykład klient z uprawnieniem odsłuchiwania będzie kierowany na identyfikator URI dla tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="34ed8-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="34ed8-112">Polecenie cmdlet **Get-AzNotificationHubAuthorizationRule** pobiera tylko informacje o regułach autoryzacji skojarzonych z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="34ed8-113">Aby uzyskać informacje na temat samego centrum, użyj polecenie Get-AzNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="34ed8-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="34ed8-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34ed8-114">EXAMPLES</span></span>

### <span data-ttu-id="34ed8-115">Przykład 1: uzyskiwanie informacji o wszystkich regułach autoryzacji przypisanych do centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="34ed8-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="34ed8-116">To polecenie pobiera informacje dotyczące wszystkich reguł autoryzacji przypisanych do centrum powiadomień o nazwie ContosoInternalHub w obszarze nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="34ed8-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="34ed8-117">Musisz określić obszar nazw, w którym znajduje się centrum, oraz grupę zasobów, do których przypisano centrum.</span><span class="sxs-lookup"><span data-stu-id="34ed8-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="34ed8-118">Przykład 2: uzyskiwanie informacji o regułach autoryzacji przypisanych do centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="34ed8-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="34ed8-119">To polecenie pobiera informacje dotyczące wszystkich reguł autoryzacji przypisanych do centrum powiadomień o nazwie ContosoInternalHub w obszarze nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="34ed8-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="34ed8-120">W poleceniu użyto parametru *AuthorizationRule* w celu ograniczenia zwracanych danych do jednej reguły autoryzacji o nazwie ListenRule.</span><span class="sxs-lookup"><span data-stu-id="34ed8-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="34ed8-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34ed8-121">PARAMETERS</span></span>

### <span data-ttu-id="34ed8-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34ed8-122">-AuthorizationRule</span></span>
<span data-ttu-id="34ed8-123">Określa nazwę reguły uwierzytelniania SAS.</span><span class="sxs-lookup"><span data-stu-id="34ed8-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="34ed8-124">Te reguły określają typ dostępu do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ed8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ed8-125">-DefaultProfile</span></span>
<span data-ttu-id="34ed8-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="34ed8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34ed8-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="34ed8-127">-Namespace</span></span>
<span data-ttu-id="34ed8-128">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="34ed8-129">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="34ed8-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="34ed8-130">-NotificationHub</span></span>
<span data-ttu-id="34ed8-131">Określa centrum powiadomień, które to polecenie cmdlet przypisuje reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="34ed8-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="34ed8-132">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="34ed8-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="34ed8-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="34ed8-133">-ResourceGroup</span></span>
<span data-ttu-id="34ed8-134">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="34ed8-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="34ed8-135">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji w celu uproszczenia zarządzania zapasami i administrowania systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="34ed8-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="34ed8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ed8-136">CommonParameters</span></span>
<span data-ttu-id="34ed8-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ed8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ed8-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ed8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ed8-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34ed8-139">INPUTS</span></span>

### <span data-ttu-id="34ed8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="34ed8-140">System.String</span></span>

## <span data-ttu-id="34ed8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34ed8-141">OUTPUTS</span></span>

### <span data-ttu-id="34ed8-142">Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="34ed8-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="34ed8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34ed8-143">NOTES</span></span>

## <span data-ttu-id="34ed8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34ed8-144">RELATED LINKS</span></span>

[<span data-ttu-id="34ed8-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34ed8-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="34ed8-146">Nowe — AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34ed8-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="34ed8-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34ed8-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="34ed8-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34ed8-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


