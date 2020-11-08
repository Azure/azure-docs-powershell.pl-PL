---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054786"
---
# <span data-ttu-id="4b29c-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b29c-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="4b29c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b29c-102">SYNOPSIS</span></span>
<span data-ttu-id="4b29c-103">Umożliwia zaktualizowanie istniejącej reguły autoryzacji usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="4b29c-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="4b29c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b29c-104">SYNTAX</span></span>

### <span data-ttu-id="4b29c-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="4b29c-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4b29c-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="4b29c-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4b29c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4b29c-107">DESCRIPTION</span></span>
<span data-ttu-id="4b29c-108">Umożliwia zaktualizowanie istniejącej reguły autoryzacji usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="4b29c-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="4b29c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b29c-109">EXAMPLES</span></span>

### <span data-ttu-id="4b29c-110">Przykład 1: odnawianie klucza podstawowego dla reguły autoryzacji na poziomie przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="4b29c-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="4b29c-111">Klucz podstawowy zostanie odnowiony.</span><span class="sxs-lookup"><span data-stu-id="4b29c-111">The primary key is renewed.</span></span>

### <span data-ttu-id="4b29c-112">Przykład 2: uprawnienie aktualizowanie reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="4b29c-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="4b29c-113">Umożliwia zaktualizowanie uprawnień.</span><span class="sxs-lookup"><span data-stu-id="4b29c-113">Updates the permissions.</span></span>

## <span data-ttu-id="4b29c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b29c-114">PARAMETERS</span></span>

### <span data-ttu-id="4b29c-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="4b29c-115">-EntityName</span></span>
<span data-ttu-id="4b29c-116">Nazwa encji, w której ma zostać zastosowana reguła.</span><span class="sxs-lookup"><span data-stu-id="4b29c-116">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b29c-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="4b29c-117">-EntityType</span></span>
<span data-ttu-id="4b29c-118">Typ jednostki (Kolejka, temat, przekazywanie, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="4b29c-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b29c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4b29c-119">-Name</span></span>
<span data-ttu-id="4b29c-120">Nazwa unikatowej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="4b29c-120">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b29c-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b29c-121">-Namespace</span></span>
<span data-ttu-id="4b29c-122">Nazwa obszaru nazw, aby zastosować regułę autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="4b29c-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="4b29c-123">Jeśli nie podano żadnej jednostki, reguła będzie na poziomie obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="4b29c-123">If no EntityName provided the rule will be on the namespace level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b29c-124">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="4b29c-124">-Permission</span></span>
<span data-ttu-id="4b29c-125">Uprawnienia autoryzacji (wysyłanie, zarządzanie, odsłuchiwanie).</span><span class="sxs-lookup"><span data-stu-id="4b29c-125">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b29c-126">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="4b29c-126">-PrimaryKey</span></span>
<span data-ttu-id="4b29c-127">Klucz podstawowy podpisu dostępu udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="4b29c-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="4b29c-128">Zostanie wygenerowana, jeśli nie podano.</span><span class="sxs-lookup"><span data-stu-id="4b29c-128">Will be generated if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b29c-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="4b29c-129">-Profile</span></span>
<span data-ttu-id="4b29c-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b29c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4b29c-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4b29c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b29c-132">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4b29c-132">-SecondaryKey</span></span>
<span data-ttu-id="4b29c-133">Pomocniczy klucz podpisu w dostępie udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="4b29c-133">The Shared Access Signature secondary key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b29c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b29c-134">CommonParameters</span></span>
<span data-ttu-id="4b29c-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b29c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b29c-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b29c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b29c-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b29c-137">INPUTS</span></span>

## <span data-ttu-id="4b29c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b29c-138">OUTPUTS</span></span>

## <span data-ttu-id="4b29c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b29c-139">NOTES</span></span>

## <span data-ttu-id="4b29c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b29c-140">RELATED LINKS</span></span>

[<span data-ttu-id="4b29c-141">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b29c-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="4b29c-142">Nowe — AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b29c-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="4b29c-143">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b29c-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


