---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e1d5dd0c8548b52fde37044d304269358a11af70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718685"
---
# <span data-ttu-id="8e625-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e625-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="8e625-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e625-102">SYNOPSIS</span></span>
<span data-ttu-id="8e625-103">Usuwa element chroniony replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e625-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e625-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e625-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e625-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8e625-105">DESCRIPTION</span></span>
<span data-ttu-id="8e625-106">Polecenie cmdlet **Remove-AzureRmSiteRecoveryReplicationProtectedItem** usuwa element chroniony replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8e625-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="8e625-107">Ta operacja powoduje zatrzymanie replikacji elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="8e625-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="8e625-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e625-108">EXAMPLES</span></span>

## <span data-ttu-id="8e625-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e625-109">PARAMETERS</span></span>

### <span data-ttu-id="8e625-110">-Force</span><span class="sxs-lookup"><span data-stu-id="8e625-110">-Force</span></span>
<span data-ttu-id="8e625-111">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8e625-111">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e625-112">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e625-112">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8e625-113">Określa obiekt elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="8e625-113">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="8e625-114">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="8e625-114">-WaitForCompletion</span></span>
<span data-ttu-id="8e625-115">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="8e625-115">Indicates that the cmdlet waits for the operation to complete.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e625-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e625-116">-Confirm</span></span>
<span data-ttu-id="8e625-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e625-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e625-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e625-118">-WhatIf</span></span>
<span data-ttu-id="8e625-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e625-119">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8e625-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e625-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e625-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e625-121">-DefaultProfile</span></span>
<span data-ttu-id="8e625-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e625-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e625-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e625-123">CommonParameters</span></span>
<span data-ttu-id="8e625-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e625-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e625-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e625-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e625-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e625-126">INPUTS</span></span>

### <span data-ttu-id="8e625-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e625-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="8e625-128">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="8e625-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="8e625-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e625-129">OUTPUTS</span></span>

### <span data-ttu-id="8e625-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8e625-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8e625-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e625-131">NOTES</span></span>

## <span data-ttu-id="8e625-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e625-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e625-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e625-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="8e625-134">Nowe — AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e625-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="8e625-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e625-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
