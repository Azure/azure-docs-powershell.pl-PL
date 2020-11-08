---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054953"
---
# <span data-ttu-id="d4dac-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4dac-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="d4dac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4dac-102">SYNOPSIS</span></span>
<span data-ttu-id="d4dac-103">Tworzy nową regułę autoryzacji usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="d4dac-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="d4dac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4dac-104">SYNTAX</span></span>

### <span data-ttu-id="d4dac-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="d4dac-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d4dac-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="d4dac-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d4dac-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d4dac-107">DESCRIPTION</span></span>
<span data-ttu-id="d4dac-108">Polecenie cmdlet **New-AzureSBAuthorizationRule** tworzy regułę autoryzacji magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="d4dac-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="d4dac-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4dac-109">EXAMPLES</span></span>

### <span data-ttu-id="d4dac-110">Przykład 1: Tworzenie reguły autoryzacji z wygenerowanym kluczem podstawowym</span><span class="sxs-lookup"><span data-stu-id="d4dac-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="d4dac-111">Tworzy nową regułę autoryzacji na poziomie obszaru nazw przy użyciu uprawnień do wysyłania.</span><span class="sxs-lookup"><span data-stu-id="d4dac-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="d4dac-112">Przykład 2: utworzenie reguły autoryzacji przez podanie klucza podstawowego</span><span class="sxs-lookup"><span data-stu-id="d4dac-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="d4dac-113">Tworzy nową regułę autoryzacji na poziomie kolejki moja Encja ze wszystkimi uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="d4dac-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="d4dac-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4dac-114">PARAMETERS</span></span>

### <span data-ttu-id="d4dac-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="d4dac-115">-EntityName</span></span>
<span data-ttu-id="d4dac-116">Określa nazwę encji, w której ma zostać zastosowana reguła.</span><span class="sxs-lookup"><span data-stu-id="d4dac-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4dac-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="d4dac-117">-EntityType</span></span>
<span data-ttu-id="d4dac-118">Określa typ jednostki.</span><span class="sxs-lookup"><span data-stu-id="d4dac-118">Specifies the entity type.</span></span>
<span data-ttu-id="d4dac-119">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d4dac-119">Valid values are:</span></span>
  
- <span data-ttu-id="d4dac-120">Wykonany</span><span class="sxs-lookup"><span data-stu-id="d4dac-120">Queue</span></span>
- <span data-ttu-id="d4dac-121">Wyspecjalizowan</span><span class="sxs-lookup"><span data-stu-id="d4dac-121">Topic</span></span>
- <span data-ttu-id="d4dac-122">Protokołu</span><span class="sxs-lookup"><span data-stu-id="d4dac-122">Relay</span></span>
- <span data-ttu-id="d4dac-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d4dac-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4dac-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4dac-124">-Name</span></span>
<span data-ttu-id="d4dac-125">Określa unikatową nazwę reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="d4dac-125">Specifies the unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4dac-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d4dac-126">-Namespace</span></span>
<span data-ttu-id="d4dac-127">Określa nazwę obszaru nazw, w którym ma zostać zastosowana reguła autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="d4dac-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="d4dac-128">Jeśli nie podano żadnej *jednostki* , reguła będzie na poziomie obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="d4dac-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="d4dac-129">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="d4dac-129">-Permission</span></span>
<span data-ttu-id="d4dac-130">Uprawnienia autoryzacji (wysyłanie, zarządzanie, odsłuchiwanie).</span><span class="sxs-lookup"><span data-stu-id="d4dac-130">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="d4dac-131">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="d4dac-131">-PrimaryKey</span></span>
<span data-ttu-id="d4dac-132">Określa klucz podstawowy podpisu dostępu udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="d4dac-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="d4dac-133">Zostanie wygenerowana, jeśli nie podano.</span><span class="sxs-lookup"><span data-stu-id="d4dac-133">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="d4dac-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="d4dac-134">-Profile</span></span>
<span data-ttu-id="d4dac-135">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4dac-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4dac-136">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d4dac-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4dac-137">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d4dac-137">-SecondaryKey</span></span>
<span data-ttu-id="d4dac-138">Określa klucz pomocniczy podpisu w dostępie udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="d4dac-138">Specifies the Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="d4dac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4dac-139">CommonParameters</span></span>
<span data-ttu-id="d4dac-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4dac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4dac-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4dac-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4dac-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4dac-142">INPUTS</span></span>

## <span data-ttu-id="d4dac-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4dac-143">OUTPUTS</span></span>

## <span data-ttu-id="d4dac-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4dac-144">NOTES</span></span>

## <span data-ttu-id="d4dac-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4dac-145">RELATED LINKS</span></span>

[<span data-ttu-id="d4dac-146">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4dac-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d4dac-147">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4dac-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d4dac-148">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d4dac-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


