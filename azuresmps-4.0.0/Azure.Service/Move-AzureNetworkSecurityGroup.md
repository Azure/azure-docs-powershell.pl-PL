---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055209"
---
# <span data-ttu-id="9b8e6-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b8e6-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="9b8e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8e6-103">Migruje grupę zabezpieczeń sieci do stosu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="9b8e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b8e6-104">SYNTAX</span></span>

### <span data-ttu-id="9b8e6-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b8e6-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b8e6-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b8e6-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b8e6-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b8e6-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b8e6-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b8e6-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b8e6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9b8e6-109">DESCRIPTION</span></span>
<span data-ttu-id="9b8e6-110">Polecenie cmdlet **Move-AzureNetworkSecurityGroup** migruje grupę zabezpieczeń sieci do grupy zasobów na stosie usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="9b8e6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b8e6-111">EXAMPLES</span></span>

### <span data-ttu-id="9b8e6-112">1:1</span><span class="sxs-lookup"><span data-stu-id="9b8e6-112">1:</span></span>
```

```

## <span data-ttu-id="9b8e6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b8e6-113">PARAMETERS</span></span>

### <span data-ttu-id="9b8e6-114">-Przerwij</span><span class="sxs-lookup"><span data-stu-id="9b8e6-114">-Abort</span></span>
<span data-ttu-id="9b8e6-115">Wskazuje, że to polecenie cmdlet anuluje migrację grup zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="9b8e6-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="9b8e6-116">-Commit</span></span>
<span data-ttu-id="9b8e6-117">Wskazuje, że to polecenie cmdlet rozpoczyna migrację grup zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="9b8e6-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9b8e6-118">-InformationAction</span></span>
<span data-ttu-id="9b8e6-119">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9b8e6-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9b8e6-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b8e6-121">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9b8e6-121">Continue</span></span>
- <span data-ttu-id="9b8e6-122">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9b8e6-122">Ignore</span></span>
- <span data-ttu-id="9b8e6-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="9b8e6-123">Inquire</span></span>
- <span data-ttu-id="9b8e6-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9b8e6-124">SilentlyContinue</span></span>
- <span data-ttu-id="9b8e6-125">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9b8e6-125">Stop</span></span>
- <span data-ttu-id="9b8e6-126">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9b8e6-126">Suspend</span></span>

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

### <span data-ttu-id="9b8e6-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9b8e6-127">-InformationVariable</span></span>
<span data-ttu-id="9b8e6-128">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9b8e6-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="9b8e6-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="9b8e6-130">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet migruje.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="9b8e6-131">-Przygotuj</span><span class="sxs-lookup"><span data-stu-id="9b8e6-131">-Prepare</span></span>
<span data-ttu-id="9b8e6-132">Wskazuje, że to polecenie cmdlet przygotowuje grupę zabezpieczeń sieci na potrzeby migracji.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="9b8e6-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="9b8e6-133">-Profile</span></span>
<span data-ttu-id="9b8e6-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b8e6-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b8e6-136">-Validate</span><span class="sxs-lookup"><span data-stu-id="9b8e6-136">-Validate</span></span>
<span data-ttu-id="9b8e6-137">Określa, że to polecenie cmdlet sprawdza poprawność grupy zabezpieczeń sieci na potrzeby migracji.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="9b8e6-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b8e6-138">-Confirm</span></span>
<span data-ttu-id="9b8e6-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b8e6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b8e6-140">-WhatIf</span></span>
<span data-ttu-id="9b8e6-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b8e6-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b8e6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8e6-143">CommonParameters</span></span>
<span data-ttu-id="9b8e6-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8e6-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b8e6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8e6-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b8e6-146">INPUTS</span></span>

## <span data-ttu-id="9b8e6-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b8e6-147">OUTPUTS</span></span>

## <span data-ttu-id="9b8e6-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b8e6-148">NOTES</span></span>

## <span data-ttu-id="9b8e6-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b8e6-149">RELATED LINKS</span></span>

[<span data-ttu-id="9b8e6-150">Przenieś — AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="9b8e6-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="9b8e6-151">Przenieś — AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="9b8e6-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="9b8e6-152">Przenieś — AzureService</span><span class="sxs-lookup"><span data-stu-id="9b8e6-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="9b8e6-153">Przenieś — AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9b8e6-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="9b8e6-154">Przenieś — AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9b8e6-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


