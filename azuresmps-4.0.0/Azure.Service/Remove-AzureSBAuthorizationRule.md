---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055097"
---
# <span data-ttu-id="cc960-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cc960-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="cc960-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc960-102">SYNOPSIS</span></span>
<span data-ttu-id="cc960-103">Usuwa istniejącą regułę autoryzacji usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="cc960-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="cc960-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc960-104">SYNTAX</span></span>

### <span data-ttu-id="cc960-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="cc960-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cc960-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="cc960-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc960-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cc960-107">DESCRIPTION</span></span>
<span data-ttu-id="cc960-108">Usuwa istniejącą regułę autoryzacji usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="cc960-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="cc960-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc960-109">EXAMPLES</span></span>

### <span data-ttu-id="cc960-110">Przykład 1: Usuwanie reguły autoryzacji na poziomie przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cc960-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="cc960-111">Usuwa regułę autoryzacji z obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="cc960-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="cc960-112">Przykład 2: Usuwanie reguły autoryzacji kolejki</span><span class="sxs-lookup"><span data-stu-id="cc960-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="cc960-113">Usuwa regułę autoryzacji o nazwie Moja reguła dla kolejki moja encja w obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="cc960-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="cc960-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc960-114">PARAMETERS</span></span>

### <span data-ttu-id="cc960-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="cc960-115">-EntityName</span></span>
<span data-ttu-id="cc960-116">Nazwa encji, w której ma zostać zastosowana reguła.</span><span class="sxs-lookup"><span data-stu-id="cc960-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="cc960-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="cc960-117">-EntityType</span></span>
<span data-ttu-id="cc960-118">Typ jednostki (Kolejka, temat, przekazywanie, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="cc960-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="cc960-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc960-119">-Name</span></span>
<span data-ttu-id="cc960-120">Nazwa unikatowej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="cc960-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="cc960-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc960-121">-Namespace</span></span>
<span data-ttu-id="cc960-122">Nazwa obszaru nazw, aby zastosować regułę autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="cc960-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="cc960-123">Jeśli nie podano żadnej jednostki, reguła będzie na poziomie obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="cc960-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="cc960-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc960-124">-PassThru</span></span>
<span data-ttu-id="cc960-125">Wskazuje, że to polecenie cmdlet zwraca obiekt reprezentujący element, na którym działa.</span><span class="sxs-lookup"><span data-stu-id="cc960-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="cc960-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cc960-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc960-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="cc960-127">-Profile</span></span>
<span data-ttu-id="cc960-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc960-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc960-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="cc960-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cc960-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc960-130">CommonParameters</span></span>
<span data-ttu-id="cc960-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc960-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc960-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc960-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc960-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc960-133">INPUTS</span></span>

## <span data-ttu-id="cc960-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc960-134">OUTPUTS</span></span>

## <span data-ttu-id="cc960-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc960-135">NOTES</span></span>

## <span data-ttu-id="cc960-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc960-136">RELATED LINKS</span></span>

[<span data-ttu-id="cc960-137">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cc960-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="cc960-138">Nowe — AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cc960-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="cc960-139">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cc960-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


