---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055208"
---
# <span data-ttu-id="643b9-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="643b9-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="643b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="643b9-102">SYNOPSIS</span></span>
<span data-ttu-id="643b9-103">Migruje zastrzeżony adres IP do stosu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="643b9-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="643b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="643b9-104">SYNTAX</span></span>

### <span data-ttu-id="643b9-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="643b9-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="643b9-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="643b9-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="643b9-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="643b9-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="643b9-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="643b9-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="643b9-109">Opis</span><span class="sxs-lookup"><span data-stu-id="643b9-109">DESCRIPTION</span></span>
<span data-ttu-id="643b9-110">Polecenie cmdlet **Move-AzureReservedIP** migruje zastrzeżony adres IP do grupy zasobów na stosie usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="643b9-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="643b9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="643b9-111">EXAMPLES</span></span>

### <span data-ttu-id="643b9-112">1:1</span><span class="sxs-lookup"><span data-stu-id="643b9-112">1:</span></span>
```

```

## <span data-ttu-id="643b9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="643b9-113">PARAMETERS</span></span>

### <span data-ttu-id="643b9-114">-Przerwij</span><span class="sxs-lookup"><span data-stu-id="643b9-114">-Abort</span></span>
<span data-ttu-id="643b9-115">Wskazuje, że to polecenie cmdlet anuluje migrację zastrzeżonych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="643b9-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643b9-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="643b9-116">-Commit</span></span>
<span data-ttu-id="643b9-117">Wskazuje, że to polecenie cmdlet rozpoczyna migrację zastrzeżonych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="643b9-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643b9-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="643b9-118">-InformationAction</span></span>
<span data-ttu-id="643b9-119">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="643b9-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="643b9-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="643b9-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="643b9-121">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="643b9-121">Continue</span></span>
- <span data-ttu-id="643b9-122">Ignorować</span><span class="sxs-lookup"><span data-stu-id="643b9-122">Ignore</span></span>
- <span data-ttu-id="643b9-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="643b9-123">Inquire</span></span>
- <span data-ttu-id="643b9-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="643b9-124">SilentlyContinue</span></span>
- <span data-ttu-id="643b9-125">Przestaw</span><span class="sxs-lookup"><span data-stu-id="643b9-125">Stop</span></span>
- <span data-ttu-id="643b9-126">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="643b9-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643b9-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="643b9-127">-InformationVariable</span></span>
<span data-ttu-id="643b9-128">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="643b9-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643b9-129">-Przygotuj</span><span class="sxs-lookup"><span data-stu-id="643b9-129">-Prepare</span></span>
<span data-ttu-id="643b9-130">Wskazuje, że to polecenie cmdlet przygotowuje zastrzeżony adres IP do migracji.</span><span class="sxs-lookup"><span data-stu-id="643b9-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643b9-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="643b9-131">-Profile</span></span>
<span data-ttu-id="643b9-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="643b9-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="643b9-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="643b9-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="643b9-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="643b9-134">-ReservedIPName</span></span>
<span data-ttu-id="643b9-135">Określa nazwę zastrzeżonych adresów IP, które wykonuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="643b9-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="643b9-136">-Validate</span><span class="sxs-lookup"><span data-stu-id="643b9-136">-Validate</span></span>
<span data-ttu-id="643b9-137">Określa, że to polecenie cmdlet sprawdza poprawność zastrzeżonego adresu IP do migracji.</span><span class="sxs-lookup"><span data-stu-id="643b9-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643b9-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="643b9-138">-Confirm</span></span>
<span data-ttu-id="643b9-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="643b9-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643b9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643b9-140">-WhatIf</span></span>
<span data-ttu-id="643b9-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="643b9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="643b9-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="643b9-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643b9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643b9-143">CommonParameters</span></span>
<span data-ttu-id="643b9-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="643b9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643b9-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643b9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643b9-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="643b9-146">INPUTS</span></span>

## <span data-ttu-id="643b9-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="643b9-147">OUTPUTS</span></span>

## <span data-ttu-id="643b9-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="643b9-148">NOTES</span></span>

## <span data-ttu-id="643b9-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="643b9-149">RELATED LINKS</span></span>

[<span data-ttu-id="643b9-150">Przenieś — AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="643b9-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="643b9-151">Przenieś — AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="643b9-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="643b9-152">Przenieś — AzureService</span><span class="sxs-lookup"><span data-stu-id="643b9-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="643b9-153">Przenieś — AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="643b9-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="643b9-154">Przenieś — AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="643b9-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


