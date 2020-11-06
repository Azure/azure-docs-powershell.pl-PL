---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 6203c5554dcdbfbd40c861a3f73e1a5947228030
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554107"
---
# <span data-ttu-id="d2805-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d2805-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="d2805-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2805-102">SYNOPSIS</span></span>
<span data-ttu-id="d2805-103">Ustawia reguły autoryzacji dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d2805-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2805-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2805-104">SYNTAX</span></span>

### <span data-ttu-id="d2805-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2805-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2805-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2805-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2805-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d2805-107">DESCRIPTION</span></span>
<span data-ttu-id="d2805-108">Polecenie cmdlet **Set-AzureRmNotificationHubAuthorizationRules** powoduje zmodyfikowanie reguły autoryzacji podpisu dostępu współużytkowanego (SAS) przypisanej do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d2805-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="d2805-109">Reguły autoryzacji zarządzają dostępem do koncentratorów powiadomień przez tworzenie linków jako identyfikatorów URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="d2805-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="d2805-110">Poziom uprawnień może być jednym z następujących:</span><span class="sxs-lookup"><span data-stu-id="d2805-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="d2805-111">Słuch</span><span class="sxs-lookup"><span data-stu-id="d2805-111">Listen</span></span>
- <span data-ttu-id="d2805-112">Wyślij</span><span class="sxs-lookup"><span data-stu-id="d2805-112">Send</span></span>
- <span data-ttu-id="d2805-113">Zarządzanie</span><span class="sxs-lookup"><span data-stu-id="d2805-113">Manage</span></span>

<span data-ttu-id="d2805-114">Klienci są kierowani do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="d2805-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="d2805-115">Na przykład klient, któremu przydzielono uprawnienie odsłuchiwania, będzie kierowany na identyfikator URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="d2805-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="d2805-116">To polecenie cmdlet oferuje dwie metody modyfikowania reguły autoryzacji przypisanej do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d2805-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="d2805-117">W przypadku jednej z nich można utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes** , a następnie skonfigurować te obiekty za pomocą wartości właściwości, które mają mieć reguła.</span><span class="sxs-lookup"><span data-stu-id="d2805-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="d2805-118">Obiekt można skonfigurować za pośrednictwem platformy .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d2805-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="d2805-119">Następnie można skopiować te wartości właściwości do reguły za pomocą parametru *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="d2805-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="d2805-120">Możesz również utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pośrednictwem parametru *plik_wejściowy* .</span><span class="sxs-lookup"><span data-stu-id="d2805-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="d2805-121">Plik JSON jest plikiem tekstowym używającym składni podobnej do następującej:</span><span class="sxs-lookup"><span data-stu-id="d2805-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="d2805-122">{"Nazwa": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="d2805-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="d2805-123">"Primaryke": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="d2805-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="d2805-124">"Prawa": \[</span><span class="sxs-lookup"><span data-stu-id="d2805-124">"Rights": \[</span></span>  
        <span data-ttu-id="d2805-125">"Odsłuchiwanie",</span><span class="sxs-lookup"><span data-stu-id="d2805-125">"Listen",</span></span>  
        <span data-ttu-id="d2805-126">Przysła</span><span class="sxs-lookup"><span data-stu-id="d2805-126">"Send"</span></span>  
    \]  
<span data-ttu-id="d2805-127">}</span><span class="sxs-lookup"><span data-stu-id="d2805-127">}</span></span>

<span data-ttu-id="d2805-128">W przypadku użycia w połączeniu z poleceniem cmdlet New-AzureRmNotificationHubAuthorizationRules poprzedni przykład JSON modyfikuje regułę autoryzacji o nazwie ContosoAuthorizationRule, aby umożliwić użytkownikom odsłuchiwanie i wysyłanie praw do centrum.</span><span class="sxs-lookup"><span data-stu-id="d2805-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="d2805-129">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2805-129">EXAMPLES</span></span>

### <span data-ttu-id="d2805-130">Przykład 1: modyfikowanie reguły autoryzacji przypisanej do centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="d2805-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="d2805-131">To polecenie modyfikuje regułę autoryzacji przypisaną do centrum powiadomień o nazwie ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="d2805-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="d2805-132">Musisz określić obszar nazw, w którym znajduje się centrum, oraz grupę zasobów, do których jest przypisany koncentrator.</span><span class="sxs-lookup"><span data-stu-id="d2805-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="d2805-133">Informacje na temat modyfikacji reguły nie są uwzględniane w samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d2805-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="d2805-134">Zamiast tego informacje są dostępne w pliku wejściowym C:\Configuration\AuthorizationRules.jsna.</span><span class="sxs-lookup"><span data-stu-id="d2805-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="d2805-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2805-135">PARAMETERS</span></span>

### <span data-ttu-id="d2805-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2805-136">-DefaultProfile</span></span>
<span data-ttu-id="d2805-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d2805-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2805-138">-Force</span><span class="sxs-lookup"><span data-stu-id="d2805-138">-Force</span></span>
<span data-ttu-id="d2805-139">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2805-139">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d2805-140">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="d2805-140">-InputFile</span></span>
<span data-ttu-id="d2805-141">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji nowej reguły.</span><span class="sxs-lookup"><span data-stu-id="d2805-141">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2805-142">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d2805-142">-Namespace</span></span>
<span data-ttu-id="d2805-143">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d2805-143">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="d2805-144">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d2805-144">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d2805-145">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d2805-145">-NotificationHub</span></span>
<span data-ttu-id="d2805-146">Określa centrum powiadomień, do którego to polecenie cmdlet przypisuje reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="d2805-146">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="d2805-147">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów bez względu na używane przez nich klientów.</span><span class="sxs-lookup"><span data-stu-id="d2805-147">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="d2805-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d2805-148">-ResourceGroup</span></span>
<span data-ttu-id="d2805-149">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d2805-149">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="d2805-150">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="d2805-150">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d2805-151">-SASRule</span><span class="sxs-lookup"><span data-stu-id="d2805-151">-SASRule</span></span>
<span data-ttu-id="d2805-152">Określa obiekt **SharedAccessAuthorizationRuleAttributes** , który zawiera informacje o konfiguracji dla reguł autoryzacji, które zostały zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="d2805-152">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2805-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2805-153">-Confirm</span></span>
<span data-ttu-id="d2805-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2805-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2805-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2805-155">-WhatIf</span></span>
<span data-ttu-id="d2805-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2805-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2805-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2805-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2805-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2805-158">CommonParameters</span></span>
<span data-ttu-id="d2805-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2805-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2805-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2805-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2805-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2805-161">INPUTS</span></span>

### <span data-ttu-id="d2805-162">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d2805-162">None</span></span>
<span data-ttu-id="d2805-163">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d2805-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2805-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2805-164">OUTPUTS</span></span>

### <span data-ttu-id="d2805-165">Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d2805-165">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d2805-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2805-166">NOTES</span></span>

## <span data-ttu-id="d2805-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2805-167">RELATED LINKS</span></span>

[<span data-ttu-id="d2805-168">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d2805-168">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="d2805-169">Nowe — AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d2805-169">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="d2805-170">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d2805-170">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


