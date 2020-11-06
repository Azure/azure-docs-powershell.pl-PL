---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ed94e34f754298e89bf1f18d5264f11c2c9c308c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554105"
---
# <span data-ttu-id="8732a-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8732a-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="8732a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8732a-102">SYNOPSIS</span></span>
<span data-ttu-id="8732a-103">Ustawia reguły autoryzacji obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8732a-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8732a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8732a-104">SYNTAX</span></span>

### <span data-ttu-id="8732a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8732a-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8732a-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="8732a-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8732a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8732a-107">DESCRIPTION</span></span>
<span data-ttu-id="8732a-108">Polecenie cmdlet **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** modyfikuje regułę autoryzacji współużytkowanego podpisu dostępu (SAS) przypisaną do obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8732a-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="8732a-109">Reguły autoryzacji zarządzają prawami użytkownika w obszarze nazw i z koncentratorami powiadomień zawartymi w tej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="8732a-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>

<span data-ttu-id="8732a-110">To polecenie cmdlet oferuje dwie metody modyfikowania reguły autoryzacji przypisanej do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="8732a-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="8732a-111">W przypadku jednej z nich można utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes** , a następnie skonfigurować te obiekty za pomocą wartości właściwości, które mają mieć reguła.</span><span class="sxs-lookup"><span data-stu-id="8732a-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="8732a-112">Aby to zrobić, możesz skorzystać z programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8732a-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="8732a-113">Następnie można skopiować te wartości właściwości do reguły za pośrednictwem parametru *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="8732a-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>

<span data-ttu-id="8732a-114">Możesz również utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pośrednictwem parametru *plik_wejściowy* .</span><span class="sxs-lookup"><span data-stu-id="8732a-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="8732a-115">Plik JSON jest plikiem tekstowym używającym składni podobnej do następującej:</span><span class="sxs-lookup"><span data-stu-id="8732a-115">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="8732a-116">{</span><span class="sxs-lookup"><span data-stu-id="8732a-116">{</span></span>  
    <span data-ttu-id="8732a-117">"Nazwa": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="8732a-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="8732a-118">"Primaryke": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="8732a-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="8732a-119">"Prawa": \[</span><span class="sxs-lookup"><span data-stu-id="8732a-119">"Rights": \[</span></span>  
        <span data-ttu-id="8732a-120">"Odsłuchiwanie",</span><span class="sxs-lookup"><span data-stu-id="8732a-120">"Listen",</span></span>  
        <span data-ttu-id="8732a-121">Przysła</span><span class="sxs-lookup"><span data-stu-id="8732a-121">"Send"</span></span>  
    \]  
<span data-ttu-id="8732a-122">}</span><span class="sxs-lookup"><span data-stu-id="8732a-122">}</span></span>

<span data-ttu-id="8732a-123">W przypadku użycia w połączeniu z poleceniem cmdlet **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** Poprzednia próbka JSON modyfikuje regułę autoryzacji o nazwie ContosoAuthorizationRule w celu nasłuchiwania i wysyłania praw do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="8732a-123">When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="8732a-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8732a-124">EXAMPLES</span></span>

### <span data-ttu-id="8732a-125">Przykład 1: modyfikowanie reguły autoryzacji przypisanej do obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="8732a-125">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="8732a-126">To polecenie modyfikuje regułę autoryzacji przypisaną do obszaru nazw o nazwie ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="8732a-126">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="8732a-127">Musisz określić grupę zasobów, do której jest przypisany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="8732a-127">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="8732a-128">Informacje dotyczące reguły autoryzacji nie są uwzględniane w samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="8732a-128">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="8732a-129">Zamiast tego informacje te są uzyskiwane z pliku wejściowego C:\Configuration\AuthorizationRules.jsna.</span><span class="sxs-lookup"><span data-stu-id="8732a-129">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="8732a-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8732a-130">PARAMETERS</span></span>

### <span data-ttu-id="8732a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8732a-131">-DefaultProfile</span></span>
<span data-ttu-id="8732a-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8732a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8732a-133">-Force</span><span class="sxs-lookup"><span data-stu-id="8732a-133">-Force</span></span>
<span data-ttu-id="8732a-134">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8732a-134">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8732a-135">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="8732a-135">-InputFile</span></span>
<span data-ttu-id="8732a-136">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji nowej reguły.</span><span class="sxs-lookup"><span data-stu-id="8732a-136">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8732a-137">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8732a-137">-Namespace</span></span>
<span data-ttu-id="8732a-138">Określa obszar nazw zawierający reguły autoryzacji, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="8732a-138">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="8732a-139">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8732a-139">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8732a-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8732a-140">-ResourceGroup</span></span>
<span data-ttu-id="8732a-141">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="8732a-141">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="8732a-142">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="8732a-142">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8732a-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="8732a-143">-SASRule</span></span>
<span data-ttu-id="8732a-144">Określa obiekt **SharedAccessAuthorizationRuleAttributes** , który zawiera informacje o konfiguracji dotyczące reguł autoryzacji, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8732a-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8732a-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8732a-145">-Confirm</span></span>
<span data-ttu-id="8732a-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8732a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8732a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8732a-147">-WhatIf</span></span>
<span data-ttu-id="8732a-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8732a-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8732a-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8732a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8732a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8732a-150">CommonParameters</span></span>
<span data-ttu-id="8732a-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8732a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8732a-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8732a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8732a-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8732a-153">INPUTS</span></span>

### <span data-ttu-id="8732a-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8732a-154">None</span></span>
<span data-ttu-id="8732a-155">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8732a-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8732a-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8732a-156">OUTPUTS</span></span>

### <span data-ttu-id="8732a-157">Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8732a-157">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8732a-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8732a-158">NOTES</span></span>

## <span data-ttu-id="8732a-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8732a-159">RELATED LINKS</span></span>

[<span data-ttu-id="8732a-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8732a-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="8732a-161">Nowe — AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8732a-161">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="8732a-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8732a-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


