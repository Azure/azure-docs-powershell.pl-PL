---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: baccd437f98a12376d564bee35bdb74d736ec225
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543163"
---
# <span data-ttu-id="0c54a-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0c54a-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="0c54a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c54a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c54a-103">Tworzy regułę autoryzacji i przypisuje tę regułę do obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0c54a-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c54a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c54a-104">SYNTAX</span></span>

### <span data-ttu-id="0c54a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c54a-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c54a-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c54a-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c54a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0c54a-107">DESCRIPTION</span></span>
<span data-ttu-id="0c54a-108">Polecenie cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** umożliwia utworzenie reguły autoryzacji współużytkowanego podpisu dostępu (SAS) i przypisanie jej do obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0c54a-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="0c54a-109">Reguły autoryzacji zarządzają prawami użytkownika w obszarze nazw i z koncentratorami powiadomień zawartymi w tej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="0c54a-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>

<span data-ttu-id="0c54a-110">To polecenie cmdlet oferuje dwa sposoby tworzenia nowej reguły autoryzacji i przypisywania jej do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="0c54a-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="0c54a-111">Możesz utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes** , a następnie skonfigurować ten obiekt z wartościami właściwości, które ma mieć Nowa reguła.</span><span class="sxs-lookup"><span data-stu-id="0c54a-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="0c54a-112">Można to zrobić za pomocą platformy .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0c54a-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="0c54a-113">Następnie można skopiować te wartości właściwości do nowej reguły za pomocą parametru *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="0c54a-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="0c54a-114">Możesz również utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pomocą parametru *plik_wejściowy* .</span><span class="sxs-lookup"><span data-stu-id="0c54a-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="0c54a-115">Plik JSON jest plikiem tekstowym używającym składni podobnej do następującej:</span><span class="sxs-lookup"><span data-stu-id="0c54a-115">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="0c54a-116">{</span><span class="sxs-lookup"><span data-stu-id="0c54a-116">{</span></span>  
    <span data-ttu-id="0c54a-117">"Nazwa": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="0c54a-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="0c54a-118">"Primaryke": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="0c54a-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="0c54a-119">"Prawa": \[</span><span class="sxs-lookup"><span data-stu-id="0c54a-119">"Rights": \[</span></span>  
        <span data-ttu-id="0c54a-120">"Odsłuchiwanie",</span><span class="sxs-lookup"><span data-stu-id="0c54a-120">"Listen",</span></span>  
        <span data-ttu-id="0c54a-121">Przysła</span><span class="sxs-lookup"><span data-stu-id="0c54a-121">"Send"</span></span>  
    \]  
<span data-ttu-id="0c54a-122">}</span><span class="sxs-lookup"><span data-stu-id="0c54a-122">}</span></span>

<span data-ttu-id="0c54a-123">W przypadku użycia w połączeniu z poleceniem cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** Poprzednia przykładu JSON tworzy regułę autoryzacji o nazwie ContosoAuthorizationRule, która umożliwia użytkownikom odsłuchiwanie i wysyłanie praw do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="0c54a-123">When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="0c54a-124">Składnik *PrimaryKey* używany do uwierzytelniania może być generowany losowo za pomocą następującego polecenia programu Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="0c54a-124">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command:</span></span>

<span data-ttu-id="0c54a-125">\[Convert \] :: ToBase64String ((1.. 32 |% { \[ byte/] (Get-losowo-minimum 0-Maksymalna 255)})</span><span class="sxs-lookup"><span data-stu-id="0c54a-125">\[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="0c54a-126">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c54a-126">EXAMPLES</span></span>

### <span data-ttu-id="0c54a-127">Przykład 1: Tworzenie reguły autoryzacji i przypisywanie jej do obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="0c54a-127">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="0c54a-128">To polecenie powoduje utworzenie reguły autoryzacji i przypisanie tej reguły do obszaru nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="0c54a-128">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="0c54a-129">Podczas tworzenia tej reguły należy określić odpowiedni obszar nazw i grupę zasobów, do których jest przypisany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="0c54a-129">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="0c54a-130">Jednak nie musisz podawać żadnych informacji na temat samej reguły: informacje o regułach zostaną pobrane z pliku wejściowego C:\Configuration\NamespaceAuthorizationRules.jsw dniu.</span><span class="sxs-lookup"><span data-stu-id="0c54a-130">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="0c54a-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c54a-131">PARAMETERS</span></span>

### <span data-ttu-id="0c54a-132">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="0c54a-132">-InputFile</span></span>
<span data-ttu-id="0c54a-133">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji dotyczące nowej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="0c54a-133">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="0c54a-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0c54a-134">-Namespace</span></span>
<span data-ttu-id="0c54a-135">Określa obszar nazw, do którego mają zostać przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="0c54a-135">Specifies the namespace to which the authorization rules will be assigned.</span></span>

<span data-ttu-id="0c54a-136">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0c54a-136">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="0c54a-137">Nowe reguły muszą być przypisane do istniejącego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="0c54a-137">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="0c54a-138">Polecenie cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** nie może utworzyć nowego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="0c54a-138">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="0c54a-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0c54a-139">-ResourceGroup</span></span>
<span data-ttu-id="0c54a-140">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="0c54a-140">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="0c54a-141">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="0c54a-141">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="0c54a-142">Musisz użyć istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c54a-142">You must use an existing resource group.</span></span>
<span data-ttu-id="0c54a-143">To polecenie cmdlet nie może utworzyć nowej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c54a-143">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="0c54a-144">-SASRule</span><span class="sxs-lookup"><span data-stu-id="0c54a-144">-SASRule</span></span>
<span data-ttu-id="0c54a-145">Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji dla nowych reguł.</span><span class="sxs-lookup"><span data-stu-id="0c54a-145">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="0c54a-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c54a-146">-Confirm</span></span>
<span data-ttu-id="0c54a-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c54a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c54a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c54a-148">-WhatIf</span></span>
<span data-ttu-id="0c54a-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c54a-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c54a-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c54a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c54a-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c54a-151">-DefaultProfile</span></span>
<span data-ttu-id="0c54a-152">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c54a-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c54a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c54a-153">CommonParameters</span></span>
<span data-ttu-id="0c54a-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c54a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c54a-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c54a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c54a-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c54a-156">INPUTS</span></span>

## <span data-ttu-id="0c54a-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c54a-157">OUTPUTS</span></span>

### <span data-ttu-id="0c54a-158">Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0c54a-158">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0c54a-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c54a-159">NOTES</span></span>

## <span data-ttu-id="0c54a-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c54a-160">RELATED LINKS</span></span>

[<span data-ttu-id="0c54a-161">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0c54a-161">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="0c54a-162">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0c54a-162">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="0c54a-163">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0c54a-163">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


