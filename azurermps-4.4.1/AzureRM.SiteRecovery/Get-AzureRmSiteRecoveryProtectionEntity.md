---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553756"
---
# <span data-ttu-id="c7211-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c7211-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="c7211-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7211-102">SYNOPSIS</span></span>
<span data-ttu-id="c7211-103">Pobiera listę jednostek chronionych lub chronionych w bieżącym magazynie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="c7211-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7211-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7211-104">SYNTAX</span></span>

### <span data-ttu-id="c7211-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c7211-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7211-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c7211-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7211-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c7211-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7211-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c7211-108">DESCRIPTION</span></span>
<span data-ttu-id="c7211-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryProtectionEntity** umożliwia wyświetlenie listy podmiotów chronionych lub chronionych, takich jak maszyny wirtualne, w bieżącym magazynie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c7211-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c7211-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7211-110">EXAMPLES</span></span>

## <span data-ttu-id="c7211-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7211-111">PARAMETERS</span></span>

### <span data-ttu-id="c7211-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c7211-112">-FriendlyName</span></span>
<span data-ttu-id="c7211-113">Określa przyjazną nazwę jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="c7211-113">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7211-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7211-114">-Name</span></span>
<span data-ttu-id="c7211-115">Określa nazwę jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="c7211-115">Specifies the name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7211-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c7211-116">-ProtectionContainer</span></span>
<span data-ttu-id="c7211-117">Określa obiekt kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="c7211-117">Specifies the protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7211-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7211-118">-DefaultProfile</span></span>
<span data-ttu-id="c7211-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7211-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7211-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7211-120">CommonParameters</span></span>
<span data-ttu-id="c7211-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7211-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7211-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7211-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7211-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7211-123">INPUTS</span></span>

### <span data-ttu-id="c7211-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c7211-124">ASRProtectionContainer</span></span>
<span data-ttu-id="c7211-125">Parametr "ProtectionContainer" akceptuje wartość typu "ASRProtectionContainer" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c7211-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="c7211-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7211-126">OUTPUTS</span></span>

### <span data-ttu-id="c7211-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="c7211-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="c7211-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7211-128">NOTES</span></span>

## <span data-ttu-id="c7211-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7211-129">RELATED LINKS</span></span>

[<span data-ttu-id="c7211-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c7211-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
