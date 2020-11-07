---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7eac7b9d23914aa909a111958d64cc9d4247d3
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889050"
---
# <span data-ttu-id="1fa63-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="1fa63-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="1fa63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fa63-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa63-103">Zwraca dostępne obecnie rozszerzenia obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1fa63-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="1fa63-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fa63-104">SYNTAX</span></span>

### <span data-ttu-id="1fa63-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1fa63-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="1fa63-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1fa63-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1fa63-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1fa63-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="1fa63-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1fa63-108">DESCRIPTION</span></span>
<span data-ttu-id="1fa63-109">Zwraca rozszerzenia obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1fa63-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="1fa63-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fa63-110">EXAMPLES</span></span>

### <span data-ttu-id="1fa63-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1fa63-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="1fa63-112">Uzyskaj wszystkie rozszerzenia maszyny wirtualnej w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="1fa63-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="1fa63-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1fa63-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="1fa63-114">Pobierz określone rozszerzenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1fa63-114">Get specific VM extension.</span></span>

## <span data-ttu-id="1fa63-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fa63-115">PARAMETERS</span></span>

### <span data-ttu-id="1fa63-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1fa63-116">-Location</span></span>
<span data-ttu-id="1fa63-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1fa63-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fa63-118">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="1fa63-118">-Publisher</span></span>
<span data-ttu-id="1fa63-119">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="1fa63-119">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fa63-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fa63-120">-ResourceId</span></span>
<span data-ttu-id="1fa63-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1fa63-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa63-122">-Type</span><span class="sxs-lookup"><span data-stu-id="1fa63-122">-Type</span></span>
<span data-ttu-id="1fa63-123">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1fa63-123">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fa63-124">-Version</span><span class="sxs-lookup"><span data-stu-id="1fa63-124">-Version</span></span>
<span data-ttu-id="1fa63-125">Wersja rozszerzenia obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1fa63-125">The version of the virtual machine image extension.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fa63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa63-126">CommonParameters</span></span>
<span data-ttu-id="1fa63-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fa63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa63-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fa63-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa63-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fa63-129">INPUTS</span></span>

## <span data-ttu-id="1fa63-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fa63-130">OUTPUTS</span></span>

### <span data-ttu-id="1fa63-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="1fa63-131">VmExtensionObject</span></span>

## <span data-ttu-id="1fa63-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fa63-132">NOTES</span></span>

## <span data-ttu-id="1fa63-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fa63-133">RELATED LINKS</span></span>

