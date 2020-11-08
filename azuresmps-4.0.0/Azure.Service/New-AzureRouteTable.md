---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054955"
---
# <span data-ttu-id="4e837-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e837-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="4e837-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e837-102">SYNOPSIS</span></span>
<span data-ttu-id="4e837-103">Tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="4e837-103">Creates a route table.</span></span>

## <span data-ttu-id="4e837-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e837-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e837-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4e837-105">DESCRIPTION</span></span>
<span data-ttu-id="4e837-106">Polecenie cmdlet **New-AzureRouteTable** tworzy tabelę tras w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4e837-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="4e837-107">Do tabeli tras można dodać trasy zdefiniowane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4e837-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="4e837-108">Tabelę tras można skojarzyć z podsiecią w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4e837-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="4e837-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e837-109">EXAMPLES</span></span>

## <span data-ttu-id="4e837-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e837-110">PARAMETERS</span></span>

### <span data-ttu-id="4e837-111">-Label</span><span class="sxs-lookup"><span data-stu-id="4e837-111">-Label</span></span>
<span data-ttu-id="4e837-112">Umożliwia określenie opisu nowej tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="4e837-112">Specifies a description for the new route table.</span></span>

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

### <span data-ttu-id="4e837-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4e837-113">-Location</span></span>
<span data-ttu-id="4e837-114">Określa lokalizację, w której to polecenie cmdlet tworzy tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="4e837-114">Specifies the location in which this cmdlet creates the route table.</span></span>

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

### <span data-ttu-id="4e837-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e837-115">-Name</span></span>
<span data-ttu-id="4e837-116">Określa nazwę tabeli routingu, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e837-116">Specifies a name for the route table that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4e837-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="4e837-117">-Profile</span></span>
<span data-ttu-id="4e837-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e837-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4e837-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4e837-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4e837-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e837-120">CommonParameters</span></span>
<span data-ttu-id="4e837-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e837-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e837-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e837-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e837-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e837-123">INPUTS</span></span>

## <span data-ttu-id="4e837-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e837-124">OUTPUTS</span></span>

## <span data-ttu-id="4e837-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e837-125">NOTES</span></span>

## <span data-ttu-id="4e837-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e837-126">RELATED LINKS</span></span>

[<span data-ttu-id="4e837-127">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e837-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="4e837-128">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e837-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


