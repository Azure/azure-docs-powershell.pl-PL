---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491349"
---
# <span data-ttu-id="7ec5b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5b-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="7ec5b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ec5b-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec5b-103">Zatrzymuje/wyłącza replikację elementu chronionego replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="7ec5b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ec5b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ec5b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ec5b-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec5b-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem** wyłącza replikację określonego elementu chronionego replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="7ec5b-107">Ta operacja powoduje zatrzymanie replikacji elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="7ec5b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ec5b-108">EXAMPLES</span></span>

### <span data-ttu-id="7ec5b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ec5b-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="7ec5b-110">Rozpoczyna operację wyłączenia replikacji dla określonego elementu chronionego replikacji i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7ec5b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ec5b-111">PARAMETERS</span></span>

### <span data-ttu-id="7ec5b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec5b-112">-DefaultProfile</span></span>
<span data-ttu-id="7ec5b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7ec5b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="7ec5b-114">-Force</span></span>
<span data-ttu-id="7ec5b-115">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="7ec5b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ec5b-116">-InputObject</span></span>
<span data-ttu-id="7ec5b-117">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacji ASR odpowiadający elementowi chronionemu replikacji, dla którego ma zostać wyłączona replikacja.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="7ec5b-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7ec5b-118">-WaitForCompletion</span></span>
<span data-ttu-id="7ec5b-119">Wskazuje, że polecenie cmdlet powinno czekać na ukończenie operacji przed powrotem.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="7ec5b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ec5b-120">-Confirm</span></span>
<span data-ttu-id="7ec5b-121">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-121">Specify if confirmation is required.</span></span> <span data-ttu-id="7ec5b-122">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="7ec5b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec5b-123">-WhatIf</span></span>
<span data-ttu-id="7ec5b-124">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="7ec5b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec5b-125">CommonParameters</span></span>
<span data-ttu-id="7ec5b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec5b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ec5b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec5b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ec5b-128">INPUTS</span></span>

### <span data-ttu-id="7ec5b-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7ec5b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ec5b-130">OUTPUTS</span></span>

### <span data-ttu-id="7ec5b-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7ec5b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7ec5b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ec5b-132">NOTES</span></span>

## <span data-ttu-id="7ec5b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ec5b-133">RELATED LINKS</span></span>

[<span data-ttu-id="7ec5b-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5b-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7ec5b-135">Nowe — AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5b-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="7ec5b-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7ec5b-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
