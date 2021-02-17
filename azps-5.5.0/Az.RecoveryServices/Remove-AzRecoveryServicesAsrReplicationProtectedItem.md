---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186611"
---
# <span data-ttu-id="f5284-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5284-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="f5284-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5284-102">SYNOPSIS</span></span>
<span data-ttu-id="f5284-103">Zatrzymuje/wyłącza replikację elementu chronionego replikacją usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f5284-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="f5284-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5284-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5284-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5284-105">DESCRIPTION</span></span>
<span data-ttu-id="f5284-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem** wyłącza replikację określonego elementu chronionego replikacją usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f5284-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="f5284-107">Ta operacja powoduje zatrzymanie replikacji chronionego elementu.</span><span class="sxs-lookup"><span data-stu-id="f5284-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="f5284-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5284-108">EXAMPLES</span></span>

### <span data-ttu-id="f5284-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5284-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="f5284-110">Uruchamia operację wyłączania replikacji dla określonego elementu chronionego replikacją i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="f5284-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f5284-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5284-111">PARAMETERS</span></span>

### <span data-ttu-id="f5284-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5284-112">-DefaultProfile</span></span>
<span data-ttu-id="f5284-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5284-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f5284-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f5284-114">-Force</span></span>
<span data-ttu-id="f5284-115">Wymusz uruchomienie polecenia bez podaniem dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="f5284-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="f5284-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5284-116">-InputObject</span></span>
<span data-ttu-id="f5284-117">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacją asr odpowiadający elementowi chronionej replikacji, dla którego replikacja ma zostać wyłączona.</span><span class="sxs-lookup"><span data-stu-id="f5284-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="f5284-118">- WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f5284-118">-WaitForCompletion</span></span>
<span data-ttu-id="f5284-119">Wskazuje, że polecenie cmdlet powinno czekać na ukończenie operacji przed jej zwróceniem.</span><span class="sxs-lookup"><span data-stu-id="f5284-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="f5284-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5284-120">-Confirm</span></span>
<span data-ttu-id="f5284-121">Określ, czy jest wymagane potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f5284-121">Specify if confirmation is required.</span></span> <span data-ttu-id="f5284-122">Ustaw wartość parametru confirm w celu $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f5284-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="f5284-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5284-123">-WhatIf</span></span>
<span data-ttu-id="f5284-124">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie wykonane bez wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5284-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="f5284-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5284-125">CommonParameters</span></span>
<span data-ttu-id="f5284-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5284-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5284-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5284-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5284-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5284-128">INPUTS</span></span>

### <span data-ttu-id="f5284-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5284-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f5284-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5284-130">OUTPUTS</span></span>

### <span data-ttu-id="f5284-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f5284-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f5284-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5284-132">NOTES</span></span>

## <span data-ttu-id="f5284-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5284-133">RELATED LINKS</span></span>

[<span data-ttu-id="f5284-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5284-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f5284-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5284-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="f5284-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f5284-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
