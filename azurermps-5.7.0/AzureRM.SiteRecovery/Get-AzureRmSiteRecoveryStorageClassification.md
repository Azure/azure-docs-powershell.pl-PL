---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 4ca96961aa99a15161e9abbbc01174f97a27968e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551548"
---
# <span data-ttu-id="a1778-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a1778-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="a1778-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1778-102">SYNOPSIS</span></span>
<span data-ttu-id="a1778-103">Pobiera klasyfikacje przestrzeni dyskowej w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="a1778-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1778-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1778-104">SYNTAX</span></span>

### <span data-ttu-id="a1778-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a1778-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1778-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a1778-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1778-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a1778-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1778-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="a1778-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1778-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="a1778-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1778-110">Opis</span><span class="sxs-lookup"><span data-stu-id="a1778-110">DESCRIPTION</span></span>
<span data-ttu-id="a1778-111">Polecenie cmdlet **Get-AzureRmSiteRecoveryStorageClassification** pobiera klasyfikacje przestrzeni dyskowej w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a1778-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="a1778-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1778-112">EXAMPLES</span></span>

## <span data-ttu-id="a1778-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1778-113">PARAMETERS</span></span>

### <span data-ttu-id="a1778-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1778-114">-DefaultProfile</span></span>
<span data-ttu-id="a1778-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1778-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1778-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="a1778-116">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1778-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a1778-117">-FriendlyName</span></span>
<span data-ttu-id="a1778-118">Określa przyjazną nazwę klasyfikacji magazynu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1778-118">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1778-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1778-119">-Name</span></span>
<span data-ttu-id="a1778-120">Określa nazwę klasyfikacji magazynu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1778-120">Specifies the name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1778-121">-Server</span><span class="sxs-lookup"><span data-stu-id="a1778-121">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1778-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1778-122">CommonParameters</span></span>
<span data-ttu-id="a1778-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1778-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1778-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1778-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1778-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1778-125">INPUTS</span></span>

### <span data-ttu-id="a1778-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a1778-126">ASRFabric</span></span>
<span data-ttu-id="a1778-127">Parametr "Fabric" akceptuje wartość typu "ASRFabric" z procesu</span><span class="sxs-lookup"><span data-stu-id="a1778-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="a1778-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="a1778-128">ASRServer</span></span>
<span data-ttu-id="a1778-129">Parametr "serwer" akceptuje wartość typu "ASRServer" z procesu</span><span class="sxs-lookup"><span data-stu-id="a1778-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="a1778-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1778-130">OUTPUTS</span></span>

### <span data-ttu-id="a1778-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="a1778-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="a1778-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1778-132">NOTES</span></span>

## <span data-ttu-id="a1778-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1778-133">RELATED LINKS</span></span>

