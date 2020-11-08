---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054814"
---
# <span data-ttu-id="0a84a-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="0a84a-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>

## <span data-ttu-id="0a84a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a84a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a84a-103">Uruchamianie zadania skojarzenia zasad replikacji witryny.</span><span class="sxs-lookup"><span data-stu-id="0a84a-103">Starts a Site Recovery replication policy association job.</span></span>

## <span data-ttu-id="0a84a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a84a-104">SYNTAX</span></span>

### <span data-ttu-id="0a84a-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0a84a-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a84a-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="0a84a-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0a84a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0a84a-107">DESCRIPTION</span></span>
<span data-ttu-id="0a84a-108">Polecenie cmdlet **Start-AzureSiteRecoveryProtectionProfileAssociationJob** inicjuje zadanie skojarzenia w celu skojarzenia zasad replikacji z kontenerem ochrony za pomocą usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0a84a-108">The **Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="0a84a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a84a-109">EXAMPLES</span></span>

### <span data-ttu-id="0a84a-110">Przykład 1: Kojarzenie profilu ochrony</span><span class="sxs-lookup"><span data-stu-id="0a84a-110">Example 1: Associate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

<span data-ttu-id="0a84a-111">Pierwsze polecenie uzyskuje kontener ochrony przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje ten kontener w zmiennej $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="0a84a-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="0a84a-112">Drugie polecenie tworzy profil ochrony za pomocą polecenia cmdlet **New-AzureSiteRecoveryProtectionProfileObject** i zapisuje ten profil ochrony w zmiennej $ProtectionProfile.</span><span class="sxs-lookup"><span data-stu-id="0a84a-112">The second command creates a protection profile by using the **New-AzureSiteRecoveryProtectionProfileObject** cmdlet, and stores that protection profile in the $ProtectionProfile variable.</span></span>

<span data-ttu-id="0a84a-113">Trzecia komenda uzyskuje kontener ochrony, a następnie zapisuje go w zmiennej $ProtectionContainer 02.</span><span class="sxs-lookup"><span data-stu-id="0a84a-113">The third command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="0a84a-114">Polecenie ostatnie powoduje skojarzenie profilu ochrony przechowywanego w $ProtectionProfile z kontenerem przechowywanym w $ProtectionContainer 01 jako głównym kontenerem ochrony.</span><span class="sxs-lookup"><span data-stu-id="0a84a-114">The final command associates the protection profile stored in $ProtectionProfile to the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="0a84a-115">Polecenie kojarzy kontener przechowywany w $ProtectionContainer 02 jako kontener ochrony przed odzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="0a84a-115">The command associates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="0a84a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a84a-116">PARAMETERS</span></span>

### <span data-ttu-id="0a84a-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0a84a-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="0a84a-118">Określa podstawowy kontener ochrony, na którym należy zastosować ustawienia profilu ochrony.</span><span class="sxs-lookup"><span data-stu-id="0a84a-118">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a84a-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="0a84a-119">-Profile</span></span>
<span data-ttu-id="0a84a-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a84a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a84a-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="0a84a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a84a-122">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="0a84a-122">-ProtectionProfile</span></span>
<span data-ttu-id="0a84a-123">Określa ustawienia profilu ochrony, które mają zostać zastosowane do kontenerów ochrony.</span><span class="sxs-lookup"><span data-stu-id="0a84a-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="0a84a-124">Aby uzyskać obiekt **ASRProtectionProfile** , użyj polecenia cmdlet New-AzureSiteRecoveryProtectionProfileObject.</span><span class="sxs-lookup"><span data-stu-id="0a84a-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a84a-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0a84a-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="0a84a-126">Określa kontener ochrony przed odzyskiwaniem, na którym należy zastosować ustawienia profilu ochrony.</span><span class="sxs-lookup"><span data-stu-id="0a84a-126">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a84a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a84a-127">CommonParameters</span></span>
<span data-ttu-id="0a84a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a84a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a84a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a84a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a84a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a84a-130">INPUTS</span></span>

## <span data-ttu-id="0a84a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a84a-131">OUTPUTS</span></span>

## <span data-ttu-id="0a84a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a84a-132">NOTES</span></span>

## <span data-ttu-id="0a84a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a84a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0a84a-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0a84a-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="0a84a-135">Nowe — AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="0a84a-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="0a84a-136">Start — AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="0a84a-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


