---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bd8a06eb85658fe2ec06d65c0663550be78d1552
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526150"
---
# <span data-ttu-id="1ff3f-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ff3f-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="1ff3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ff3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff3f-103">Zatrzymuje/wyłącza replikację elementu chronionego replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ff3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ff3f-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ff3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ff3f-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff3f-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** wyłącza replikację określonego elementu chronionego replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="1ff3f-107">Ta operacja powoduje zatrzymanie replikacji elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="1ff3f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ff3f-108">EXAMPLES</span></span>

### <span data-ttu-id="1ff3f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ff3f-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="1ff3f-110">Rozpoczyna operację wyłączenia replikacji dla określonego elementu chronionego replikacji i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1ff3f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ff3f-111">PARAMETERS</span></span>

### <span data-ttu-id="1ff3f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff3f-112">-DefaultProfile</span></span>
<span data-ttu-id="1ff3f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1ff3f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="1ff3f-114">-Force</span></span>
<span data-ttu-id="1ff3f-115">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="1ff3f-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1ff3f-116">-InputObject</span></span>
<span data-ttu-id="1ff3f-117">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionemu replikacji, dla którego ma zostać wyłączona replikacja.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff3f-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1ff3f-118">-WaitForCompletion</span></span>
<span data-ttu-id="1ff3f-119">Wskazuje, że polecenie cmdlet powinno czekać na ukończenie operacji przed powrotem.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="1ff3f-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ff3f-120">-Confirm</span></span>
<span data-ttu-id="1ff3f-121">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-121">Specify if confirmation is required.</span></span> <span data-ttu-id="1ff3f-122">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff3f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ff3f-123">-WhatIf</span></span>
<span data-ttu-id="1ff3f-124">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff3f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff3f-125">CommonParameters</span></span>
<span data-ttu-id="1ff3f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff3f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff3f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ff3f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff3f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ff3f-128">INPUTS</span></span>

### <span data-ttu-id="1ff3f-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ff3f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1ff3f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ff3f-130">OUTPUTS</span></span>

### <span data-ttu-id="1ff3f-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1ff3f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1ff3f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ff3f-132">NOTES</span></span>

## <span data-ttu-id="1ff3f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ff3f-133">RELATED LINKS</span></span>

[<span data-ttu-id="1ff3f-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ff3f-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="1ff3f-135">Nowe — AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ff3f-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="1ff3f-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ff3f-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
