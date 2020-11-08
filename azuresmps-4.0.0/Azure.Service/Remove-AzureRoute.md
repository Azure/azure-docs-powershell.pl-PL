---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055101"
---
# <span data-ttu-id="e2853-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="e2853-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="e2853-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2853-102">SYNOPSIS</span></span>
<span data-ttu-id="e2853-103">Usuwa trasę z tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="e2853-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="e2853-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2853-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2853-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2853-105">DESCRIPTION</span></span>
<span data-ttu-id="e2853-106">Polecenie cmdlet **Remove-AzureRoute** usuwa trasę z tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="e2853-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="e2853-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2853-107">EXAMPLES</span></span>

### <span data-ttu-id="e2853-108">Przykład 1: Usuwanie trasy</span><span class="sxs-lookup"><span data-stu-id="e2853-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="e2853-109">To polecenie pobiera tabelę tras o nazwie ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="e2853-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="e2853-110">Polecenie przekazuje tę tabelę routingu do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2853-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="e2853-111">Bieżące polecenie cmdlet usuwa trasę o nazwie InternetRoute.</span><span class="sxs-lookup"><span data-stu-id="e2853-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="e2853-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2853-112">PARAMETERS</span></span>

### <span data-ttu-id="e2853-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e2853-113">-Force</span></span>
<span data-ttu-id="e2853-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e2853-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2853-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="e2853-115">-Profile</span></span>
<span data-ttu-id="e2853-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2853-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e2853-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e2853-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2853-118">-RouteName</span><span class="sxs-lookup"><span data-stu-id="e2853-118">-RouteName</span></span>
<span data-ttu-id="e2853-119">Określa nazwę nowej trasy, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2853-119">Specifies a name for the new route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2853-120">-Routeing</span><span class="sxs-lookup"><span data-stu-id="e2853-120">-RouteTable</span></span>
<span data-ttu-id="e2853-121">Określa tabelę tras, z której to polecenie cmdlet usuwa trasę.</span><span class="sxs-lookup"><span data-stu-id="e2853-121">Specifies the route table from which this cmdlet removes a route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2853-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2853-122">CommonParameters</span></span>
<span data-ttu-id="e2853-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2853-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2853-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2853-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2853-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2853-125">INPUTS</span></span>

## <span data-ttu-id="e2853-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2853-126">OUTPUTS</span></span>

## <span data-ttu-id="e2853-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2853-127">NOTES</span></span>

## <span data-ttu-id="e2853-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2853-128">RELATED LINKS</span></span>

[<span data-ttu-id="e2853-129">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="e2853-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)


