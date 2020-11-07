---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 8bea83b033ffb8a2e56ba6d28759e88280529a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717716"
---
# <span data-ttu-id="51409-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="51409-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="51409-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51409-102">SYNOPSIS</span></span>
<span data-ttu-id="51409-103">Pobiera dostępne (odnalezione) klasyfikacje magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="51409-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51409-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51409-104">SYNTAX</span></span>

### <span data-ttu-id="51409-105">ByFabricObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="51409-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51409-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="51409-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51409-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="51409-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51409-108">Opis</span><span class="sxs-lookup"><span data-stu-id="51409-108">DESCRIPTION</span></span>
<span data-ttu-id="51409-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrStorageClassification** pobiera szczegóły odnalezionych klasyfikacji magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="51409-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="51409-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51409-110">EXAMPLES</span></span>

### <span data-ttu-id="51409-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51409-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="51409-112">Lista odnalezionych klasyfikacji magazynu odpowiadających określonej sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="51409-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="51409-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51409-113">PARAMETERS</span></span>

### <span data-ttu-id="51409-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51409-114">-DefaultProfile</span></span>
<span data-ttu-id="51409-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51409-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="51409-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="51409-116">-Fabric</span></span>
<span data-ttu-id="51409-117">Określa obiekt sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="51409-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="51409-118">Polecenie cmdlet umożliwia pobieranie szczegółów dotyczących odnalezionych klasyfikacji magazynu odpowiadających określonej sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="51409-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51409-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="51409-119">-FriendlyName</span></span>
<span data-ttu-id="51409-120">Określa przyjazną nazwę obiektu klasyfikacji magazynu, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="51409-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="51409-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51409-121">-Name</span></span>
<span data-ttu-id="51409-122">Określa nazwę obiektu klasyfikacji magazynu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="51409-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="51409-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51409-123">CommonParameters</span></span>
<span data-ttu-id="51409-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51409-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51409-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51409-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51409-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51409-126">INPUTS</span></span>

### <span data-ttu-id="51409-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="51409-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="51409-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51409-128">OUTPUTS</span></span>

### <span data-ttu-id="51409-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="51409-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="51409-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51409-130">NOTES</span></span>

## <span data-ttu-id="51409-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51409-131">RELATED LINKS</span></span>
