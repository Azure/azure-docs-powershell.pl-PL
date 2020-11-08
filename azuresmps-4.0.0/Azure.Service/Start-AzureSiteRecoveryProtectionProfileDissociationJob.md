---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055376"
---
# <span data-ttu-id="ebb85-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="ebb85-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="ebb85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebb85-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb85-103">Rozpoczyna zadanie tworzenia skojarzenia w zasadach replikacji skojarzonych z kontenerem ochrona przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="ebb85-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="ebb85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebb85-104">SYNTAX</span></span>

### <span data-ttu-id="ebb85-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ebb85-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ebb85-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ebb85-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ebb85-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ebb85-107">DESCRIPTION</span></span>
<span data-ttu-id="ebb85-108">Polecenie cmdlet **Starting-AzureSiteRecoveryProtectionProfileDissociationJob** inicjuje zadanie skojarzenia zabezpieczeń w zasadach replikacji skojarzonych z kontenerem Ochrona usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ebb85-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="ebb85-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebb85-109">EXAMPLES</span></span>

### <span data-ttu-id="ebb85-110">Przykład 1: deskojarzenie profilu ochrony</span><span class="sxs-lookup"><span data-stu-id="ebb85-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="ebb85-111">Pierwsze polecenie uzyskuje kontener ochrony przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje ten kontener w zmiennej $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="ebb85-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="ebb85-112">Drugie polecenie pobiera kontener ochrony, a następnie zapisuje go w zmiennej $ProtectionContainer 02.</span><span class="sxs-lookup"><span data-stu-id="ebb85-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="ebb85-113">Polecenie ostatnie umożliwia skojarzenie profilu ochrony z kontenerem przechowywanym w $ProtectionContainer 01 jako głównym kontenerem ochrony.</span><span class="sxs-lookup"><span data-stu-id="ebb85-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="ebb85-114">Polecenie umożliwia skojarzenie kontenera przechowywanego w $ProtectionContainer 02 z kontenerem ochrona przed odzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="ebb85-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="ebb85-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebb85-115">PARAMETERS</span></span>

### <span data-ttu-id="ebb85-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ebb85-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="ebb85-117">Określa podstawowy kontener ochrony.</span><span class="sxs-lookup"><span data-stu-id="ebb85-117">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="ebb85-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="ebb85-118">-Profile</span></span>
<span data-ttu-id="ebb85-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebb85-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ebb85-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ebb85-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ebb85-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="ebb85-121">-ProtectionProfile</span></span>
<span data-ttu-id="ebb85-122">Określa ustawienia profilu ochrony, które można usunąć z kontenerów ochrony.</span><span class="sxs-lookup"><span data-stu-id="ebb85-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="ebb85-123">Określa ustawienia profilu ochrony, które mają zostać zastosowane do kontenerów ochrony.</span><span class="sxs-lookup"><span data-stu-id="ebb85-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="ebb85-124">Aby uzyskać obiekt **ASRProtectionProfile** , użyj polecenia cmdlet New-AzureSiteRecoveryProtectionProfileObject.</span><span class="sxs-lookup"><span data-stu-id="ebb85-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

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

### <span data-ttu-id="ebb85-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ebb85-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="ebb85-126">Określa kontener ochrona przed odzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="ebb85-126">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="ebb85-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb85-127">CommonParameters</span></span>
<span data-ttu-id="ebb85-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebb85-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb85-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb85-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb85-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebb85-130">INPUTS</span></span>

## <span data-ttu-id="ebb85-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebb85-131">OUTPUTS</span></span>

## <span data-ttu-id="ebb85-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebb85-132">NOTES</span></span>

## <span data-ttu-id="ebb85-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebb85-133">RELATED LINKS</span></span>

[<span data-ttu-id="ebb85-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ebb85-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="ebb85-135">Nowe — AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="ebb85-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="ebb85-136">Start — AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="ebb85-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


