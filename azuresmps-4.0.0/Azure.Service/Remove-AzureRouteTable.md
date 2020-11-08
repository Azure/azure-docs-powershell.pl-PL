---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055098"
---
# <span data-ttu-id="e4173-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4173-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="e4173-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4173-102">SYNOPSIS</span></span>
<span data-ttu-id="e4173-103">Usuwa tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="e4173-103">Removes a route table.</span></span>

## <span data-ttu-id="e4173-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4173-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4173-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4173-105">DESCRIPTION</span></span>
<span data-ttu-id="e4173-106">Polecenie cmdlet **Remove-AzureRouteTable** usuwa tabelę tras z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e4173-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="e4173-107">Jeśli tabela tras jest skojarzona z podsiecią, nie można usunąć tabeli.</span><span class="sxs-lookup"><span data-stu-id="e4173-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="e4173-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4173-108">EXAMPLES</span></span>

### <span data-ttu-id="e4173-109">Przykład 1: Usuwanie tabeli tras</span><span class="sxs-lookup"><span data-stu-id="e4173-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="e4173-110">To polecenie usuwa tabelę tras o nazwie PublicRouteTable.</span><span class="sxs-lookup"><span data-stu-id="e4173-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="e4173-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4173-111">PARAMETERS</span></span>

### <span data-ttu-id="e4173-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e4173-112">-Force</span></span>
<span data-ttu-id="e4173-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e4173-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4173-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4173-114">-Name</span></span>
<span data-ttu-id="e4173-115">Określa nazwę tabeli routingu, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4173-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4173-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4173-116">-PassThru</span></span>
<span data-ttu-id="e4173-117">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e4173-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e4173-118">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e4173-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4173-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="e4173-119">-Profile</span></span>
<span data-ttu-id="e4173-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4173-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4173-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e4173-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4173-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4173-122">CommonParameters</span></span>
<span data-ttu-id="e4173-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4173-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4173-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4173-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4173-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4173-125">INPUTS</span></span>

## <span data-ttu-id="e4173-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4173-126">OUTPUTS</span></span>

## <span data-ttu-id="e4173-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4173-127">NOTES</span></span>

## <span data-ttu-id="e4173-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4173-128">RELATED LINKS</span></span>

[<span data-ttu-id="e4173-129">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4173-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="e4173-130">Nowe — AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4173-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)
