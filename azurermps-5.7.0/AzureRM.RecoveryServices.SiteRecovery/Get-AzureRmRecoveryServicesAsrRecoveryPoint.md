---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: f5300e120b008540e116596f126e8d2cb9cb2e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542408"
---
# <span data-ttu-id="8a202-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8a202-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="8a202-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a202-102">SYNOPSIS</span></span>
<span data-ttu-id="8a202-103">Pobiera dostępne punkty odzyskiwania dla elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="8a202-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a202-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a202-104">SYNTAX</span></span>

### <span data-ttu-id="8a202-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a202-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a202-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="8a202-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a202-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8a202-107">DESCRIPTION</span></span>
<span data-ttu-id="8a202-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrRecoveryPoint** pobiera listę dostępnych punktów odzyskiwania elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="8a202-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="8a202-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a202-109">EXAMPLES</span></span>

### <span data-ttu-id="8a202-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a202-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="8a202-111">Pobiera punkty odzyskiwania dla określonego elementu chronionego replikacji ASR.</span><span class="sxs-lookup"><span data-stu-id="8a202-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="8a202-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a202-112">PARAMETERS</span></span>

### <span data-ttu-id="8a202-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a202-113">-DefaultProfile</span></span>
<span data-ttu-id="8a202-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a202-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a202-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a202-115">-Name</span></span>
<span data-ttu-id="8a202-116">Określa nazwę punktu odzyskiwania, który należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="8a202-116">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a202-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8a202-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8a202-118">Określa obiekt chronionej replikacji odzyskiwania witryny platformy Azure, dla którego ma zostać wykorzystana lista dostępnych punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8a202-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a202-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a202-119">CommonParameters</span></span>
<span data-ttu-id="8a202-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a202-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a202-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a202-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a202-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a202-122">INPUTS</span></span>

### <span data-ttu-id="8a202-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8a202-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8a202-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a202-124">OUTPUTS</span></span>

### <span data-ttu-id="8a202-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8a202-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8a202-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a202-126">NOTES</span></span>

## <span data-ttu-id="8a202-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a202-127">RELATED LINKS</span></span>

[<span data-ttu-id="8a202-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8a202-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="8a202-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8a202-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="8a202-130">Nowe — AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8a202-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="8a202-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8a202-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="8a202-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8a202-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
