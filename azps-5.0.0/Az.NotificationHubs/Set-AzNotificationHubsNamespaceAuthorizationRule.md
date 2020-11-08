---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 34f63dfc89f2bb1b3b9601e8ff51b280fee9ee42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231703"
---
# <span data-ttu-id="3d01d-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d01d-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="3d01d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d01d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d01d-103">Ustawia reguły autoryzacji obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3d01d-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="3d01d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d01d-104">SYNTAX</span></span>

### <span data-ttu-id="3d01d-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d01d-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d01d-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d01d-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d01d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3d01d-107">DESCRIPTION</span></span>
<span data-ttu-id="3d01d-108">Polecenie cmdlet **Set-AzNotificationHubsNamespaceAuthorizationRule** modyfikuje regułę autoryzacji współużytkowanego podpisu dostępu (SAS) przypisaną do obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3d01d-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="3d01d-109">Reguły autoryzacji zarządzają prawami użytkownika w obszarze nazw i z koncentratorami powiadomień zawartymi w tej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="3d01d-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="3d01d-110">To polecenie cmdlet oferuje dwie metody modyfikowania reguły autoryzacji przypisanej do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="3d01d-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="3d01d-111">W przypadku jednej z nich można utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes** , a następnie skonfigurować te obiekty za pomocą wartości właściwości, które mają mieć reguła.</span><span class="sxs-lookup"><span data-stu-id="3d01d-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="3d01d-112">Aby to zrobić, możesz skorzystać z programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="3d01d-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="3d01d-113">Następnie można skopiować te wartości właściwości do reguły za pośrednictwem parametru *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="3d01d-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="3d01d-114">Możesz również utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pośrednictwem parametru *plik_wejściowy* .</span><span class="sxs-lookup"><span data-stu-id="3d01d-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="3d01d-115">Plik JSON jest plikiem tekstowym używającym składni podobnej do następującej: {</span><span class="sxs-lookup"><span data-stu-id="3d01d-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="3d01d-116">"Nazwa": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="3d01d-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="3d01d-117">"Primaryke": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="3d01d-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="3d01d-118">"Prawa": \[</span><span class="sxs-lookup"><span data-stu-id="3d01d-118">"Rights": \[</span></span>  
        <span data-ttu-id="3d01d-119">"Odsłuchiwanie",</span><span class="sxs-lookup"><span data-stu-id="3d01d-119">"Listen",</span></span>  
        <span data-ttu-id="3d01d-120">Przysła</span><span class="sxs-lookup"><span data-stu-id="3d01d-120">"Send"</span></span>  
    \]  
<span data-ttu-id="3d01d-121">} Gdy jest używana w połączeniu z poleceniem cmdlet **Set-AzNotificationHubsNamespaceAuthorizationRule** , poprzednia próbka JSON modyfikuje regułę autoryzacji o nazwie ContosoAuthorizationRule, aby dać użytkownikom możliwość odsłuchiwania i wysyłania praw do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="3d01d-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="3d01d-122">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d01d-122">EXAMPLES</span></span>

### <span data-ttu-id="3d01d-123">Przykład 1: modyfikowanie reguły autoryzacji przypisanej do obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="3d01d-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="3d01d-124">To polecenie modyfikuje regułę autoryzacji przypisaną do obszaru nazw o nazwie ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="3d01d-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="3d01d-125">Musisz określić grupę zasobów, do której jest przypisany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="3d01d-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="3d01d-126">Informacje dotyczące reguły autoryzacji nie są uwzględniane w samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3d01d-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="3d01d-127">Zamiast tego informacje te są uzyskiwane z pliku wejściowego C:\Configuration\AuthorizationRules.jsna.</span><span class="sxs-lookup"><span data-stu-id="3d01d-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="3d01d-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d01d-128">PARAMETERS</span></span>

### <span data-ttu-id="3d01d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d01d-129">-DefaultProfile</span></span>
<span data-ttu-id="3d01d-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3d01d-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d01d-131">-Force</span><span class="sxs-lookup"><span data-stu-id="3d01d-131">-Force</span></span>
<span data-ttu-id="3d01d-132">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3d01d-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3d01d-133">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="3d01d-133">-InputFile</span></span>
<span data-ttu-id="3d01d-134">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji nowej reguły.</span><span class="sxs-lookup"><span data-stu-id="3d01d-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="3d01d-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d01d-135">-Namespace</span></span>
<span data-ttu-id="3d01d-136">Określa obszar nazw zawierający reguły autoryzacji, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="3d01d-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="3d01d-137">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3d01d-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3d01d-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3d01d-138">-ResourceGroup</span></span>
<span data-ttu-id="3d01d-139">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="3d01d-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="3d01d-140">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="3d01d-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3d01d-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="3d01d-141">-SASRule</span></span>
<span data-ttu-id="3d01d-142">Określa obiekt **SharedAccessAuthorizationRuleAttributes** , który zawiera informacje o konfiguracji dotyczące reguł autoryzacji, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d01d-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3d01d-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d01d-143">-Confirm</span></span>
<span data-ttu-id="3d01d-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d01d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d01d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d01d-145">-WhatIf</span></span>
<span data-ttu-id="3d01d-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d01d-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d01d-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d01d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d01d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d01d-148">CommonParameters</span></span>
<span data-ttu-id="3d01d-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d01d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d01d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d01d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d01d-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d01d-151">INPUTS</span></span>

### <span data-ttu-id="3d01d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3d01d-152">System.String</span></span>

## <span data-ttu-id="3d01d-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d01d-153">OUTPUTS</span></span>

### <span data-ttu-id="3d01d-154">Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3d01d-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3d01d-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d01d-155">NOTES</span></span>

## <span data-ttu-id="3d01d-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d01d-156">RELATED LINKS</span></span>

[<span data-ttu-id="3d01d-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d01d-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="3d01d-158">Nowe — AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d01d-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="3d01d-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d01d-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


