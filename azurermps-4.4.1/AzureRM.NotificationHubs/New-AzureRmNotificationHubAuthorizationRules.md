---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: c3a30457e6fd25aa633a0faa0510ed4ce61efbd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546183"
---
# <span data-ttu-id="2da90-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2da90-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="2da90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2da90-102">SYNOPSIS</span></span>
<span data-ttu-id="2da90-103">Powoduje utworzenie reguły autoryzacji i przypisanie jej do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="2da90-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2da90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2da90-104">SYNTAX</span></span>

### <span data-ttu-id="2da90-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da90-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2da90-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da90-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2da90-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2da90-107">DESCRIPTION</span></span>
<span data-ttu-id="2da90-108">Polecenie cmdlet **New-AzureRmNotificationHubAuthorizationRules** umożliwia utworzenie reguły autoryzacji podpisu dostępu udostępnionej w centrum powiadomień (SAS).</span><span class="sxs-lookup"><span data-stu-id="2da90-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="2da90-109">Reguły autoryzacji są używane do zarządzania dostępem do koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="2da90-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="2da90-110">W tym celu Utwórz linki jako identyfikatory URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="2da90-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="2da90-111">Klienci są kierowani do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="2da90-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="2da90-112">Na przykład klient, któremu przydzielono uprawnienie odsłuchiwania, będzie kierowany na identyfikator URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="2da90-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="2da90-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2da90-113">EXAMPLES</span></span>

### <span data-ttu-id="2da90-114">Przykład 1. Tworzenie reguły autoryzacji centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="2da90-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="2da90-115">To polecenie powoduje utworzenie nowej reguły autoryzacji i przypisanie jej do centrum powiadomień o nazwie ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="2da90-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="2da90-116">Ten centrum znajduje się w obszarze nazw ContosoNamespace i jest przypisany do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="2da90-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="2da90-117">Zwróć uwagę, że wszystkie informacje o konfiguracji dla reguły, w tym nazwa reguły, zostaną pobrane z pliku wejściowego, na C:\Configuration\ExternalAccessRule.js.</span><span class="sxs-lookup"><span data-stu-id="2da90-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="2da90-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2da90-118">PARAMETERS</span></span>

### <span data-ttu-id="2da90-119">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="2da90-119">-InputFile</span></span>
<span data-ttu-id="2da90-120">Określa plik wejściowy reguły autoryzacji tworzonego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2da90-120">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2da90-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2da90-121">-Namespace</span></span>
<span data-ttu-id="2da90-122">Określa obszar nazw, do którego są przypisywane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="2da90-122">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="2da90-123">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="2da90-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="2da90-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="2da90-124">-NotificationHub</span></span>
<span data-ttu-id="2da90-125">Określa centrum powiadomień, do którego zostaną przydzielone reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="2da90-125">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="2da90-126">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="2da90-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="2da90-127">Pamiętaj, że musisz określić nazwę istniejącego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="2da90-127">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="2da90-128">Polecenie cmdlet **New-AzureRmNotificationHubAuthorizationRules** nie może utworzyć nowych koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="2da90-128">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="2da90-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2da90-129">-ResourceGroup</span></span>
<span data-ttu-id="2da90-130">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="2da90-130">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="2da90-131">-SASRule</span><span class="sxs-lookup"><span data-stu-id="2da90-131">-SASRule</span></span>
<span data-ttu-id="2da90-132">Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji dla nowych reguł.</span><span class="sxs-lookup"><span data-stu-id="2da90-132">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="2da90-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2da90-133">-Confirm</span></span>
<span data-ttu-id="2da90-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2da90-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2da90-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2da90-135">-WhatIf</span></span>
<span data-ttu-id="2da90-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2da90-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2da90-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2da90-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2da90-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da90-138">-DefaultProfile</span></span>
<span data-ttu-id="2da90-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2da90-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da90-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da90-140">CommonParameters</span></span>
<span data-ttu-id="2da90-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da90-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da90-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da90-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da90-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2da90-143">INPUTS</span></span>

## <span data-ttu-id="2da90-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2da90-144">OUTPUTS</span></span>

### <span data-ttu-id="2da90-145">Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2da90-145">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2da90-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2da90-146">NOTES</span></span>

## <span data-ttu-id="2da90-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2da90-147">RELATED LINKS</span></span>

[<span data-ttu-id="2da90-148">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2da90-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="2da90-149">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2da90-149">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="2da90-150">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2da90-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


