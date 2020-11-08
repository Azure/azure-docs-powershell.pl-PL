---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055207"
---
# <span data-ttu-id="231cf-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="231cf-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="231cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="231cf-102">SYNOPSIS</span></span>
<span data-ttu-id="231cf-103">Migruje tabelę routingu do stosu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="231cf-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="231cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="231cf-104">SYNTAX</span></span>

### <span data-ttu-id="231cf-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="231cf-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="231cf-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="231cf-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="231cf-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="231cf-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="231cf-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="231cf-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="231cf-109">Opis</span><span class="sxs-lookup"><span data-stu-id="231cf-109">DESCRIPTION</span></span>
<span data-ttu-id="231cf-110">Polecenie cmdlet **Move-AzureRouteTable** migruje tabelę routingu do grupy zasobów na stosie usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="231cf-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="231cf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="231cf-111">EXAMPLES</span></span>

### <span data-ttu-id="231cf-112">1:1</span><span class="sxs-lookup"><span data-stu-id="231cf-112">1:</span></span>
```

```

## <span data-ttu-id="231cf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="231cf-113">PARAMETERS</span></span>

### <span data-ttu-id="231cf-114">-Przerwij</span><span class="sxs-lookup"><span data-stu-id="231cf-114">-Abort</span></span>
<span data-ttu-id="231cf-115">Wskazuje, że to polecenie cmdlet anuluje migrację tabeli routingu.</span><span class="sxs-lookup"><span data-stu-id="231cf-115">Indicates that this cmdlet cancels the route table migration.</span></span>

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

### <span data-ttu-id="231cf-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="231cf-116">-Commit</span></span>
<span data-ttu-id="231cf-117">Wskazuje, że to polecenie cmdlet rozpoczyna migrację tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="231cf-117">Indicates that this cmdlet starts the route table migration.</span></span>

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

### <span data-ttu-id="231cf-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="231cf-118">-InformationAction</span></span>
<span data-ttu-id="231cf-119">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="231cf-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="231cf-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="231cf-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="231cf-121">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="231cf-121">Continue</span></span>
- <span data-ttu-id="231cf-122">Ignorować</span><span class="sxs-lookup"><span data-stu-id="231cf-122">Ignore</span></span>
- <span data-ttu-id="231cf-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="231cf-123">Inquire</span></span>
- <span data-ttu-id="231cf-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="231cf-124">SilentlyContinue</span></span>
- <span data-ttu-id="231cf-125">Przestaw</span><span class="sxs-lookup"><span data-stu-id="231cf-125">Stop</span></span>
- <span data-ttu-id="231cf-126">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="231cf-126">Suspend</span></span>

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

### <span data-ttu-id="231cf-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="231cf-127">-InformationVariable</span></span>
<span data-ttu-id="231cf-128">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="231cf-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="231cf-129">-Przygotuj</span><span class="sxs-lookup"><span data-stu-id="231cf-129">-Prepare</span></span>
<span data-ttu-id="231cf-130">Wskazuje, że to polecenie cmdlet przygotowuje tabelę tras do migracji.</span><span class="sxs-lookup"><span data-stu-id="231cf-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

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

### <span data-ttu-id="231cf-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="231cf-131">-Profile</span></span>
<span data-ttu-id="231cf-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="231cf-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="231cf-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="231cf-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="231cf-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="231cf-134">-RouteTableName</span></span>
<span data-ttu-id="231cf-135">Określa nazwę tabeli routingu, którą to polecenie cmdlet migruje.</span><span class="sxs-lookup"><span data-stu-id="231cf-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="231cf-136">-Validate</span><span class="sxs-lookup"><span data-stu-id="231cf-136">-Validate</span></span>
<span data-ttu-id="231cf-137">Określa, że to polecenie cmdlet sprawdza poprawność tabeli tras do migracji.</span><span class="sxs-lookup"><span data-stu-id="231cf-137">Specifies that this cmdlet validates the route table for migration.</span></span>

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

### <span data-ttu-id="231cf-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="231cf-138">-Confirm</span></span>
<span data-ttu-id="231cf-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="231cf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="231cf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="231cf-140">-WhatIf</span></span>
<span data-ttu-id="231cf-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="231cf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="231cf-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="231cf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="231cf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="231cf-143">CommonParameters</span></span>
<span data-ttu-id="231cf-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="231cf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="231cf-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="231cf-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="231cf-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="231cf-146">INPUTS</span></span>

## <span data-ttu-id="231cf-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="231cf-147">OUTPUTS</span></span>

## <span data-ttu-id="231cf-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="231cf-148">NOTES</span></span>

## <span data-ttu-id="231cf-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="231cf-149">RELATED LINKS</span></span>

[<span data-ttu-id="231cf-150">Przenieś — AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="231cf-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="231cf-151">Przenieś — AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="231cf-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="231cf-152">Przenieś — AzureService</span><span class="sxs-lookup"><span data-stu-id="231cf-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="231cf-153">Przenieś — AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="231cf-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="231cf-154">Przenieś — AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="231cf-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


