---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 2a857c538188c2b9ddf7516ccebda291f3161e1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551564"
---
# <span data-ttu-id="e897f-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e897f-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="e897f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e897f-102">SYNOPSIS</span></span>
<span data-ttu-id="e897f-103">Pobierz elementy do zabezpieczenia w kontenerze ochrony.</span><span class="sxs-lookup"><span data-stu-id="e897f-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e897f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e897f-104">SYNTAX</span></span>

### <span data-ttu-id="e897f-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e897f-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e897f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e897f-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e897f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e897f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e897f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e897f-108">DESCRIPTION</span></span>
<span data-ttu-id="e897f-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryProtectableItem** Pobiera elementy, które należy chronić w kontenerze ochrona odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e897f-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="e897f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e897f-110">EXAMPLES</span></span>

## <span data-ttu-id="e897f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e897f-111">PARAMETERS</span></span>

### <span data-ttu-id="e897f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e897f-112">-DefaultProfile</span></span>
<span data-ttu-id="e897f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e897f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e897f-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e897f-114">-FriendlyName</span></span>
<span data-ttu-id="e897f-115">Określa przyjazną nazwę elementu ochrony przed odzyskiwaniem witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e897f-115">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="e897f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e897f-116">-Name</span></span>
<span data-ttu-id="e897f-117">Określa nazwę elementu do ochrony przed odzyskiwaniem witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e897f-117">Specifies the name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="e897f-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e897f-118">-ProtectionContainer</span></span>
<span data-ttu-id="e897f-119">Określa obiekt kontenera ochrony przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="e897f-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="e897f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e897f-120">CommonParameters</span></span>
<span data-ttu-id="e897f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e897f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e897f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e897f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e897f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e897f-123">INPUTS</span></span>

### <span data-ttu-id="e897f-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e897f-124">ASRProtectionContainer</span></span>
<span data-ttu-id="e897f-125">Parametr "ProtectionContainer" akceptuje wartość typu "ASRProtectionContainer" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e897f-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="e897f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e897f-126">OUTPUTS</span></span>

### <span data-ttu-id="e897f-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e897f-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e897f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e897f-128">NOTES</span></span>

## <span data-ttu-id="e897f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e897f-129">RELATED LINKS</span></span>

[<span data-ttu-id="e897f-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e897f-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="e897f-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e897f-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
