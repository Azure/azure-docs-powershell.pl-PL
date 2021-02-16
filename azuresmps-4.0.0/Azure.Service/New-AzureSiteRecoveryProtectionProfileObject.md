---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: d7681631d98f80def1076a04ab57f1774bad245c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403650"
---
# <span data-ttu-id="d287a-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="d287a-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="d287a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d287a-102">SYNOPSIS</span></span>
<span data-ttu-id="d287a-103">Tworzy obiekt profilu ochrony odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="d287a-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="d287a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d287a-104">SYNTAX</span></span>

### <span data-ttu-id="d287a-105">EnterpriseToAzure (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d287a-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d287a-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d287a-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d287a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d287a-107">DESCRIPTION</span></span>
<span data-ttu-id="d287a-108">Polecenie **cmdlet New-AzureSiteRecoveryProtectionProfileObject** tworzy obiekt profilu ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d287a-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="d287a-109">To polecenie cmdlet tworzy obiekt **ASRProtectionProfile** do użycia z innymi poleceniami cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d287a-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="d287a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d287a-110">EXAMPLES</span></span>

### <span data-ttu-id="d287a-111">Przykład 1. Tworzenie profilu ochrony</span><span class="sxs-lookup"><span data-stu-id="d287a-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="d287a-112">To polecenie tworzy obiekt profilu ochrony.</span><span class="sxs-lookup"><span data-stu-id="d287a-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="d287a-113">Przykład 2. Tworzenie profilu ochrony dla dostawcy HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="d287a-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="d287a-114">To polecenie tworzy profil ochrony dla dostawcy HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="d287a-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="d287a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d287a-115">PARAMETERS</span></span>

### <span data-ttu-id="d287a-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="d287a-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="d287a-117">Wskazuje, że profil ochrony umożliwia usuwanie replik obiektów.</span><span class="sxs-lookup"><span data-stu-id="d287a-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

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

### <span data-ttu-id="d287a-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="d287a-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="d287a-119">Określa częstotliwość (w godzinach) migawek zgodnych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="d287a-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="d287a-120">— Uwierzytelnianie</span><span class="sxs-lookup"><span data-stu-id="d287a-120">-Authentication</span></span>
<span data-ttu-id="d287a-121">Określa typ uwierzytelniania do użycia.</span><span class="sxs-lookup"><span data-stu-id="d287a-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="d287a-122">Dopuszczalne wartości dla tego parametru to: Certificate i Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d287a-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

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

### <span data-ttu-id="d287a-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="d287a-123">-CompressionEnabled</span></span>
<span data-ttu-id="d287a-124">Wskazuje, że profil ochrony umożliwia kompresję.</span><span class="sxs-lookup"><span data-stu-id="d287a-124">Indicates that the protection profile enables compression.</span></span>

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

### <span data-ttu-id="d287a-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d287a-125">-Force</span></span>
<span data-ttu-id="d287a-126">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d287a-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d287a-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d287a-127">-Name</span></span>
<span data-ttu-id="d287a-128">Określa nazwę profilu ochrony.</span><span class="sxs-lookup"><span data-stu-id="d287a-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="d287a-129">— Profil</span><span class="sxs-lookup"><span data-stu-id="d287a-129">-Profile</span></span>
<span data-ttu-id="d287a-130">Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d287a-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d287a-131">Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="d287a-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d287a-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d287a-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="d287a-133">Określa nazwę konta magazynu platformy Azure, na którym ma być przechowana replika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d287a-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="d287a-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="d287a-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="d287a-135">Określa identyfikator subskrypcji platformy Azure dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d287a-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="d287a-136">Ten parametr odwołuje się do konta, na którym ma być przechowywane replika platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d287a-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="d287a-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="d287a-137">-RecoveryPoints</span></span>
<span data-ttu-id="d287a-138">Określa liczbę godzin, przez które mają być zachowywane punkty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d287a-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="d287a-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="d287a-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="d287a-140">Określa interwał częstotliwości (w sekundach) dla replikacji.</span><span class="sxs-lookup"><span data-stu-id="d287a-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="d287a-141">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d287a-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d287a-142">30</span><span class="sxs-lookup"><span data-stu-id="d287a-142">30</span></span> 
- <span data-ttu-id="d287a-143">300</span><span class="sxs-lookup"><span data-stu-id="d287a-143">300</span></span> 
- <span data-ttu-id="d287a-144">900</span><span class="sxs-lookup"><span data-stu-id="d287a-144">900</span></span>

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

### <span data-ttu-id="d287a-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="d287a-145">-ReplicationMethod</span></span>
<span data-ttu-id="d287a-146">Określa metodę replikacji.</span><span class="sxs-lookup"><span data-stu-id="d287a-146">Specifies the replication method.</span></span> <span data-ttu-id="d287a-147">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d287a-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d287a-148">Online.</span><span class="sxs-lookup"><span data-stu-id="d287a-148">Online.</span></span>
<span data-ttu-id="d287a-149">Replikacja za pośrednictwem sieci.</span><span class="sxs-lookup"><span data-stu-id="d287a-149">Replication over the network.</span></span>
- <span data-ttu-id="d287a-150">W trybie offline.</span><span class="sxs-lookup"><span data-stu-id="d287a-150">Offline.</span></span>

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

### <span data-ttu-id="d287a-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="d287a-151">-ReplicationPort</span></span>
<span data-ttu-id="d287a-152">Określa numer portu, na którym występuje replikacja.</span><span class="sxs-lookup"><span data-stu-id="d287a-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="d287a-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="d287a-153">-ReplicationProvider</span></span>
<span data-ttu-id="d287a-154">Określa typ dostawcy replikacji.</span><span class="sxs-lookup"><span data-stu-id="d287a-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="d287a-155">Dopuszczalne wartości dla tego parametru to: HyperVReplica i HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="d287a-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="d287a-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="d287a-156">-ReplicationStartTime</span></span>
<span data-ttu-id="d287a-157">Określa czas rozpoczęcia replikacji.</span><span class="sxs-lookup"><span data-stu-id="d287a-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="d287a-158">Określ czas w ciągu 24 godzin od rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="d287a-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="d287a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d287a-159">CommonParameters</span></span>
<span data-ttu-id="d287a-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d287a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d287a-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d287a-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d287a-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d287a-162">INPUTS</span></span>

## <span data-ttu-id="d287a-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d287a-163">OUTPUTS</span></span>

## <span data-ttu-id="d287a-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d287a-164">NOTES</span></span>

## <span data-ttu-id="d287a-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d287a-165">RELATED LINKS</span></span>




