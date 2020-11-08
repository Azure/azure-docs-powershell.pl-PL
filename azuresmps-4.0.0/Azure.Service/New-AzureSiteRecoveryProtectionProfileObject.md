---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054857"
---
# <span data-ttu-id="5a385-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="5a385-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="5a385-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a385-102">SYNOPSIS</span></span>
<span data-ttu-id="5a385-103">Tworzy obiekt profilu ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="5a385-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="5a385-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a385-104">SYNTAX</span></span>

### <span data-ttu-id="5a385-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5a385-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a385-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="5a385-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a385-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5a385-107">DESCRIPTION</span></span>
<span data-ttu-id="5a385-108">Polecenie cmdlet **New-AzureSiteRecoveryProtectionProfileObject** tworzy obiekt profilu ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5a385-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="5a385-109">To polecenie cmdlet tworzy obiekt **ASRProtectionProfile** , który będzie używany z innymi poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a385-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="5a385-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a385-110">EXAMPLES</span></span>

### <span data-ttu-id="5a385-111">Przykład 1. Tworzenie profilu ochrony</span><span class="sxs-lookup"><span data-stu-id="5a385-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="5a385-112">To polecenie tworzy obiekt profilu ochrony.</span><span class="sxs-lookup"><span data-stu-id="5a385-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="5a385-113">Przykład 2: Tworzenie profilu ochrony dla dostawcy usługi HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="5a385-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="5a385-114">To polecenie tworzy profil ochrony dla dostawcy HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="5a385-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="5a385-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a385-115">PARAMETERS</span></span>

### <span data-ttu-id="5a385-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="5a385-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="5a385-117">Wskazuje, że profil ochrony umożliwia usuwanie jednostek repliki.</span><span class="sxs-lookup"><span data-stu-id="5a385-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="5a385-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="5a385-119">Określa częstotliwość (w godzinach) tworzenia migawek zgodnych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="5a385-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-120">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="5a385-120">-Authentication</span></span>
<span data-ttu-id="5a385-121">Określa typ uwierzytelniania, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="5a385-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="5a385-122">Dopuszczalne wartości tego parametru to: certyfikat i protokół Kerberos.</span><span class="sxs-lookup"><span data-stu-id="5a385-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="5a385-123">-CompressionEnabled</span></span>
<span data-ttu-id="5a385-124">Wskazuje, że profil ochrony umożliwia kompresję.</span><span class="sxs-lookup"><span data-stu-id="5a385-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5a385-125">-Force</span></span>
<span data-ttu-id="5a385-126">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5a385-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a385-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a385-127">-Name</span></span>
<span data-ttu-id="5a385-128">Określa nazwę profilu ochrony.</span><span class="sxs-lookup"><span data-stu-id="5a385-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="5a385-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="5a385-129">-Profile</span></span>
<span data-ttu-id="5a385-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a385-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a385-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5a385-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a385-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a385-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="5a385-133">Określa nazwę konta usługi Azure Storage, na którym ma być przechowywana encja usługi Azure Replica.</span><span class="sxs-lookup"><span data-stu-id="5a385-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="5a385-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="5a385-135">Określa identyfikator subskrypcji usługi Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5a385-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="5a385-136">Ten parametr odwołuje się do konta, na którym jest przechowywana jednostka usługi Azure Replica.</span><span class="sxs-lookup"><span data-stu-id="5a385-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="5a385-137">-RecoveryPoints</span></span>
<span data-ttu-id="5a385-138">Określa liczbę godzin do przechowywania punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5a385-138">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="5a385-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="5a385-140">Określa interwał częstotliwości (w sekundach) replikacji.</span><span class="sxs-lookup"><span data-stu-id="5a385-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="5a385-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5a385-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a385-142">30</span><span class="sxs-lookup"><span data-stu-id="5a385-142">30</span></span> 
- <span data-ttu-id="5a385-143">300</span><span class="sxs-lookup"><span data-stu-id="5a385-143">300</span></span> 
- <span data-ttu-id="5a385-144">900</span><span class="sxs-lookup"><span data-stu-id="5a385-144">900</span></span>

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

### <span data-ttu-id="5a385-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="5a385-145">-ReplicationMethod</span></span>
<span data-ttu-id="5a385-146">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="5a385-146">Specifies the replication method.</span></span> <span data-ttu-id="5a385-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5a385-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a385-148">Ekran.</span><span class="sxs-lookup"><span data-stu-id="5a385-148">Online.</span></span>
<span data-ttu-id="5a385-149">Replikacja za pośrednictwem sieci.</span><span class="sxs-lookup"><span data-stu-id="5a385-149">Replication over the network.</span></span>
- <span data-ttu-id="5a385-150">Pracy.</span><span class="sxs-lookup"><span data-stu-id="5a385-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="5a385-151">-ReplicationPort</span></span>
<span data-ttu-id="5a385-152">Określa numer portu, na którym odbywa się replikacja.</span><span class="sxs-lookup"><span data-stu-id="5a385-152">Specifies the number of the port on which the replication occurs.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="5a385-153">-ReplicationProvider</span></span>
<span data-ttu-id="5a385-154">Określa typ dostawcy replikacji.</span><span class="sxs-lookup"><span data-stu-id="5a385-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="5a385-155">Dopuszczalne wartości tego parametru to: HyperVReplica oraz HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="5a385-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="5a385-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="5a385-156">-ReplicationStartTime</span></span>
<span data-ttu-id="5a385-157">Określa godzinę rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="5a385-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="5a385-158">Określ czas w ciągu 24 godzin po rozpoczęciu zadania.</span><span class="sxs-lookup"><span data-stu-id="5a385-158">Specify a time within 24 hours after you start the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a385-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a385-159">CommonParameters</span></span>
<span data-ttu-id="5a385-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a385-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a385-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a385-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a385-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a385-162">INPUTS</span></span>

## <span data-ttu-id="5a385-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a385-163">OUTPUTS</span></span>

## <span data-ttu-id="5a385-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a385-164">NOTES</span></span>

## <span data-ttu-id="5a385-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a385-165">RELATED LINKS</span></span>

[<span data-ttu-id="5a385-166">Polecenia cmdlet usług Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="5a385-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


