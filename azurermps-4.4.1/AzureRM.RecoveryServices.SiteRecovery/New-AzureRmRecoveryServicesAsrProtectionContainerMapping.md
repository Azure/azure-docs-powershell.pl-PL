---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543084"
---
# <span data-ttu-id="d247c-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d247c-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="d247c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d247c-102">SYNOPSIS</span></span>
<span data-ttu-id="d247c-103">Tworzy mapowanie kontenera ochrony witryny platformy Azure, kojarząc określone zasady replikacji z określonym kontenerem ochrony przed Autoodzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="d247c-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d247c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d247c-104">SYNTAX</span></span>

### <span data-ttu-id="d247c-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d247c-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d247c-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d247c-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d247c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d247c-107">DESCRIPTION</span></span>
<span data-ttu-id="d247c-108">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** tworzy mapowanie kontenera ochrony usługi Azure Site Recovery, kojarząc określone zasady replikacji z określonym kontenerem ochrony.</span><span class="sxs-lookup"><span data-stu-id="d247c-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="d247c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d247c-109">EXAMPLES</span></span>

### <span data-ttu-id="d247c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d247c-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="d247c-111">Rozpoczyna Tworzenie mapowania kontenera ochrony przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="d247c-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d247c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d247c-112">PARAMETERS</span></span>

### <span data-ttu-id="d247c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d247c-113">-Name</span></span>
<span data-ttu-id="d247c-114">Określa nazwę mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="d247c-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="d247c-115">-Policy</span><span class="sxs-lookup"><span data-stu-id="d247c-115">-Policy</span></span>
<span data-ttu-id="d247c-116">Określa obiekt zasad replikacji ASR dla zasad replikacji, które mają być używane w mapowaniu.</span><span class="sxs-lookup"><span data-stu-id="d247c-116">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d247c-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d247c-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="d247c-118">Określa obiekt kontenera ochrony przed Autoodzyskiwaniem dla głównego kontenera ochrony, który ma być wykorzystywany w mapowaniu.</span><span class="sxs-lookup"><span data-stu-id="d247c-118">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="d247c-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d247c-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="d247c-120">Określa obiekt kontenera ochrony przed odzyskaniem dla kontenera ochrony przed odzyskiwaniem, który ma być wykorzystywany w mapowaniu (używane w przypadku replikowania do lokalizacji odzyskiwania, która nie jest platformą Azure).</span><span class="sxs-lookup"><span data-stu-id="d247c-120">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="d247c-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d247c-121">-Confirm</span></span>
<span data-ttu-id="d247c-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d247c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d247c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d247c-123">-WhatIf</span></span>
<span data-ttu-id="d247c-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d247c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d247c-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d247c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d247c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d247c-126">CommonParameters</span></span>
<span data-ttu-id="d247c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d247c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d247c-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d247c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d247c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d247c-129">INPUTS</span></span>

### <span data-ttu-id="d247c-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d247c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="d247c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d247c-131">OUTPUTS</span></span>

### <span data-ttu-id="d247c-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d247c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d247c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d247c-133">NOTES</span></span>

## <span data-ttu-id="d247c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d247c-134">RELATED LINKS</span></span>

[<span data-ttu-id="d247c-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d247c-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="d247c-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d247c-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
