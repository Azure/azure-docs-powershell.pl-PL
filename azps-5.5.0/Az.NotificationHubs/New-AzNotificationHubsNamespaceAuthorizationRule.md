---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240483"
---
# <span data-ttu-id="ca826-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ca826-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="ca826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca826-102">SYNOPSIS</span></span>
<span data-ttu-id="ca826-103">Tworzy regułę autoryzacji i przypisuje regułę do przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ca826-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="ca826-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca826-104">SYNTAX</span></span>

### <span data-ttu-id="ca826-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca826-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca826-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca826-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca826-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca826-107">DESCRIPTION</span></span>
<span data-ttu-id="ca826-108">Polecenie **cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** tworzy regułę autoryzacji sas (Shared Access Signature) i przypisuje ją do przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ca826-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="ca826-109">Reguły autoryzacji zarządzają prawami użytkowników do przestrzeni nazw i do centrum powiadomień zawartych w tej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="ca826-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="ca826-110">To polecenie cmdlet udostępnia dwa sposoby tworzenia nowej reguły autoryzacji i przypisywania jej do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="ca826-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="ca826-111">Możesz utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes,** a następnie skonfigurować ten obiekt przy użyciu wartości właściwości, które ma posiadać nowa reguła.</span><span class="sxs-lookup"><span data-stu-id="ca826-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="ca826-112">Można to zrobić za pomocą programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ca826-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="ca826-113">Następnie możesz skopiować te wartości właściwości do nowej reguły, używając *parametru SASRule.*</span><span class="sxs-lookup"><span data-stu-id="ca826-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="ca826-114">Ewentualnie możesz utworzyć plik JSON (JavaScript Object Notation) zawierający odpowiednie wartości konfiguracyjne, a następnie zastosować te wartości, używając *parametru InputFile.*</span><span class="sxs-lookup"><span data-stu-id="ca826-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="ca826-115">Plik JSON to plik tekstowy o składni podobnej do następującej: {</span><span class="sxs-lookup"><span data-stu-id="ca826-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="ca826-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="ca826-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="ca826-117">"Klucz Podstawowy": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="ca826-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="ca826-118">"Prawa": \[</span><span class="sxs-lookup"><span data-stu-id="ca826-118">"Rights": \[</span></span>  
        <span data-ttu-id="ca826-119">"Słuchaj",</span><span class="sxs-lookup"><span data-stu-id="ca826-119">"Listen",</span></span>  
        <span data-ttu-id="ca826-120">"Wyślij"</span><span class="sxs-lookup"><span data-stu-id="ca826-120">"Send"</span></span>  
    \]  
<span data-ttu-id="ca826-121">} W połączeniu z poleceniem cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** poprzedni przykład JSON tworzy regułę autoryzacji o nazwie ContosoAuthorizationRule, która zapewnia użytkownikom prawa do odsłuchiwanie i wysyłanie do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="ca826-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="ca826-122">Klucz *Podstawowy używany* do uwierzytelniania można losowo wygenerować za pomocą następującego polecenia programu Windows PowerShell: Convert \[ \] ::ToBase64String((1,32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))</span><span class="sxs-lookup"><span data-stu-id="ca826-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="ca826-123">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca826-123">EXAMPLES</span></span>

### <span data-ttu-id="ca826-124">Przykład 1. Tworzenie reguły autoryzacji i przypisywanie jej do przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="ca826-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="ca826-125">To polecenie tworzy regułę autoryzacji i przypisuje tę regułę do przestrzeni nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="ca826-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="ca826-126">Tworząc tę regułę, należy określić odpowiednią przestrzeń nazw i grupę zasobów, do których jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="ca826-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="ca826-127">Nie trzeba jednak określać żadnych informacji na temat samej reguły: informacje o regułach będą pochodzić z pliku C:\Configuration\NamespaceAuthorizationRules.jswejściowych.</span><span class="sxs-lookup"><span data-stu-id="ca826-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="ca826-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca826-128">PARAMETERS</span></span>

### <span data-ttu-id="ca826-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca826-129">-DefaultProfile</span></span>
<span data-ttu-id="ca826-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ca826-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca826-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ca826-131">-InputFile</span></span>
<span data-ttu-id="ca826-132">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji dla nowej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="ca826-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca826-133">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="ca826-133">-Namespace</span></span>
<span data-ttu-id="ca826-134">Określa przestrzeń nazw, do której zostaną przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="ca826-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="ca826-135">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ca826-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="ca826-136">Nowe reguły muszą zostać przypisane do istniejącej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="ca826-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="ca826-137">Polecenie **cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** nie może utworzyć nowej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="ca826-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="ca826-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca826-138">-ResourceGroup</span></span>
<span data-ttu-id="ca826-139">Określa grupę zasobów, do której jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="ca826-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="ca826-140">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca826-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="ca826-141">Należy użyć istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca826-141">You must use an existing resource group.</span></span>
<span data-ttu-id="ca826-142">To polecenie cmdlet nie może utworzyć nowej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca826-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="ca826-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="ca826-143">-SASRule</span></span>
<span data-ttu-id="ca826-144">Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji dla nowych reguł.</span><span class="sxs-lookup"><span data-stu-id="ca826-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca826-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca826-145">-Confirm</span></span>
<span data-ttu-id="ca826-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ca826-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca826-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca826-147">-WhatIf</span></span>
<span data-ttu-id="ca826-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca826-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca826-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ca826-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca826-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca826-150">CommonParameters</span></span>
<span data-ttu-id="ca826-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca826-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca826-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca826-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca826-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca826-153">INPUTS</span></span>

### <span data-ttu-id="ca826-154">System.String</span><span class="sxs-lookup"><span data-stu-id="ca826-154">System.String</span></span>

## <span data-ttu-id="ca826-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca826-155">OUTPUTS</span></span>

### <span data-ttu-id="ca826-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ca826-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ca826-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca826-157">NOTES</span></span>

## <span data-ttu-id="ca826-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca826-158">RELATED LINKS</span></span>

[<span data-ttu-id="ca826-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ca826-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="ca826-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ca826-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="ca826-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ca826-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


