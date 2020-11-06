---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 34977acc0889a3fa557af7dfc9f02d6937e22fde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542432"
---
# <span data-ttu-id="21acd-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="21acd-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="21acd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21acd-102">SYNOPSIS</span></span>
<span data-ttu-id="21acd-103">Pobiera informacje o sieciach zarządzanych przez odzyskiwanie witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="21acd-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21acd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21acd-104">SYNTAX</span></span>

### <span data-ttu-id="21acd-105">ByFabricObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21acd-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21acd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="21acd-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21acd-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="21acd-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21acd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="21acd-108">DESCRIPTION</span></span>
<span data-ttu-id="21acd-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrNetwork** pobiera informacje o sieciach usługi Azure Site Recovery dla bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="21acd-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="21acd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21acd-110">EXAMPLES</span></span>

### <span data-ttu-id="21acd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21acd-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="21acd-112">Pobiera wszystkie znane sieci w określonej sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="21acd-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="21acd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21acd-113">PARAMETERS</span></span>

### <span data-ttu-id="21acd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21acd-114">-DefaultProfile</span></span>
<span data-ttu-id="21acd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21acd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="21acd-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="21acd-116">-Fabric</span></span>
<span data-ttu-id="21acd-117">Obiekt sieci szkieletowej ASR</span><span class="sxs-lookup"><span data-stu-id="21acd-117">ASR fabric object</span></span>

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

### <span data-ttu-id="21acd-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="21acd-118">-FriendlyName</span></span>
<span data-ttu-id="21acd-119">Przyjazna nazwa sieciowego obiektu ASR.</span><span class="sxs-lookup"><span data-stu-id="21acd-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="21acd-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21acd-120">-Name</span></span>
<span data-ttu-id="21acd-121">Nazwa obiektu ASR (Network ASR).</span><span class="sxs-lookup"><span data-stu-id="21acd-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="21acd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21acd-122">CommonParameters</span></span>
<span data-ttu-id="21acd-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21acd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21acd-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21acd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21acd-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21acd-125">INPUTS</span></span>

### <span data-ttu-id="21acd-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="21acd-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="21acd-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21acd-127">OUTPUTS</span></span>

### <span data-ttu-id="21acd-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="21acd-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="21acd-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21acd-129">NOTES</span></span>

## <span data-ttu-id="21acd-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21acd-130">RELATED LINKS</span></span>
