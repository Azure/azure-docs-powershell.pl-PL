---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 441e3108053aa55c93ab0f9ee150bebd592a091e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985713"
---
# <span data-ttu-id="ad6cd-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ad6cd-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="ad6cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6cd-103">Pobiera dostępne (odkryte) klasyfikacje magazynu ASR w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="ad6cd-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="ad6cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad6cd-104">SYNTAX</span></span>

### <span data-ttu-id="ad6cd-105">ByFabricObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ad6cd-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6cd-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ad6cd-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6cd-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ad6cd-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad6cd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad6cd-108">DESCRIPTION</span></span>
<span data-ttu-id="ad6cd-109">Polecenie **cmdlet Get-AzRecoveryServicesAsrStorageClassification** pobiera szczegółowe informacje o wykrytych klasyfikacjach magazynu asr w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="ad6cd-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="ad6cd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad6cd-110">EXAMPLES</span></span>

### <span data-ttu-id="ad6cd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad6cd-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="ad6cd-112">W tym celu należy wyświetlić listę wykrytych klasyfikacji magazynu, które są odpowiednie dla określonego materiału ASR.</span><span class="sxs-lookup"><span data-stu-id="ad6cd-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="ad6cd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad6cd-113">PARAMETERS</span></span>

### <span data-ttu-id="ad6cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6cd-114">-DefaultProfile</span></span>
<span data-ttu-id="ad6cd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad6cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ad6cd-116">— Materiał</span><span class="sxs-lookup"><span data-stu-id="ad6cd-116">-Fabric</span></span>
<span data-ttu-id="ad6cd-117">Określa obiekt z materiału ASR.</span><span class="sxs-lookup"><span data-stu-id="ad6cd-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="ad6cd-118">Polecenie cmdlet pobiera szczegółowe informacje o wykrytych klasyfikacjach magazynu, które są odpowiadające określonej materiałowi ASR.</span><span class="sxs-lookup"><span data-stu-id="ad6cd-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="ad6cd-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ad6cd-119">-FriendlyName</span></span>
<span data-ttu-id="ad6cd-120">Określa przyjazną nazwę obiektu klasyfikacji magazynu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="ad6cd-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6cd-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad6cd-121">-Name</span></span>
<span data-ttu-id="ad6cd-122">Określa nazwę obiektu klasyfikacji magazynu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="ad6cd-122">Specifies the name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6cd-123">CommonParameters</span></span>
<span data-ttu-id="ad6cd-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6cd-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad6cd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6cd-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad6cd-126">INPUTS</span></span>

### <span data-ttu-id="ad6cd-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ad6cd-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ad6cd-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad6cd-128">OUTPUTS</span></span>

### <span data-ttu-id="ad6cd-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ad6cd-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="ad6cd-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad6cd-130">NOTES</span></span>

## <span data-ttu-id="ad6cd-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad6cd-131">RELATED LINKS</span></span>
