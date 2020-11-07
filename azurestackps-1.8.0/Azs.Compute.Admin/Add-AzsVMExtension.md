---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0390c3f55c444b4a0e37e25c93536b60d10bc7b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888874"
---
# <span data-ttu-id="0efaa-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0efaa-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="0efaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0efaa-102">SYNOPSIS</span></span>
<span data-ttu-id="0efaa-103">Tworzenie nowego obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0efaa-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="0efaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0efaa-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0efaa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0efaa-105">DESCRIPTION</span></span>
<span data-ttu-id="0efaa-106">Tworzenie obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0efaa-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="0efaa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0efaa-107">EXAMPLES</span></span>

### <span data-ttu-id="0efaa-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0efaa-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="0efaa-109">Dodawanie nowego rozszerzenia obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="0efaa-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="0efaa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0efaa-110">PARAMETERS</span></span>

### <span data-ttu-id="0efaa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0efaa-111">-AsJob</span></span>
<span data-ttu-id="0efaa-112">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="0efaa-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0efaa-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="0efaa-113">-ComputeRole</span></span>
<span data-ttu-id="0efaa-114">Typ roli, IaaS lub PaaS, obsługiwany przez to rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="0efaa-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="0efaa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0efaa-115">-Force</span></span>
<span data-ttu-id="0efaa-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0efaa-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0efaa-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="0efaa-117">-IsSystemExtension</span></span>
<span data-ttu-id="0efaa-118">Wskazuje, czy rozszerzenie dotyczy systemu.</span><span class="sxs-lookup"><span data-stu-id="0efaa-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="0efaa-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0efaa-119">-Location</span></span>
<span data-ttu-id="0efaa-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0efaa-120">Location of the resource.</span></span>

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

### <span data-ttu-id="0efaa-121">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="0efaa-121">-Publisher</span></span>
<span data-ttu-id="0efaa-122">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="0efaa-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="0efaa-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="0efaa-123">-SourceBlob</span></span>
<span data-ttu-id="0efaa-124">Identyfikator URI do pakietu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0efaa-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0efaa-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="0efaa-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="0efaa-126">Prawda, jeśli obsługuje wiele rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="0efaa-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="0efaa-127">-Type</span><span class="sxs-lookup"><span data-stu-id="0efaa-127">-Type</span></span>
<span data-ttu-id="0efaa-128">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0efaa-128">Type of extension.</span></span>

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

### <span data-ttu-id="0efaa-129">-Version</span><span class="sxs-lookup"><span data-stu-id="0efaa-129">-Version</span></span>
<span data-ttu-id="0efaa-130">Wersja rozszerzenia obrazu maszyny vritual.</span><span class="sxs-lookup"><span data-stu-id="0efaa-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="0efaa-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="0efaa-131">-VmOsType</span></span>
<span data-ttu-id="0efaa-132">Docelowy typ systemu operacyjnego maszyny wirtualnej potrzebny do wdrożenia obsługi rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="0efaa-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="0efaa-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="0efaa-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="0efaa-134">Wartość wskazująca, czy rozszerzenie obsługuje funkcję skalowania skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0efaa-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="0efaa-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0efaa-135">-Confirm</span></span>
<span data-ttu-id="0efaa-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0efaa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efaa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efaa-137">-WhatIf</span></span>
<span data-ttu-id="0efaa-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0efaa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0efaa-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0efaa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efaa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efaa-140">CommonParameters</span></span>
<span data-ttu-id="0efaa-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efaa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efaa-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0efaa-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efaa-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0efaa-143">INPUTS</span></span>

## <span data-ttu-id="0efaa-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0efaa-144">OUTPUTS</span></span>

### <span data-ttu-id="0efaa-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="0efaa-145">VmExtensionObject</span></span>

## <span data-ttu-id="0efaa-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0efaa-146">NOTES</span></span>

## <span data-ttu-id="0efaa-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0efaa-147">RELATED LINKS</span></span>

