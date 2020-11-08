---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055279"
---
# <span data-ttu-id="5b960-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b960-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="5b960-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b960-102">SYNOPSIS</span></span>
<span data-ttu-id="5b960-103">Pobiera tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="5b960-103">Gets a route table.</span></span>

## <span data-ttu-id="5b960-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b960-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5b960-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5b960-105">DESCRIPTION</span></span>
<span data-ttu-id="5b960-106">Polecenie cmdlet **Get-AzureRouteTable** pobiera tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="5b960-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="5b960-107">Określ *szczegółowy* parametr, aby wyświetlić trasy w tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="5b960-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="5b960-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b960-108">EXAMPLES</span></span>

### <span data-ttu-id="5b960-109">Przykład 1: uzyskiwanie szczegółów dotyczących tabeli tras</span><span class="sxs-lookup"><span data-stu-id="5b960-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="5b960-110">To polecenie pobiera szczegóły tabeli tras o nazwie ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="5b960-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="5b960-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b960-111">PARAMETERS</span></span>

### <span data-ttu-id="5b960-112">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="5b960-112">-Detailed</span></span>
<span data-ttu-id="5b960-113">Wskazuje, że w tym poleceniu cmdlet są wyświetlane trasy w tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="5b960-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

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

### <span data-ttu-id="5b960-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b960-114">-Name</span></span>
<span data-ttu-id="5b960-115">Określa nazwę tabeli routingu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b960-115">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5b960-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="5b960-116">-Profile</span></span>
<span data-ttu-id="5b960-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b960-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5b960-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5b960-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b960-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b960-119">CommonParameters</span></span>
<span data-ttu-id="5b960-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b960-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b960-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b960-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b960-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b960-122">INPUTS</span></span>

## <span data-ttu-id="5b960-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b960-123">OUTPUTS</span></span>

## <span data-ttu-id="5b960-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b960-124">NOTES</span></span>

## <span data-ttu-id="5b960-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b960-125">RELATED LINKS</span></span>

[<span data-ttu-id="5b960-126">Nowe — AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b960-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="5b960-127">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="5b960-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


