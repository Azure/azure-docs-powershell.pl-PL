---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ec1f3e70752a5386cd5dad78d867da68091b96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887566"
---
# <span data-ttu-id="ffa06-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="ffa06-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="ffa06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffa06-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa06-103">Dodaj obraz platformy maszyny wirtualnej z danej konfiguracji obrazu.</span><span class="sxs-lookup"><span data-stu-id="ffa06-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="ffa06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffa06-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ffa06-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa06-106">Dodaj obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="ffa06-106">Add a platform image.</span></span>

## <span data-ttu-id="ffa06-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffa06-107">EXAMPLES</span></span>

### <span data-ttu-id="ffa06-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ffa06-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="ffa06-109">Dodaj nowy obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="ffa06-109">Add a new platform image.</span></span>

## <span data-ttu-id="ffa06-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffa06-110">PARAMETERS</span></span>

### <span data-ttu-id="ffa06-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa06-111">-AsJob</span></span>
<span data-ttu-id="ffa06-112">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="ffa06-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="ffa06-113">-BillingPartNumber</span></span>
<span data-ttu-id="ffa06-114">Numer części jest wykorzystywany do naliczania kosztów oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="ffa06-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-115">-Datadyski</span><span class="sxs-lookup"><span data-stu-id="ffa06-115">-DataDisks</span></span>
<span data-ttu-id="ffa06-116">Dyski danych używane przez obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="ffa06-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ffa06-117">-Force</span></span>
<span data-ttu-id="ffa06-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ffa06-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ffa06-119">-Location</span></span>
<span data-ttu-id="ffa06-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffa06-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-121">-Offer</span><span class="sxs-lookup"><span data-stu-id="ffa06-121">-Offer</span></span>
<span data-ttu-id="ffa06-122">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="ffa06-122">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="ffa06-123">-OsType</span></span>
<span data-ttu-id="ffa06-124">Typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="ffa06-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="ffa06-125">-OsUri</span></span>
<span data-ttu-id="ffa06-126">Lokalizacja dysku.</span><span class="sxs-lookup"><span data-stu-id="ffa06-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-127">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="ffa06-127">-Publisher</span></span>
<span data-ttu-id="ffa06-128">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="ffa06-128">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="ffa06-129">-Sku</span></span>
<span data-ttu-id="ffa06-130">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="ffa06-130">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-131">-Version</span><span class="sxs-lookup"><span data-stu-id="ffa06-131">-Version</span></span>
<span data-ttu-id="ffa06-132">Wersja obrazu platformy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ffa06-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ffa06-133">-Confirm</span></span>
<span data-ttu-id="ffa06-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffa06-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa06-135">-WhatIf</span></span>
<span data-ttu-id="ffa06-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffa06-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa06-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ffa06-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa06-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa06-138">CommonParameters</span></span>
<span data-ttu-id="ffa06-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa06-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa06-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa06-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa06-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffa06-141">INPUTS</span></span>

## <span data-ttu-id="ffa06-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffa06-142">OUTPUTS</span></span>

### <span data-ttu-id="ffa06-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="ffa06-143">PlatformImageObject</span></span>

## <span data-ttu-id="ffa06-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffa06-144">NOTES</span></span>

## <span data-ttu-id="ffa06-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffa06-145">RELATED LINKS</span></span>

