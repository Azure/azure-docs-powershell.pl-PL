---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CE15E01D-5D86-4960-8E37-7757B35F4464
online version: ''
schema: 2.0.0
ms.openlocfilehash: a87a825249d7d7cda3fc2dc43a93869f8d869705
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055535"
---
# <span data-ttu-id="0fca6-101">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="0fca6-101">Get-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="0fca6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fca6-102">SYNOPSIS</span></span>
<span data-ttu-id="0fca6-103">Pobiera informacje o maszynach wirtualnych zarządzanych przez odzyskiwanie witryny.</span><span class="sxs-lookup"><span data-stu-id="0fca6-103">Gets information about Site Recovery-managed virtual machines.</span></span>

## <span data-ttu-id="0fca6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fca6-104">SYNTAX</span></span>

### <span data-ttu-id="0fca6-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0fca6-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fca6-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="0fca6-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fca6-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="0fca6-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fca6-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0fca6-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0fca6-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="0fca6-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fca6-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="0fca6-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainerId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0fca6-111">Opis</span><span class="sxs-lookup"><span data-stu-id="0fca6-111">DESCRIPTION</span></span>
<span data-ttu-id="0fca6-112">Polecenie cmdlet **Get-AzureSiteRecoveryVM** pobiera informacje o maszynach wirtualnych zarządzanych w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0fca6-112">The **Get-AzureSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="0fca6-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fca6-113">EXAMPLES</span></span>

### <span data-ttu-id="0fca6-114">Przykład 1: uzyskiwanie informacji o maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0fca6-114">Example 1: Get information about a virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer
ID                          : a205fd17-3848-4896-bab6-9dbccc3cd8ed
ServerId                    : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId       : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                        : vm1
Type                        : VirtualMachine
FabricObjectId              : 86447b9e-d877-4e9a-8302-adcd6bbf18c0
Protected                   : False
CanCommit                   : False
CanFailover                 : True
CanReverseReplicate         : False
ActiveLocation              : Primary
ProtectionState             : Enabled
ReplicationHealth           : Healthy
TestFailoverState           : None
ReplicationProvider         : HyperVReplica
```

<span data-ttu-id="0fca6-115">W pierwszym poleceniu jest używane polecenie cmdlet **Get-AzureSiteRecoveryProtectionContainer** w celu uzyskania chronionego kontenera, a następnie zapisanie go w zmiennej $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="0fca6-115">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="0fca6-116">Drugie polecenie pobiera informacje o maszynach wirtualnych w $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="0fca6-116">The second command gets information about the virtual machines in $ProtectionContainer.</span></span>

## <span data-ttu-id="0fca6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fca6-117">PARAMETERS</span></span>

### <span data-ttu-id="0fca6-118">-ID</span><span class="sxs-lookup"><span data-stu-id="0fca6-118">-Id</span></span>
<span data-ttu-id="0fca6-119">Określa identyfikator maszyny wirtualnej, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="0fca6-119">Specifies the ID of the virtual machine about which to get information.</span></span>

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

### <span data-ttu-id="0fca6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0fca6-120">-Name</span></span>
<span data-ttu-id="0fca6-121">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0fca6-121">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0fca6-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="0fca6-122">-Profile</span></span>
<span data-ttu-id="0fca6-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fca6-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0fca6-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="0fca6-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0fca6-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0fca6-125">-ProtectionContainer</span></span>
<span data-ttu-id="0fca6-126">Określa obiekt kontenera ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="0fca6-126">Specifies the Site Recovery protection container object.</span></span>

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

### <span data-ttu-id="0fca6-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="0fca6-127">-ProtectionContainerId</span></span>
<span data-ttu-id="0fca6-128">Określa identyfikator chronionego kontenera, o którym należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="0fca6-128">Specifies the ID of a protected container about which to get information.</span></span>

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

### <span data-ttu-id="0fca6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fca6-129">CommonParameters</span></span>
<span data-ttu-id="0fca6-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fca6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fca6-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fca6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fca6-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fca6-132">INPUTS</span></span>

## <span data-ttu-id="0fca6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fca6-133">OUTPUTS</span></span>

## <span data-ttu-id="0fca6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fca6-134">NOTES</span></span>

## <span data-ttu-id="0fca6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fca6-135">RELATED LINKS</span></span>

[<span data-ttu-id="0fca6-136">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="0fca6-136">Set-AzureSiteRecoveryVM</span></span>](./Set-AzureSiteRecoveryVM.md)


