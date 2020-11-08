---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055366"
---
# <span data-ttu-id="f5d8d-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="f5d8d-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="f5d8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d8d-103">Umożliwia zaktualizowanie serwera źródłowego i docelowego w celu ochrony obiektu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="f5d8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5d8d-104">SYNTAX</span></span>

### <span data-ttu-id="f5d8d-105">ByRPObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f5d8d-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f5d8d-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="f5d8d-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f5d8d-107">ByPEId</span><span class="sxs-lookup"><span data-stu-id="f5d8d-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f5d8d-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="f5d8d-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f5d8d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f5d8d-109">DESCRIPTION</span></span>
<span data-ttu-id="f5d8d-110">Polecenie cmdlet **Update-AzureSiteRecoveryProtectionDirection** aktualizuje serwer źródłowy i docelowy w celu ochrony obiektu odzyskiwania witryny Azure po zakończeniu operacji zatwierdzania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="f5d8d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5d8d-111">EXAMPLES</span></span>

### <span data-ttu-id="f5d8d-112">Przykład 1. Zmienianie kierunku chronionego obiektu w kontenerze</span><span class="sxs-lookup"><span data-stu-id="f5d8d-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="f5d8d-113">Pierwsze polecenie pobiera chronione kontenery w bieżącym magazynie odzyskiwania witryny Azure przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje je w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="f5d8d-114">Drugie polecenie pobiera maszyny wirtualne należące do kontenera przechowywanego w $Container przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="f5d8d-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="f5d8d-115">Polecenie zapisuje wyniki w zmiennej $Protected.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="f5d8d-116">Ostatnie polecenie ustawia kierunek RecoverToPrimary dla obiektów przechowywanych w $Protected.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="f5d8d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5d8d-117">PARAMETERS</span></span>

### <span data-ttu-id="f5d8d-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="f5d8d-118">-Direction</span></span>
<span data-ttu-id="f5d8d-119">Określa kierunek zatwierdzania.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="f5d8d-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f5d8d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5d8d-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f5d8d-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="f5d8d-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f5d8d-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="f5d8d-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="f5d8d-123">-Profile</span></span>
<span data-ttu-id="f5d8d-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5d8d-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5d8d-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="f5d8d-126">-ProtectionContainerId</span></span>
<span data-ttu-id="f5d8d-127">Określa identyfikator chronionego kontenera.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="f5d8d-128">To polecenie cmdlet umożliwia modyfikację kierunku chronionej maszyny wirtualnej należącej do kontenera, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d8d-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f5d8d-129">-ProtectionEntity</span></span>
<span data-ttu-id="f5d8d-130">Określa obiekt jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-130">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="f5d8d-131">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="f5d8d-131">-ProtectionEntityId</span></span>
<span data-ttu-id="f5d8d-132">Określa identyfikator chronionej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="f5d8d-133">To polecenie cmdlet modyfikuje kierunek chronionej maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d8d-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f5d8d-134">-RecoveryPlan</span></span>
<span data-ttu-id="f5d8d-135">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d8d-136">-RPId</span><span class="sxs-lookup"><span data-stu-id="f5d8d-136">-RPId</span></span>
<span data-ttu-id="f5d8d-137">Określa identyfikator planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="f5d8d-138">To polecenie cmdlet modyfikuje kierunek planu odzyskiwania określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d8d-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f5d8d-139">-WaitForCompletion</span></span>
<span data-ttu-id="f5d8d-140">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f5d8d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d8d-141">CommonParameters</span></span>
<span data-ttu-id="f5d8d-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d8d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d8d-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5d8d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d8d-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5d8d-144">INPUTS</span></span>

## <span data-ttu-id="f5d8d-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5d8d-145">OUTPUTS</span></span>

## <span data-ttu-id="f5d8d-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5d8d-146">NOTES</span></span>

## <span data-ttu-id="f5d8d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5d8d-147">RELATED LINKS</span></span>

[<span data-ttu-id="f5d8d-148">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f5d8d-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="f5d8d-149">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f5d8d-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


