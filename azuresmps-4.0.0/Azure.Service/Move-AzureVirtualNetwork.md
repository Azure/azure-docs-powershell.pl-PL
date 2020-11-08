---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055204"
---
# <span data-ttu-id="811dc-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="811dc-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="811dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="811dc-102">SYNOPSIS</span></span>
<span data-ttu-id="811dc-103">Migruje sieć wirtualną do stosu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="811dc-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="811dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="811dc-104">SYNTAX</span></span>

### <span data-ttu-id="811dc-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="811dc-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="811dc-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="811dc-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="811dc-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="811dc-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="811dc-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="811dc-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="811dc-109">Opis</span><span class="sxs-lookup"><span data-stu-id="811dc-109">DESCRIPTION</span></span>
<span data-ttu-id="811dc-110">Polecenie cmdlet **Move-AzureVirtualNetwork** migruje sieć wirtualną do grupy zasobów na stosie usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="811dc-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="811dc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="811dc-111">EXAMPLES</span></span>

### <span data-ttu-id="811dc-112">Przykład 1: przygotowywanie migracji sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="811dc-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="811dc-113">To polecenie przygotowuje wirtualną sieć o nazwie ContosoVNET do migracji na stos Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="811dc-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="811dc-114">Przykład 2: uruchamianie migracji sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="811dc-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="811dc-115">To polecenie rozpoczyna migrację sieci wirtualnej o nazwie ContosoVNET na stos usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="811dc-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="811dc-116">Przykład 3: sprawdzanie poprawności migracji sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="811dc-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="811dc-117">To polecenie sprawdza poprawność migracji dla sieci wirtualnej o nazwie ContosoVNET na stosie Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="811dc-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="811dc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="811dc-118">PARAMETERS</span></span>

### <span data-ttu-id="811dc-119">-Przerwij</span><span class="sxs-lookup"><span data-stu-id="811dc-119">-Abort</span></span>
<span data-ttu-id="811dc-120">Wskazuje, że to polecenie cmdlet anuluje migrację sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="811dc-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

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

### <span data-ttu-id="811dc-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="811dc-121">-Commit</span></span>
<span data-ttu-id="811dc-122">Wskazuje, że to polecenie cmdlet rozpoczyna migrację sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="811dc-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

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

### <span data-ttu-id="811dc-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="811dc-123">-InformationAction</span></span>
<span data-ttu-id="811dc-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="811dc-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="811dc-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="811dc-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="811dc-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="811dc-126">Continue</span></span>
- <span data-ttu-id="811dc-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="811dc-127">Ignore</span></span>
- <span data-ttu-id="811dc-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="811dc-128">Inquire</span></span>
- <span data-ttu-id="811dc-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="811dc-129">SilentlyContinue</span></span>
- <span data-ttu-id="811dc-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="811dc-130">Stop</span></span>
- <span data-ttu-id="811dc-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="811dc-131">Suspend</span></span>

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

### <span data-ttu-id="811dc-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="811dc-132">-InformationVariable</span></span>
<span data-ttu-id="811dc-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="811dc-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="811dc-134">-Przygotuj</span><span class="sxs-lookup"><span data-stu-id="811dc-134">-Prepare</span></span>
<span data-ttu-id="811dc-135">Wskazuje, że to polecenie cmdlet przygotowuje wirtualną sieć do migracji.</span><span class="sxs-lookup"><span data-stu-id="811dc-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

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

### <span data-ttu-id="811dc-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="811dc-136">-Profile</span></span>
<span data-ttu-id="811dc-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="811dc-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="811dc-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="811dc-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="811dc-139">-Validate</span><span class="sxs-lookup"><span data-stu-id="811dc-139">-Validate</span></span>
<span data-ttu-id="811dc-140">Określa, że to polecenie cmdlet sprawdza poprawność sieci wirtualnej do migracji.</span><span class="sxs-lookup"><span data-stu-id="811dc-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

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

### <span data-ttu-id="811dc-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="811dc-141">-VirtualNetworkName</span></span>
<span data-ttu-id="811dc-142">Nazwa sieci wirtualnej do zmigrowania</span><span class="sxs-lookup"><span data-stu-id="811dc-142">Name of the Virtual Network to migrate</span></span>

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

### <span data-ttu-id="811dc-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="811dc-143">-Confirm</span></span>
<span data-ttu-id="811dc-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="811dc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="811dc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="811dc-145">-WhatIf</span></span>
<span data-ttu-id="811dc-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="811dc-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="811dc-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="811dc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="811dc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811dc-148">CommonParameters</span></span>
<span data-ttu-id="811dc-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="811dc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811dc-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="811dc-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811dc-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="811dc-151">INPUTS</span></span>

## <span data-ttu-id="811dc-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="811dc-152">OUTPUTS</span></span>

## <span data-ttu-id="811dc-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="811dc-153">NOTES</span></span>

## <span data-ttu-id="811dc-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="811dc-154">RELATED LINKS</span></span>

[<span data-ttu-id="811dc-155">Przenieś — AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="811dc-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="811dc-156">Przenieś — AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="811dc-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="811dc-157">Przenieś — AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="811dc-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="811dc-158">Przenieś — AzureService</span><span class="sxs-lookup"><span data-stu-id="811dc-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="811dc-159">Przenieś — AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="811dc-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


