---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553147"
---
# <span data-ttu-id="79c73-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="79c73-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="79c73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79c73-102">SYNOPSIS</span></span>
<span data-ttu-id="79c73-103">Pobierz elementy do ochrony w kontenerze ochrona przed Autoodzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="79c73-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79c73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79c73-104">SYNTAX</span></span>

### <span data-ttu-id="79c73-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79c73-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="79c73-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="79c73-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="79c73-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="79c73-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="79c73-108">Opis</span><span class="sxs-lookup"><span data-stu-id="79c73-108">DESCRIPTION</span></span>
<span data-ttu-id="79c73-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrProtectableItem** Pobiera elementy, które należy chronić w kontenerze ochrona odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79c73-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="79c73-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79c73-110">EXAMPLES</span></span>

### <span data-ttu-id="79c73-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79c73-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="79c73-112">Pobiera wszystkie elementy chronione w określonym kontenerze ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="79c73-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="79c73-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79c73-113">PARAMETERS</span></span>

### <span data-ttu-id="79c73-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="79c73-114">-FriendlyName</span></span>
<span data-ttu-id="79c73-115">Określa przyjazną nazwę elementu z możliwością ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="79c73-115">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c73-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79c73-116">-Name</span></span>
<span data-ttu-id="79c73-117">Określa nazwę elementu do ochrony przed ASR.</span><span class="sxs-lookup"><span data-stu-id="79c73-117">Specifies the name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c73-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="79c73-118">-ProtectionContainer</span></span>
<span data-ttu-id="79c73-119">Określa obiekt kontenera ochrony przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="79c73-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79c73-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c73-120">CommonParameters</span></span>
<span data-ttu-id="79c73-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c73-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c73-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c73-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c73-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79c73-123">INPUTS</span></span>

### <span data-ttu-id="79c73-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="79c73-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="79c73-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79c73-125">OUTPUTS</span></span>

### <span data-ttu-id="79c73-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="79c73-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="79c73-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79c73-127">NOTES</span></span>

## <span data-ttu-id="79c73-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79c73-128">RELATED LINKS</span></span>

[<span data-ttu-id="79c73-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="79c73-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="79c73-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="79c73-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
