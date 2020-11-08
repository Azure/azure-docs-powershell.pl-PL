---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219292"
---
# <span data-ttu-id="f3ba9-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f3ba9-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="f3ba9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ba9-103">Pobiera dostępne (odnalezione) klasyfikacje magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="f3ba9-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="f3ba9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3ba9-104">SYNTAX</span></span>

### <span data-ttu-id="f3ba9-105">ByFabricObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3ba9-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ba9-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f3ba9-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ba9-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f3ba9-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3ba9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f3ba9-108">DESCRIPTION</span></span>
<span data-ttu-id="f3ba9-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrStorageClassification** pobiera szczegóły odnalezionych klasyfikacji magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="f3ba9-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="f3ba9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3ba9-110">EXAMPLES</span></span>

### <span data-ttu-id="f3ba9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3ba9-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="f3ba9-112">Lista odnalezionych klasyfikacji magazynu odpowiadających określonej sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="f3ba9-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="f3ba9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3ba9-113">PARAMETERS</span></span>

### <span data-ttu-id="f3ba9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ba9-114">-DefaultProfile</span></span>
<span data-ttu-id="f3ba9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ba9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f3ba9-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="f3ba9-116">-Fabric</span></span>
<span data-ttu-id="f3ba9-117">Określa obiekt sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="f3ba9-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="f3ba9-118">Polecenie cmdlet umożliwia pobieranie szczegółów dotyczących odnalezionych klasyfikacji magazynu odpowiadających określonej sieci szkieletowej ASR.</span><span class="sxs-lookup"><span data-stu-id="f3ba9-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="f3ba9-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f3ba9-119">-FriendlyName</span></span>
<span data-ttu-id="f3ba9-120">Określa przyjazną nazwę obiektu klasyfikacji magazynu, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="f3ba9-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="f3ba9-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3ba9-121">-Name</span></span>
<span data-ttu-id="f3ba9-122">Określa nazwę obiektu klasyfikacji magazynu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f3ba9-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="f3ba9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ba9-123">CommonParameters</span></span>
<span data-ttu-id="f3ba9-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ba9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ba9-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3ba9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ba9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3ba9-126">INPUTS</span></span>

### <span data-ttu-id="f3ba9-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f3ba9-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f3ba9-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3ba9-128">OUTPUTS</span></span>

### <span data-ttu-id="f3ba9-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f3ba9-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="f3ba9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3ba9-130">NOTES</span></span>

## <span data-ttu-id="f3ba9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3ba9-131">RELATED LINKS</span></span>
