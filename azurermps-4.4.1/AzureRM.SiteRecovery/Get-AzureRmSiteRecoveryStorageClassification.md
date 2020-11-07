---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 8e2b563563ca50e0fdf6913a9e9999e1a642ff9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718689"
---
# <span data-ttu-id="28988-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="28988-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="28988-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28988-102">SYNOPSIS</span></span>
<span data-ttu-id="28988-103">Pobiera klasyfikacje przestrzeni dyskowej w ramach odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="28988-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28988-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28988-104">SYNTAX</span></span>

### <span data-ttu-id="28988-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="28988-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28988-106">ByName</span><span class="sxs-lookup"><span data-stu-id="28988-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28988-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="28988-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28988-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="28988-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28988-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="28988-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28988-110">Opis</span><span class="sxs-lookup"><span data-stu-id="28988-110">DESCRIPTION</span></span>
<span data-ttu-id="28988-111">Polecenie cmdlet **Get-AzureRmSiteRecoveryStorageClassification** pobiera klasyfikacje przestrzeni dyskowej w usłudze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="28988-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="28988-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28988-112">EXAMPLES</span></span>

## <span data-ttu-id="28988-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28988-113">PARAMETERS</span></span>

### <span data-ttu-id="28988-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="28988-114">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28988-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="28988-115">-FriendlyName</span></span>
<span data-ttu-id="28988-116">Określa przyjazną nazwę klasyfikacji magazynu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28988-116">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28988-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28988-117">-Name</span></span>
<span data-ttu-id="28988-118">Określa nazwę klasyfikacji magazynu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28988-118">Specifies the name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28988-119">-Server</span><span class="sxs-lookup"><span data-stu-id="28988-119">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28988-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28988-120">-DefaultProfile</span></span>
<span data-ttu-id="28988-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28988-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28988-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28988-122">CommonParameters</span></span>
<span data-ttu-id="28988-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28988-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28988-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28988-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28988-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28988-125">INPUTS</span></span>

### <span data-ttu-id="28988-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="28988-126">ASRFabric</span></span>
<span data-ttu-id="28988-127">Parametr "Fabric" akceptuje wartość typu "ASRFabric" z procesu</span><span class="sxs-lookup"><span data-stu-id="28988-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="28988-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="28988-128">ASRServer</span></span>
<span data-ttu-id="28988-129">Parametr "serwer" akceptuje wartość typu "ASRServer" z procesu</span><span class="sxs-lookup"><span data-stu-id="28988-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="28988-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28988-130">OUTPUTS</span></span>

### <span data-ttu-id="28988-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="28988-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="28988-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28988-132">NOTES</span></span>

## <span data-ttu-id="28988-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28988-133">RELATED LINKS</span></span>

