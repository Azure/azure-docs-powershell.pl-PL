---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193035"
---
# <span data-ttu-id="238ff-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="238ff-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="238ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="238ff-102">SYNOPSIS</span></span>
<span data-ttu-id="238ff-103">Pobiera informacje o mapowaniu sieci odzyskiwania witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="238ff-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="238ff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="238ff-104">SYNTAX</span></span>

### <span data-ttu-id="238ff-105">ByObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="238ff-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="238ff-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="238ff-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="238ff-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="238ff-107">DESCRIPTION</span></span>
<span data-ttu-id="238ff-108">Polecenie **cmdlet Get-AzRecoveryServicesAsrNetworkMapping** pobiera informacje o mapowaniu sieci usługi Azure Site Recovery dla magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="238ff-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="238ff-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="238ff-109">EXAMPLES</span></span>

### <span data-ttu-id="238ff-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="238ff-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="238ff-111">Pobiera wszystkie mapowania sieci dla przekazywanej sieci.</span><span class="sxs-lookup"><span data-stu-id="238ff-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="238ff-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="238ff-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="238ff-113">Otrzymuje mapowanie sieci pod podaną nazwą w określonym szkieletie odzyskiwania witryn azure.</span><span class="sxs-lookup"><span data-stu-id="238ff-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="238ff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="238ff-114">PARAMETERS</span></span>

### <span data-ttu-id="238ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238ff-115">-DefaultProfile</span></span>
<span data-ttu-id="238ff-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="238ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="238ff-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="238ff-117">-Name</span></span>
<span data-ttu-id="238ff-118">Nazwa obiektu mapowania sieci asr, który ma być uzyskać.</span><span class="sxs-lookup"><span data-stu-id="238ff-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="238ff-119">— Sieć</span><span class="sxs-lookup"><span data-stu-id="238ff-119">-Network</span></span>
<span data-ttu-id="238ff-120">Pobierz mapowania sieci asr odpowiadające określoneowi obiektowi asr sieci.</span><span class="sxs-lookup"><span data-stu-id="238ff-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="238ff-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="238ff-121">-PrimaryFabric</span></span>
<span data-ttu-id="238ff-122">Uzyskaj mapowania sieci ASR odpowiadające określoneowi podstawoweowi obiektu szkieletowego.</span><span class="sxs-lookup"><span data-stu-id="238ff-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="238ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238ff-123">CommonParameters</span></span>
<span data-ttu-id="238ff-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="238ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238ff-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="238ff-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238ff-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="238ff-126">INPUTS</span></span>

### <span data-ttu-id="238ff-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="238ff-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="238ff-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="238ff-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="238ff-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="238ff-129">OUTPUTS</span></span>

### <span data-ttu-id="238ff-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="238ff-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="238ff-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="238ff-131">NOTES</span></span>

## <span data-ttu-id="238ff-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="238ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="238ff-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="238ff-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="238ff-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="238ff-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
