---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 27f1f0f03da7a4ad912be28a2de85bf6e7cf58f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014938"
---
# <span data-ttu-id="c8250-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c8250-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="c8250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8250-102">SYNOPSIS</span></span>
<span data-ttu-id="c8250-103">Pobiera dostępne punkty odzyskiwania dla elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="c8250-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="c8250-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c8250-104">SYNTAX</span></span>

### <span data-ttu-id="c8250-105">ByObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c8250-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8250-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c8250-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8250-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c8250-107">DESCRIPTION</span></span>
<span data-ttu-id="c8250-108">Polecenie **cmdlet Get-AzRecoveryServicesAsrRecoveryPoint** pobiera listę dostępnych punktów odzyskiwania dla elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="c8250-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="c8250-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c8250-109">EXAMPLES</span></span>

### <span data-ttu-id="c8250-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8250-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="c8250-111">Pobiera punkty odzyskiwania dla określonego elementu chronionego replikacją asr.</span><span class="sxs-lookup"><span data-stu-id="c8250-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="c8250-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8250-112">PARAMETERS</span></span>

### <span data-ttu-id="c8250-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8250-113">-DefaultProfile</span></span>
<span data-ttu-id="c8250-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8250-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c8250-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c8250-115">-Name</span></span>
<span data-ttu-id="c8250-116">Określa nazwę punktu odzyskiwania, który ma być uzyskać.</span><span class="sxs-lookup"><span data-stu-id="c8250-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="c8250-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c8250-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c8250-118">Określa obiekt elementu chronionego replikacją usługi Azure Site Recovery, dla którego ma być chwalona lista dostępnych punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c8250-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="c8250-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8250-119">CommonParameters</span></span>
<span data-ttu-id="c8250-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8250-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8250-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8250-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8250-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8250-122">INPUTS</span></span>

### <span data-ttu-id="c8250-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c8250-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c8250-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8250-124">OUTPUTS</span></span>

### <span data-ttu-id="c8250-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c8250-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="c8250-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c8250-126">NOTES</span></span>

## <span data-ttu-id="c8250-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8250-127">RELATED LINKS</span></span>

[<span data-ttu-id="c8250-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8250-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c8250-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8250-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c8250-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8250-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c8250-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8250-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="c8250-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8250-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
