---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB1A36E9-75BE-43CF-9092-9713DFEB96F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5329d50f87b92254136c222f406bb49586d6d7a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054554"
---
# <span data-ttu-id="566f0-101">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="566f0-101">Get-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="566f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="566f0-102">SYNOPSIS</span></span>
<span data-ttu-id="566f0-103">Pobiera ochronę lub chronione jednostki w magazynie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="566f0-103">Gets protectable or protected entities in a Site Recovery vault.</span></span>

## <span data-ttu-id="566f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="566f0-104">SYNTAX</span></span>

### <span data-ttu-id="566f0-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="566f0-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="566f0-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="566f0-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="566f0-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="566f0-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="566f0-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="566f0-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="566f0-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="566f0-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainerId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="566f0-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="566f0-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="566f0-111">Opis</span><span class="sxs-lookup"><span data-stu-id="566f0-111">DESCRIPTION</span></span>
<span data-ttu-id="566f0-112">Polecenie cmdlet **Get-AzureSiteRecoveryProtectionEntity** umożliwia włączanie ochrony lub chronionych jednostek, takich jak maszyny wirtualne, w bieżącym magazynie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="566f0-112">The **Get-AzureSiteRecoveryProtectionEntity** cmdlet gets the protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="566f0-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="566f0-113">EXAMPLES</span></span>

### <span data-ttu-id="566f0-114">Przykład 1: wyświetlanie chronionej maszyny wirtualnej w kontenerze</span><span class="sxs-lookup"><span data-stu-id="566f0-114">Example 1: Display a protected virtual machine in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
ID                           : 43aaab46-1cb0-4c39-8077-9a091c3b05ce
ServerId                     : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId        : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                         : testvm
Type                         : VirtualMachine
FabricObjectId               : 506B3CAC-5758-49E2-98C4-E5B0512E4D8E
Protected                    : False
CanCommit                    : False
CanFailover                  : False
CanReverseReplicate          : False
ActiveLocation               : Primary
ProtectionStateDescription   : Enabling protection
ReplicationHealth            : 
TestFailoverStateDescription : Nonev
ReplicationProvider          : HyperVReplica
```

<span data-ttu-id="566f0-115">Pierwsze polecenie uzyskuje chroniony kontener za pomocą polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="566f0-115">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="566f0-116">Drugie polecenie pobiera chronioną maszynę wirtualną, która należy do kontenera w $Container, a następnie ją wyświetla.</span><span class="sxs-lookup"><span data-stu-id="566f0-116">The second command gets the protected virtual machine that belongs to the container in $Container, and then displays it.</span></span>

## <span data-ttu-id="566f0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="566f0-117">PARAMETERS</span></span>

### <span data-ttu-id="566f0-118">-ID</span><span class="sxs-lookup"><span data-stu-id="566f0-118">-Id</span></span>
<span data-ttu-id="566f0-119">Określa identyfikator jednostki ochrony, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="566f0-119">Specifies the ID of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithId, ByIDsWithId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566f0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="566f0-120">-Name</span></span>
<span data-ttu-id="566f0-121">Określa nazwę jednostki ochrony, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="566f0-121">Specifies the name of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByIDsWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566f0-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="566f0-122">-Profile</span></span>
<span data-ttu-id="566f0-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="566f0-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="566f0-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="566f0-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="566f0-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="566f0-125">-ProtectionContainer</span></span>
<span data-ttu-id="566f0-126">Określa kontener ochrony.</span><span class="sxs-lookup"><span data-stu-id="566f0-126">Specifies a protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithId, ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="566f0-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="566f0-127">-ProtectionContainerId</span></span>
<span data-ttu-id="566f0-128">Określa identyfikator chronionego kontenera.</span><span class="sxs-lookup"><span data-stu-id="566f0-128">Specifies the ID of a protected container.</span></span>

```yaml
Type: String
Parameter Sets: ByIDsWithId, ByIDsWithName, ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566f0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566f0-129">CommonParameters</span></span>
<span data-ttu-id="566f0-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="566f0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566f0-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="566f0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566f0-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="566f0-132">INPUTS</span></span>

## <span data-ttu-id="566f0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="566f0-133">OUTPUTS</span></span>

## <span data-ttu-id="566f0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="566f0-134">NOTES</span></span>

## <span data-ttu-id="566f0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="566f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="566f0-136">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="566f0-136">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="566f0-137">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="566f0-137">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="566f0-138">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="566f0-138">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


