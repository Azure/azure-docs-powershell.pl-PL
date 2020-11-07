---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 851978fafa35d36923adf4dd2c2a6e071c054d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718452"
---
# <span data-ttu-id="9d3d5-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9d3d5-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="9d3d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="9d3d5-103">Pobiera listę jednostek chronionych lub chronionych w bieżącym magazynie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d3d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d3d5-104">SYNTAX</span></span>

### <span data-ttu-id="9d3d5-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d3d5-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d3d5-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9d3d5-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d3d5-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9d3d5-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d3d5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9d3d5-108">DESCRIPTION</span></span>
<span data-ttu-id="9d3d5-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryProtectionEntity** umożliwia wyświetlenie listy podmiotów chronionych lub chronionych, takich jak maszyny wirtualne, w bieżącym magazynie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9d3d5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d3d5-110">EXAMPLES</span></span>

## <span data-ttu-id="9d3d5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d3d5-111">PARAMETERS</span></span>

### <span data-ttu-id="9d3d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d3d5-112">-DefaultProfile</span></span>
<span data-ttu-id="9d3d5-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d3d5-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9d3d5-114">-FriendlyName</span></span>
<span data-ttu-id="9d3d5-115">Określa przyjazną nazwę jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-115">Specifies the friendly name of the protection entity.</span></span>

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

### <span data-ttu-id="9d3d5-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d3d5-116">-Name</span></span>
<span data-ttu-id="9d3d5-117">Określa nazwę jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-117">Specifies the name of the protection entity.</span></span>

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

### <span data-ttu-id="9d3d5-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9d3d5-118">-ProtectionContainer</span></span>
<span data-ttu-id="9d3d5-119">Określa obiekt kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-119">Specifies the protection container object.</span></span>

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

### <span data-ttu-id="9d3d5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d3d5-120">CommonParameters</span></span>
<span data-ttu-id="9d3d5-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d3d5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d3d5-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d3d5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d3d5-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d3d5-123">INPUTS</span></span>

### <span data-ttu-id="9d3d5-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9d3d5-124">ASRProtectionContainer</span></span>
<span data-ttu-id="9d3d5-125">Parametr "ProtectionContainer" akceptuje wartość typu "ASRProtectionContainer" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9d3d5-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="9d3d5-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d3d5-126">OUTPUTS</span></span>

### <span data-ttu-id="9d3d5-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="9d3d5-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="9d3d5-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d3d5-128">NOTES</span></span>

## <span data-ttu-id="9d3d5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d3d5-129">RELATED LINKS</span></span>

[<span data-ttu-id="9d3d5-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9d3d5-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
