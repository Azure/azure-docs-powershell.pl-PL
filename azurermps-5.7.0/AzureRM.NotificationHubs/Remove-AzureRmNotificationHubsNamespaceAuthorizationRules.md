---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: eee4d9db5cbc64f8ae7e17f18026f5bd2aeca310
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719446"
---
# <span data-ttu-id="b97b6-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b97b6-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="b97b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b97b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b97b6-103">Usuwa regułę autoryzacji z obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="b97b6-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b97b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b97b6-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b97b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b97b6-105">DESCRIPTION</span></span>
<span data-ttu-id="b97b6-106">Polecenie cmdlet **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** usuwa regułę autoryzacji współużytkowanego podpisu dostępu (SAS) z obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="b97b6-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>

<span data-ttu-id="b97b6-107">Reguły autoryzacji zarządzają dostępem do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="b97b6-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="b97b6-108">Odbywa się to za pomocą tworzenia linków, takich jak identyfikatory URI, na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="b97b6-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="b97b6-109">Poziomy uprawnień mogą być następujące:</span><span class="sxs-lookup"><span data-stu-id="b97b6-109">Permission levels can be of the following:</span></span> 

- <span data-ttu-id="b97b6-110">Słuch</span><span class="sxs-lookup"><span data-stu-id="b97b6-110">Listen</span></span>
- <span data-ttu-id="b97b6-111">Wyślij</span><span class="sxs-lookup"><span data-stu-id="b97b6-111">Send</span></span>
- <span data-ttu-id="b97b6-112">Zarządzanie</span><span class="sxs-lookup"><span data-stu-id="b97b6-112">Manage</span></span>

<span data-ttu-id="b97b6-113">Klienci są kierowani do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="b97b6-113">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="b97b6-114">Na przykład klient, który udzielił uprawnień do odsłuchiwania, jest kierowany na identyfikator URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="b97b6-114">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>

<span data-ttu-id="b97b6-115">Usunięcie reguły autoryzacji powoduje również usunięcie odpowiednich uprawnień użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b97b6-115">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="b97b6-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b97b6-116">EXAMPLES</span></span>

### <span data-ttu-id="b97b6-117">Przykład 1: Usuwanie reguły autoryzacji z obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="b97b6-117">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="b97b6-118">To polecenie usuwa regułę autoryzacji o nazwie ListenRule z obszaru nazw o nazwie ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="b97b6-118">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="b97b6-119">Po uruchomieniu tego polecenia musisz określić grupę zasobów, do której jest przypisany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="b97b6-119">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="b97b6-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b97b6-120">PARAMETERS</span></span>

### <span data-ttu-id="b97b6-121">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b97b6-121">-AuthorizationRule</span></span>
<span data-ttu-id="b97b6-122">Określa nazwę reguły uwierzytelniania SAS do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b97b6-122">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="b97b6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97b6-123">-DefaultProfile</span></span>
<span data-ttu-id="b97b6-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b97b6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b97b6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b97b6-125">-Force</span></span>
<span data-ttu-id="b97b6-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b97b6-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b97b6-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b97b6-127">-Namespace</span></span>
<span data-ttu-id="b97b6-128">Określa obszar nazw, do którego są przypisywane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="b97b6-128">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="b97b6-129">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="b97b6-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b97b6-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b97b6-130">-ResourceGroup</span></span>
<span data-ttu-id="b97b6-131">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="b97b6-131">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="b97b6-132">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="b97b6-132">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b97b6-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b97b6-133">-Confirm</span></span>
<span data-ttu-id="b97b6-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b97b6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b97b6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b97b6-135">-WhatIf</span></span>
<span data-ttu-id="b97b6-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b97b6-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b97b6-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b97b6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b97b6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97b6-138">CommonParameters</span></span>
<span data-ttu-id="b97b6-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97b6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97b6-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b97b6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97b6-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b97b6-141">INPUTS</span></span>

### <span data-ttu-id="b97b6-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b97b6-142">None</span></span>
<span data-ttu-id="b97b6-143">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b97b6-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b97b6-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b97b6-144">OUTPUTS</span></span>

### <span data-ttu-id="b97b6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b97b6-145">System.Boolean</span></span>

## <span data-ttu-id="b97b6-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b97b6-146">NOTES</span></span>

## <span data-ttu-id="b97b6-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b97b6-147">RELATED LINKS</span></span>

[<span data-ttu-id="b97b6-148">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b97b6-148">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="b97b6-149">Nowe — AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b97b6-149">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="b97b6-150">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b97b6-150">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


