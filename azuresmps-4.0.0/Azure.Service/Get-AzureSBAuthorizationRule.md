---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054580"
---
# <span data-ttu-id="61253-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="61253-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="61253-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61253-102">SYNOPSIS</span></span>
<span data-ttu-id="61253-103">Pobiera reguły autoryzacji magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="61253-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="61253-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61253-104">SYNTAX</span></span>

### <span data-ttu-id="61253-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="61253-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="61253-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="61253-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="61253-107">Opis</span><span class="sxs-lookup"><span data-stu-id="61253-107">DESCRIPTION</span></span>
<span data-ttu-id="61253-108">Pobiera reguły autoryzacji magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="61253-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="61253-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61253-109">EXAMPLES</span></span>

### <span data-ttu-id="61253-110">Przykład 1: pobieranie reguły autoryzacji na poziomie przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="61253-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="61253-111">Pobiera wszystkie dostępne reguły autoryzacji w obszarze Moja przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="61253-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="61253-112">Przykład 2: uzyskiwanie reguły autoryzacji dla kolejki</span><span class="sxs-lookup"><span data-stu-id="61253-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="61253-113">Pobiera wszystkie dostępne reguły autoryzacji w kolejce moja jednostka w obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="61253-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="61253-114">Przykład 3: uzyskiwanie reguły autoryzacji według nazwy</span><span class="sxs-lookup"><span data-stu-id="61253-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="61253-115">Pobiera regułę autoryzacji o nazwie Moja reguła na poziomie mój obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="61253-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="61253-116">Przykład 4: uzyskiwanie reguły autoryzacji według uprawnień</span><span class="sxs-lookup"><span data-stu-id="61253-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="61253-117">Pobiera wszystkie reguły autoryzacji, które mają uprawnienie Wyślij do na poziomie obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="61253-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="61253-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61253-118">PARAMETERS</span></span>

### <span data-ttu-id="61253-119">-EntityName</span><span class="sxs-lookup"><span data-stu-id="61253-119">-EntityName</span></span>
<span data-ttu-id="61253-120">Nazwa encji, w której ma zostać zastosowana reguła.</span><span class="sxs-lookup"><span data-stu-id="61253-120">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="61253-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="61253-121">-EntityType</span></span>
<span data-ttu-id="61253-122">Typ jednostki (Kolejka, temat, przekazywanie, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="61253-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="61253-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61253-123">-Name</span></span>
<span data-ttu-id="61253-124">Nazwa unikatowej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="61253-124">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61253-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="61253-125">-Namespace</span></span>
<span data-ttu-id="61253-126">Nazwa obszaru nazw, aby zastosować regułę autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="61253-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="61253-127">Jeśli nie podano żadnej jednostki, reguła będzie na poziomie obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="61253-127">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="61253-128">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="61253-128">-Permission</span></span>
<span data-ttu-id="61253-129">Uprawnienia autoryzacji do filtrowania (wysyłanie, zarządzanie, odsłuchiwanie).</span><span class="sxs-lookup"><span data-stu-id="61253-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="61253-130">Ta funkcja jest dokładna.</span><span class="sxs-lookup"><span data-stu-id="61253-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61253-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="61253-131">-Profile</span></span>
<span data-ttu-id="61253-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61253-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61253-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="61253-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61253-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61253-134">CommonParameters</span></span>
<span data-ttu-id="61253-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61253-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61253-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61253-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61253-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61253-137">INPUTS</span></span>

## <span data-ttu-id="61253-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61253-138">OUTPUTS</span></span>

## <span data-ttu-id="61253-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61253-139">NOTES</span></span>

## <span data-ttu-id="61253-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61253-140">RELATED LINKS</span></span>

[<span data-ttu-id="61253-141">Nowe — AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="61253-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="61253-142">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="61253-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="61253-143">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="61253-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


