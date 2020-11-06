---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 442fd62393b33cc69e8f5a38f726bb8816c5bc64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542435"
---
# <span data-ttu-id="9d735-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9d735-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="9d735-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d735-102">SYNOPSIS</span></span>
<span data-ttu-id="9d735-103">Pobiera informacje o mapowaniach sieciowych odzyskiwania witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="9d735-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d735-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d735-104">SYNTAX</span></span>

### <span data-ttu-id="9d735-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d735-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d735-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="9d735-106">ByFabricObject</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d735-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9d735-107">DESCRIPTION</span></span>
<span data-ttu-id="9d735-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrNetworkMapping** pobiera informacje o mapowaniach sieciowych usługi Azure Site Recovery dla magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="9d735-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="9d735-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d735-109">EXAMPLES</span></span>

### <span data-ttu-id="9d735-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d735-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="9d735-111">Pobiera wszystkie mapowania sieci dla przekazanej sieci.</span><span class="sxs-lookup"><span data-stu-id="9d735-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="9d735-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9d735-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="9d735-113">Pobiera mapowanie sieci z podaną nazwą w określonej sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="9d735-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="9d735-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d735-114">PARAMETERS</span></span>

### <span data-ttu-id="9d735-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d735-115">-DefaultProfile</span></span>
<span data-ttu-id="9d735-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d735-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="9d735-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d735-117">-Name</span></span>
<span data-ttu-id="9d735-118">Nazwa obiektu mapowania sieci funkcji ASR do pobrania.</span><span class="sxs-lookup"><span data-stu-id="9d735-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="9d735-119">-Network</span><span class="sxs-lookup"><span data-stu-id="9d735-119">-Network</span></span>
<span data-ttu-id="9d735-120">Pobierz mapowania sieci funkcji ASR odpowiadające określonemu obiektowi sieci ASR.</span><span class="sxs-lookup"><span data-stu-id="9d735-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d735-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="9d735-121">-PrimaryFabric</span></span>
<span data-ttu-id="9d735-122">Pobierz mapowania sieci funkcji ASR odpowiadające określonemu głównemu obiektowi Fabric.</span><span class="sxs-lookup"><span data-stu-id="9d735-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="9d735-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d735-123">CommonParameters</span></span>
<span data-ttu-id="9d735-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d735-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d735-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d735-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d735-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d735-126">INPUTS</span></span>

### <span data-ttu-id="9d735-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="9d735-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="9d735-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d735-128">OUTPUTS</span></span>

### <span data-ttu-id="9d735-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9d735-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9d735-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d735-130">NOTES</span></span>

## <span data-ttu-id="9d735-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d735-131">RELATED LINKS</span></span>

[<span data-ttu-id="9d735-132">Nowe — AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9d735-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="9d735-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9d735-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
