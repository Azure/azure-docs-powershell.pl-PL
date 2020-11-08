---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055229"
---
# <span data-ttu-id="5332b-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="5332b-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="5332b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5332b-102">SYNOPSIS</span></span>
<span data-ttu-id="5332b-103">Pobiera sieci wirtualne.</span><span class="sxs-lookup"><span data-stu-id="5332b-103">Gets virtual networks.</span></span>

## <span data-ttu-id="5332b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5332b-104">SYNTAX</span></span>

### <span data-ttu-id="5332b-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5332b-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5332b-106">FromId</span><span class="sxs-lookup"><span data-stu-id="5332b-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5332b-107">Odname</span><span class="sxs-lookup"><span data-stu-id="5332b-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5332b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5332b-108">DESCRIPTION</span></span>
<span data-ttu-id="5332b-109">Polecenie cmdlet **Get-WAPackVNet** pobiera wirtualne sieci.</span><span class="sxs-lookup"><span data-stu-id="5332b-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="5332b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5332b-110">EXAMPLES</span></span>

### <span data-ttu-id="5332b-111">Przykład 1: pobieranie wszystkich sieci wirtualnych</span><span class="sxs-lookup"><span data-stu-id="5332b-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="5332b-112">To polecenie pobiera wszystkie sieci wirtualne.</span><span class="sxs-lookup"><span data-stu-id="5332b-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="5332b-113">Przykład 2: uzyskiwanie sieci wirtualnej przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="5332b-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="5332b-114">To polecenie pobiera sieć wirtualną o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="5332b-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="5332b-115">Przykład 3: uzyskiwanie sieci wirtualnej za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="5332b-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="5332b-116">To polecenie pobiera sieć wirtualną o nazwie ContosoVNet08.</span><span class="sxs-lookup"><span data-stu-id="5332b-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="5332b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5332b-117">PARAMETERS</span></span>

### <span data-ttu-id="5332b-118">-ID</span><span class="sxs-lookup"><span data-stu-id="5332b-118">-ID</span></span>
<span data-ttu-id="5332b-119">Określa unikatowy identyfikator sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5332b-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5332b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5332b-120">-Name</span></span>
<span data-ttu-id="5332b-121">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5332b-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5332b-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="5332b-122">-Profile</span></span>
<span data-ttu-id="5332b-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5332b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5332b-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5332b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5332b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5332b-125">CommonParameters</span></span>
<span data-ttu-id="5332b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5332b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5332b-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5332b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5332b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5332b-128">INPUTS</span></span>

## <span data-ttu-id="5332b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5332b-129">OUTPUTS</span></span>

## <span data-ttu-id="5332b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5332b-130">NOTES</span></span>

## <span data-ttu-id="5332b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5332b-131">RELATED LINKS</span></span>

