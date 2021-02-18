---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202034"
---
# <span data-ttu-id="64a09-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="64a09-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="64a09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64a09-102">SYNOPSIS</span></span>
<span data-ttu-id="64a09-103">Pobiera klasyfikacje dostępnego(odkrytego) magazynu ASR w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="64a09-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="64a09-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64a09-104">SYNTAX</span></span>

### <span data-ttu-id="64a09-105">ByFabricObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="64a09-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64a09-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="64a09-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64a09-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="64a09-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64a09-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="64a09-108">DESCRIPTION</span></span>
<span data-ttu-id="64a09-109">Polecenie **cmdlet Get-AzRecoveryServicesAsrStorageClassification** pobiera szczegółowe informacje o wykrytych klasyfikacjach magazynu asr w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="64a09-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="64a09-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64a09-110">EXAMPLES</span></span>

### <span data-ttu-id="64a09-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64a09-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="64a09-112">W tym celu należy wyświetlić listę wykrytych klasyfikacji magazynu, które są odpowiednie dla określonego materiału ASR.</span><span class="sxs-lookup"><span data-stu-id="64a09-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="64a09-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64a09-113">PARAMETERS</span></span>

### <span data-ttu-id="64a09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a09-114">-DefaultProfile</span></span>
<span data-ttu-id="64a09-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64a09-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="64a09-116">— Materiał</span><span class="sxs-lookup"><span data-stu-id="64a09-116">-Fabric</span></span>
<span data-ttu-id="64a09-117">Określa obiekt z materiału ASR.</span><span class="sxs-lookup"><span data-stu-id="64a09-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="64a09-118">Polecenie cmdlet pobiera szczegółowe informacje o wykrytych klasyfikacjach magazynu, które są odpowiadające określonej materiałowi ASR.</span><span class="sxs-lookup"><span data-stu-id="64a09-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="64a09-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="64a09-119">-FriendlyName</span></span>
<span data-ttu-id="64a09-120">Określa przyjazną nazwę obiektu klasyfikacji magazynu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="64a09-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="64a09-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="64a09-121">-Name</span></span>
<span data-ttu-id="64a09-122">Określa nazwę obiektu klasyfikacji magazynu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="64a09-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="64a09-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a09-123">CommonParameters</span></span>
<span data-ttu-id="64a09-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a09-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a09-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64a09-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a09-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64a09-126">INPUTS</span></span>

### <span data-ttu-id="64a09-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="64a09-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="64a09-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64a09-128">OUTPUTS</span></span>

### <span data-ttu-id="64a09-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="64a09-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="64a09-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64a09-130">NOTES</span></span>

## <span data-ttu-id="64a09-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64a09-131">RELATED LINKS</span></span>
