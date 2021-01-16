---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364763"
---
# <span data-ttu-id="c2a08-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2a08-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="c2a08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2a08-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a08-103">Pobiera informacje o mapowaniach sieciowych odzyskiwania witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="c2a08-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="c2a08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2a08-104">SYNTAX</span></span>

### <span data-ttu-id="c2a08-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2a08-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2a08-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="c2a08-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2a08-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2a08-107">DESCRIPTION</span></span>
<span data-ttu-id="c2a08-108">Polecenie cmdlet **Get-AzRecoveryServicesAsrNetworkMapping** pobiera informacje o mapowaniach sieciowych usługi Azure Site Recovery dla magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="c2a08-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="c2a08-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2a08-109">EXAMPLES</span></span>

### <span data-ttu-id="c2a08-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2a08-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="c2a08-111">Pobiera wszystkie mapowania sieci dla przekazanej sieci.</span><span class="sxs-lookup"><span data-stu-id="c2a08-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="c2a08-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c2a08-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="c2a08-113">Pobiera mapowanie sieci z podaną nazwą w określonej sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a08-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="c2a08-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2a08-114">PARAMETERS</span></span>

### <span data-ttu-id="c2a08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a08-115">-DefaultProfile</span></span>
<span data-ttu-id="c2a08-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a08-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c2a08-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2a08-117">-Name</span></span>
<span data-ttu-id="c2a08-118">Nazwa obiektu mapowania sieci funkcji ASR do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c2a08-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a08-119">-Network</span><span class="sxs-lookup"><span data-stu-id="c2a08-119">-Network</span></span>
<span data-ttu-id="c2a08-120">Pobierz mapowania sieci funkcji ASR odpowiadające określonemu obiektowi sieci ASR.</span><span class="sxs-lookup"><span data-stu-id="c2a08-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a08-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="c2a08-121">-PrimaryFabric</span></span>
<span data-ttu-id="c2a08-122">Pobierz mapowania sieci funkcji ASR odpowiadające określonemu głównemu obiektowi Fabric.</span><span class="sxs-lookup"><span data-stu-id="c2a08-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a08-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a08-123">CommonParameters</span></span>
<span data-ttu-id="c2a08-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a08-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a08-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2a08-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a08-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2a08-126">INPUTS</span></span>

### <span data-ttu-id="c2a08-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="c2a08-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="c2a08-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c2a08-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c2a08-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2a08-129">OUTPUTS</span></span>

### <span data-ttu-id="c2a08-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2a08-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="c2a08-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2a08-131">NOTES</span></span>

## <span data-ttu-id="c2a08-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2a08-132">RELATED LINKS</span></span>

[<span data-ttu-id="c2a08-133">Nowe — AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2a08-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="c2a08-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2a08-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
