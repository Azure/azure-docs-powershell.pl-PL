---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d39721f1a9ed243242bd08053f9a22f0ed53df30
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889962"
---
# <span data-ttu-id="a4a85-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="a4a85-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="a4a85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4a85-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a85-103">Dodaj obraz platformy maszyny wirtualnej z danej konfiguracji obrazu.</span><span class="sxs-lookup"><span data-stu-id="a4a85-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="a4a85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4a85-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4a85-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4a85-105">DESCRIPTION</span></span>
<span data-ttu-id="a4a85-106">Dodaj obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="a4a85-106">Add a platform image.</span></span>

## <span data-ttu-id="a4a85-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4a85-107">EXAMPLES</span></span>

### <span data-ttu-id="a4a85-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4a85-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="a4a85-109">Dodaj nowy obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="a4a85-109">Add a new platform image.</span></span>

## <span data-ttu-id="a4a85-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4a85-110">PARAMETERS</span></span>

### <span data-ttu-id="a4a85-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4a85-111">-AsJob</span></span>
<span data-ttu-id="a4a85-112">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="a4a85-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a4a85-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="a4a85-113">-BillingPartNumber</span></span>
<span data-ttu-id="a4a85-114">Numer części jest wykorzystywany do naliczania kosztów oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="a4a85-114">The part number is used to bill for software costs.</span></span>

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

### <span data-ttu-id="a4a85-115">-Datadyski</span><span class="sxs-lookup"><span data-stu-id="a4a85-115">-DataDisks</span></span>
<span data-ttu-id="a4a85-116">Dyski danych używane przez obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="a4a85-116">Data disks used by the platform image.</span></span>

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

### <span data-ttu-id="a4a85-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a4a85-117">-Force</span></span>
<span data-ttu-id="a4a85-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4a85-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a4a85-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a4a85-119">-Location</span></span>
<span data-ttu-id="a4a85-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="a4a85-120">Location of the resource.</span></span>

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

### <span data-ttu-id="a4a85-121">-Offer</span><span class="sxs-lookup"><span data-stu-id="a4a85-121">-Offer</span></span>
<span data-ttu-id="a4a85-122">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="a4a85-122">Name of the offer.</span></span>

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

### <span data-ttu-id="a4a85-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="a4a85-123">-OsType</span></span>
<span data-ttu-id="a4a85-124">Typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="a4a85-124">Operating system type.</span></span>

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

### <span data-ttu-id="a4a85-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="a4a85-125">-OsUri</span></span>
<span data-ttu-id="a4a85-126">Lokalizacja dysku.</span><span class="sxs-lookup"><span data-stu-id="a4a85-126">Location of the disk.</span></span>

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

### <span data-ttu-id="a4a85-127">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="a4a85-127">-Publisher</span></span>
<span data-ttu-id="a4a85-128">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="a4a85-128">Name of the publisher.</span></span>

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

### <span data-ttu-id="a4a85-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="a4a85-129">-Sku</span></span>
<span data-ttu-id="a4a85-130">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="a4a85-130">Name of the SKU.</span></span>

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

### <span data-ttu-id="a4a85-131">-Version</span><span class="sxs-lookup"><span data-stu-id="a4a85-131">-Version</span></span>
<span data-ttu-id="a4a85-132">Wersja obrazu platformy maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a4a85-132">The version of the virtual machine platform image.</span></span>

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

### <span data-ttu-id="a4a85-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4a85-133">-Confirm</span></span>
<span data-ttu-id="a4a85-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4a85-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4a85-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4a85-135">-WhatIf</span></span>
<span data-ttu-id="a4a85-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4a85-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4a85-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4a85-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4a85-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a85-138">CommonParameters</span></span>
<span data-ttu-id="a4a85-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a85-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a85-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a85-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a85-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4a85-141">INPUTS</span></span>

## <span data-ttu-id="a4a85-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4a85-142">OUTPUTS</span></span>

### <span data-ttu-id="a4a85-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="a4a85-143">PlatformImageObject</span></span>

## <span data-ttu-id="a4a85-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4a85-144">NOTES</span></span>

## <span data-ttu-id="a4a85-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4a85-145">RELATED LINKS</span></span>

