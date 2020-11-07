---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 56b8f70494a8575c569aa7a2ee9636521f8a87ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708708"
---
# <span data-ttu-id="2c310-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c310-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="2c310-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c310-102">SYNOPSIS</span></span>
<span data-ttu-id="2c310-103">Pobiera informacje o mapowaniach sieciowych odzyskiwania witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c310-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="2c310-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c310-104">SYNTAX</span></span>

### <span data-ttu-id="2c310-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2c310-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c310-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="2c310-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c310-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2c310-107">DESCRIPTION</span></span>
<span data-ttu-id="2c310-108">Polecenie cmdlet **Get-AzRecoveryServicesAsrNetworkMapping** pobiera informacje o mapowaniach sieciowych usługi Azure Site Recovery dla magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2c310-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="2c310-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c310-109">EXAMPLES</span></span>

### <span data-ttu-id="2c310-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c310-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="2c310-111">Pobiera wszystkie mapowania sieci dla przekazanej sieci.</span><span class="sxs-lookup"><span data-stu-id="2c310-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="2c310-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2c310-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="2c310-113">Pobiera mapowanie sieci z podaną nazwą w określonej sieci szkieletowej odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="2c310-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="2c310-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c310-114">PARAMETERS</span></span>

### <span data-ttu-id="2c310-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c310-115">-DefaultProfile</span></span>
<span data-ttu-id="2c310-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c310-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2c310-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c310-117">-Name</span></span>
<span data-ttu-id="2c310-118">Nazwa obiektu mapowania sieci funkcji ASR do pobrania.</span><span class="sxs-lookup"><span data-stu-id="2c310-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="2c310-119">-Network</span><span class="sxs-lookup"><span data-stu-id="2c310-119">-Network</span></span>
<span data-ttu-id="2c310-120">Pobierz mapowania sieci funkcji ASR odpowiadające określonemu obiektowi sieci ASR.</span><span class="sxs-lookup"><span data-stu-id="2c310-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="2c310-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="2c310-121">-PrimaryFabric</span></span>
<span data-ttu-id="2c310-122">Pobierz mapowania sieci funkcji ASR odpowiadające określonemu głównemu obiektowi Fabric.</span><span class="sxs-lookup"><span data-stu-id="2c310-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="2c310-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c310-123">CommonParameters</span></span>
<span data-ttu-id="2c310-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c310-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c310-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c310-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c310-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c310-126">INPUTS</span></span>

### <span data-ttu-id="2c310-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="2c310-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="2c310-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2c310-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2c310-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c310-129">OUTPUTS</span></span>

### <span data-ttu-id="2c310-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c310-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="2c310-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c310-131">NOTES</span></span>

## <span data-ttu-id="2c310-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c310-132">RELATED LINKS</span></span>

[<span data-ttu-id="2c310-133">Nowe — AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c310-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="2c310-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2c310-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
