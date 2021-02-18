---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193018"
---
# <span data-ttu-id="f20e7-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f20e7-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="f20e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f20e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f20e7-103">Pobiera dostępne punkty odzyskiwania dla elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="f20e7-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="f20e7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f20e7-104">SYNTAX</span></span>

### <span data-ttu-id="f20e7-105">ByObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f20e7-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f20e7-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f20e7-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f20e7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f20e7-107">DESCRIPTION</span></span>
<span data-ttu-id="f20e7-108">Polecenie **cmdlet Get-AzRecoveryServicesAsrRecoveryPoint** pobiera listę dostępnych punktów odzyskiwania dla elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="f20e7-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="f20e7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f20e7-109">EXAMPLES</span></span>

### <span data-ttu-id="f20e7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f20e7-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="f20e7-111">Pobiera punkty odzyskiwania dla określonego elementu chronionego replikacją asr.</span><span class="sxs-lookup"><span data-stu-id="f20e7-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="f20e7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f20e7-112">PARAMETERS</span></span>

### <span data-ttu-id="f20e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20e7-113">-DefaultProfile</span></span>
<span data-ttu-id="f20e7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f20e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f20e7-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f20e7-115">-Name</span></span>
<span data-ttu-id="f20e7-116">Określa nazwę punktu odzyskiwania, który ma być uzyskać.</span><span class="sxs-lookup"><span data-stu-id="f20e7-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="f20e7-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f20e7-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f20e7-118">Określa obiekt elementu chronionego replikacją usługi Azure Site Recovery, dla którego zostanie wyświetlona lista dostępnych punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f20e7-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f20e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20e7-119">CommonParameters</span></span>
<span data-ttu-id="f20e7-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f20e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20e7-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f20e7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20e7-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f20e7-122">INPUTS</span></span>

### <span data-ttu-id="f20e7-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f20e7-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f20e7-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f20e7-124">OUTPUTS</span></span>

### <span data-ttu-id="f20e7-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f20e7-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="f20e7-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f20e7-126">NOTES</span></span>

## <span data-ttu-id="f20e7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f20e7-127">RELATED LINKS</span></span>

[<span data-ttu-id="f20e7-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f20e7-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f20e7-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f20e7-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f20e7-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f20e7-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f20e7-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f20e7-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f20e7-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f20e7-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
