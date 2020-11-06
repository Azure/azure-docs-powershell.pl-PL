---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542888"
---
# <span data-ttu-id="7ea45-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7ea45-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="7ea45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ea45-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea45-103">Zmienia punkt odzyskiwania dla uszkodzonego elementu chronionego przed zatwierdzeniem operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="7ea45-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ea45-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ea45-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea45-106">**Uruchomienie programu AzureRmSiteRecoveryApplyRecoveryPoint** powoduje zmianę punktu odzyskiwania dla elementu chronionego niepowodzeniem przed zatwierdzeniem operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="7ea45-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="7ea45-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ea45-107">EXAMPLES</span></span>

## <span data-ttu-id="7ea45-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ea45-108">PARAMETERS</span></span>

### <span data-ttu-id="7ea45-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="7ea45-109">-DataEncryptionPrimaryCertFile</span></span>
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

### <span data-ttu-id="7ea45-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="7ea45-110">-DataEncryptionSecondaryCertFile</span></span>
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

### <span data-ttu-id="7ea45-111">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7ea45-111">-RecoveryPoint</span></span>
<span data-ttu-id="7ea45-112">Określa obiekt punktu odzyskiwania, który został zmieniony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea45-112">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea45-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ea45-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7ea45-114">Określa obiekt elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="7ea45-114">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="7ea45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea45-115">-DefaultProfile</span></span>
<span data-ttu-id="7ea45-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea45-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ea45-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea45-117">CommonParameters</span></span>
<span data-ttu-id="7ea45-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea45-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea45-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea45-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea45-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ea45-120">INPUTS</span></span>

### <span data-ttu-id="7ea45-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ea45-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="7ea45-122">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="7ea45-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="7ea45-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ea45-123">OUTPUTS</span></span>

### <span data-ttu-id="7ea45-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7ea45-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7ea45-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ea45-125">NOTES</span></span>

## <span data-ttu-id="7ea45-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ea45-126">RELATED LINKS</span></span>

[<span data-ttu-id="7ea45-127">Polecenia cmdlet dotyczące odzyskiwania witryny Azure Site</span><span class="sxs-lookup"><span data-stu-id="7ea45-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
