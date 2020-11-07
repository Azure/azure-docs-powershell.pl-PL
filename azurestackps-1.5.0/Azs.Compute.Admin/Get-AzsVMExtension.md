---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f81cf1ed28b822a0686d1db71541585023f1e57b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523389"
---
# <span data-ttu-id="49e92-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="49e92-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="49e92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49e92-102">SYNOPSIS</span></span>
<span data-ttu-id="49e92-103">Zwraca dostępne obecnie rozszerzenia obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="49e92-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="49e92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49e92-104">SYNTAX</span></span>

### <span data-ttu-id="49e92-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="49e92-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="49e92-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="49e92-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="49e92-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="49e92-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="49e92-108">Opis</span><span class="sxs-lookup"><span data-stu-id="49e92-108">DESCRIPTION</span></span>
<span data-ttu-id="49e92-109">Zwraca rozszerzenia obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="49e92-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="49e92-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49e92-110">EXAMPLES</span></span>

### <span data-ttu-id="49e92-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="49e92-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="49e92-112">Uzyskaj wszystkie rozszerzenia maszyny wirtualnej w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="49e92-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="49e92-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="49e92-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="49e92-114">Pobierz określone rozszerzenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="49e92-114">Get specific VM extension.</span></span>

## <span data-ttu-id="49e92-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49e92-115">PARAMETERS</span></span>

### <span data-ttu-id="49e92-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="49e92-116">-Location</span></span>
<span data-ttu-id="49e92-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="49e92-117">Location of the resource.</span></span>

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

### <span data-ttu-id="49e92-118">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="49e92-118">-Publisher</span></span>
<span data-ttu-id="49e92-119">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="49e92-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="49e92-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49e92-120">-ResourceId</span></span>
<span data-ttu-id="49e92-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="49e92-121">The resource id.</span></span>

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

### <span data-ttu-id="49e92-122">-Type</span><span class="sxs-lookup"><span data-stu-id="49e92-122">-Type</span></span>
<span data-ttu-id="49e92-123">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="49e92-123">Type of extension.</span></span>

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

### <span data-ttu-id="49e92-124">-Version</span><span class="sxs-lookup"><span data-stu-id="49e92-124">-Version</span></span>
<span data-ttu-id="49e92-125">Wersja rozszerzenia obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="49e92-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="49e92-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e92-126">CommonParameters</span></span>
<span data-ttu-id="49e92-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e92-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e92-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e92-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e92-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49e92-129">INPUTS</span></span>

## <span data-ttu-id="49e92-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49e92-130">OUTPUTS</span></span>

### <span data-ttu-id="49e92-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="49e92-131">VmExtensionObject</span></span>

## <span data-ttu-id="49e92-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49e92-132">NOTES</span></span>

## <span data-ttu-id="49e92-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49e92-133">RELATED LINKS</span></span>
