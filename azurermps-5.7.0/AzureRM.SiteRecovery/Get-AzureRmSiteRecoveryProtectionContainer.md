---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: d5c2032828c5d34b94af8d448155c18b6d8b06c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718454"
---
# <span data-ttu-id="af65b-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="af65b-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="af65b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af65b-102">SYNOPSIS</span></span>
<span data-ttu-id="af65b-103">Pobiera kontenery ochrony dla bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="af65b-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af65b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af65b-104">SYNTAX</span></span>

### <span data-ttu-id="af65b-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="af65b-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af65b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="af65b-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af65b-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="af65b-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af65b-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="af65b-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af65b-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="af65b-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af65b-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="af65b-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af65b-111">Opis</span><span class="sxs-lookup"><span data-stu-id="af65b-111">DESCRIPTION</span></span>
<span data-ttu-id="af65b-112">Polecenie cmdlet **Get-AzureRmSiteRecoveryProtectionContainer** pobiera kontenery ochrony dla bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="af65b-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="af65b-113">Kontener ochrona jest logicznym kontenerem dla obiektów chronionych, takich jak maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="af65b-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="af65b-114">Zasady ochrony definiują ustawienia replikacji dla elementów chronionych i mogą być skojarzone z kontenerem ochrony i stosowane do jednostki chronionej.</span><span class="sxs-lookup"><span data-stu-id="af65b-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="af65b-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af65b-115">EXAMPLES</span></span>

## <span data-ttu-id="af65b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af65b-116">PARAMETERS</span></span>

### <span data-ttu-id="af65b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af65b-117">-DefaultProfile</span></span>
<span data-ttu-id="af65b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af65b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af65b-119">-Fabric</span><span class="sxs-lookup"><span data-stu-id="af65b-119">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af65b-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="af65b-120">-FriendlyName</span></span>
<span data-ttu-id="af65b-121">Określa przyjazną nazwę kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="af65b-121">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af65b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af65b-122">-Name</span></span>
<span data-ttu-id="af65b-123">Określa nazwę kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="af65b-123">Specifies the name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af65b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af65b-124">CommonParameters</span></span>
<span data-ttu-id="af65b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af65b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af65b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af65b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af65b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af65b-127">INPUTS</span></span>

### <span data-ttu-id="af65b-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="af65b-128">ASRFabric</span></span>
<span data-ttu-id="af65b-129">Parametr "Fabric" akceptuje wartość typu "ASRFabric" z procesu</span><span class="sxs-lookup"><span data-stu-id="af65b-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="af65b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af65b-130">OUTPUTS</span></span>

### <span data-ttu-id="af65b-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="af65b-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="af65b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af65b-132">NOTES</span></span>

## <span data-ttu-id="af65b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af65b-133">RELATED LINKS</span></span>

