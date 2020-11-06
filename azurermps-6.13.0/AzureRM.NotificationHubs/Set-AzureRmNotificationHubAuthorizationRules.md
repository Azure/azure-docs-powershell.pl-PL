---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 24c65b6f7bf39d4fe046b020a9427dba7bf53aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544972"
---
# <span data-ttu-id="fcdc2-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fcdc2-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="fcdc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcdc2-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdc2-103">Ustawia reguły autoryzacji dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcdc2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcdc2-104">SYNTAX</span></span>

### <span data-ttu-id="fcdc2-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdc2-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcdc2-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcdc2-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcdc2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fcdc2-107">DESCRIPTION</span></span>
<span data-ttu-id="fcdc2-108">Polecenie cmdlet **Set-AzureRmNotificationHubAuthorizationRules** powoduje zmodyfikowanie reguły autoryzacji podpisu dostępu współużytkowanego (SAS) przypisanej do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="fcdc2-109">Reguły autoryzacji zarządzają dostępem do koncentratorów powiadomień przez tworzenie linków jako identyfikatorów URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="fcdc2-110">Poziom uprawnień może być jednym z następujących:</span><span class="sxs-lookup"><span data-stu-id="fcdc2-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="fcdc2-111">Słuch</span><span class="sxs-lookup"><span data-stu-id="fcdc2-111">Listen</span></span>
- <span data-ttu-id="fcdc2-112">Wyślij</span><span class="sxs-lookup"><span data-stu-id="fcdc2-112">Send</span></span>
- <span data-ttu-id="fcdc2-113">Zarządzanie klientami jest przekierowywane do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="fcdc2-114">Na przykład klient, któremu przydzielono uprawnienie odsłuchiwania, będzie kierowany na identyfikator URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="fcdc2-115">To polecenie cmdlet oferuje dwie metody modyfikowania reguły autoryzacji przypisanej do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="fcdc2-116">W przypadku jednej z nich można utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes** , a następnie skonfigurować te obiekty za pomocą wartości właściwości, które mają mieć reguła.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="fcdc2-117">Obiekt można skonfigurować za pośrednictwem platformy .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="fcdc2-118">Następnie można skopiować te wartości właściwości do reguły za pomocą parametru *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="fcdc2-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="fcdc2-119">Możesz również utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pośrednictwem parametru *plik_wejściowy* .</span><span class="sxs-lookup"><span data-stu-id="fcdc2-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="fcdc2-120">Plik JSON to plik tekstowy, w którym jest używana składnia podobna do następującej: {"name": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="fcdc2-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="fcdc2-121">"Primaryke": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="fcdc2-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="fcdc2-122">"Prawa": \[</span><span class="sxs-lookup"><span data-stu-id="fcdc2-122">"Rights": \[</span></span>  
        <span data-ttu-id="fcdc2-123">"Odsłuchiwanie",</span><span class="sxs-lookup"><span data-stu-id="fcdc2-123">"Listen",</span></span>  
        <span data-ttu-id="fcdc2-124">Przysła</span><span class="sxs-lookup"><span data-stu-id="fcdc2-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="fcdc2-125">} Gdy jest używana w połączeniu z poleceniem cmdlet New-AzureRmNotificationHubAuthorizationRules, przed powyższym przykładem JSON jest modyfikowana reguła autoryzacji o nazwie ContosoAuthorizationRule w celu zapewnienia użytkownikom odsłuchiwania i wysyłania praw do centrum.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-125">} When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="fcdc2-126">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcdc2-126">EXAMPLES</span></span>

### <span data-ttu-id="fcdc2-127">Przykład 1: modyfikowanie reguły autoryzacji przypisanej do centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="fcdc2-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="fcdc2-128">To polecenie modyfikuje regułę autoryzacji przypisaną do centrum powiadomień o nazwie ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="fcdc2-129">Musisz określić obszar nazw, w którym znajduje się centrum, oraz grupę zasobów, do których jest przypisany koncentrator.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="fcdc2-130">Informacje na temat modyfikacji reguły nie są uwzględniane w samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="fcdc2-131">Zamiast tego informacje są dostępne w pliku wejściowym C:\Configuration\AuthorizationRules.jsna.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="fcdc2-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcdc2-132">PARAMETERS</span></span>

### <span data-ttu-id="fcdc2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdc2-133">-DefaultProfile</span></span>
<span data-ttu-id="fcdc2-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fcdc2-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcdc2-135">-Force</span><span class="sxs-lookup"><span data-stu-id="fcdc2-135">-Force</span></span>
<span data-ttu-id="fcdc2-136">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fcdc2-137">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="fcdc2-137">-InputFile</span></span>
<span data-ttu-id="fcdc2-138">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji nowej reguły.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="fcdc2-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fcdc2-139">-Namespace</span></span>
<span data-ttu-id="fcdc2-140">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="fcdc2-141">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="fcdc2-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="fcdc2-142">-NotificationHub</span></span>
<span data-ttu-id="fcdc2-143">Określa centrum powiadomień, do którego to polecenie cmdlet przypisuje reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="fcdc2-144">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów bez względu na używane przez nich klientów.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="fcdc2-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fcdc2-145">-ResourceGroup</span></span>
<span data-ttu-id="fcdc2-146">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="fcdc2-147">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="fcdc2-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="fcdc2-148">-SASRule</span></span>
<span data-ttu-id="fcdc2-149">Określa obiekt **SharedAccessAuthorizationRuleAttributes** , który zawiera informacje o konfiguracji dla reguł autoryzacji, które zostały zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="fcdc2-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fcdc2-150">-Confirm</span></span>
<span data-ttu-id="fcdc2-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcdc2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcdc2-152">-WhatIf</span></span>
<span data-ttu-id="fcdc2-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcdc2-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcdc2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdc2-155">CommonParameters</span></span>
<span data-ttu-id="fcdc2-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcdc2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdc2-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcdc2-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdc2-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcdc2-158">INPUTS</span></span>

### <span data-ttu-id="fcdc2-159">System. String</span><span class="sxs-lookup"><span data-stu-id="fcdc2-159">System.String</span></span>

## <span data-ttu-id="fcdc2-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcdc2-160">OUTPUTS</span></span>

### <span data-ttu-id="fcdc2-161">Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fcdc2-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="fcdc2-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcdc2-162">NOTES</span></span>

## <span data-ttu-id="fcdc2-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcdc2-163">RELATED LINKS</span></span>

[<span data-ttu-id="fcdc2-164">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fcdc2-164">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="fcdc2-165">Nowe — AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fcdc2-165">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="fcdc2-166">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fcdc2-166">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


