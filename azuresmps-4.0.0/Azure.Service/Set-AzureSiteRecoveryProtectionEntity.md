---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055389"
---
# <span data-ttu-id="1e631-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1e631-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="1e631-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e631-102">SYNOPSIS</span></span>
<span data-ttu-id="1e631-103">Umożliwia ustawienie stanu jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="1e631-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="1e631-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e631-104">SYNTAX</span></span>

### <span data-ttu-id="1e631-105">ByPEObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1e631-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e631-106">ByIDs</span><span class="sxs-lookup"><span data-stu-id="1e631-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e631-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1e631-107">DESCRIPTION</span></span>
<span data-ttu-id="1e631-108">Polecenie cmdlet **Set-AzureSiteRecoveryProtectionEntity** włącza lub wyłącza ochronę jednostki ochrony przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="1e631-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="1e631-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e631-109">EXAMPLES</span></span>

### <span data-ttu-id="1e631-110">Przykład 1: Włączanie ochrony obiektów w kontenerze</span><span class="sxs-lookup"><span data-stu-id="1e631-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="1e631-111">Pierwsze polecenie pobiera kontenery dla bieżącego magazynu witryny platformy Azure przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje je w zmiennej $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="1e631-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="1e631-112">Drugie polecenie pobiera chronione maszyny wirtualne należące do kontenera przechowywanego w $ProtectionContainer przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="1e631-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="1e631-113">Polecenie zapisuje wyniki w zmiennej $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="1e631-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="1e631-114">Polecenie ostatnie umożliwia ochronę jednostek przechowywanych w $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="1e631-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="1e631-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e631-115">PARAMETERS</span></span>

### <span data-ttu-id="1e631-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1e631-116">-Force</span></span>
<span data-ttu-id="1e631-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1e631-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e631-118">-ID</span><span class="sxs-lookup"><span data-stu-id="1e631-118">-Id</span></span>
<span data-ttu-id="1e631-119">Określa identyfikator chronionej maszyny wirtualnej, dla której należy włączyć lub wyłączyć ochronę.</span><span class="sxs-lookup"><span data-stu-id="1e631-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e631-120">-OS</span><span class="sxs-lookup"><span data-stu-id="1e631-120">-OS</span></span>
<span data-ttu-id="1e631-121">Określa typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="1e631-121">Specifies the operating system type.</span></span>
<span data-ttu-id="1e631-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1e631-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e631-123">Microsoft</span><span class="sxs-lookup"><span data-stu-id="1e631-123">Windows</span></span>
- <span data-ttu-id="1e631-124">Linux</span><span class="sxs-lookup"><span data-stu-id="1e631-124">Linux</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e631-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="1e631-125">-OSDiskName</span></span>
<span data-ttu-id="1e631-126">Określa nazwę dysku zawierającego system operacyjny.</span><span class="sxs-lookup"><span data-stu-id="1e631-126">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e631-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="1e631-127">-Profile</span></span>
<span data-ttu-id="1e631-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e631-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e631-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1e631-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e631-130">-Ochrona</span><span class="sxs-lookup"><span data-stu-id="1e631-130">-Protection</span></span>
<span data-ttu-id="1e631-131">Określa, czy ochrona ma być włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="1e631-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="1e631-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1e631-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e631-133">Włączony</span><span class="sxs-lookup"><span data-stu-id="1e631-133">Enable</span></span>
- <span data-ttu-id="1e631-134">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="1e631-134">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e631-135">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="1e631-135">-ProtectionContainerId</span></span>
<span data-ttu-id="1e631-136">Określa identyfikator chronionego kontenera.</span><span class="sxs-lookup"><span data-stu-id="1e631-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="1e631-137">To polecenie cmdlet włącza lub wyłącza ochronę maszyny wirtualnej należącej do kontenera, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1e631-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e631-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1e631-138">-ProtectionEntity</span></span>
<span data-ttu-id="1e631-139">Określa obiekt jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="1e631-139">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e631-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="1e631-140">-ProtectionProfile</span></span>
<span data-ttu-id="1e631-141">Określa profil ochrony, aby włączyć ochronę.</span><span class="sxs-lookup"><span data-stu-id="1e631-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="1e631-142">Określ obiekt **ASRProtectionProfile** , który jest jednym z dostępnych profilów ochrony w skojarzonym kontenerze ochrony.</span><span class="sxs-lookup"><span data-stu-id="1e631-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e631-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1e631-143">-WaitForCompletion</span></span>
<span data-ttu-id="1e631-144">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e631-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e631-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e631-145">-Confirm</span></span>
<span data-ttu-id="1e631-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e631-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e631-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e631-147">-WhatIf</span></span>
<span data-ttu-id="1e631-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e631-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e631-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1e631-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e631-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e631-150">CommonParameters</span></span>
<span data-ttu-id="1e631-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e631-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e631-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e631-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e631-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e631-153">INPUTS</span></span>

## <span data-ttu-id="1e631-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e631-154">OUTPUTS</span></span>

## <span data-ttu-id="1e631-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e631-155">NOTES</span></span>

## <span data-ttu-id="1e631-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e631-156">RELATED LINKS</span></span>

[<span data-ttu-id="1e631-157">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1e631-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="1e631-158">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1e631-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="1e631-159">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1e631-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


