---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 2f5ff44e6d96900afe36b9ade8360fb0a69ec726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951098"
---
# <span data-ttu-id="d5b7d-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d5b7d-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="d5b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b7d-103">Ustawia reguły autoryzacji dla przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="d5b7d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5b7d-104">SYNTAX</span></span>

### <span data-ttu-id="d5b7d-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5b7d-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5b7d-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5b7d-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5b7d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5b7d-107">DESCRIPTION</span></span>
<span data-ttu-id="d5b7d-108">Polecenie cmdlet **Set-AzNotificationHubsNamespaceAuthorizationRule** modyfikuje regułę autoryzacji sas (Shared Access Signature) przypisaną do przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="d5b7d-109">Reguły autoryzacji zarządzają prawami użytkowników do przestrzeni nazw i do centrum powiadomień zawartych w tej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="d5b7d-110">To polecenie cmdlet udostępnia dwa sposoby modyfikowania reguły autoryzacji przypisanej do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="d5b7d-111">Na przykład możesz utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes,** a następnie skonfigurować ten obiekt przy użyciu wartości właściwości, które mają być posiadania reguły.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="d5b7d-112">Aby to .NET Framework, możesz użyć tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="d5b7d-113">Następnie można skopiować te wartości właściwości do reguły za pomocą *parametru SASRule.*</span><span class="sxs-lookup"><span data-stu-id="d5b7d-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="d5b7d-114">Ewentualnie możesz utworzyć plik JSON (JavaScript Object Notation) zawierający odpowiednie wartości konfiguracyjne, a następnie zastosować te wartości za pomocą *parametru InputFile.*</span><span class="sxs-lookup"><span data-stu-id="d5b7d-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="d5b7d-115">Plik JSON to plik tekstowy o składni podobnej do tej: {</span><span class="sxs-lookup"><span data-stu-id="d5b7d-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="d5b7d-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="d5b7d-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="d5b7d-117">"Klucz Podstawowy": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="d5b7d-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="d5b7d-118">"Prawa": \[</span><span class="sxs-lookup"><span data-stu-id="d5b7d-118">"Rights": \[</span></span>  
        <span data-ttu-id="d5b7d-119">"Słuchaj",</span><span class="sxs-lookup"><span data-stu-id="d5b7d-119">"Listen",</span></span>  
        <span data-ttu-id="d5b7d-120">"Wyślij"</span><span class="sxs-lookup"><span data-stu-id="d5b7d-120">"Send"</span></span>  
    \]  
<span data-ttu-id="d5b7d-121">} W połączeniu z poleceniem cmdlet **Set-AzNotificationHubsNamespaceAuthorizationRule** poprzedni przykład JSON modyfikuje regułę autoryzacji o nazwie ContosoAuthorizationRule, aby nadać użytkownikom prawa do odsłuchiania i wysyłania do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="d5b7d-122">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5b7d-122">EXAMPLES</span></span>

### <span data-ttu-id="d5b7d-123">Przykład 1. Modyfikowanie reguły autoryzacji przypisanej do przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="d5b7d-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="d5b7d-124">To polecenie modyfikuje regułę autoryzacji przypisaną do przestrzeni nazw o nazwie ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="d5b7d-125">Należy określić grupę zasobów, do których jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="d5b7d-126">Informacje na temat reguły autoryzacji nie są zawarte w samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="d5b7d-127">Zamiast tego informacje są uzyskiwane z pliku wejściowego, C:\Configuration\AuthorizationRules.jsdalej.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="d5b7d-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5b7d-128">PARAMETERS</span></span>

### <span data-ttu-id="d5b7d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b7d-129">-DefaultProfile</span></span>
<span data-ttu-id="d5b7d-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d5b7d-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5b7d-131">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d5b7d-131">-Force</span></span>
<span data-ttu-id="d5b7d-132">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d5b7d-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="d5b7d-133">-InputFile</span></span>
<span data-ttu-id="d5b7d-134">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji nowej reguły.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="d5b7d-135">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="d5b7d-135">-Namespace</span></span>
<span data-ttu-id="d5b7d-136">Określa przestrzeń nazw zawierającą reguły autoryzacji, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="d5b7d-137">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d5b7d-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d5b7d-138">-ResourceGroup</span></span>
<span data-ttu-id="d5b7d-139">Określa grupę zasobów, do której jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="d5b7d-140">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d5b7d-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="d5b7d-141">-SASRule</span></span>
<span data-ttu-id="d5b7d-142">Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji reguł autoryzacji, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d5b7d-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5b7d-143">-Confirm</span></span>
<span data-ttu-id="d5b7d-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5b7d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5b7d-145">-WhatIf</span></span>
<span data-ttu-id="d5b7d-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5b7d-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5b7d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b7d-148">CommonParameters</span></span>
<span data-ttu-id="d5b7d-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b7d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b7d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5b7d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b7d-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5b7d-151">INPUTS</span></span>

### <span data-ttu-id="d5b7d-152">System.String</span><span class="sxs-lookup"><span data-stu-id="d5b7d-152">System.String</span></span>

## <span data-ttu-id="d5b7d-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5b7d-153">OUTPUTS</span></span>

### <span data-ttu-id="d5b7d-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d5b7d-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d5b7d-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5b7d-155">NOTES</span></span>

## <span data-ttu-id="d5b7d-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5b7d-156">RELATED LINKS</span></span>

[<span data-ttu-id="d5b7d-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d5b7d-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="d5b7d-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d5b7d-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="d5b7d-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d5b7d-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


