---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 68e005a4e54277ad1be304911645c3eeda455d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719239"
---
# <span data-ttu-id="56fed-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="56fed-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="56fed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56fed-102">SYNOPSIS</span></span>
<span data-ttu-id="56fed-103">Pobiera dostępne punkty odzyskiwania dla elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="56fed-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56fed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56fed-104">SYNTAX</span></span>

### <span data-ttu-id="56fed-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56fed-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56fed-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="56fed-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56fed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="56fed-107">DESCRIPTION</span></span>
<span data-ttu-id="56fed-108">Polecenie cmdlet **Get-AzureRmSiteRecoveryRecoveryPoint** pobiera listę dostępnych punktów odzyskiwania elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="56fed-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="56fed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56fed-109">EXAMPLES</span></span>

## <span data-ttu-id="56fed-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56fed-110">PARAMETERS</span></span>

### <span data-ttu-id="56fed-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56fed-111">-Name</span></span>
<span data-ttu-id="56fed-112">Określa nazwę punktu odzyskiwania, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56fed-112">Specifies the name of the recovery point this cmdlet gets.</span></span>

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

### <span data-ttu-id="56fed-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="56fed-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="56fed-114">Określa obiekt elementu chronionego replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="56fed-114">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56fed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fed-115">-DefaultProfile</span></span>
<span data-ttu-id="56fed-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56fed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56fed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fed-117">CommonParameters</span></span>
<span data-ttu-id="56fed-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56fed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fed-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56fed-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fed-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56fed-120">INPUTS</span></span>

### <span data-ttu-id="56fed-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="56fed-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="56fed-122">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="56fed-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="56fed-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56fed-123">OUTPUTS</span></span>

### <span data-ttu-id="56fed-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="56fed-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="56fed-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56fed-125">NOTES</span></span>

## <span data-ttu-id="56fed-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56fed-126">RELATED LINKS</span></span>

[<span data-ttu-id="56fed-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56fed-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="56fed-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56fed-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="56fed-129">Nowe — AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56fed-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="56fed-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56fed-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="56fed-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="56fed-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
