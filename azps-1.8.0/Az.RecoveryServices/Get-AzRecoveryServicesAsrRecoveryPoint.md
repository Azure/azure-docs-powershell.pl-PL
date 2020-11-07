---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: b381f611d47306c9327d1b276aa3773c34c7b3e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708692"
---
# <span data-ttu-id="afb7b-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="afb7b-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="afb7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afb7b-102">SYNOPSIS</span></span>
<span data-ttu-id="afb7b-103">Pobiera dostępne punkty odzyskiwania dla elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="afb7b-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="afb7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afb7b-104">SYNTAX</span></span>

### <span data-ttu-id="afb7b-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="afb7b-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afb7b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="afb7b-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afb7b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="afb7b-107">DESCRIPTION</span></span>
<span data-ttu-id="afb7b-108">Polecenie cmdlet **Get-AzRecoveryServicesAsrRecoveryPoint** pobiera listę dostępnych punktów odzyskiwania elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="afb7b-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="afb7b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afb7b-109">EXAMPLES</span></span>

### <span data-ttu-id="afb7b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="afb7b-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="afb7b-111">Pobiera punkty odzyskiwania dla określonego elementu chronionego replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="afb7b-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="afb7b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afb7b-112">PARAMETERS</span></span>

### <span data-ttu-id="afb7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb7b-113">-DefaultProfile</span></span>
<span data-ttu-id="afb7b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="afb7b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="afb7b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="afb7b-115">-Name</span></span>
<span data-ttu-id="afb7b-116">Określa nazwę punktu odzyskiwania, który należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="afb7b-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="afb7b-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="afb7b-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="afb7b-118">Określa obiekt chronionej replikacji odzyskiwania witryny platformy Azure, dla którego ma zostać wykorzystana lista dostępnych punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="afb7b-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="afb7b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb7b-119">CommonParameters</span></span>
<span data-ttu-id="afb7b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb7b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb7b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb7b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb7b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afb7b-122">INPUTS</span></span>

### <span data-ttu-id="afb7b-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="afb7b-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="afb7b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afb7b-124">OUTPUTS</span></span>

### <span data-ttu-id="afb7b-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="afb7b-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="afb7b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afb7b-126">NOTES</span></span>

## <span data-ttu-id="afb7b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afb7b-127">RELATED LINKS</span></span>

[<span data-ttu-id="afb7b-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="afb7b-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="afb7b-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="afb7b-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="afb7b-130">Nowe — AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="afb7b-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="afb7b-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="afb7b-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="afb7b-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="afb7b-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)