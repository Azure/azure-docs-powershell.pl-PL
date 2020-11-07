---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: e344dd4b5284a29c84b4f4c4b90d5a99f5d8d4ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872763"
---
# <span data-ttu-id="14a34-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="14a34-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="14a34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14a34-102">SYNOPSIS</span></span>
<span data-ttu-id="14a34-103">Pobiera informacje o sieciach zarządzanych przez odzyskiwanie witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="14a34-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="14a34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14a34-104">SYNTAX</span></span>

### <span data-ttu-id="14a34-105">ByFabricObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="14a34-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14a34-106">ByName</span><span class="sxs-lookup"><span data-stu-id="14a34-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14a34-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="14a34-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14a34-108">Opis</span><span class="sxs-lookup"><span data-stu-id="14a34-108">DESCRIPTION</span></span>
<span data-ttu-id="14a34-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrNetwork** pobiera informacje o sieciach usługi Azure Site Recovery dla bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="14a34-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="14a34-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14a34-110">EXAMPLES</span></span>

### <span data-ttu-id="14a34-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14a34-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="14a34-112">Pobiera wszystkie znane sieci w określonej sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="14a34-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="14a34-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14a34-113">PARAMETERS</span></span>

### <span data-ttu-id="14a34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a34-114">-DefaultProfile</span></span>
<span data-ttu-id="14a34-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="14a34-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a34-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="14a34-116">-Fabric</span></span>
<span data-ttu-id="14a34-117">Obiekt sieci szkieletowej ASR</span><span class="sxs-lookup"><span data-stu-id="14a34-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14a34-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="14a34-118">-FriendlyName</span></span>
<span data-ttu-id="14a34-119">Przyjazna nazwa sieciowego obiektu ASR.</span><span class="sxs-lookup"><span data-stu-id="14a34-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="14a34-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14a34-120">-Name</span></span>
<span data-ttu-id="14a34-121">Nazwa obiektu ASR (Network ASR).</span><span class="sxs-lookup"><span data-stu-id="14a34-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="14a34-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a34-122">CommonParameters</span></span>
<span data-ttu-id="14a34-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a34-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a34-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a34-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a34-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14a34-125">INPUTS</span></span>

### <span data-ttu-id="14a34-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="14a34-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="14a34-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14a34-127">OUTPUTS</span></span>

### <span data-ttu-id="14a34-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="14a34-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="14a34-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14a34-129">NOTES</span></span>

## <span data-ttu-id="14a34-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14a34-130">RELATED LINKS</span></span>
